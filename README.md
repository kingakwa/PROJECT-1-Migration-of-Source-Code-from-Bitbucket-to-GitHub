# PROJECT 1: MIGRATION OF SOURCE CODE FROM BITBUCKET TO GITHUB

# Mirror-and-synchronizing (BITBUCKET TO GITHUB MIGRTION AND SYNCRONIZATION)

Mirror and synchronizing GitHub & Bitbucket repository.

# OBJECTIVE: Migrating your existing bitbucket repository to GitHub repository, synchronizing them in shuch a way that when ever a change is made in the source repository(Bitbucket) the same change will be replecated in GitHub without any manuel intervention.
https://github.com/kingakwa/Mirror-and-synchronizing-akwa/blob/main/migration-bitbucket-github.jpg

#1. On GitHub, create a new repository
  - On your Bitbucket
      Navigate to your Bitbucket repository Example "Mirroring-Repo" Create an access token under `Repository settings > Security > Access tokens`
      Create Repository Access Token with selecting all the "READ" Permission
      Copy the last Access token Example { "https://x-token-auth:ATCTT3xFfGN0TSG5xC5PMZex1aEWC2wMY7j1SiYTwLpR7WTpHQ4DJ1oRfevWbd-LVn9bRzmr3csDN4DEjT57KYlsxWcKXnk5zW17DLJ9ssRcOFFwegxzPTMS-MAfumre3yDmXup-z1nHb8XSRGI9N_McR6FRyHArzIoPIWiJSk6cQfYqfAkIw_w=65FC4ty63@bitbucket.org/demo-migration12/solstice_demo.git" }
    
    ![Screen Shot 2024-01-04 at 00 27 57](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/666aed90-75a8-4c57-bbe0-fe4f266ad578)
    
- Navigate To Github and Import the Repository while keeping the same name "Mirroring-Repo"
     - To navigate to GitHub and import a repository while keeping the same name "Mirroring-Repo", follow these steps:
       
       Step 1: Log in to GitHub
     - Open GitHub in your browser.
     - Sign in with your GitHub credentials.

       Import a Repository
     - Click on your profile icon in the top-right corner.
     - Select "Your repositories" from the dropdown.
      - Click the green "New" button and select "Import a repository" (or go directly to GitHub Importer).
     - Enter the URL of the repository you want to import (e.g., from GitHub, GitLab, or Bitbucket).
     - In the "Repository Name" field, type "Mirroring-Repo" to maintain the same name.
     - Choose your preferred visibility (Public or Private).
     - Click "Begin Import" and wait for the process to complete.
       <img width="640" alt="importing repo" src="https://github.com/user-attachments/assets/d034d6aa-ba05-4dfe-8d3f-8091cd1b4885" />


 
  - On Bitbucket, Enable Pipelines under Repository settings > Pipelines > Settings
    <img width="920" alt="enable pipeline" src="https://github.com/user-attachments/assets/702872be-05f7-499d-855a-79fc47a8ba29" />

  - On Bitbucket, Generate keys under Repository settings > Pipelines > SSH keys. Copy the public key to clipboard
    <img width="918" alt="copy public key" src="https://github.com/user-attachments/assets/216bf37f-8df1-40d6-87df-00ba6ea417b6" />

  - On the same page, under Known hosts enter github.com as the Host address and then click Fetch followed by Add host
    <img width="914" alt="github com" src="https://github.com/user-attachments/assets/7acf3c1b-2e88-4837-9952-4db482454f29" />

  - On GitHub, add the public key under Settings > Security > Deploy keys > Add deploy key. Tick the checkbox to Allow write access
   <img width="758" alt="image" src="https://github.com/user-attachments/assets/dca749e2-21b0-4c19-a48a-c2c7d93f3266" />

    
    ![Screen Shot 2024-01-04 at 00 35 39](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/2545afe7-52c3-4934-a181-6a1a9b06e447)
    
  - On Bitbucket, add the public key under Repository settings > Security > Access keys > Add key
    
    ![Screen Shot 2024-01-04 at 00 36 53](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/39271cf9-d5f6-4488-abe4-5fd91dcecb08)
    
  - On Bitbucket, Create an access tokens under Repository settings > Security > Access tokens. Create Repository Access Token, give a name with selecting all the "READ" Permission and tick the checkbox of Webhooks
  - Copy the first Token Example { "ATCTT3xFfGN0TSG5xC5PMZex1aEWC2wMY7j1SiYTwLpR7WTpHQ4DJ1oRfevWbd-LVn9bRzmr3csDN4DEjT57KYlsxWcKXnk5zW17DLJ9ssRcOFFwegxzPTMS-MAfumre3yDmXup-z1nHb8XSRGI9N_McR6FRyHArzIoPIWiJSk6cQfYqfAkIw_w=65FC4ty63" }
    
   ![Screen Shot 2024-01-04 at 00 37 47](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/0af2b9ef-5063-49fa-8170-88dae0d09844)

  - On Bitbucket, Create a Repository variables under Repository Settings > Pipeline > Repository variable. Naming the variable Example " BITBUCKET_VARIABLE"
    
    ![Screen Shot 2024-01-04 at 00 39 25](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/ede419ec-4553-4dd4-adb6-649f2fe56602)
    
  - On Github, At the top right click on your Profile, Scroll down at the bottom click on settings
    
    ![Screen Shot 2024-01-04 at 00 45 35](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/68a20ce1-ad1e-44cb-8b84-1729dbc8b212)
    
  - At the bottom left of the page click Developer Settings, Create a Personal access tokens Under Personal access tokens > Token (classic) > Generate new token > Generate new token (classic)
    
    ![Screen Shot 2024-01-04 at 00 49 19](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/88398cca-a40f-4afd-ba11-50f2a7ee1ecf)
    
  - Check the "repo" box, "Workflow" box and the "write:package" box. Genarate Token and copy the token Example "ghp_zY5GxaeytuAZlR4tPcwqovPz7c2ZVy1kdfg"
   
    ![Screen Shot 2024-01-04 at 00 52 09](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/a0237460-df31-480e-b2df-136dab880c68)
    
  - On Bitbucket, Create a Repository variables with the Access Token from Github under Repository Settings > Pipeline > Repository variable. Naming the variable Example "GITHUB_VARIABLE"

# Inside the Bitbucket repo, create a bitbucket-pipelines.yml file containing the following:

```
  pipelines:
    default:
      - step:
          name: Sync GitHub Mirror
          image: alpine/git:latest
          clone:
            enabled: false
          script:
            - git clone --mirror https://x-token-auth:"$BITBUCKET_VARIABLE"@bitbucket.org/demo-migration12/Mirroring-Repo.git ## @bitbucket.org follow by your Bitbucket repository path
            - cd Mirroring-Repo.git ## cd followed by your Github repository Name
            - git push --mirror https://x-token-auth:"$GITHUB_VARIABLE"@github.com/asaphdanchi/Mirroring-Repo.git ## @github.com followed by your Github repository path
```

On your code replace the "$BITBUCKET_VARIABLE" and "$GITHUB_VARIABLE" with your corresponding variable names while keeping the $ and the "" sign. 

# Run the pipeline in Bitbucket


![Screen Shot 2024-01-04 at 02 57 05](https://github.com/asaphdanchi/Mirror-and-synchronizing/assets/112729006/4b9e2dab-e59c-41a8-9b1f-9a09db958d75)


