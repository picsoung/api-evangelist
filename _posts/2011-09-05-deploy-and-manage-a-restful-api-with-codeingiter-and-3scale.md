---
layout: post
title: 'Deploy and Manage a RESTful API with CodeIngiter and 3Scale'
url: 'http://apievangelist.com2011/09/05/deploy-and-manage-a-restful-api-with-codeingiter-and-3scale/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/3scale-500.png'
---
{% include JB/setup %}

     <a href="http://www.3scale.net/" target="_blank"><img src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/3scale-logo.jpg"  width="250" align="right" /></a>At Mimeo, my API developers were running into problems integrating with our cloud print API, I needed a fast way to virtualize and deploy an API built on top of my existing REST API.  A quick and dirty way I could research and develop new APIs, launch, measure and manage without getting IT involved.  <br />
     <br />
     So I <a title="virtualized four document APIs" href="http://apievangelist.com/2011/09/05/virtualized-document-printing-apis/">virtualized four document APIs</a> using the <a title="CodeIgniter" href="http://codeigniter.com/">CodeIgniter open-source PHP web framework</a>, <a title="Amazon EC2" href="http://apievangelist.com/apis/amazon_ec2.php">Amazon EC2</a>, <a title="3Scale API Management Service" href="http://www.3scale.net">3Scale self-service API management service</a> and <a title="Mimeo Connect Cloud Print API" href="http://developer.mimeo.com">Mimeo Connect Cloud Print API</a>.<br />
     <br />
     First I launched a copy of the CodeIgniter framework on my existing Amazon EC2 instance, configured mod_rewrite to handle my URLs, and wrote seven API methods dedicated to printing just one type of document, like a poster.  I now had a simple RESTful API that handled requests, and returned XML and JSON responses.<br />
     <br />
     <a href="http://codeigniter.com/" target="_blank"><img src="http://kinlane-productions.s3.amazonaws.com/api-tools/codeigniter-logo.jpg"  width="200" align="right" /></a>I need a quick way to manage access to my API and measure its usage.  So I would know who was using it, how they were using it, and if it was worth while to keep the API and put more resources into it.  I selected <a title="3Scale API Management" href="http://apievangelist.com/serviceproviders/3scale.php">3Scale API management</a>, one of two free, self-service API mangement platforms out there.  The other is <a title="Mashape" href="http://apievangelist.com/serviceproviders/mashape.php">Mashape</a>, but they are still in BETA, so 3Scale was the only other solution I could deploy for free, and scale as I needed when things were successful.<br />
     <br />
     I deployed the 3Scale PHP connector on my Amazon EC2 instance as part of the CodeIgniter REST framework.  I then launched my 3Scale self-service API area, which provides me with:
</p>
<ul >
     <li>Self-Service Developer Registration / Login / Key Management
     </li>
     <li>Documentation
     </li>
     <li>Forum &amp; Support
     </li>
     <li>API Metering / Billing 
     </li>
     <li>Analytics and API Usage Reporting
     </li>
</ul>
<p>
     I now had a simple RESTful API, that had self-service documentation, app key registration, forum, and support.  I received emails when new developers registered, could track how much they used, and turn off access when needed.<br />
     <br />
     I was open for business, using the CodeIgniter tools as a RESTful framework and 3Scale as API management solution I was able to deploy and manage my APIs on an existing Amazon EC2 instance for free, with minimal work, and the platform will scale as my APIs get more usage.
</p>
