---
layout: post
title: Categorizing Azure DevOps Mails
subtitle: How to categorize Azure DevOps mails in your mailclient.
tags: [Azure DevOps]
---

## Problem

Since VSTS migrated to Azure Devops notification mails do no longer contain the project name in the message body. If you had outlook-rules (or any other mailclient) using this data in de mail-body to categorize (or move, prioritize, etc) mails these rules will no longer work.

## Solution

You can still detect the organization, project, repo name etc by looking at the email headers.You'll have to  look at the X-VSS-Scope header. This header's format is as follows:
- X-VSS-Scope: {organization}{project}{repo\team\etc...}

If your organization is named deguffroy ( dev.azure.com/deguffroy or before: deguffroy.visualstudio.com) and your project is named alexander you can filter on "X-VSS-Scope: deguffroy\alexander" in the message header.
