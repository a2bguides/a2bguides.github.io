---
layout: page
title: "Keeping track of enquiries: a starter guide to basic and automated options"
permalink: /guides/enquiry-tracking/
description: "How a solo trade or service business can log every enquiry once and follow up on time, with a free spreadsheet method and a comparison of Make, n8n and Zapier."
---

> **Last checked: 11 October 2026.** Vendor details below were checked on each vendor's own page on that date. Prices and plans change, so check the vendor's page before deciding.

> **Free spreadsheet** (Excel files that also open in Google Sheets and Numbers):
>
> - [Enquiry log]({{ '/downloads/a2b-enquiry-log.xlsx' | relative_url }}){: data-goatcounter-click="download-enquiry-log" data-goatcounter-title="Enquiry log" } (sets a 2-day follow-up date and flags anything waiting for a reply)
>
> Free to use. No sign-up.

## Who this is for

This guide is for solo service businesses and freelancers in the UK and other English-speaking countries: cleaners, tradespeople, designers, bookkeepers, coaches and similar. You receive enquiries by email and through a website form, and you are choosing your first way to keep track of them.

The aim is simple:

1. Capture every enquiry once.
2. See its status at a glance.
3. Know when to follow up.

You do not need to buy anything to do this. Start with the simplest approach that works, and add tools only when a specific problem justifies them.

## Free or basic option

The basic approach uses two things you probably already have: an email account and a spreadsheet.

**Step 1: Make one place where enquiries land.** Create one label (in Gmail) or folder (in Outlook) called "Enquiries".

