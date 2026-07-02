# AWS Services Used

## Overview

This document describes the AWS services and configurations used in the AWS S3 Static Website Hosting project. Each service plays a critical role in deploying, securing, and managing the static website hosted on Amazon Web Services (AWS).

---

# Amazon S3 (Simple Storage Service)

## Description

Amazon S3 is a highly durable, scalable, and secure object storage service provided by AWS. It is designed to store and retrieve any amount of data from anywhere on the web.

## Purpose in this Project

- Hosted the static website.
- Stored website source files (HTML, CSS, JavaScript, images, and media).
- Generated a public website endpoint for users.

## Key Features

- Highly scalable storage
- 99.999999999% (11 9's) durability
- Cost-effective cloud storage
- Static Website Hosting support

---

# Static Website Hosting

## Description

Static Website Hosting is an Amazon S3 feature that enables a bucket to serve web pages directly over HTTP.

## Purpose in this Project

- Hosted the website without requiring a traditional web server.
- Configured the landing page using `index.html`.
- Enabled public access through the S3 website endpoint.

## Benefits

- Simple deployment
- High availability
- Low maintenance
- Cost-efficient hosting

---

# AWS Identity and Access Management (IAM)

## Description

AWS IAM is a security service that manages authentication and authorization for AWS resources.

## Purpose in this Project

- Managed secure access to AWS resources.
- Controlled administrative permissions.
- Protected cloud resources from unauthorized access.

## Key Features

- User management
- Role-based access control
- Permission policies
- Secure authentication

---

# Amazon S3 Bucket Policy

## Description

A Bucket Policy is a JSON-based access policy attached directly to an Amazon S3 bucket.

## Purpose in this Project

- Allowed public read access to website files.
- Defined permissions for visitors accessing the website.
- Ensured secure object-level access.

---

# Public Access Configuration

## Description

Amazon S3 Public Access settings control whether bucket objects are accessible over the internet.

## Purpose in this Project

- Enabled public website access.
- Configured the required permissions for website hosting.
- Worked together with Bucket Policies to allow users to view website content.

---

# AWS Management Console

## Description

The AWS Management Console is a web-based interface used to manage AWS resources.

## Purpose in this Project

- Created and configured the S3 bucket.
- Uploaded website files.
- Managed bucket policies and permissions.
- Enabled Static Website Hosting.

---

# Summary

The AWS S3 Static Website Hosting project demonstrates the integration of multiple AWS services to build a secure, scalable, and cost-effective cloud-hosted static website. Amazon S3 serves as the hosting platform, IAM manages security and permissions, Bucket Policies define public access rules, and Static Website Hosting enables web content to be delivered directly to users through a public endpoint.
