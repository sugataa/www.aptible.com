---
title: "FAQ"
tracked_title: FAQ
description: "Frequently asked questions about Aptible"
posted: 2015-07-21
section: FAQ
layout: 'faq'
---

<h2 id="company">Company</h2>

**What does Aptible do?**

Aptible helps digital health companies secure data and demonstrate HIPAA
compliance.

We have two core products: Our deployment platform is a container service built
on Amazon Web Services. It helps your engineers scale modern web architecture
in secure, private, PHI-ready cloud environments.

Our compliance platform provides comprehensive risk, security, and HIPAA
compliance management.

--------

**What are the benefits of using Aptible?**

The Aptible deployment platform manages servers, network topology, security,
backups, encryption, and backend access so your engineers can focus on building
great products.  Our operations team monitors your stack 24/7 and resolves most
issues before you are even aware of them.

Each PHI­-ready Aptible stack is deployed into a secure, managed network. As a
customer, you receive your own AWS Virtual Private Cloud, with dedicated
infrastructure resources.

Our Managed Accounts also include our SaaS compliance platform, which streamlines and automates the administrative aspects of HIPAA, including risk assessments, policies and procedures, workforce training, and incident response.  As your company grows and your technology changes, your documentation changes along with it.

Many customers report that the most valuable aspect of a Managed Account is our premium audit prep and assistance, to ensure you are able to pass security reviews for your customers, business partners, and HHS.

----------

<h2 id="pricing">
  Pricing
  <a class="side-nav__to-top">↑ Back to top</a>
</h2>

**What is the difference between Platform and Managed Accounts?**

With a Managed Account, Aptible helps you set up and run a comprehensive HIPAA Business Associate compliance program, including risk assessments, policies and procedures, workforce training, incident response, BAA management, and application security management. As a Managed Account partner, our engineering and compliance teams will work with you directly to help you quickly pass security reviews and audits at the largest healthcare institutions in the country.

Platform Accounts are ideal for customers who just want to use the Aptible deployment platform. You can create, run, and scale apps and databases in dedicated, secure, PHI-ready environments.

Managed Accounts include the functionality of Platform Accounts.

----------

**How does pricing work?**

Each Aptible plan has a base price and included resources. After the base fee, simply pay for what you use beyond the included resources. Our [pricing calculator](/pricing) will help find the right plan and estimate your bill.

----------

**Are there discounts at scale?**

Yes, as you add planned capacity, we can offer discounts for larger platform users.

----------

**Do I have to sign a long-term contract?**

No. Platform Account customers can choose a month-to-month option for $1299/mo base. Most customers sign up for a 90-day trial at $999/mo base and continue on annual contracts at that base price.

--------

<h2 id="platform">
  Technology Platform
  <a class="side-nav__to-top">↑ Back to top</a>
</h2>

**What technology can I use with Aptible?**

Any Linux-based language or framework. We have  [Quickstart Guides](/support/quickstart) for many popular languages and databases. No Windows, sorry.

--------

**How can I get a demo of Aptible?**

