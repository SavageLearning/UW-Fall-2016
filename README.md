# UW-Fall-2016

Welcome!

Machete is an open source project that performs a vital function for Casa Latina, a Seattle non-profit. It’s also used by several other day labor centers around the US. This [status report](https://docs.google.com/presentation/d/1Ag1Z_f2F0HTQRIEIA33_DmlaVxAHgUbRcjDoov8KIkA/edit?usp=sharing) is information I’ve presented previously, and provides more information on Machete’s history and future direction.

Machete v1 is a web application built on ASP.NET and jQuery. Most of it was written in 2011-2012, just prior to the explosion of client side javascript frameworks like Knockout, Ember, and Angular. It serves its function well, but is dated. The layout is not responsive and the UI environment is a custom jQuery solution that needs to be retired. The day labor centers that use it need more from it, but getting volunteers to work in a proprietary environment (MS) with outdated code has not been possible. Thus, it’s time for an overhaul.

My plan for Machete v2 is to cut from its existing technology stack and re-implement everything. Having worked in C#, Ruby, Python, and Javascript, I am leaning heavily toward a new implementation in TypeScript and Angular2.

My role will be multi-faceted. I will be the product owner, but will also work as a developer and  as the main release engineer. We will take a micro-services approach, implementing separate services for data, application, and UI layers. We will implement full text search and internationalization, and allow authentication through the standard OAuth providers. Developer commits to github will trigger container builds, testing, and deployment to pre-prod environments. 

What I ask from you is passion to do great work. What we build will be used daily by volunteers in Seattle, San Francisco, LA, NYC, and other locations in the country for many years to come. There is a small, dedicated group of people in the Machete community and I welcome you to it. Let’s build something awesome!

-Jimmy @jcii

 |                           |
 ------------ | -----------: |
 Slack        | https://savagelearning.slack.com/ |
Machete v1 repository |  https://github.com/savagelearning/machete |
Machete v1 documentation  | https://github.com/savagelearning/machete/wiki |
Casa Latina               | http://casa-latina.org/ |
National Day Laborer Organizing Network | http://ndlon.org/en/ |

