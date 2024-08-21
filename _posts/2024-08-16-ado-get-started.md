---
title: "Getting started with Azure DevOps (Pt 1)"
date: 2024-08-16
categories:
  - blog
  - AzureDevOps
  - QuickStart
tags:
  - QuickStart
  - ADo
---
Part 1 of this guide looks at creating a new Azure DevOps Organization and a new Project to hold your code.

## Table of Contents
1. [Introduction](#introduction)
2. [Create a new Azure DevOps Organization](#new_organization)
3. [Create a new Azure DevOps Project](#new_project)
4. [Delete an Azure DevOps Project](#delete_project)
5. [Choose a project type - Agile, Scrum, etc.](#project_type)
6. [Extensions in Azure DevOps](#extensions)

## Introduction <a name="introduction"></a>
If an Organization already exists for your client you can skip to the Project creation section. I would advise reviewing the section on 'Organization settings' Vs. 'Project Settings'.

In many cases your client may have already created an Azure DevOps organization. It will often be aligned towards the clients business name and can be accessed via the url [https://dev.azure.com/{Org__Name}](https://dev.azure.com/contoso). Selecting the previous link would have returned an error as you are unlikely to have permissions within Microsofts ACME equivalent *Contoso*.

![dev.azure.com/contoso](/assets/images/2024-08-16/AzureDevOps-Contoso.png "Contoso's DevOps Organization")

Luckily new organisations within Azure DevOps are configured securely for free by default. Having a look at an organization that I frequently use for [Microsoft Learn](https://learn.microsoft.com/en-us/training/topics/universities) related projects we can see it is similarly restricted.

![dev.azure.com/pshortt](/assets/images/2024-08-16/AzureDevOps-PShortt.png "My PShortt organisation")

**Note:** Yes, these restrictions can be modified.

## Create a new Azure DevOps Organization <a name="new_organization"></a>
Modify the below instructions appropriately for the account you want to login as. If you are creating a new Organization for your client, permissions will be more easily aligned if you use an Entra account from their tenant. To create a personal organization this consideration is less important.

 LetsIf your project repositories are to be stored in their organization then you skip this first step. Otherwise navigate to [dev.azure.com](https://dev.azure.com) and select the option to 'Start free'.

1. Launch a new browser window and navigate to [https://dev.azure.com](https://dev.azure.com) which will redirect you to the appropriate launch page. Select the option to 'Start free'.

    ![Azure DevOps - Start free](/assets/images/2024-08-16/AzureDevOps-Start_free.png "Azure DevOps - Start free")

2. Sign in with an appropriate account - giving consideration to the longer term lifecycle of the new Devops Organization.

    ![Azure DevOps - Sign In](/assets/images/2024-08-16/AzureDevOps-Sign_in.png "Azure DevOps - Sign In")

3. As is standard with Microsoft Live/Entra accounts you will generally be prompted to complete the relevant MFA requirements.

    ![Azure DevOps - MFA Prompt](/assets/images/2024-08-16/AzureDevOps-MFA_prompt.png "Azure DevOps - MFA Prompt")

4. Complete the appropriate MFA prompt

    ![Azure DevOps - Complete MFA](/assets/images/2024-08-16/AzureDevOps-Complete_MFA.png "Azure DevOps - Complete MFA")

5. Welcome to the **Get started with Azure DevOps** screen

    ![Azure DevOps - Choose Region](/assets/images/2024-08-16/AzureDevOps-Choose-region.png "Azure DevOps - Choose Region")

6. Set the appropriate region for your location [^ADoRegion]

    ![Azure DevOps - Set Region](/assets/images/2024-08-16/AzureDevOps-Set-region.png "Azure DevOps - Set Region")

7. You are now prompted to name your Organization. As illustrated at the top of this article your organization name must be globally unique.

    ![Azure DevOps - Name Organization](/assets/images/2024-08-16/AzureDevOps-Set_Org_name.png "Azure DevOps - Name Organization")

8. In the event you already have an Azure DevOps organization and you are creating a new one via the 'New organization' link below:

    ![Azure DevOps - Create new organization](/assets/images/2024-08-16/AzureDevOps-Create_new_org.png "Azure DevOps - Create new organization")

9. You can see that Step 7. and this, Step 9. offer the same organization creation experience.

    ![Azure DevOps - ](/assets/images/2024-08-16/AzureDevOps-name_org.png "Azure DevOps - Name Organization")

10. The new organization wizard will complete the creation process.

    ![Azure DevOps - New Org creation](/assets/images/2024-08-16/AzureDevOps-wait_4_setup.png "Azure DevOps - New Org creation")

11. The organization has been created and you are prompted to create a new project.

    ![Azure DevOps - Create first project](/assets/images/2024-08-16/AzureDevOps-get_started.png "Azure DevOps - Create first project")

    **You will note:**
    - By default the project will default to 'Private'
    - Public Projects can be enabled by modifying the relevant **organization policies**
    - In a new Organization the default Project type is **Basic** which is often not what you want. Review the section on [Choose a project type - Agile, Scrum, etc.](#project_type) to see if this is right for your needs.

12. Give the new project a name and click '**+ Create project**'. The project name must only be unique within your organization.

    ![Azure DevOps - New project name](/assets/images/2024-08-16/AzureDevOps-new-project.png "Azure DevOps - New project name")

    **Note** the indicated URL for your Azure DevOps organization.

13. Project creation will take a few seconds to complete.

    ![Azure DevOps - Project creation](/assets/images/2024-08-16/AzureDevOps-project_setup.png "Azure DevOps - Project creation")

14. The new project will be opened with the default components - Overview, Boards, Repos etc.

    ![Azure DevOps - Project Welcome](/assets/images/2024-08-16/AzureDevOps-welcome_to_project.png "Azure DevOps - Project Welcome")

    **Note** the globally unique URL for your project.

[^ADoRegion]: When your Azure DevOps Organization is in the same region as your Azure tenant you cannot restrict the IP's used by Azure DevOps as it will natively use the Azure Backbone network

## Create a new Azure DevOps Project <a name="new_project"></a>
You will generally not create very many new organizations, you will instead create new projects as required.

1. Open your organization. In this worked example I can navigate directly to it via its unique URL - https://dev.azure.com/tilt-recall.

   Select the '**+ New project**' option.

    ![Azure DevOps - New project](/assets/images/2024-08-16/AzureDevOps-new-project2.png "Azure DevOps - New project")

2. Give the new project a name and desciption as appropriate.

    ![Azure DevOps - New project name](/assets/images/2024-08-16/AzureDevOps-create-project-detailed_01.png "Azure DevOps - New project name")

3. Observe the *Advanced* dropdown. Select this and review the options.

    ![Azure DevOps - New project advanced](/assets/images/2024-08-16/AzureDevOps-create-project-detailed_02.png "Azure DevOps - New project advanced")

    **Note:** Observe the default project methodology of *Basic*.

4. From within the **Work item process** list choose an option that will align with your project methodology.

    ![Azure DevOps - Choose Process](/assets/images/2024-08-16/AzureDevOps-project__methodology.png "Azure DevOps - Choose Process")

5. Review your selections and select **Create**.

    ![Azure DevOps - Create Project](/assets/images/2024-08-16/AzureDevOps-create-project-detailed_03.png "Azure DevOps - Create Project")

6. The new project will take a few seconds to create.

    ![Azure DevOps - Project creation](/assets/images/2024-08-16/AzureDevOps-create-project-detailed_04.png "Azure DevOps - Project Creation")

7. The new project has been successfully created. The project methodology chosen in Step 4 may influence what you see in your project.

    ![Azure DevOps - Project Welcome](/assets/images/2024-08-16/AzureDevOps-new-project2-complete.png "Azure DevOps - Project Welcome")

## Delete an Azure DevOps Project <a name="delete_project"></a>
The following section will detail the deletion of a project. **Absent the configuration of some backup methodology this process is irreversible.**

As observed previously the default project methodology is 'Basic' if you have configured a project as such and require an alternate configuration the fastest remediation is to delete the project and recreate it with the appropriate settings.

To delete an Azure DevOps Project:

1. Navigate to the project to be deleted.

    ![Azure DevOps - Select Project](/assets/images/2024-08-16/AzureDevOps-project2-settings.png "Azure DevOps - Select Project")

2. Open 'Project settings' and within the 'General'  'Overview' pane scroll to the bottom.

    ![Azure DevOps - Project Settings](/assets/images/2024-08-16/AzureDevOps-delete-project-02.png "Azure DevOps - Project Settings")

3. Select the option to 'Delete project' at the bottom of the page.

    ![Azure DevOps - Delete Project](/assets/images/2024-08-16/AzureDevOps-delete-project-03.png "Azure DevOps - Delete Project")

4. Enter the project name in the confirmation box and select 'Delete'.

    ![Azure DevOps - Confirm Deletion](/assets/images/2024-08-16/AzureDevOps-delete-project-04.png "Azure DevOps - Confirm Deletion")

## Choose a project type - Agile, Scrum, etc. <a name="project_type"></a>

When creating a new Project we observed 4 options in the Advanced section:

![Azure DevOps - Work process options](/assets/images/2024-08-16/AzureDevOps-project__methodology.png "Azure DevOps - Work process options")

We can navigate to the 'Work Process' settings in 2 ways:

1. From within the project:

   1. Open the 'Project Settings'.

      ![Azure DevOps - Project Settings](/assets/images/2024-08-16/AzureDevOps-create-settings-01.png "Azure DevOps - Project Settings")

   2. Select the 'Project configuration' blade and click on the hyperlink to 'go to the process customization page'.

      ![Azure DevOps - Process customization](/assets/images/2024-08-16/AzureDevOps-create-settings-02.png "Azure DevOps - Process customization")

   3. You can review the current configuration directly here.

      ![Azure DevOps - Review current configuration](/assets/images/2024-08-16/AzureDevOps-create-settings-03.png "Azure DevOps - Review current configuration")

2. Alternatively from the 'Organization settings' link at the Organization level.

    1. Choose 'Organization settings'.

       ![Azure DevOps - Organization Settings](/assets/images/2024-08-16/AzureDevOps-Org-settings-01.png "Azure DevOps - Organization Settings")

    2. Select 'Process' in the navigation bar.

       ![Azure DevOps - Process](/assets/images/2024-08-16/AzureDevOps-Org-settings-02.png "Azure DevOps - Process")

    3. Note the various default methodologies - if you have not created at least one project of each type you will not see it represented in the list.

       ![Azure DevOps - Default methodologies](/assets/images/2024-08-16/AzureDevOps-Org-settings-03.png "Azure DevOps - Default methodologies")

    4. Choose the relevant work process you want to review.

Let's have a look at what processes are included by default in each option:

- Agile

   ![Azure DevOps - Agile defaults](/assets/images/2024-08-16/AzureDevOps-default-process-Agile.png "Azure DevOps - Agile defaults")

- Basic

  ![Azure DevOps - Basic defaults](/assets/images/2024-08-16/AzureDevOps-default-process-Basic.png "Azure DevOps - Basic defaults")

- CMMI

  ![Azure DevOps - CMMI defaults](/assets/images/2024-08-16/AzureDevOps-default-process-CMMI.png "Azure DevOps - CMMI defaults")

- Scrum

  ![Azure DevOps - Scrum defaults](/assets/images/2024-08-16/AzureDevOps-default-process-Scrum.png "Azure DevOps - Scrum defaults")

  The below table outlines the features in each.

  Work Item Types | Agile | Basic | CMMI |Scrum |
  ---|:---:|:---:|:---:|:---:|
  Bug | X | | X | X |
  Change Request | | | X | |
  Epic | X | X | X | X |
  Feature | X | | X | X |
  Impediment | | | | X |
  Issue | X | X | X | |
  Product Backlog Item | | | | X |
  Requirement | | | X | |
  Review | | | X | |
  Risk | | | X | |
  Task | X | X | X | X |
  Test Case | X | X | X | X |
  Test Plan | X | X | X | X |
  Test Suite | X | X | X | X |
  User Story | X | | | |

## Extensions in Azure DevOps <a name="extensions"></a>

Extensions in Azure DevOps are essentially plugins that extend the base functionality of the platform. Similar to plugins for a browser or Extensions in VSCode. In a new organization from within the 'Organization settings' we can see that none are installed by default.

![Azure DevOps - Installed Extensions](/assets/images/2024-08-16/AzureDevOps-extensions-01.png "Azure DevOps - Installed Extensions")

Depending on your authorization within the Organization you may not have permissions to install additional extensions. As extensions are installed they will populate accordingly.

![Azure DevOps - Some installed extensions](/assets/images/2024-08-16/AzureDevOps-extensions-02.png "Azure DevOps - Some installed extensions")

Extensions are most often visible via the Pipelines wizard if they have been installed. Many tasks are native to Azure DevOps and will not require a specific extension.

![Azure DevOps - Where we can see extensions](/assets/images/2024-08-16/AzureDevOps-extensions-03a.png "Azure DevOps - Where we can see extensions")

Generally they will be browsed and installed via the [Visual Studio Marketplace](https://marketplace.visualstudio.com/azuredevops).

![Azure DevOps - Visual Studio Marketplace](/assets/images/2024-08-16/AzureDevOps-extensions-03.png "Azure DevOps - Visual Studio Marketplace")

We can see there are many potential extensions for the various Azure DevOps components - Boards, Repos, Pipelines etc.

![Azure DevOps - Extension Types](/assets/images/2024-08-16/AzureDevOps-extensions-04.png "Azure DevOps - Extension Types")

Not all extensions are free and many are written by 3rd parties so exercise caution and restraint in the extensions deployed.

If you do not have permissions or cannot see an extension you know is available discuss your request with an administrator of your Azure DevOps Organization.