
# Application Monitoring

In the previous demo, we saw how easy it is to setup automated CI/CD pipelines with Azure Pipelines to build, test and deploy application from GitHub and deploy to Azure. At Contoso, we develop applications in a cycle of continuous delivery: release a new feature or improvement; observe how well it works for the users; plan the next increment of development based on that knowledge. 

In this demo, I am going to show you how we use Application Insights to monitor a web application for performance and usage. The Contoso Air website is the lifeline of the company and we  can't let it go down. So, with Application Insights we monitor the web application around the clock to make sure it is always on, always responsive and if things go down alert us so we are the first person to know.  

The website is instrumented to send usage and performance metrics to Application Insights. It is very easy to set this up. Once it is setup, the app starts sending telemetry data to the portal.  All these telemetry streams are integrated in the Azure portal, where you can apply powerful analytic and search tools to the raw data.

I can choose to see data for different time ranges, from the last 30 minutes to the last 30 days.   To make sure that the web application is continuously available, we monitor the availability and responsiveness of the web application - this is done by creating a simple web test that continuously pings the web URL from multiple locations and alerts if the availability of the site goes down. 

Similarly we measure the responsiveness of the site. With Application Insights, we can measure performance of both server and client side operations and if we find anything slowing down, we can get into to the details to identify the root cause.

Next, let me show you usage. Azure Application Insights helps us gain powerful insights into how our customers use our app. We get deep understanding of where customers such as where do they come from, how do they access your application in terms of browsers, network etc., what is the usage flow of your users. These information  help us answer questions such as:
Which features of the app are most popular? Do your users achieve their goals with our app? Do they drop out at particular points, and do they return later? And with this knowledge, we make data driven decisions about our next development cycles.

Next let us talk about issues - businesses want to find issues before their customers find them but it is easier said than done. There are two aspects that you need to find - first you will need to find where and when the issues happen and then you will need some deep insights into why it happens. The first set of questions can be answered with the application map which helps us to spot performance bottlenecks or failure hotspots across all components of our  distributed application. The sample demo app that I use here has only a couple of components but we have other large application that have hundreds of components. Finding issues on such applications are  difficult and time consuming.  Each node on the map here  represents an application component or its dependencies; and has health KPI and alerts status. Here I can see a few issues on this particular component, I am going to select this to get more detailed diagnostics

I can see a couple of failures that have happened here and I can see this has happened in the last couple of hours. NOw, I want to find more about the issue. I can get a rich stack trace on these errors. I can do more deep profiling. I can also configure to create a bug automatically in Azure DevOps whenever an error is generated in the application. All of the captured data can be stored as metadata or linked artifacts with the bug. Now, all bugs and their relevant information are successfully captured resulting in quicker resolution through improved team efficiency.









