---
layout: page
title: "Set up a free enquiry logger with Google Forms and Google Sheets"
permalink: /guides/enquiry-logger/
description: "Set up a free Google Form that logs every enquiry into Google Sheets automatically, with repeat-customer detection and a 48-hour follow-up date."
---

> **Get the script:** [open the enquiry logger script (Code-form-only.gs) as plain text]({{ '/templates/enquiry-logger-script.txt' | relative_url }}). Select all, copy, and paste it where step 1 of the setup says. **Last checked: 11 October 2026.**

> **Free spreadsheet** (Excel files that also open in Google Sheets and Numbers):
>
> - [Enquiry log]({{ '/downloads/a2b-enquiry-log.xlsx' | relative_url }}){: data-goatcounter-click="download-enquiry-log" data-goatcounter-title="Enquiry log" } (sets a 2-day follow-up date and flags anything waiting for a reply)
>
> Free to use. No sign-up.

This guide walks you through setting up the enquiry logger script (Code-form-only.gs). It gives you a web form to share with customers. Every submission is logged automatically into a Google Sheet, with repeat detection, a Rejected tab, an Activity tab and a follow-up date 48 hours after each enquiry arrives. It is free to run on a standard Google account.

The Google facts below come from extracts of Google's own help pages, recorded on 11 October 2026. Google can change its pages and screens at any time, so what you see may differ slightly.

## Who this is for

This guide is for solo service businesses and freelancers, in the UK or elsewhere, who:

- want a free way to keep a record of enquiries in one place;
- do not want to put a personal email address on their website or in front of customers;
- are comfortable following written steps, copying and pasting, and clicking through screens. You do not need to know how to code.

## What you'll set up

When you run the script once, it creates three things in your Google account:

1. **A Google Form** called "Enquiry form". It asks for a name, an email address and the enquiry itself. All three are required, and the email box checks that what is typed looks like an email address. The form does not collect the visitor's email address from their Google sign-in, and the link you share shows no email address of yours.
2. **A Google Sheet** called "Enquiries" with three tabs:
   - **Enquiries**: one row per enquiry, with the time received, name, email address, message, a status (New, Replied, Quote sent, Won or Lost, chosen from a drop-down list), a "Follow up by" time and a Notes column. A row turns a light red when its follow-up time has passed and its status is still New, Replied or Quote sent.
   - **Rejected**: submissions that could not be stored as enquiries, with the reasons (for example "name missing" or "email address not valid"). Because the form already makes all three boxes required and checks the email format, you may rarely see anything here.
   - **Activity**: a log of what the script did, such as "stored", "rejected" or "repeat ignored".
