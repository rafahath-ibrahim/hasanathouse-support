# Privacy policy corrections

Five passages to replace in the Notion original, so it matches what the app
actually does. Each one is "find this / replace with this". The published page
at `privacy.html` already has these applied.

Written against the code as of 30 August 2026: no analytics or ad SDK in
`pubspec.yaml`; Anthropic used for moderation (`server.js:592`); messages and
uploads deleted with the account (`server.js:3358`).

---

## 1. Section 3 — third-party list

**Remove this line entirely:**

> **Web and Mobile Analytics** — Google Analytics for Firebase

There is no analytics SDK in the app. Firebase is present for push
notifications only, and is already listed on the line above. Leaving this in
contradicts the "no tracking, no usage data" answers in App Store Connect.

---

## 2. Section 4 — cookies and tracking

**Replace the whole section body with:**

> **In Short:** We do not use cookies, advertising identifiers, or third-party
> tracking technologies.
>
> HasanatHouse is a mobile application and does not use cookies, web beacons,
> pixels, or similar tracking technologies. We do not run advertising, we do not
> use an analytics SDK, and we do not allow third parties to track your activity
> across other apps or websites for advertising purposes.
>
> The only device-level identifier we process is a push notification token,
> which exists solely to deliver the reminders and notifications you have turned
> on. You can revoke it at any time in your device settings.

The original text described advertising, interest-based targeting, abandoned
shopping cart reminders, and a Google Analytics opt-out. None of that applies,
and it directly conflicts with Advertising = No in App Store Connect.

---

## 3. Section 1 — what we collect

**Replace the "Personal Information Provided by You" list with:**

> * email addresses
> * usernames
> * passwords
> * contact or authentication data
> * profile pictures
> * project names, intentions (niyyah), goals, and daily check-in records
> * journal entries and any photographs you attach to them
> * messages you send to an accountability buddy or to a project group
> * posts, comments, and reports you submit to the community

The original listed only the first four, which is roughly a tenth of what the
app stores.

---

## 4. Chat and messaging

**Add to Section 1, after the Application Data block:**

> **Messages.** The app includes private one-to-one messaging with an
> accountability buddy, and group messaging shared between the members of a
> group project. We store the content of these messages, the sender, and the
> time sent, so that they can be delivered and shown in your conversation
> history. Messages are visible to their recipients and to no one else, except
> where a message is reported to us, in which case we may review it to enforce
> our community rules. Your messages are deleted when your account is deleted.

**And replace the "To enable user-to-user communications" bullet in Section 2
with:**

> * **To enable user-to-user communications.** We process your messages so we
>   can deliver them to your accountability buddy or to the members of a group
>   project, and so we can show you your conversation history.

The original policy predates these features and did not describe them.

---

## 5. Section 8 — minimum age

**Replace "18" with "13" throughout the section**, so it reads:

> **In Short:** We do not knowingly collect data from or market to children
> under 13 years of age.
>
> We do not knowingly collect, solicit data from, or market to children under 13
> years of age, nor do we knowingly sell such personal information. By using the
> Services, you represent that you are at least 13 years of age. If we learn
> that personal information from users less than 13 years of age has been
> collected, we will deactivate the account and take reasonable measures to
> promptly delete such data from our records. If you become aware of any data we
> may have collected from children under age 13, please contact us at
> hello@hasanathouse.com.

18 is unusually restrictive for a habit tracker and excludes the teenagers most
likely to benefit. 13 is the common floor and matches the age rating the App
Store questionnaire will produce for an app with open chat and a community feed.

Keep 18 instead if you genuinely want an adults-only service — but then the
sign-up screen should ask, because right now the app collects no age at all and
the claim is unenforceable either way.
