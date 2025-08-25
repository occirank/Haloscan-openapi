# Custom GPT for Haloscan

This repository provides a guide and setup for creating a **Custom GPT** that integrates with **Haloscan**, allowing your chatbot to fetch SEO data and provide actionable insights.

---

## Table of Contents

- [Introduction](#introduction)  
- [Prerequisites](#prerequisites)  
- [Creating Your Custom GPT](#creating-your-custom-gpt)  
  - [Step 1: Fill in GPT Details](#step-1-fill-in-gpt-details)  
  - [Step 2: Set up Actions](#step-2-set-up-actions)  
  - [Step 3: Configure GPT Access](#step-3-configure-gpt-access)  
  - [Step 4: Modify GPT Privacy Settings](#step-4-modify-gpt-privacy-settings)  
- [Haloscan Actions](#haloscan-actions)  
- [Example API Calls](#example-api-calls)  

---

## Introduction

Haloscan is an SEO tool that provides insights into:

- Website performance  
- Keyword metrics  
- Online visibility  

It helps users analyze data and make informed SEO decisions. This tutorial guides you step by step through creating a **Custom GPT** that integrates with Haloscan.

---

## Prerequisites

To work with Haloscan API in your Custom GPT:

### Haloscan

1. A valid Haloscan account and API key.  
2. Log in to Haloscan or register for a new account.  
3. Get your API key: [Click here](#)  
4. Keep your API key secret.

### OpenAI / ChatGPT

1. A ChatGPT account with a **Plus plan** or **Enterprise plan** (required for Custom GPTs).  
2. Log in or register.  
3. Create your first GPT: [Click here](#)  
4. Click **+ Create** to start.

---

## Creating Your Custom GPT

### Step 1: Fill in GPT Details

- **Avatar:** Optional  
- **Name:** e.g., `Haloscan SEO Assistant`  
- **Description:** e.g., `Fetches SEO data from Haloscan and provides actionable insights`  
- Leave other fields empty.

### Step 2: Set up Actions

1. Scroll to the bottom of the form to **Actions**  
2. Click **Create new action**  
3. Authentication:
   - **Authentication Type:** API Key  
   - **API Key:** Your Haloscan API Key  
   - **Auth Type:** Custom  
   - **Custom Header Name:** `haloscan-api-key`  
4. Schema:
   - Copy the OpenAPI spec link  
   - Click **Import from URL** and paste the link  
5. Privacy policy: Paste the link

### Step 3: Configure GPT Access

1. Click **Create**  
2. Choose who can use the GPT (**Only me** for personal use)  
3. Click **Save**  
4. Click **View GPT** to see your newly created GPT

### Step 4: Modify GPT Privacy Settings

- Change from **Ask** to **Always allow**

---

## Haloscan Actions

The GPT will include a list of actions, for example:

- Keywords Overview  
- Keywords Match  
- Keywords Similar  
- Domains Overview  
- Domains Positions  
- Domains Top Pages  

> Haloscan API provides **33 actions**. Each OpenAPI file can have a maximum of 30 operations, so the actions are split into **two OpenAPI files**.  
> - First file link: provided in Step 2  
> - Second file link: use the same steps to create another GPT  

Second GPT actions include:

- Domains Expired  
- Domains Expired Reveal  
- Domains GMB Backlinks  
- Domains GMB Backlinks Map  
- Domains GMB Backlinks Categories  
- User Credit  

---

## Example API Calls

- Test your GPT by sending simple prompts, such as a website URL or keyword.  
- The GPT should return structured SEO data fetched from Haloscan API.  

Once tested, your GPT can answer SEO-related questions like:

- Keyword ranking trends  
- Website visibility metrics  
- Competitor analysis data  

This integration allows your chatbot to provide **real-time, actionable SEO insights directly from Haloscan**.

---