The best way to find out if Aptible is right for you is to sign up for a [free Development account](https://dashboard.aptible.com/signup?plan=development).  Development Accounts allow you to try all the the functionality of any of our PHI-ready accounts.  That said, if you'd like to talk with us about the platform, don't hesitate to [get in touch](http://contact.aptible.com).

--------

**How many containers will I need?**

It depends on your app and load patterns. We normally recommend opening a Development Account to test your app's performance with standard 1 GB RAM containers. The platform is highly scalable and designed to work with service components. Each service can scale independently, allowing you to adjust your usage to the level that suits your needs best.

--------

**What about lock-in?**

Aptible is designed around open source software and engineering best practices. Configuring your app to deploy is often as easy as adding a single, one-line file to your repo. Should you ever need to migrate, you will not need to re-engineer your architecture.

--------

**What about uptime? Do you have an SLA?**

We provide a [99.95% Service Level Agreement](/legal/service_level_agreement.html) for all dedicated, PHI-ready stacks. Custom SLAs are available upon request.
We report availability for the Aptible services at http://status.aptible.com.

--------

**Where is Aptible hosted? What regions are supported?**

Aptible runs on AWS, so you enjoy the benefits and reliability of the AWS platform. You can currently run your dedicated Aptible stacks in any AWS region except China (Beijing) or GovCloud.

--------

**How should I manage staging environments on Aptible?**

Platform and Managed Accounts include the ability to create both Development (shared) and PHI-ready (dedicated) environments. You stage your apps and databases in either.
Using a Development environment for staging has the benefit of server isolation between staging and production. Many large healthcare customers prefer this.
Dedicated environments may have better performance, especially during long staging builds.
If you want both separation and the best possible performance, you can provision additional dedicated stacks for your staging environments.

--------

<h2 id="glossary">
  Glossary
  <a class="side-nav__to-top">↑ Back to top</a>
</h2>

**Container**

A container is a lightweight virtual machine. Aptible uses Docker to build and run containers. Standard containers are allocated 1 GB of RAM. Higher RAM configurations are available upon request.

--------


**Disk**

Disk storage refers to the underlying volumes used for database storage. Disk storage is encrypted at the filesystem level with 192-bit AES encryption. Aptible manages the encryption keys for you. Disk pricing includes nightly backups for 90 days and monthly backups for 6 years. Backups are stored in a geographic region separate from where your database runs.

--------


**Endpoint**

An endpoint is a networking resource that exposes an app or database service. An SSL/TLS endpoint, for example, is often used to expose a web service to the Internet. Endpoints consist of a DNS service, an AWS Elastic Load Balancer, and at least one NGiNX container.
To configure an SSL/TLS endpoint, register a domain and procure an SSL certificate. (Wildcard, subdomain, and EV certificates all work.) After loading your endpoint with the certificate bundle and private key, you can point your domain's DNS to the endpoint address.
"Internal" endpoints can be used to expose a private service to other services on the same stack. Internal endpoints receive private IP addresses and cannot be accessed from the Internet.

--------


**Service**

A service is comprised of one or more containers running the same process. By adding containers to a service, you can easily and quickly scale. Services run in your stack's app layer (see our [Reference Architecture Diagram](/pages/assets/aptible-reference-architecture.pdf)).

--------


**Environment**

Environments are used to manage permissions. PHI-ready environments run on dedicated stacks. Dev environments run on shared stacks and must not handle PHI. Multiple environments on the same stack do not provide network isolation.

--------


**Stack**

The underlying infrastructure we use to build your environments. Each stack consists of an AWS VPC, EC2 instances, Elastic Load Balancers, Elastic Block Store volumes, and the Aptible platform utilities. Stacks provide network isolation.

--------

<h2 id="compliance">
  Compliance
  <a class="side-nav__to-top">↑ Back to top</a>
</h2>

**How do Business Associate Agreements work?**

You must have a Business Associate Agreement (BAA) in place with Aptible before you can use the Aptible services to create, receive, maintain, or transmit PHI. You will also need to sign BAAs with any other companies that handle PHI on your behalf. You do not need a BAA with AWS unless you intend to use an AWS service directly, such as S3 or RDS.

--------


**What else might I need to comply with HIPAA?**

In addition to a Managed Account, you may want:

  * Third-party services such as analytics, object storage, and messaging;
  * Productivity services, such as Google Apps for Business or Salesforce;
  * Workforce security services, such as password and mobile device management; and
  * Security assessments performed by an independent third party.

Our compliance platform will help you select the most appropriate services and integrate them into your compliance program.

--------


**Is Aptible audited?**

We go through security and compliance audits alongside our customers at the largest entities in healthcare.  In the past year we have passed audits with Kaiser Permanente, MD Anderson, UnitedHealth Group, Johns Hopkins, Stanford, and many others.
