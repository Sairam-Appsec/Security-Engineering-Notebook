As per the inconsistent normalization I did previously I understood why the load balancers or reverse proxy's strip or filter the header or extra informtion we send.

Actually, I implemented the CSP header for all the non prod and prod environments for our application, But I was not able to see the header reflecting in the browser response headers.

I Faced the major issue after deploying it into the INT environment, after configuring at the tomcat server level the headers are missing

After digging deep, I understood that our load balancer (DWEB) is stripping the custom headers from the response.

We know that with the Inconsistent normalization, there is a possiblity for the mismatch in the request url and x-original url, To avoid these type of issues our network team stricty
filtering the custom configured headers at the load balancer level.

This reasearch helped in understanding the real issues of inconsistent normalization.
 
