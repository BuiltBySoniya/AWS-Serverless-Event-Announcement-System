# 🚀 AWS Serverless Event Announcement System

Serverless Event-Driven Notification Platform on AWS

## Short Description

Built a scalable, event-driven system using AWS serverless services to capture event announcements (such as marketing campaigns, alerts or system events) and push real-time notifications to subscribers via email/SMS—with minimal infrastructure management.

## 🛠️ AWS Services Used:

Amazon EventBridge,
AWS Lambda,
Amazon SNS,
Amazon DynamoDB,
AWS IAM,

## 🧰 Technical Tools:

Node.js (or Python) Lambda Functions,
AWS CLI,
CloudFormation or AWS SAM for deployment,

## 🧠 Skills Demonstrated:

Event-driven architecture design,
Real-time notification workflows,
Serverless integration across AWS services,
Subscription and alerting mechanisms,

## 📋 Steps Performed

### Set Up Event Bus and Rules:

Created an EventBridge event bus named `event-announcement-bus`.
Defined rules that match announcement-type events, triggering downstream workflows when events arrive.

### Create DynamoDB Subscription Table:

Provisioned a DynamoDB table `Subscribers` with partition key `subscriberId`.
Stored metadata for subscribers including email, phone number, preferences and the event-types they subscribe to.

### Develop Lambda Notification Handler:

Built a Lambda function (`handleAnnouncement`) that gets triggered by EventBridge.
The Lambda reads the event payload, queries the `Subscribers` table for matching subscribers, and publishes messages via SNS based on their preferences.

### Configure Amazon SNS Topics and Subscriptions:

Created SNS topics for each channel (email, SMS).
Subscribed endpoints (email addresses, phone numbers) to the relevant SNS topics.
Configured SNS using topics & subscriptions for fan-out notification delivery.

### Deploy, Test & Monitor Workflow:

Deployed the stack using AWS SAM/CloudFormation.
Published test announcement events into EventBridge.
Confirmed notifications were delivered, verified logs in CloudWatch, and validated handling of multiple subscribers and channels.

## ✅ Final Result:

Real-time Event Announcement & Notification System

## 💼 Business Implication:

This serverless platform enables organizations to broadcast critical event announcements instantly across multiple channels without maintaining servers. It supports high-scale, cost-efficient delivery of alerts—ideal for product updates, infrastructure alerts, promotional campaigns or operational notifications—while focusing on business logic instead of infrastructure.
