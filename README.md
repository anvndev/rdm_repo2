14 Website Speed Optimization Tips: Techniques to Improve Performance and User Experience
Amir Hadžić Amir Hadžić on June 18, 2021

Why Is Page Speed Important
What Affects Site Speed
How to Measure Website Speed
What Is a Good Website Speed?
Best Practices to Speed Up Your Website
1. Reduce the Number of HTTP Requests
2. Switch to HTTP/2
3. Optimize Image Sizes
4. Use a Content Delivery Network (CDN)
5. Write Mobile-First Code
6. Minimize Time to First Byte
7. Choose the Right Hosting Service Plan
8. Implement Gzip Compression
9. Minify and Combine CSS, JavaScript, and HTML Files
10. Load JavaScript Asynchronously
11. Consider Using Prefetch, Preconnect, and Prerender Techniques
12. Reduce the Number of Plugins
13. Use Website Caching
14. Adopt Cloud-Based Website Monitoring
Wrap Up
In today’s digital world, everything comes down to speed. It doesn’t matter if you have the most complex and good-looking site if it takes forever to load. There are various reasons why your web pages may load slowly, but no matter the cause, today I’m going to show you some useful tips and techniques on how to improve your website performance and speedand ensure a smooth user experience.

But first things first.

Why Is Page Speed Important
Research shows that the amount of time a user will wait before losing focus is roughly from 0.3 to 3 seconds. If your website takes longer than that to display important information, the user will lose focus and possibly close the browser window.

Websites that are faster will have lower bounce rates, higher conversion rates, higher ranking in organic search, and, of course, they will have an overall better user experience.

The bottom line is that slow websites will cost you money and will hurt your brand. On the other hand, making your web pages load faster will positively impact traffic, user retention, and sales.

What Affects Site Speed
There are a number of reasons why your site load time might be lagging. It could be anything, but the most common factors are:

Heavy CSS and JavaScript use
Poor server/hosting plan
Large image sizes
Not using browser cache
Too many widgets and plugins
Hotlinking images and other resources from slow servers
Traffic volume
Older browsers
Slow network connection (mobile devices)
That means there is a whole range of steps you can take to enhance page speed, which I’ll explain later in the post. But before you start troubleshooting to improve website performance, you need to test your page load time.

You can learn more about page speed in our blog post about the key website performance metrics that can help optimize your site and improve user experience.

How to Measure Website Speed
Before making any changes, it’s important to measure first. Measuring specific metrics will let you compare your website performance before and after the changes, and will let you know if your changes are actually working.

There are many metrics that you can measure as the website owner, but I would suggest focusing on Largest Contentful Paint, First Input Delay, and Cumulative Layout Shift.

These three metrics are defined as Core Web Vitals by Google.

There are several solutions available that you could use to monitor Core Web Vitals metrics, such as our synthetic monitoring tool, Sematext Synthetics, or our real user monitoring software, Sematext Experience.

Learn more about how to check website speed the right way. If you want to see the two tools in action, check out the Experience docs or Synthetics docs.

What Is a Good Website Speed?
Research shows that the amount of time a user will wait before losing focus is roughly from 0.3 to 3 seconds. That means that you should aim to show some content to the user in under 3 seconds.

If we assume that you decided to use the Core Web Vitals metrics as mentioned earlier, then these are the recommended thresholds that you should aim for:

 

Good	Poor	Percentile
Largest Contentful Paint	≤2500ms	>4000ms	75
First Input Delay	≤100ms	>300ms	75
Cumulative Layout Shift	≤0.1	>0.25	75
You can read more about what criteria Google used to arrive at these thresholds here.

Note that when measuring page load time it’s best to try to get as much data as possible, from all types of visits. For example, you will need to have data for both desktop and mobile devices. The reality is that you will most likely need to do extra work to get the same performance on mobile devices, even when the metrics for desktop devices are well under the thresholds mentioned above.

Best Practices to Speed Up Your Website
As you’ve seen, there are a lot of factors that influence how long it takes to load each page on your website. But there are just as many ways you can improve the performance of your website. Here are some of them:

1. Reduce the Number of HTTP Requests
HTTP requests are used by the web browser to fetch different parts of the page, like images, stylesheets, and scripts from a web server. Each request, especially using HTTP/1.1, will have some overhead in establishing the connection between the browser and the remote web server.

Furthermore, browsers usually have a limit on the number of parallel network requests, so if you have many requests queued up, some of them will be blocked if the queue is too long.

Your first step should be to eliminate requests that are simply unnecessary. What is the minimum render time required for your website? Find that out, and load only the necessary external resources.

You should remove any unnecessary images, JavaScript files, stylesheets, fonts, etc. If you are using a CMS like WordPress you should remove any unnecessary plugins as they often load additional files on each page.

Now that you have trimmed everything you could, the next step is to optimize the rest. You should look into compressing your CSS and JavaScript files. Optimized websites often load all the required CSS and JavasScript in a single request for each.

Sematext Experience can help you monitor and identify HTTP requests and resources that are loading slowly for your real users.

