
## Challenge Tasks

### Task 1: Understanding Ownership (10 minutes)

1. Run `ls -l` in your home directory
2. Identify the **owner** and **group** columns
3. Check who owns your files
========================================================================
Owner = the main user who created/controls the file
Group = a team of users who may share access to the file
<img width="431" height="185" alt="image" src="https://github.com/user-attachments/assets/f7fb9ba3-d9d4-40fb-b280-d7761c92cb7d" />


### Task 2: Basic chown Operations (20 minutes)

1. Create file `devops-file.txt`
2. Check current owner: `ls -l devops-file.txt`
3. Change owner to `tokyo` (create user if needed)
4. Change owner to `berlin`
5. Verify the changes
<img width="445" height="183" alt="image" src="https://github.com/user-attachments/assets/89cddcae-b71e-443e-ac6d-819b988efbfd" />

### Task 3: Basic chgrp Operations (15 minutes)

1. Create file `team-notes.txt`
2. Check current group: `ls -l team-notes.txt`
3. Create group: `sudo groupadd heist-team`
4. Change file group to `heist-team`
5. Verify the change
<img width="469" height="238" alt="image" src="https://github.com/user-attachments/assets/1feec898-b3fc-40e7-a074-b9a0e3e31e20" />

### Task 4: Combined Owner & Group Change (15 minutes)

Using `chown` you can change both owner and group together:

1. Create file `project-config.yaml`
2. Change owner to `professor` AND group to `heist-team` (one command)
3. Create directory `app-logs/`
4. Change its owner to `berlin` and group to `heist-team`

<img width="545" height="289" alt="image" src="https://github.com/user-attachments/assets/66d51f82-890a-4c70-b5ad-7214a9f11c6f" />

### Task 5: Recursive Ownership (20 minutes)

1. Create directory structure:
   ```
   mkdir -p heist-project/vault
   mkdir -p heist-project/plans
   touch heist-project/vault/gold.txt
   touch heist-project/plans/strategy.conf
   ```

2. Create group `planners`: `sudo groupadd planners`

3. Change ownership of entire `heist-project/` directory:
   - Owner: `professor`
   - Group: `planners`
   - Use recursive flag (`-R`)

4. Verify all files and subdirectories changed: `ls -lR heist-project/`

<img width="554" height="275" alt="image" src="https://github.com/user-attachments/assets/0f7c1b0f-aa39-4902-aa18-29be498da06c" />


### Task 6: Practice Challenge (20 minutes)

1. Create users: `tokyo`, `berlin`, `nairobi` (if not already created)
2. Create groups: `vault-team`, `tech-team`
3. Create directory: `bank-heist/`
4. Create 3 files inside:
   ```
   touch bank-heist/access-codes.txt
   touch bank-heist/blueprints.pdf
   touch bank-heist/escape-plan.txt
   ```

5. Set different ownership:
   - `access-codes.txt` → owner: `tokyo`, group: `vault-team`
   - `blueprints.pdf` → owner: `berlin`, group: `tech-team`
   - `escape-plan.txt` → owner: `nairobi`, group: `vault-team`

<img width="751" height="323" alt="image" src="https://github.com/user-attachments/assets/fde1df06-6c34-487b-9984-8d80807b1489" />

