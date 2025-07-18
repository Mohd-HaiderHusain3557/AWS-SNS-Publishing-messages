# 📩 AWS SNS Notification Setup (Email & SMS)

This guide walks you through creating an Amazon SNS topic and publishing a message to both **email** and **SMS** recipients using 11 simple steps.

---

## ✅ Steps to Publish a Message via AWS SNS

- **Step 1: Login / Sign Up**
  - Visit [https://aws.amazon.com](https://aws.amazon.com) and sign in to your AWS account.
  - If you don't have an account, click “Create an AWS Account” and complete the signup process.
  - Once signed in, search for **SNS** in the AWS Console.

- **Step 2: Navigate to SNS Console**
  - Open the SNS (Simple Notification Service) from the AWS Management Console.
  - Click on **Topics** in the sidebar.

- **Step 3: Create a New Topic**
  - Click **Create topic**.
  - Choose **Standard** as the topic type.
  - Provide a name for your topic (e.g., `MyNotificationTopic`).
  - Click **Next step**, then **Create topic**.

- **Step 4: View Topic Details**
  - Once the topic is created, you'll see its details.
  - Note the **Topic ARN**, which is used to identify this topic.

- **Step 5: Subscribe an Email Endpoint**
  - Click **Create subscription**.
  - Select **Protocol: Email**.
  - Enter the email address you want to notify.
  - Click **Create subscription**.

- **Step 6: Confirm Email Subscription**
  - The email recipient will receive a confirmation mail.
  - They must click the **confirmation link** to activate the subscription.

- **Step 7: Subscribe an SMS Endpoint**
  - Create another subscription.
  - Select **Protocol: SMS**.
  - Enter a valid mobile number with country code (e.g., `+919812345678`).
  - Click **Create subscription** (no confirmation required).

- **Step 8: Check Subscription Status**
  - Go back to the topic’s details page.
  - Email will show as **Pending** until confirmed.
  - SMS will show as **Confirmed** immediately.

- **Step 9: Publish a Message**
  - Click **Publish message** under the topic.
  - Enter a **subject** (only for email) and a **message body**.
  - Select **Send to all subscriptions**.

- **Step 10: Confirm Publish**
  - Click **Publish message** to send notifications.
  - Email and SMS subscribers will receive the message accordingly.

- **Step 11: Verify Delivery**
  - Email subscriber receives full message with subject.
  - SMS subscriber receives plain message text.
  - You can monitor deliveries and failures in the **CloudWatch** or **SNS metrics**.

---