2. Switch to HTTP/2
I mentioned above the overhead of sending many requests over HTTP/1.1. HTTP is the protocol that the browser uses to communicate with a remote web server. The HTML of your website, along with all other resources such as images, stylesheets, and JavaScript files are transferred using this protocol.

One way of solving this problem is reducing the number of requests. This is a good approach in any case. Fewer resources required to render your website is always going to result in faster page load times, but there is another way to avoid this overhead.

You could switch your website to HTTP/2. The details on how to do this will depend on the hosting provider you use.

HTTP/2 has several advantages over HTTP/1.1. Among them is the ability to send multiple files at the same time, over the same connection. This avoids the overhead of multiple requests.

3. Optimize Image Sizes
Many websites use graphics heavily. If your images are not compressed, or if you use too high of a resolution it will slow down your website’s performance.

For example, websites sometimes use images with 2x or even 3x resolution so they are displayed well on high-density displays such as retina screens. But if your users are not using a HiDP display, then you are just wasting bandwidth and increasing the load time for your visitors, especially if they are on slow mobile data connections.

You can read this MDN guide for using responsive images correctly. Specifying multiple image sizes will allow the browser to select the appropriate image based on screen resolution.

When you are certain that you are loading the correct resolution across all device types, then it’s time to optimize the size of the images. Shopify has a good guide on how to do that.

Make sure that you use the correct file type too! Use JPEG for images with lots of colors (e.g., photos), and use PNG for simpler graphics.

4. Use a Content Delivery Network (CDN)
Serving static files can get tricky. Since this is not the primary business of 99% of websites out there, it’s smart to outsource this part of your infrastructure to someone else. Luckily there are services designed especially for this: Content Delivery Networks or CDN.

CDNs will optimize the delivery of static files such as CSS, images, fonts, and JavaScript to your visitors. Setting them up is usually very simple.

CDNs use geographically distributed servers. What this means is that the server closest to your visitor will be serving the files. So the load time for e.g., images will be the same, regardless of where the user is connecting. Generally, when serving static files from your own servers, the load time increases when users are physically far from the server.

You can use Sematext Experience to monitor the performance of files hosted on CDNs so you can actually measure if outsourcing this part of your infrastructure makes sense. When we first started using a CDN for serving assets for Sematext Cloud we actually used Sematext Experience that showed that we were indeed serving things faster to our users.

how to optimize website speed
Fig 1. Experience chart showing the avg. load time for the top five slowest domains

5. Write Mobile-First Code
Mobile devices are eating the world. Or so I am told. You should check what your users are using a RUM solution such as Sematext Experience or even with your website analytics tool of choice (e.g. Google Analytics) just in case.

Usually, developers write and test websites on their own desktop devices, and only later they optimize the website for mobile devices. This can often be a painful process, depending on the choices made while writing the website.

website performance best practices
Fig 2. Experience chart showing the difference between Mobile and Desktop load time performance

But what if, while testing the website we used mobile devices (or emulators)? That way we would write for mobile first. The experience would be by default optimized for mobile devices.

Then adjusting the website for desktop devices would be a more straightforward process. We can progressively enhance the experience for devices with more power and screen real-estate. Just remember to also throttle the network and CPU to better simulate the experience of mobile users.

6. Minimize Time to First Byte
Time to first byte, or TTFB, is the time it takes for the browser to receive the first byte of data from the server. This is therefore a server-side concern but it plays an important role in the overall performance of your website, so you should take some time to improve it.

The main factor under your control when it comes to TTFB is server processing time. Therefore you can try some of the tips recommended by Google to improve TTFB:

Optimize the server’s application logic to prepare pages faster. If you use a server framework, the framework may have recommendations on how to do this.
Optimize how your server queries databases, or migrate to faster database systems.
Upgrade your server hardware to have more memory or CPU
A TTFB below 200ms is considered great. The 200ms to 500ms range is considered normal and okay. A TTFB consistently higher than 600ms will need to be investigated. And Sematext Experience can help you with that along with monitoring other Web Vitals metrics as well.

improving website performance
Fig 3. Experience chart showing Time To First Byte

7. Choose the Right Hosting Service Plan
This ties into the previous point about minimizing time to first byte. If you are using a shared web hosting provider, then it’s very likely that the overall performance will be subpar. You should look into upgrading the hosting service plan or if you are using WordPress, consider using a managed service that is well known for stable and high-performance hosting.

You have three main options (plus a bonus one) for hosting:

Shared – traditionally the cheapest of the hosting options is a way to share the resources of the server with other customers.
VPS – a virtual private server is significantly faster than a shared host but instead of using just one machine it uses multiple machines.
Dedicated – dedicated servers are obviously the most expensive of the three and with this one, you basically rent an entire machine that can be usually configured to your wildest desire.
Serverless – as of late, serverless has gotten a foothold in server space as it offers unmatched scalability at a fraction of the cost.
Of course, as always, you should measure your performance first before making the switch.

