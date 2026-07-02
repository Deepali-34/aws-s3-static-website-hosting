# Amazon S3 Bucket Policy

## Overview

Amazon S3 Bucket Policies are JSON-based access control documents that define permissions for resources stored within an Amazon S3 bucket. In this project, a bucket policy was configured to allow public read access to the website files, enabling users to access the hosted static website through the generated website endpoint.

---

# Objective

The primary objective of the bucket policy is to:

- Allow public users to access website files.
- Enable Amazon S3 Static Website Hosting.
- Maintain secure administrative control while exposing only the required objects.
- Ensure that website resources are publicly accessible without compromising bucket management permissions.

---

# Bucket Policy Used

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```

> Replace **YOUR-BUCKET-NAME** with the name of your Amazon S3 bucket.

---

# Policy Explanation

## Version

Specifies the policy language version.

```
2012-10-17
```

---

## Statement

Defines one or more permission rules.

---

## Effect

```
Allow
```

Grants permission for the specified action.

---

## Principal

```
*
```

Represents all users on the internet.

---

## Action

```
s3:GetObject
```

Allows users to retrieve objects stored inside the bucket.

---

## Resource

```
arn:aws:s3:::YOUR-BUCKET-NAME/*
```

Specifies that every object inside the bucket can be publicly accessed.

---

# Security Considerations

While public read access is required for hosting a static website, administrative permissions remain restricted to authorized AWS users through IAM. Only object retrieval is permitted, preventing unauthorized users from uploading, modifying, or deleting website files.

---

# Best Practices

- Grant only the minimum permissions required.
- Restrict write access to authorized IAM users.
- Regularly review bucket policies.
- Enable versioning for production environments.
- Monitor bucket access using AWS CloudTrail or AWS CloudWatch.

---

# Summary

The configured bucket policy enables secure public access to the website's static resources while maintaining administrative control over the Amazon S3 bucket. This configuration is a fundamental requirement for hosting publicly accessible static websites using Amazon S3.
