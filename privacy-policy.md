# Privacy Policy: Unabridged (formerly AI Chat Exporter)

Effective date: October 22, 2026

Last updated: October 29, 2026

Unabridged (formerly AI Chat Exporter) ("the Extension") is published by **CCE Partners LLC** ("we", "us"), 2501 Chatham Rd #4369, Springfield, IL 62704, USA. Contact: support@hichrisgrant.com. This policy applies to the Google Chrome version of the Extension, distributed through the Chrome Web Store (item bikcjbaffadliihjcbodbkddhlnpahhf). The Firefox and Microsoft Edge versions (version 0.2.8) work differently in two respects, described in "Firefox and Microsoft Edge versions" below.

## Summary
- The Extension turns the AI chat you are viewing into a file that your browser downloads. Your conversations are processed **only inside your browser**. They are never sent to us, to our payment providers or to anyone else.
- **Free exports contact no server of ours or of our payment provider.** The only request a free export makes is on ChatGPT, where the Extension asks ChatGPT's own website for the conversation you are viewing (see below). This holds even if you have an installation key from an earlier Unlock Pro or Restore purchase; with a key, only using Pro or visiting ExtensionPay's own pages can trigger a licence check (see Licence checks).
- **The only other network contact is ExtensionPay (extensionpay.com)**, our payment provider, and only for Pro: when you use a Pro feature, unlock or restore Pro, or visit ExtensionPay's own pages (such as its checkout or account pages). Those requests carry an installation key, never your chats.
- We run no server that receives data from the Extension. The Extension has no analytics, telemetry, advertising or tracking, and loads no remote code.

## What the Extension accesses
- **The chat page you are viewing on a supported site** (chatgpt.com, chat.openai.com, claude.ai, gemini.google.com, grok.com, perplexity.ai, www.perplexity.ai), **only when you click an export button**. The conversation is read and converted to a file in your browser.
- **ChatGPT (same-site request):** on chatgpt.com and chat.openai.com, when you click export, the Extension asks ChatGPT's own website, using your existing logged-in session, for the conversation you are viewing (the same kind of request the ChatGPT page itself makes). This request goes only to ChatGPT (OpenAI), never to us or anyone else. The temporary session token it uses is held in memory for that one export and is never stored or sent anywhere else. If the request fails, the Extension reads the conversation from the page instead.
- **`activeTab` and `scripting`:** when you open the Extension's popup on a supported chat tab that was open before the Extension was installed or updated, these let it load its own packaged exporter code into that one tab, so export works without reloading the page. They give no access to other tabs or sites.
- **"Export all open AI chats" (Pro):** the Extension sends an export request to your open tabs; only tabs on the supported sites, where its exporter is running, respond and save a file. It does not read the addresses or content of other tabs.
- **`storage`:** see "What is stored in your browser" below.

## Pro purchases: what ExtensionPay and Stripe receive (Pro buyers only)
Pro is optional: a **$4.99 one-time purchase, no subscription**. It adds JSON export, PDF export (through your browser's print dialog) and exporting every open AI chat in one click. Like the free export, these files are created inside your browser. Pro is sold through **ExtensionPay** (extensionpay.com), a payment service for browser extensions, and paid through **Stripe**, which processes the card payment.

- **The first time you click Unlock Pro or Restore purchase:** the Extension asks ExtensionPay to create an **installation key**, a random identifier for your copy of the Extension. This request contains no personal data, but like any web request it reveals your IP address and browser type to ExtensionPay. The Extension then opens ExtensionPay's checkout page in a new tab (or, for Restore purchase, ExtensionPay's login page in a small window).
- **On the checkout pages (ExtensionPay / Stripe Checkout):** you type your **email address** and **payment details** directly into those web pages, not into the Extension. **Stripe** processes the payment details. **ExtensionPay** receives your email address and the purchase record (for example amount, date and paid status) and links them to your installation key. The Extension never sees your card details.
- **Licence checks:** each time you use a Pro feature, and whenever you visit one of ExtensionPay's own pages (for example its checkout, payment-confirmation or account-management pages), the Extension sends ExtensionPay your **installation key** and nothing else from the Extension. While such a page is open, ExtensionPay's library can repeat this check about once per second for up to two minutes, without any click in the Extension. If you have never clicked Unlock Pro or Restore purchase, there is no key and nothing is sent. ExtensionPay answers with your licence status (whether and when you paid, and the email linked to the purchase). The Extension itself uses only the paid / not-paid answer. If ExtensionPay can't be reached, Pro keeps working offline for up to 7 days after your last successful check.
- **Opening the popup never contacts ExtensionPay.** The popup shows Pro as unlocked or locked from the last result saved on your device. (Visiting ExtensionPay's own pages can, as described under Licence checks.)
- **ExtensionPay's pages:** the Extension includes ExtensionPay's small script that runs only on extensionpay.com pages, so those pages can tell the Extension when a purchase is complete or your account has changed. That is what starts the repeated licence check described above.
- **Using Pro on another device or after reinstalling:** click **Restore purchase** and log in on ExtensionPay's page with the email you paid with.
- **Never sent** to ExtensionPay or Stripe: your conversations, chat titles, the addresses of the pages you visit, or your ChatGPT session.
- **What we receive:** as the seller, CCE Partners LLC can see the purchase record (your email, amount and date) in our ExtensionPay and Stripe accounts. We use it only for accounting, support and refunds, and keep it only as long as legally required.
- Stripe's privacy policy: https://stripe.com/privacy. ExtensionPay describes how it handles user data in the FAQ on its website (https://extensionpay.com, "What about user privacy?"). For questions about it, contact us and we will help.

## What is stored in your browser
- The Extension stores **no conversation content**. Exported files go to your Downloads folder like any other download, and you control them.
- Everything the Extension stores is kept in the browser's **local extension storage** (`chrome.storage.local`), **on this device only**. Nothing is written to Chrome sync storage.
- The Extension's own settings: **whether Pro is unlocked** (`cce.license`: paid yes/no and when it was last checked), a one-time "Pro unlocked" note (`cce.proWelcome`), and when the Pro hint was last shown or dismissed (`cce.nudge`).
- When the Extension first runs, the ExtensionPay library records the date it was installed (`extensionpay_installed_at`). This date is not sent anywhere.
- **Only if you click Unlock Pro or Restore purchase:** the ExtensionPay library also stores the **installation key** (`extensionpay_api_key`) and your latest **ExtensionPay status** (`extensionpay_user`: paid status and date and the email you paid with).
- **If you are updating from version 0.2.2 or earlier:** those versions kept the ExtensionPay items above in Chrome's sync storage. The Extension reads (never writes) its old sync data to migrate existing purchases: it copies those items into local storage, without any network request, so an existing purchase keeps working. Until an installation key is found there or this device has its own (for example, if you never clicked Unlock Pro or Restore purchase, or sync hasn't finished downloading yet), it repeats this read, on this device only, when the Extension is installed or updated and before a Pro feature, Unlock Pro or Restore purchase. After that, `cce.syncMigrated` records that the migration is done and sync storage is not read again. It never changes or removes anything in sync storage.
- Uninstalling the Extension removes its local storage from your browser.