8. Implement Gzip Compression
You should enable gzip compression on your HTTP servers. Gzip compression minimizes the size of HTTP responses for certain file types. It is usually used for textual responses only. This should reduce the load times and save on bandwidth.

9. Minify and Combine CSS, JavaScript, and HTML Files
I already mentioned that you should try to load both JS and CSS in a single request for each. This is accomplished by minifying and combining separate JS and CSS files into single bundles.

Browsers have a limit on parallel network requests so if your website needs 3 requests in total to load, it will be most likely faster than if it had to load 30 different resources. Developers can use tools like webpack to have the convenience of using multiple files while developing the website and to have the performance benefit of a single bundle when deploying to production. But in general, combining files means exactly that, all files are copied as-is into a single file.

Minification is the process of optimizing the size of JavaScript and CSS files by removing or shortening symbols in the source code. The output is functionally equivalent, but not entirely human-readable. Browsers don’t have a problem reading it though, and the smaller file sizes will be faster to load.

What most optimized websites end up doing is first minifying JavaScript and CSS files and then combining them into single bundles.

10. Load JavaScript Asynchronously
When the browser reaches a &lt;script&gt; tag that loads JavaScript from a remote source, it will wait for the file to be loaded before continuing with rendering the website. That is called synchronous loading.

If you set the async flag on the &lt;script&gt; tag then the browser will load the script asynchronously. It will continue parsing the page while the script is loaded.

We also suggest moving the script tags to the bottom of the page, near the closing &lt;/body&gt; tag. This way older browsers that don’t support the async attribute will load the script after parsing the rest of the page.

11. Consider Using Prefetch, Preconnect, and Prerender Techniques
There are different prefetching and preloading techniques that you can use to give hints to the browser about which resources will be required to render the page before the browser actually needs those resources.

Consider the following performance optimization techniques:

DNS prefetching. You can tell the browser that certain domain names will need to be resolved to an IP address before the browser actually sees resources from that domain name. This can seem like a small optimization, but it can make a difference when you have exhausted other techniques.

<link rel="dns-prefetch" href="//sematext.com">
TCP preconnect. Much like the DNS prefetch method, preconnect will resolve the DNS but it will also make the TCP handshake, and optionally the TLS negotiation.

<link rel="preconnect" href="https://www.sematext.com">
Prefetching. If we’re certain that a specific resource will be required in the future, then we can ask the browser to request that item and store it in the cache for reference later.

<link rel="prefetch" href="logo.png">
Prerendering. This should be reserved for when you really know that the next step a user will take is to go to a certain page. You can instruct the browser to prerender the complete page, along with downloading all the required assets by specifying the URL like this:

<link rel="prerender" href="https://www.sematext.com/next-page">
12. Reduce the Number of Plugins
Plugins are reusable pieces of functionality, usually used in content management systems like WordPress or other pre-built website platforms. Plugins give website owners additional functionality such as analytics or the ability to leave comments on blog posts.

But plugins come at a cost. Each plugin will almost certainly load additional CSS and JavaScript files. Some plugins will increase the TTFB time as well because they require additional processing on the server for each page request.

So I would recommend going through your plugins list and making sure that you really need each plugin. You should delete any plugins that are not critical for your website.

13. Use Website Caching
I’ve briefly mentioned cache but I want to explain what that is. Caching is the process of saving a version of your files in a temporary storage location – a cache – that can be accessed faster. There are lots of advantages to enabling browser caching as it can reduce bandwidth consumption, increase load times, reduce latency, and the workload of the server. The main downside is that basically there will always be at least two versions of your website at any given time. This can cause issues if you are running a real-time service that relies on accurate data but even this can be addressed to some degree forcing subsection of the cache to clear when new data is imported.

14. Adopt Cloud-Based Website Monitoring
The first step to improving the performance of your website is to measure it. Measuring the performance requires specific tools, and ongoing monitoring is a must if you want to be alerted if your changes are improving the performance or if performance is degraded over time.

There are two approaches to website monitoring: synthetic monitoring and real user monitoring. If you’re not sure how they work and which one is best for your use case, check out our blog post about real user monitoring vs. synthetic monitoring where we compare the two types of monitoring.

In either case, we suggest using cloud-based website monitoring tools so you can focus on growing your business instead of building or managing your own tools. Sematext Cloud offers solutions for both synthetic monitoring and real user monitoring. Try it free for 14 days!

If you’re on the market for monitoring tools to help measure and improve website performance and availability, check out these blog posts:

Best Real User Monitoring Tools
Best Synthetic Monitoring Tools
Best Front-end Performance SaaS & Tools
Wrap Up
Improving website performance can be challenging, especially with the vast differences in devices, connectivity, browsers, and operating systems, but it will have a significant positive impact on your business if your business relies on your website as one of the main channels for reaching your customers.

Also, keep in mind that this is a process that doesn’t have a clearly defined start and endpoint. You don’t have to implement all of the suggested changes today. Spend some time looking into the monitoring tool results, make changes on the website, and then compare the performance before and after the changes.
