---
title: Automated customer data collection
slug: "gmnotion"
summary: "Здесь краткое описание, которое появится на главной странице."
date: 2025-11-29T18:12:00+03:00
type: "project"
tags: []

# Настройки для кнопки Демо (опционально)
links:
  - name: "Демо"
    url: "https://project-live.com" 
---
# PROJECT DESCRIPTION
---

## 1. Main problems

This case study considers a situation where a user receives messages from customers via email. This could be an online store that accepts requests for product purchases, or it could simply be an email address that receives a large number of messages. The main problem is "manually" copying data and transferring it to another environment for processing, which is a very monotonous, routine, and time-consuming process.

## 2. Objectives

Create and configure the system in such a way as to relieve the user of routine work altogether, automating all data transfer actions.
The Make(Integromat) platform was chosen for implementation due to the availability of flexible template modules.

## 3. Step-by-step solution (screenshots)

1. Creating a new project in Make. I chose the Gmail module (Watch emails) because it is the most suitable for this situation. It starts the script execution as soon as a new message arrives in the mailbox.

![choosing Gmail module](imgproj/modul.jpg)

2. Created a new table in the Notion workspace. Added columns for the required type of information and filtering by data type (it's very convenient to sort the list by a specific type). You can also configure the ability to view and edit the table by multiple team members in real time.

![Table in Notion](imgproj/tablenotion.jpg)

3. In the Gmail module settings, I selected the email address to which messages will be sent. The folder to view is Inbox. It is from there that messages will be sent to the Notion environment.

![Gmail module settings](imgproj/gmailset.jpg)

4. We select the Notion module (Create a Database item Legacy) to create a new row in the Notion database each time a new message is received. In the module settings, we select the desired database via ID search and indicate with tags what type of data from the message we expect to see in our database. We indicate the corresponding tag in the corresponding column.

![Gmail module settings](imgproj/notionset.jpg)
  Теги даних  
![Gmail module settings](imgproj/tags.jpg)

## 4. Results

After configuring the modules, we can check the system result

As soon as a new message appears in the "inbox", the Gmail trigger module runs the script. The new message and the data types that we specified in the Notion module settings will automatically populate the table

![Results](imgproj/all.gif)

Summary of work performed:

Designed and implemented a no-code automation that allows you to automatically transfer incoming messages from Gmail to the Notion database. The solution eliminates manual data copying, reduces the risk of errors, and provides convenient access to structured information in a single environment.

Tools:
- Gmail API documentation
- Notion API documentation
- Make(Integromat)
- Notion workspace