## What we do not do
- We do not collect, sell, rent or transfer your conversations or browsing data.
- We use payment data only for the Pro purchase and licence check, and never for advertising, creditworthiness or lending.
- No remote code: all code, including ExtensionPay's library (ExtPay.js 3.1.2, minimally modified so it uses local storage instead of sync storage), ships inside the Extension package.
- The source of the modified ExtPay.js used in the Chrome version, with its licence notice, is published at https://chrisgrant303.github.io/ai-chat-exporter/third-party/ExtPay.js (licence details: https://chrisgrant303.github.io/ai-chat-exporter/third-party/README.md).
- The Extension's use of information complies with the Chrome Web Store User Data Policy, including the Limited Use requirements.

## Firefox and Microsoft Edge versions
This section applies only to Unabridged on Firefox (addons.mozilla.org) and Microsoft Edge (Edge Add-ons), version 0.2.8. Everything above applies to them too, except where this section differs.

- **Unmodified ExtPay.js and sync storage:** these versions use the unmodified ExtensionPay library (ExtPay.js 3.1.2), which keeps its data in the browser's **sync storage** (`storage.sync`), not only on this device. (It uses local storage on this device only if sync storage is unavailable.) Firefox may copy sync storage to your other devices if you use Firefox Sync with add-on data syncing turned on; Microsoft Edge may copy it to your other devices where you are signed in to Edge with sync turned on. The items are the same ExtensionPay items listed above (`extensionpay_installed_at`, and after you click Unlock Pro, `extensionpay_api_key` and `extensionpay_user`). These ExtensionPay items are not copied to local storage. As in the Chrome version, the Extension's own settings (`cce.*`, listed above) are kept in local storage on this device only. Uninstalling the Extension removes its storage from this browser; copies held by your browser's sync service are removed according to that service's own rules.
- **Firefox: consent first.** The Firefox version declares no required data collection. When you click **Unlock Pro**, Firefox asks you to allow three optional data-collection categories: **authentication information**, **financial and payment information** and **personally identifying information**. Until you allow them, the Extension makes no ExtensionPay request at all (no installation key, no checkout, no licence check) and Pro stays locked. If you later remove that permission (in about:addons), the Extension reloads and stops contacting ExtensionPay.
- **Licence checks:** the same as in the Chrome version, described above: opening the popup never contacts ExtensionPay, and ExtensionPay is contacted only when you use a Pro feature, unlock or restore Pro, or visit ExtensionPay's own pages (where, if you already have an installation key, the unmodified ExtensionPay library checks about once per second for up to 2 minutes, without any click in the Extension), and never with your chats. On Firefox, none of this happens until you have allowed the optional permission. Pro keeps working offline for up to 7 days after your last successful check, as in the Chrome version.

## Children
The Extension is not directed to children under 13.

## Not affiliated
Unabridged is an independent tool made by CCE Partners LLC. It is not affiliated with, endorsed by or sponsored by OpenAI, Anthropic, Google, xAI or Perplexity AI. Their product names and trademarks are used only to describe compatibility.

## Changes
We will post updates on this page and change the effective date.

## Contact
CCE Partners LLC, 2501 Chatham Rd #4369, Springfield, IL 62704, USA: support@hichrisgrant.com