- In Gmail, labels help you organise your email. Gmail's own help page says labels are different from folders, and that only you can access your labels; the people you email do not get them ([Gmail Help: labels](https://support.google.com/mail/answer/118708), checked 2026-10-11). A Gmail filter can apply a label to matching emails automatically: use the search options in the search bar, enter something that identifies your form emails (for example the sender address or subject line), click "Create filter" and choose the label ([Gmail Help: filters](https://support.google.com/mail/answer/6579), checked 2026-10-11).
- In Outlook, a rule can move matching messages to a folder. In most versions you right-click a message, choose "Rules" and then "Create rule", and pick the folder ([Microsoft Support: rules in Outlook](https://support.microsoft.com/en-gb/office/manage-email-messages-by-using-rules-in-outlook-c24f5dea-9465-4df4-ad17-a50704d66c59), checked 2026-10-11).

**Step 2: Make a simple spreadsheet.** Use any spreadsheet app, with one row per enquiry and these columns:

| Column | What goes in it |
|---|---|
| Received | Date and time the enquiry arrived |
| Name | The person's name |
| Email | Their email address |
| Message | A short summary or the full text |
| Status | New, Replied, Quote sent, Won, Lost |
| Follow up by | Received date and time plus 48 hours (or your own rule) |

**Step 3: Add each enquiry once.** When a new enquiry arrives, add a row to the sheet. Then mark the email as logged:

- **In Outlook:** move the email from the "Enquiries" folder into a second folder called "Logged".
- **In Gmail:** first create a second label called "Logged". Then tick the box next to the email, click the Labels button at the top, untick "Enquiries" and tick "Logged". Gmail Help describes these steps under "Move an email to another label" ([Gmail Help: labels](https://support.google.com/mail/answer/118708), checked 2026-10-11). Make sure "Enquiries" is unticked, or the email will still show under that label.

Anything still under "Enquiries" has not been recorded yet. Before adding a row, search the sheet for the person's email address. If the identical message is already there, do not add it again.

**Step 4: Check the sheet at a fixed time each day.** Sort by "Follow up by" and deal with anything due. If your spreadsheet offers colour rules (often called conditional formatting), you can shade rows whose date has passed, but sorting works just as well.

### Honest limits of the basic option

- It relies on you. If you skip a day, enquiries wait.
- Nothing stops you entering the same enquiry twice or leaving a field empty.
- It does not remind you unless you look at the sheet.
- It becomes awkward if several people share the work or enquiries arrive in large numbers.

For many solo businesses, none of these limits is serious enough to justify a paid tool. Whether it is enough for you depends on how many enquiries you get and how often one slips through. This guide has no measured figures on that, so judge it from your own experience.

## Automation options

Automation tools connect your form or inbox to a spreadsheet and do the logging for you. They can add the row, check for repeats and set the follow-up date without you doing it by hand.

### When automation is worth considering

- You have lost or forgotten enquiries more than once, even with the basic method.
- Entering rows by hand is a task you keep putting off.
- Enquiries arrive when you cannot log them (evenings, or while on a job).

### When it is probably not worth it

- You get few enquiries and your spreadsheet is up to date.
- Learning a new tool would cost more time and money than the problem does.
- Your enquiries are too varied for simple rules (for example, long phone-call notes).

Automation also adds its own failure points. A connection can stop working without warning, so you need to check it now and then.

### Three tools to look at

The figures below are copied from each vendor's own pricing page as it appeared on 11 October 2026. They may differ for you depending on your country, currency and the billing option you choose.

**Make** ([pricing page](https://www.make.com/en/pricing), checked 2026-10-11)

- Free plan: $0 a month, with 1,000 credits a month and a maximum of 2 active scenarios (a "scenario" is one automation). Scheduled runs can be no more often than every 15 minutes.
- Cheapest paid plan: "Core", shown as $9 a month for 10,000 credits a month.
- Make counts usage in credits. The page says most actions use 1 credit, so one enquiry passing through several steps uses several credits.
- The page has a "Pay monthly / Pay annually" switch and says paying annually saves "15% or more". When checked, the page did not make clear whether the $9 figure is the monthly or the annual rate, so check this on the page yourself.

**n8n** ([pricing page](https://n8n.io/pricing/), checked 2026-10-11)

- No permanent free hosted plan is listed. The hosted plans offer a free trial with no card needed, and the page's questions section says the trial includes 1,000 executions (an "execution" is one run of a workflow).
- Cheapest paid hosted plan: "Starter", €20 a month billed annually, with 2,500 executions a month. The page says annual billing saves 17% but did not show the monthly-billing price.
- n8n can also be installed on your own server. n8n's documentation says that "Without a license key, n8n runs as the free Community edition" ([n8n Docs: hosting](https://docs.n8n.io/hosting/), checked 2026-10-11). Running your own server is a technical job, so most non-technical readers should treat this as not suitable for a first system.

**Zapier** ([pricing page](https://zapier.com/pricing), checked 2026-10-11)

- Free plan: $0, with 100 tasks a month, two-step automations only ("Zaps") and checks for new data every 15 minutes. Premium apps and webhooks are not included.
- Cheapest paid plan: "Professional", $19.99 a month billed yearly or $29.99 billed monthly, for 750 tasks a month.
- The page says prices are set in US dollars, and payments in other currencies are converted at the exchange rate when you pay, so the amount in pounds can vary between bills.

### Things to check on each pricing page

- Whether the free plan is enough for the number of enquiries you get each month, and how the tool counts usage (per step or per run).
- Whether the price shown is for monthly or yearly billing.
- The currency, and whether VAT is shown. If you have questions about how a purchase affects your business accounts, ask an accountant; this guide does not give tax advice.

A sensible approach is to try a free plan or free trial with a few test enquiries before relying on it for real ones. You are never required to pay, and the basic option above may be all you need.

## Worked example

This example uses fictional test data. Imagine your process receives **10 deliveries**. A delivery is one message arriving from your form or inbox. Here is what happens to them.

| Result | Count | What happens |
|---|---|---|
| Stored as new enquiries | 7 | Each gets one record |
| Repeated delivery of an enquiry already stored | 1 | Ignored; no second record |
| Invalid, rejected with a reason | 2 | Not stored; the reason is noted |
| **Total deliveries** | **10** | 7 + 1 + 2 = 10 |

**The repeated delivery.** One enquiry arrives twice, with the same sender, the same message and the same time. This can happen when a form or tool resends a message it thinks did not go through. The second copy is recognised as the same enquiry and ignored. So 8 of the 10 deliveries are valid, but only 7 are unique enquiries.

**The two rejected enquiries.**

1. **A malformed email address.** For example, the address is missing the "@" sign. Reason recorded: "email address not valid". You cannot reply to it, so it is not stored as an enquiry.
2. **A missing message and an unreadable time.** The form arrived with no message, and the arrival time could not be read. Reason recorded: "message missing; received time unreadable". Without a time, a follow-up date cannot be worked out, so the item is rejected rather than stored half-complete.

Both rejected items go into a separate "Rejected" list with their reasons, so nothing disappears silently. You can glance at that list and decide whether anything needs a manual reply.

**Two enquiries from the same person.** Among the 7 stored enquiries, one person has sent two *different* enquiries: say, one about a regular kitchen clean and a separate one about an end-of-tenancy clean. These stay as **two separate records**. Only an identical repeat delivery counts as a duplicate. A different message from the same person is a new enquiry, and merging the two could hide a job.

**Follow-up dates.** Every stored enquiry gets a follow-up date **48 hours after it arrived**. For example, an enquiry that arrived at 09:30 on Monday is due for follow-up at 09:30 on Wednesday. In most spreadsheets, if the received date and time is in cell A2, typing `=A2+2` in the "Follow up by" column adds two days. An automation tool would do the same sum for you.

**What you would see at the end:** 7 records, each with a name, a valid email address, a message, a received time, a status of "New" and a follow-up time 48 hours later, plus 2 rejected items with their reasons.

You can do all of this by hand with the basic option. Automation simply does the checking and the date sum for you.

## Common failure points

**Duplicate deliveries.** Forms and tools sometimes send the same message twice. Before adding a record, check for an identical sender, message and time. Do not remove a second enquiry from the same person if the message is different.

**Missing fields.** An enquiry without a usable email address or message is hard to act on. Decide in advance what is required (we suggest a valid email address, a message and a received time) and where rejected items go, so they are not lost.

**Follow-ups that slip.** A follow-up date is only useful if you look at it. Pick a fixed time each day to check the list, sorted by follow-up date. If you automate, make sure any reminder goes somewhere you will actually see it.

**Silent breakage.** If you use automation, send a test enquiry through your own website form from time to time and check that it appears.

## Where to get product support

This business does not provide support for any of these products. For help, go to each vendor's own help pages:

- **Gmail:** [Gmail Help on labels](https://support.google.com/mail/answer/118708) and [Gmail Help on filters](https://support.google.com/mail/answer/6579) (both checked 2026-10-11)
- **Outlook:** [Microsoft Support on Outlook rules](https://support.microsoft.com/en-gb/office/manage-email-messages-by-using-rules-in-outlook-c24f5dea-9465-4df4-ad17-a50704d66c59) (checked 2026-10-11)
- **Make:** [Make Help Centre](https://help.make.com/) (checked 2026-10-11)
- **n8n:** [n8n Docs](https://docs.n8n.io/) (checked 2026-10-11)
- **Zapier:** [Zapier Help Center](https://help.zapier.com/) (checked 2026-10-11)

## Referral disclosure

This business may, in future, earn a commission if you buy a product through some of the links in our guides. This draft contains **no referral, affiliate or tracking links**, and we have not joined any referral scheme. Our recommendations do not depend on commission, and a free option is recommended wherever it is enough.

If we add referral links later, we will label them clearly before you reach the content they relate to. The UK Advertising Standards Authority's guidance says marketing must be "obviously identifiable as such", and that for blog posts and social media posts "A disclaimer of this nature at the bottom of such a post is unlikely to be sufficient" ([ASA: affiliate marketing](https://www.asa.org.uk/advice-online/affiliate-marketing.html), checked 2026-10-11).

## Limits

- This is a self-service guide. No personal setup help is offered.
- Prices, free tiers and features change. The figures here were checked on 11 October 2026; always check the vendor's own page before deciding.
- This guide does not give financial, legal or tax advice. If you have questions about data protection, VAT or your accounts, ask a qualified professional.
- The worked example uses fictional test data and is not a measure of how any tool will perform for you.

## Sources

Each page below was opened and read on the date shown.

- https://www.make.com/en/pricing (checked 2026-10-11): Make plans, credits and free-plan limits
- https://help.make.com/ (checked 2026-10-11): Make Help Centre
- https://n8n.io/pricing/ (checked 2026-10-11): n8n plans, trial and executions
- https://docs.n8n.io/hosting/ (checked 2026-10-11): n8n free Community edition
- https://docs.n8n.io/ (checked 2026-10-11): n8n documentation
- https://zapier.com/pricing (checked 2026-10-11): Zapier plans, tasks, free-plan limits and currency
- https://help.zapier.com/ (checked 2026-10-11): Zapier Help Center
- https://support.google.com/mail/answer/118708 (checked 2026-10-11): Gmail labels, including that labels are different from folders and how to move an email to another label
- https://support.google.com/mail/answer/6579 (checked 2026-10-11): Gmail filters
- https://support.microsoft.com/en-gb/office/manage-email-messages-by-using-rules-in-outlook-c24f5dea-9465-4df4-ad17-a50704d66c59 (checked 2026-10-11): Outlook rules
- https://www.asa.org.uk/advice-online/affiliate-marketing.html (checked 2026-10-11): ASA guidance on affiliate marketing

---

Spotted something wrong or out of date? [Report a correction]({{ site.corrections_form }}). This is a self-service guide; we can't offer personal setup help.
