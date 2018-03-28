---
layout: post
title: Cashflow PA
subtitle: v1.0 Release and Roadmap
---

## v1.0 Release

Cue the ham horn because [Cash Flow PA](http://cashflowpa.org) v1 is up!
Please check it out when you can and search for some locations and filers.

Prior to the release, we finished up the site architecture and then polished up the functionality with a few last minute revisions.

Here's an example:
![Cashflow PA query plan](/img/cashflow-pa/cashflow-pa-query_plan.png)
Take note of the planning time and execution time in the middle as compared to the old query times at the bottom. We condensed the time for each database query by about 2/3rds!

### Governor's Office presentation

On March 14th, the PhRIG team got together for a Skype conversation with members of the Pennsylvania Governor’s Office, the Secretary of Administration, the State CIO, and the Innovation Architect, and other executives from the PA Department of State. We showed them our site, discussed the obstacles we overcame, and answered questions about it. Our audience gave us a positive response and said they'd need some time to play around with the site and get back to us.

## Roadmap:

With the v1 rollout, we can now focus on shoring up the site so it remains functional and informative for future development. Here are the main points we want to work on:

### Tests!

<details>
  <summary>
    Show details
  </summary>
  <ul>
    <li>We need meaningful tests. We want to shoot for 80% coverage.</li>
    <li>Add Rubocop to lint code</li>
    <li>Set up CI integration</li>
    <li>Cause deploys to fail if tests to not pass</li>
    <li>Have some very basic integration testing</li>
  </ul>
</details>

### Refining the data

<details>
  <summary>
    Show details
  </summary>
  <p>The data is occasionally inconsistent. For example, sometimes records come in with bad or missing addresses. Here are some ways to fix that.</p>
  <ul>
    <li>Provide documentation of the basic state of our data and put it in the README</li>
    <li>When we find errors in the original data, we will collect them in a spreadsheet   that we will share with our contacts at the government in an effort to help them in the future.</li>
    <li>Figure out what is going on with the lat and longs placing objects in the wrong continent.</li>
    <li>Add approximate geocoding for bad / crufty addresses.</li>
    <li>Add corrected columns for data we add. Eg. if we find addresses that we want to add, we cannot just edit the address. A corrected address should be stored in its own field.</li>
  </ul>
</details>

### Site deployment and reliability

<details>
  <summary>
    Show details
  </summary>
  <p>We need to write an SOP for site deployment and install tools that help make the site reliable. Here's what we need to monitor:</p>
  <ul>
    <li>Free space</li>
    <li>Database is running</li>
    <li>Rails is running</li>
    <li>NGINX is running</li>
    <li>404 check</li>
    <li>CPU usage</li>
    <li>Ram usage</li>
    <li>Latency</li>
    <li>Log for error messages</li>
  </ul>
</details>

#### Further on out

As we move forward with the project, we'd like to visualize data with charts and graphs, and we'd also like to take the site on the road to conferences like Barcamp Philly.

We'll post more details soon!