3. **A trigger**, which is Google's word for an automatic instruction. This one tells Google to run the script every time someone submits the form. Google's documentation says an installable form submit trigger "runs when a user responds to a form" and that installable triggers "always run under the account of the person who created them" (https://developers.google.com/apps-script/guides/triggers/installable, checked 11 October 2026).

### What it does, and what it does not do

It does:

- store each enquiry once;
- ignore an identical message from the same email address if it arrives within 30 minutes of one already logged, treating it as a repeat delivery, and note this on the Activity tab;
- keep different enquiries from the same person as separate rows;
- cut any message longer than 2,000 characters when storing it;
- set a "Follow up by" time 48 hours after the enquiry arrived.

It does not:

- read your email or send any email. The script never reads or sends email;
- send reminders or notifications. The follow-up time is a date in a column and the row colour change described above; nothing prompts you to look;
- reply to customers. You do that yourself, from whichever email account you choose;
- do anything beyond what is listed above.

## Before you start

You need:

- a computer with a web browser (the steps below assume a desktop or laptop);
- an email address you already use, which does not have to be a Gmail address, to register the Google account;
- the enquiry logger script (Code-form-only.gs), which the site you got this guide from links to. Open it in a text editor and be ready to copy the whole file.

### Create a free Google account with your existing email address

You do not need Gmail. Google states: "You don't need to have a Gmail address to create a Google Account." Using an existing address (Outlook, for example) means your personal Gmail address, if you have one, never needs to be involved. (https://support.google.com/accounts/answer/27441, checked 11 October 2026.)

According to that page, the steps are:

1. Go to the Google Account sign-in page and choose **Create account**, then **For my personal use**.
2. Enter your basic information.
3. Choose **Use your existing email** and enter the email address you want to use, then choose **Next**.
4. Google sends a code to that address. Enter the code to verify it.
5. Create a password and finish.

Two points from the same page: account notifications go to your non-Google address unless you change your contact email, and you cannot use an email address that is already linked to a Google Account.

Make sure you are signed in to this account for every step below. Everything the script creates belongs to whichever account is signed in.

## Step-by-step setup

### 1. Start a new Apps Script project

1. Sign in to the Google account you created.
2. Go to **script.google.com**.
3. Choose **New project**. A page opens with a code editor containing a few lines of placeholder code.

### 2. Paste in the script

1. Open the enquiry logger script (Code-form-only.gs) in a text editor, select everything (Ctrl+A on Windows, Cmd+A on a Mac) and copy it.
2. In the Apps Script editor, click inside the code box, select all the placeholder code and delete it.
3. Paste the script in.
4. Save the project (the disk icon, or Ctrl+S / Cmd+S). If asked, give the project a name such as "Enquiry logger".

### 3. Run `setup`

1. Near the top of the editor there is a drop-down list of function names beside the **Run** and **Debug** buttons. Choose **setup**.
2. Press **Run**.
3. Run `setup` once only. The script itself says that running it again does nothing if it is already set up; it simply writes the existing links to the log again.

### 4. Approve the permission screens

The first time you run it, Google asks for permission, because the script needs to create a spreadsheet and a form, and a trigger, in your account. The screens may look different from the descriptions here, so read each one.

1. A box saying **Authorization required** appears. Choose **Review permissions**.
2. Choose your Google account.
3. You will probably see a warning: **"Google hasn't verified this app"**. The owner of this business saw it during their own test on 11 October 2026.
4. To continue, choose **Advanced**, then the link at the bottom that begins **Go to … (unsafe)**.
5. Read the list of things the script is asking permission to do, then choose **Allow**.

#### Why the warning appears, and when to continue

The warning appears because Google has not reviewed this script. You added it yourself to your own project, so it is not an app that Google has checked. That does not mean Google has found anything wrong with it. My Google sources do not include Google's own explanation of the warning, so this explanation is not from a Google page; see "Where to get help" if you want Google's wording.

Only continue for a script you have read or trust. Look through the script you pasted, or ask someone you trust to, before you allow it. If you pasted in anything other than the enquiry logger script (Code-form-only.gs), or are unsure where your copy came from, stop and do not allow it.

### 5. Find your form link and spreadsheet

1. After the run finishes, the **Execution log** appears at the bottom of the editor. If it does not, open **Execution log** from the left-hand menu.
2. The log shows "Done.", then a line starting **Spreadsheet:** with a web address, and a line starting **Form link to share:** with another.
3. Copy both addresses somewhere safe. The form link is the one you share with customers. The spreadsheet link is for you only. Do not share it.

Both files are also in your Google Drive, called "Enquiry form" and "Enquiries".

### 6. Set the spreadsheet to UK dates

Google Sheets may show dates in US order (MM/DD/YYYY). This happened during the owner's test. To fix it:

1. Open the spreadsheet using the link from the log.
2. Choose **File**, then **Settings**.
3. Under **Locale**, choose **United Kingdom**, then save the settings.

Dates should then show as DD/MM/YYYY. One caution: the script gives the Received and Follow up by columns a fixed layout, such as "Sun 11 Oct 2026 14:30", so those columns may not change. I have not checked column by column which ones do.

### 7. Have a look at the form

Open the form link in your browser. You should see a form titled "Enquiry form" with a short description, then Name, Email address and Your enquiry. The description tells visitors that their details are used only to reply to the enquiry. Check that this is true for how you use them, and change it if not. For your obligations on handling customers' personal information, get qualified advice; this guide cannot give it.

## Test it

Do these tests before you share the link. Use a test name and your own email address.

### Test 1: a normal submission

1. Open the form link and fill in a name, an email address and a message, then submit.
2. Open the spreadsheet and go to the **Enquiries** tab. Refresh the page if nothing appears.
3. Look for a new row with the status **New**.
4. Check the **Follow up by** column. It should show a date and time two days (48 hours) after the **Received** time, and the "Follow-up rule" column should say "48 hours after it arrived".
5. Open the **Activity** tab. There should be a line with the outcome **stored**.

### Test 2: an immediate repeat

1. Submit the form again straight away with exactly the same email address and message. The name is not part of the check.
2. Return to the spreadsheet. The expected result is **no new row** on the Enquiries tab.
3. On the Activity tab you should see a new line with the outcome **repeat ignored**, and a detail saying "same address and message as" followed by the earlier enquiry's reference.

**Please note:** I have not seen this second test work live. See "What has been tested" below.

### Test 3: a different message

Submit once more with the same email address but a different message. This should be stored as a separate row. Afterwards, delete your test rows if you do not want them in your records; the script does not do this for you.

### What has been tested

- **Live test, 11 October 2026:** the owner created a Google account with an Outlook address, pasted the script into a new Apps Script project, ran `setup`, approved the permission screens (including the "hasn't verified this app" warning), and submitted two test enquiries. Both appeared on the Enquiries tab with the status "New" and a follow-up date two days later. The spreadsheet first showed US-format dates, and changing the locale to United Kingdom fixed this.
- **Automated tests:** the script's repeat-detection logic is covered by automated tests.
- **Not yet observed live:** the repeat-ignored path. Nobody has yet watched a repeat submission being ignored in a real form and sheet. If Test 2 does not behave as described, treat that as a fault to look into rather than assuming it is right.

That is the full extent of the testing.

## Limits

### Google's published limits for free accounts

Google publishes limits for Apps Script (the tool this script runs in). For consumer (free) accounts, the page lists:

- triggers total runtime: 90 minutes per day;
- script runtime: 6 minutes per execution;
- triggers: 20 per user per script.

Google also states: "All quotas are subject to elimination, reduction, or change at any time, without notice." (https://developers.google.com/apps-script/guides/services/quotas, checked 11 October 2026.) Treat these as Google's published numbers on that date and check the page for current values. I have not measured how many enquiries the script can handle within them.

### Other limits of the script

- It logs only what the form collects: name, email address and message.
- The repeat check only compares the email address and message text of enquiries within 30 minutes of each other. Messages with even slight differences count as different enquiries.
- It does not tell you when a new enquiry arrives. You need to look at the sheet.
- Anyone with the account's login can see the enquiries, so protect it with a strong password.
- Deleted responses cannot be recovered, according to Google's help page (https://support.google.com/docs/answer/2917686, checked 11 October 2026).
- This guide gives no legal, data-protection or tax advice. If you are unsure about your duties when collecting customers' details, ask a qualified adviser.

### How to switch it off

To stop the script logging enquiries, delete its trigger:

1. Open your project at script.google.com.
2. In the left-hand menu, choose **Triggers** (the alarm clock icon).
3. Find the trigger for `onFormSubmitHandler` and use the three-dot menu at its right to delete it.

Google's documentation says triggers can be added or managed through the Triggers section of the project (https://developers.google.com/apps-script/guides/triggers/installable, checked 11 October 2026). Menu wording may differ from what you see.

Deleting the trigger only stops the logging. The form stays published and can still accept responses unless you close it in the form's own settings.

Deleting the spreadsheet does not delete the form: Google states "Deleting a spreadsheet doesn't delete the form, and vice versa" (https://support.google.com/docs/answer/2917686, checked 11 October 2026).
## Where to get help

No personal setup help is offered with this guide, and I cannot answer individual questions about your account. For help, use Google's own pages:

- Creating a Google Account: https://support.google.com/accounts/answer/27441
- Where form responses are saved: https://support.google.com/docs/answer/2917686
- Apps Script triggers: https://developers.google.com/apps-script/guides/triggers/installable
- Apps Script quotas: https://developers.google.com/apps-script/guides/services/quotas

For questions about the law, data protection or tax, speak to a qualified adviser.

## Sources

- Create a Google Account (Google Account Help): https://support.google.com/accounts/answer/27441 (checked 11 October 2026)
- Choose where to save form responses (Google Docs Editors Help): https://support.google.com/docs/answer/2917686 (checked 11 October 2026)
- Installable Triggers (Apps Script, Google for Developers): https://developers.google.com/apps-script/guides/triggers/installable (checked 11 October 2026)
- Quotas for Google Services (Apps Script, Google for Developers): https://developers.google.com/apps-script/guides/services/quotas (checked 11 October 2026)
- The owner's live test, 11 October 2026: first-hand evidence, not a web page.
- The enquiry logger script (Code-form-only.gs): the source for everything this guide says the script does.

---

Spotted something wrong or out of date? [Report a correction]({{ site.corrections_form }}). This is a self-service guide; we can't offer personal setup help.
