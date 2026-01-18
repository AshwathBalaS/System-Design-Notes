# System-Design-Notes
This Repository contains my "System Design" Notes from Euron

**I) System Design Introduction**

**II) Low Level Design Introduction - What, Why, Goal, SOLID Design Principles**


# **I) System Design Introduction**

Hello everyone, my name is Ang Gupta and I’m presently working with Microsoft and their Windows team. Here we are conducting a course on system design where we are going to be learning what system design is, why you even have to learn system design, how it is helpful for developers, and if you are actually stuck in some system design rounds, how you should be answering. So I’m going to be helping you by providing you some guidelines about how to answer in any system design rounds, like how you can be interview ready for a system design round. At the same time, we are also going to be discussing some of the case studies with the help of which you will be able to understand any of the systems end to end. So this course is going to be super interesting. Let’s get started.

So, you know, before jumping into system design, let’s just take some example. Let us say you have bought a land and you want to build a house. It’s not that you will straight away go and construct a house, correct? What you will do is, you are going to be taking help of some architect who is going to come to your house, see the dimensions of your land, and based upon that he’s going to be creating a layout for that. Now, after that layout is ready, it’s not that it is going to be the final one. You are going to give some of your feedbacks. If you’re not liking something, you are going to say that, “Hey, can we have a bedroom here? Hey, can we have a kitchen there? Can we have a lobby there?” Based upon your requirements, you’re just going to be having some of your inputs. By taking those inputs, the architect is going to create another layout and once you approve it, then he will go ahead and perform the construction for that, correct?

So if you take that same example in the field of software development, something similar to that happens even here. Here what we are going to be doing is, a person is going to come up with some request that, “Hey, I want this problem to get addressed.” In order to solve that problem, what you will be doing is, you are going to provide some solution. Now before jumping into implementation of that solution, what you will do is you are going to create a layout for that, then you are going to be proposing that layout to that company. If that company is approving it, then you will go ahead and perform the implementation. But prior to that, there are going to be several rounds of discussions where we are going to be seeing what the new needs of the customer are, and are our solutions correctly optimized, performing the solution well or not. So that is how it is going to be there. So this system design is extremely interesting and important.

So here as a part of this course, we are going to be learning your low-level design as well as the high-level design. As a part of your low-level design, we are going to be learning certain things like what design principles are, what design patterns are, how you are going to be applying those in your software. And in the part of high-level design, we are going to be discussing things like how you can scale your system, how you can optimize your system, how you are going to be applying databases. Like, you know, as a student, even I am sharing my own example: as a student I used to think that okay, if we have something called RDBMS, that is something which we are going to be applying everywhere. But when I grew up, I understood that even for a project it’s not going to be same for all the scenarios. We are going to be having different set of databases. So what those different databases are, how you’re going to be making those decisions, what CAP theorem is there, what is horizontal scaling, what is partitioning — all of those things we are going to be covering as a part of your high-level design.

If you will see, like you know, when you are working for any of the company, what your role is going to be there. Let us say you are a developer there. So what as a developer you are going to be doing for that company, how you are going to be contributing there. So you are going to see what any of these companies across us are doing. We are actually having some real-life problems and what any of these companies are doing is, they are trying to provide you some solution for your real-life problems.

Now we can actually discuss what are these real-life problems and what are we actually seeing here. Let’s talk about some time back, let us say 15 years back or 20 years back. At that particular time, it was not easy to do anything through your phone. If you want to get something done, you will have to step outside your home and you will have to get all of those things done. Everything required a lot of patience plus a lot of process. But now, if you will see, if you want anything, everything is available at your fingertips.

Let’s take the example of cabs. Previously, if my family wanted to go out for some vacation, it’s not that we can just book some cab. We used to go outside, we used to talk to some travel agents who were willing to provide us some cab, provide us some quotation. We used to take quotations from different people, finalize one, and we used to wait for that guy to come to our home to pick us up. And if he’s not showing up, we used to go outside and try out other agents. So that is how it used to be working back then.

But if you will see today’s scenario, what is happening? If you want to book a cab, you have options of Ola, Uber. All of these applications are helping you in booking a cab. If you want to buy groceries, previously the only option was stepping outside. But now, if you are not well or if you are just feeling lazy, if you don’t want to step outside, then you have applications available for that. These days they are literally delivering at your doorsteps in 10 minutes, which is really incredible. You have options of Blinkit, Zepto, BigBasket, and so on.

Now let us say you are hungry and you just want to eat some food and you don’t feel like cooking. Previously you just had the option of going to some restaurant, ordering some food, taking it home, and then eating. Now if you will see, if you want to order food, you have options like Zomato, Swiggy, based upon different regions where you guys are staying. Previously, if you were not well, you did not have the option of getting medicines at your home. But now you have options like 1mg, PharmEasy, and so on.

So these are the things where we are just ordering some service at our doorsteps. If you want to make friends, previously it was only possible by going outside, meeting new folks, making friends. But now, everything is possible even from home. You have applications like Facebook, Instagram. If you want to date people, you have applications like Bumble, Tinder, and whatnot. So these are the applications.

So what these applications are doing is, they are actually targeting and providing solutions for your real-life problems. And how they are providing solutions? They are actually building a software, and that software is helping us in providing the solution for all of these things.

Now we are going to be discussing what all steps are involved while developing any of the project in any of the organization. I’m not going to be telling you how we have done it in books. I’m going to be telling you how we do it in the practical perspective.

The first step is requirement gathering. As the name suggests, we are going to be gathering the requirements. This is the first step in any application development. You cannot go ahead without gathering the requirements. So what we are going to be doing here is, we are going to be collecting all the information and we are going to be understanding what the problem we are trying to solve from that project.

Now the question is, from where you are going to be gathering it? From where you are going to be getting all that information? So we have two sources. The first one is customers. You can go ahead and directly talk to the customers. You can conduct surveys, polls, ask what problems they are facing, what features they are actually looking for, what issues they are facing, where you need to put more energy. You need to understand what the customer requirement is.

The second one is product managers. In large companies, product managers define the requirements. They understand what competitors are doing, they study market needs, and they come up with what is the best that can be delivered. Based upon the research, they come up with ideas like new features or improvements, and later pass it to the developers.

For example, Urban Company (previously UrbanClap). Their main approach is helping you by providing technicians for home services. Previously this was very difficult — people used to make multiple calls and face uncertainty. Urban Company recognized this problem and created a platform where with just a single click you could book a technician. By solving a common issue, they automated the process and made life easier for everyone.

In startups, since the team is smaller, developers themselves take the initiative to identify problems and suggest solutions. Once requirements are gathered, the next step is defining the problem statement. For example, instead of saying “implement a button,” you define “implement a login button which opens a login page.”

Requirement gathering is important because it sets the foundation for everything that comes next. Without a clear understanding of the problem, it is not easy to build any useful and scalable product.

Application development does not happen in a day. It involves design, development, testing, and deployment. Even big companies like Facebook still need engineering teams for updates, improvements, enhancements, new features, performance, and scaling. That is why development never really stops as long as the application exists.

After requirements, the next step is scoping. Scoping means defining what features will be delivered in which phase. Instead of delivering everything at once, you break it into phases. Just like going floor by floor in a building — you can’t jump directly to the top floor.

So what I’m trying to explain is that if you want to do something big, you have to do it step by step. You cannot reach the end in a single go.

It’s not that if you are hungry you can just straight away eat it. The first step is going to be buying it from the market, buying the groceries from the market. The second step is going to be cleaning it down, performing the initial chopping and everything. Then you will have to start the cooking. The cooking also involves a lot of procedure and time frame, and once everything is done then only you will have it already in your plate and then you can consume it. So if you want to eat something, I’m not giving you the option of buying it from outside, I’m just saying if you have to cook it on your own you will have to follow certain steps. So that way only it will be easier for you to consume it, it will be possible for you to consume.

So in the same way, when you start working on any of the big application or any of the software project, you do not try to build everything all at once. Instead, what you do, you start with some of the core features. Like if you take the example of the story building, if you want to climb one, you are actually defining your work like, okay in one go I have to reach the first floor. So how you are going here, step by step. Similarly, when you talk about any of the application, that is how it is going to be working.

So basically what we do, just how we have broken down our work here, similarly if you want to perform any implementation of any of the project, your task is actually going to be breaking it down into smaller, smaller manageable pieces. Even if you talk about some of the big products like Microsoft, Facebook, Amazon, LinkedIn, Google — none of these things was built in a single day. These apps were built over time with smaller features which were added gradually.

So when you work on any of the application, it is very essential for you to focus upon what features you want at first. For example, if you talk about any application, let us say you were building some shopping application. You cannot go ahead and perform each and every step in one day, but what you can do is plan your work. Like, in one day I will be listing down all the products, in the second day I’m going to be implementing the login page, third day I’m going to be adding the support for card, fourth day I’m going to be adding the support for checkout. Although here I’m taking very less time frame, but all I’m trying to do is break it down, like okay these are the steps I’m going to be needing, and once it is already ready then only you can work on the delivery.

Why I’m putting a lot of focus here on the scoping is because that is one of the most common mistakes which a lot of developers do. Even when I was a student, I thought of building an application, but since I was just a student I had zero idea about how to do it. I was thinking that if I am creating any application, I have to look into all of those things from day one itself. But no, it doesn’t happen that way. If you are building any application, you don’t have to make everything ready on day one. Even if you talk about any application like Facebook, the initial UI of that application was different as compared to what you have today. That application has grown over a period of time. They have added a lot of features as well which were not there earlier. So that app has grown over the period of time.

So when you build any application, it is very essential for you to understand that you are not going to do everything on day one. It’s going to get scattered over a period of time.

Now let’s take the example of building some application like Facebook. It can have a lot of complex features, so you cannot build everything at once. But what you can do is build smaller features. Now what can be the smaller features? Let us say the first one is going to be sending friend requests and you also want to add friends. This is going to be one feature: that you should be able to send requests and you should be able to add friends.

Now the second one could be something like posting on wall. I’m talking about the initial Facebook. That time we had wall. So if you want to post something on your wall, that could be one of the features. Now after this, if you have friends added, maybe you want to add the support for chatting so that you can go ahead and chat with your friends. So add chat support.

So what I have done here is I have broken down all my features that okay, these are the three features which I want to implement first. And once these features are going to get implemented, then I can go ahead and implement the next set of features. The next set of features could be something like upload, image upload, video. You can also add support for liking or commenting.

So once the initial set of features are delivered, then these are the next set of features I’m going to be doing. So if you will see what I’m doing, I am breaking down my entire project into smaller, smaller features. And with this what I’m doing is I’m making my entire process, entire development process manageable and achievable. So this is what we refer to as scoping, where we are defining the work which needs to get done and how I can break it down into smaller, smaller and achievable tasks.

If you talk about any typical company or the software development process, we don’t work on the entire project or the entire product from start to finish all by yourself. We actually go ahead and take help from other teams as well. One team is going to be dedicated for testing. Of course, we have certain teams where everything is taken care by one person only, but if you see on a broader picture, there will be experts in testing, front end, back end. So what we will be doing is dividing it. You don’t have to do everything on your own. You are going to be dividing it in that team so that everyone can take care of some responsibilities.

So it is very important for you to understand, especially if you are still learning or if you’re very new in the industry, that you don’t have to do everything on your own. It’s going to get broken down in the entire team with a scope that okay, I want it by the end of this month or I want it at the end of this quarter.

So in organizations, basically what happens is we break down our entire feature into smaller, smaller features. Even if it is a bigger feature, we break it down into smaller ones. And if it is achievable in certain number of days, we scope it down: okay this work five days, this work ten days. So that is how we scope it out. Once we are breaking it down into smaller, smaller features, then we plan when we can work on them.

In the industry generally, all these things happen in quarters. In the entire year we will have four quarters — quarter one, quarter two, quarter three, quarter four. So basically in organizations, our work is divided into four quarters. You will be focusing upon developing special features in all these quarters. This is also going to be helping the entire team so that they can set their clear goals and they will know what features are to be done in the given time frame.

Even in my organization, we have some core responsibility where we build a roadmap. We will say something like starting off Q1, Q2, Q3, Q4, and then we will say okay by this time at least this task is going to get done, by this time I’m going to be testing it, by this time I’m going to be deploying it. And this I’m going to be doing even on the feature level — that okay this feature is going to get completed by this time, tested by this time, and deployed by this time. So that is how I’m going to be creating a roadmap where I’m scoping my work spread over the entire year.

So if you are going to be defining the scope, it’s going to give you a lot of clarity. People are not going to come to you repeatedly and ask, “Hey, is this task done or not?” If you have this clear roadmap, people will have clarity about what they have to do, when. Even the teammates are going to know when to do what. So in the part of scoping, we plan which features will be developed in which quarter.

Now let’s say you are working on some social media application. Now you are defining what work you want to get done at the end of each quarter. Let us say in quarter one you are going to be focusing on some of the core features, like you will go ahead and perform user registration. The second feature could be something like login. These are the core features. On the first go you want a user to register themselves, they should be able to log in, and the last one could be profile creation.

Now in the next quarter, what features can we have? It can have features like adding friends, you should be able to post on wall, you should also be able to like posts. These are the tasks which I’m dividing in quarter two. Now in quarter three, we can have the functionality of add chat support, and at the same time we are also going to be providing the option of image and video upload.

Now let us say in quarter four, you are adding the support of notifications, you are also adding the support of searching some user, like you want to add someone so you’re going to be searching them. That option should also be there. Then you can also go ahead and add some premium features. If you will see, I have separated down my work in different quarters. I am not going ahead and implementing everything on day one. Even the premium features are added at the end because if you come up with a new application and on day one itself you market it as paid, how is a user even going to use it?

In order to make it work, many applications provide some basic features for free. For the advanced features, they are going to charge. With the basic ones, people are going to test your application. If it is really good, if they are going to get some good use case out of it or not. Once they see how your application is working in the basic manner, it becomes easier for the customers to understand your application and start using it.

So basically what we are doing here is we are breaking down our bigger project into smaller ones and we are also trying to see that when we are breaking it down, we are breaking it down based upon achievable goals. It should not be something that is not at all achievable. So that the entire project stays on track and we can ensure that it is going to get delivered on time, plus it can have a visible growth.

Now the next thing which we have here is why scoping is important. So far we have discussed what scoping is, now we are going to discuss why scoping is important. If you talk about scoping, how it is actually helping you — you are having a bigger project which is complex, and with the help of scoping what you are doing is you are managing the complexity. Instead of building everything at once, you are focusing upon some set of features at a time, and with that you are trying to make the project go smooth.

With the help of scoping, you are also setting clear goals. I discussed about roadmaps. With that, you are telling the organization or the team that this is what work we have. You are setting the goals very clearly and you are achieving them by breaking them down into smaller tasks so that everyone in the team knows what needs to get done and when. Along with this, it also helps you in better time management. If you talk about any big project, on day one it will be very difficult to understand how much work you need to deliver and when. In that case it will be very difficult to manage time effectively. But if you break down your work into quarters, you are setting some realistic targets for each phase of development.

You are also ensuring steady progress. If you talk about any application, if you are not going to see any outcome, you will not understand what you are doing or where things are going. But if you set smaller and achievable goals, your project can evolve gradually and you avoid delays. If you are setting timelines, you are also ensuring that you are matching those deadlines.

Now the next topic we are going to discuss is MVP. MVP stands for minimal viable product. Now what is the meaning of this? If you look around today, we have a lot of startups. Behind all of these startups, mostly there are young brains. By young brains, I mean people early in their careers who are enthusiastic about what they want to do. They want to have something of their own, start their own company. They are very excited about their idea and they want to pitch it to investors.

However, if you approach investors with just an idea and talk about it vaguely, they might not consider you serious enough. Anyone can talk about an idea, but that does not make a strong impression. What you should do is come up with a POC — proof of concept. In this POC, you create a simple prototype or a basic version of your application. If you want to pitch to investors, you should not go directly. You should first build a POC that has some basic features, a simple prototype that shows what your idea is about, how you envision it, and how you can achieve it.

That POC is going to have some core features which tell how your idea is going to work. And that is actually called MVP. Once you have a minimal viable product ready, then you should go and pitch it to investors. That helps them understand that you not only have a great idea but also the ability to implement it. Based on that, they evaluate you and see that you are serious and that your idea has potential to grow over time.

This is going to be a smaller application only. It will not have everything implemented end to end. Similarly, in a corporate setting, as a developer, you might have a great idea for a new feature or tool. But you cannot just say, “I have this idea and I want to implement it.” Everything requires approvals. If you want to convince higher authorities like VPs or directors, it is difficult with words alone. But if you have a small application with minimal features that demonstrates your idea, that demo acts as proof. They can see the value and may give you more resources to build it out.

So the MVP is very much required. To simplify this, you can think of MVP as a tester. If you go to a shop to buy perfume and perfumes are expensive, you can ask for a tester. Instead of spending your entire 10,000 rupees, you can buy a tester for 100 or 200 rupees, try the fragrance, and then decide.

You can see for how long that is lasting on you, and accordingly you can take a call if you want to go ahead and invest your money in that. So what basically this tester is doing here, this is actually helping you by providing a smaller version of the entire product so that it can help you guys to decide if you really want to buy it or not.

So far, if you will see what and all we have covered as a part of our software development here, the first one which we discussed was requirement gathering, and the second one which we have covered is scoping. I hope by now you must be very clear about all of these things.

Now once we have created an MVP, what is going to be the next work here? So once you have provided your concept, the next step is going to be building any application. And if you want to build any of the application, that requires understanding what the infrastructure requirement is going to be doing and all of those things are actually going to be covered as a part of this system design.

So you will tell that okay, if I want to create a chatting application, if one message is taking 1 KB and if 1 million users are using it, then how much space it is going to take overall. So all of those things are going to be covered as a part of infrastructure requirement.

So like you know, whenever you will have to build any of the application, it is going to be requiring three major components. The first one which we will have here is going to be compute, the second one is going to be storage, and the third one is going to be network. Now what and all these are, how we are considering them while making any of the application, all of those things we are going to be covering one by one.

But I hope by now you will have a fair idea about if we are building any of the application, what and all things we are going to be requiring there.

If you talk about today’s world, everything is revolving around data. All the devices, all the applications — if you talk about mobile phones or the laptops — everything is working upon processing and manipulating the data. It’s not that these apps are trying to track you to spy on you, but what they all are actually trying to do is they are trying to help you in improving the personalized user experience.

Let us take some examples so that you can understand it better. Let’s take the example of Uber. If you talk about Uber, let us say you want to book a ride. In that case what will happen? You will expect that the driver should reach to your doorstep to pick you and then drop you to the destination. That is what your end goal is from Uber.

Now if you will see how Uber is able to process your request, it is using the map data to locate where you are and at the same time to navigate to your destination. So all of those things are only possible by providing your own data there. If you are not providing your current location, the driver is not able to reach to your destination.

The next one which we have here is Google. If you talk about Google, what is happening there? Let us say you have gone outside. Even if you open maps, based upon what your user data is, they are going to be suggesting you places accordingly. If you see what maps is doing, they are constantly taking care of your location. If you go and see the timeline on Google Maps, it will actually be able to tell you how you have spent your entire day. It will have the entire timeline about where you have gone, how you have commuted. It will also be providing you a summary in the mails where it will tell you that you have been to these many places, you have eaten at these many places, you have spent this much time here and there.

So all of those things, how is it able to provide you? With the help of your user data only. Even if you will see your mobile phones, they also provide you how much time you have spent on all of these applications. They are tracking your user data — like if you are opening WhatsApp, how much time you have spent there — and then accordingly they are telling you how much time you have spent on each application.

The next we have is Netflix or YouTube. Now if you will have observed here, what happens? Let us say you have watched some animated movie or some cooking shows on YouTube. The next time you open their application, they are going to be providing you some personalized recommendations based upon your preferences. If you have watched some animated movie, next time they will say that based upon your watch history we are recommending you movies which you may like. Or if you have watched some YouTube cooking video, the next time you open YouTube you will see a lot of cooking videos by different YouTubers.

So what they are doing is they are taking the user data or the user preference and based upon that they are able to provide personalized recommendations. And how is it even helpful? If you are very much interested in watching only cooking videos, then you do not have to navigate to different YouTube channels to see related content. Instead, it will provide you recommendations on the YouTube homepage, where it becomes easier for you to see different videos. So it is helping your experience overall.

Similarly, let’s take the example of ads. Let us say you have opened some Myntra and you have looked for certain trousers. Later on, if you open any website, they are going to be showing you some trouser recommendations from different websites. So based upon your browsing data, it is providing you recommendations of what you might like.

And how is it helpful for you? Because as a user, your major target is to buy a trouser. If it is providing you some personalized recommendation, that is going to make your work easier. You do not have to go to different websites to see what collection and what price they are offering. In the form of ads, you are able to see all of that.

So if you will see here overall, what we have is interaction with the data. And if you will see in today’s world, what is driving today’s modern world? Data is something which is driving it. That is why you see concepts like data science and big data coming into the picture. Data is the new oil which has gained a lot of prominence over a period of time.

If you see what all the businesses are doing, they are understanding what is the importance of the data, what is the power of data, and how it is actually going to be helping them overall. Data is something which was already there, but it has evolved over time. Previously data was limited, but now data has evolved exponentially.

Now we are going to see at a higher level how applications are dealing with data. Applications are dealing with data in two forms. The first one is how you are storing your data. Now why is this coming into the picture? Because if you have some data — for example Google Drive, where we upload our pictures — what is the one thing we want as a user? We want our data to be safe, and at the same time we want our data to be accessible.

That is why all of these applications are targeting these things: whatever data we are putting there should be safe, and it should be accessible so that if we want it later, it should be easier for us to access it.

The second one which we have here is computing the data. What is the meaning of computing data? I’ll give you a very small example. Let us say you are creating some profile on some application and you are providing your name. Once you log in, you must have seen on the top they will mention your name: “Hi ABC,” and then you will have your entire landing page.

So from where they have taken this out? They have computed the data. They have taken your name out, processed it, analyzed it to make decisions and provide the results. This is a very small example, but in the broader picture also we have a lot of data.

Let’s talk about a banking application. You want to see your transactions. In the database it will have all the transactions from the beginning till now. But let us say you only want to see March 2024 data. You will apply a filter. Applications like Amazon do the same thing. In order history they show a limited set of orders and give you the option to filter: cancelled orders, regular orders, time frame, year, etc., so that you do not have to scroll through everything.

So this is what we actually refer to as computing the data. Whenever we are building any application, these are the two operations which determine what infrastructure you are going to be needing.

Now we are going to break down the infrastructure. The first one which we see here is compute. We are going to need some computational power to process the data. Just now I gave you the example where you want only March data or only data from a particular year. To perform that computation, you will have some running algorithms that help manage user requests and perform calculations. This power is coming from servers or computers which are doing the “thinking” part of your application.

The next one which we have here is storage. After computing, the next thing which we require is storage. All applications require storage to save data, whether it is user data, application configurations, or large datasets. Everything needs to be stored somewhere. This storage is often hosted on servers or cloud platforms.

For example, Google Drive or Google Photos: they provide you some cloud storage, like 15 GB. They are not taking it from your phone, they are providing it on the cloud, and from there it is easier for you to access it.

Now the next one is network. The example which I have just taken will make more sense now. If you want to access your Google Photos, since they are not on your phone, how will you access them? With the help of the internet. Because they are stored on the cloud, you need a network connection.

In the age of the internet, no application works in isolation. We use different servers, different devices. If everything has to communicate with each other, we need networks. The network connects everything and helps in maintaining data transfer. Google Photos has syncing — it takes photos from your phone and uploads them to the cloud. And when the photo is not on your phone, you have the option to download it back.

So all of these things are happening by maintaining data transfer between users, servers, and databases. Without a network, applications like Uber, Netflix, or YouTube will not work. To make all of these things work, we need internet and network connections.

Now we will see why compute, storage, and network are interconnected. Whenever you are building any application, these components work together. Computation processes the data on servers. Storage is needed to save both raw data and processed data. And network is needed so that users and devices can interact with the servers, access the application, and share information.

Now when we plan any application, we need to perform estimates. We need to know how much compute is required, how much processing power the application needs. Not every application requires the same level of processing. Some applications perform a lot of computation, while others perform very little.

For example, in Amazon, you need computation at the cart level, for order history, and for sorting products on the landing page. These all come under compute requirements. Next is storage: you need to know how much data your application needs to store, such as products, user data, etc.

The next is network. Network also plays a vital role. You should know how much data transfer is required between users and servers. Applications like Netflix or YouTube consume more data because they stream videos. Chat applications consume less for text messages, but more when sending images or videos. Also, for messaging applications, you want messages to be delivered instantly. That requires a constant network.

So based on the type of application, you decide how much compute, storage, and network capabilities you need.

So if you talk about all of these things — computation, storage, and network — these are the foundation for any application. They help in processing the data, storing the data, and sharing the data over the internet effectively. All of these things must be planned before starting to work on any application.

So that’s all we have completed in the first module of our system design. Now we are going to discuss more things in the next one. I’ll see you there. Till then, happy learning.

# **II) Low Level Design Introduction - What, Why, Goal, SOLID Design Principles**

Hello everyone. In today’s module, we are going to learn **Low-Level Design (LLD)**. First, I will explain what all topics we are going to cover as part of low-level design. In this particular module, we will be covering only one part, and the remaining portion will be covered in the next module.

When we talk about low-level design, we broadly cover two major things. The first one is **design principles**, and the second one is **design patterns**. In today’s module, we will focus only on design principles.

When you hear the term low-level design, there is nothing entirely new that we are learning. These concepts already exist, and we are simply understanding how to implement them correctly in order to achieve different design principles and design patterns. All of these ideas are things you have already studied as part of object-oriented programming (OOP).

In system design, one of the most important goals is to ensure that the application we build is **future-proof**. What does future-proof mean? It means that if today we build one feature, and tomorrow we want to integrate a new feature, the existing feature should continue to work perfectly. Adding new functionality should not break existing logic.

Future-proofing also means that the software we build today should remain usable months or even years down the line. When companies like Amazon or Facebook were created, they were not built with the intention of lasting only a few months. They were designed with a long-term vision, allowing them to scale massively over time. That is why we are still using these platforms today.

Whenever we build an application, we must ensure it is flexible enough to adapt to changing requirements. If we want to add new features or enhancements in the future, the system should allow that without breaking existing functionality. If the existing system stops working, the new feature becomes useless.

Whenever we talk about designing any system, we are essentially addressing real-world problems. In the real world, we deal with two main things: entities and relationships. For example, a person and a car are individual entities. There is no relationship between them until we say, “This is my car.” The moment we say that, a relationship is established.

This idea of entities and relationships is something you have already learned in object-oriented programming. Using OOP, we try to model real-world entities and define relationships between them. This becomes extremely useful when designing applications.

Whenever you are given a problem statement, your first approach should be to identify the different entities involved. The next step is to determine how these entities are related to each other. This is where object-oriented programming plays a key role.

In OOP, we implement these ideas using **classes and objects**. We represent problem statements in the form of classes, and objects are used to interact with these classes. These are the building blocks of the object-oriented paradigm.

A class acts as a template or blueprint. For example, if we create a `Person` class, it may have attributes like name, age, and gender. Similarly, a `Car` class may have attributes such as model number and color. Attributes describe the characteristics of an entity.

However, attributes alone are not enough. We also define **methods** to describe behavior. A `Person` class may have methods like `eat()` or `sleep()`. A `Car` class may have methods like `start()` or `stop()`. Attributes define what an entity is, and methods define what it does.

When defining a class, we specify the class name, its attributes, and its behaviors. This is how a class is represented in code.

Now let us quickly revise the **core concepts of object-oriented programming**. There are four major concepts:

1. Encapsulation – Wrapping data and methods together inside a class.
2. Abstraction – Hiding unnecessary details and exposing only essential functionality. For example, when you withdraw money from an ATM, you don’t see how the cash is processed internally; you only interact with the interface.
3. Polymorphism – The ability of the same function or operator to behave differently in different situations.
4. Inheritance – Establishing a parent-child relationship where a child class can reuse properties of the parent class.

Polymorphism can be of two types: **compile-time polymorphism** and **runtime polymorphism**. Compile-time polymorphism includes function overloading and operator overloading. Function overloading allows multiple functions with the same name but different parameters. Operator overloading allows operators like `+` to perform different tasks, such as addition or string concatenation.

Runtime polymorphism is achieved through **method overriding**, where a child class provides its own implementation of a method defined in the parent class.

Inheritance allows a child class to reuse properties and methods of a parent class. Access specifiers determine what can be accessed by the child. Inheritance can be single-level, multi-level, hierarchical, or multiple. Multiple inheritance is not supported in languages like Java or C#, but similar functionality can be achieved using interfaces.

Now let us move on to **design principles**. The goal of design principles is to help us write code that is easy to extend, test, and maintain. These principles are not strict rules but guidelines that help avoid future problems.

Design principles help ensure that systems remain flexible, scalable, and easy to work with. They reduce complexity and prevent unnecessary headaches as the system grows.

When learning any concept, you should understand three things: **what it is**, **why it is needed**, and **how it is useful**. The same applies to design principles.

Design principles are strategies that guide how we implement components, write clean code, and design system architecture. By following these principles, we save ourselves from future issues and build systems that are adaptable and maintainable.

The purpose of teaching design principles is similar to traditional learning methods where individuals were trained not just with knowledge but with values and structure. In the same way, system design prepares developers to build meaningful, scalable, and long-lasting software systems.

The goal of system design principles is to provide a strong foundation for building scalable, efficient, and user-friendly systems. These principles help create software that is easy to understand, customize, and extend in the future.

As applications grow, several challenges arise. Bugs may appear over time as the system interacts with more components. Frequent changes become inevitable, and even simple tasks can require significant effort if the system is not designed properly. That is why domain knowledge and proper design become crucial.

Now let us discuss some important **software design principles** commonly asked in interviews.

The first principle is **DRY – Don’t Repeat Yourself**. This principle states that you should not duplicate code. If the same logic is used multiple times, it should be written once and reused, usually by placing it inside a method.

The next principle is **YAGNI – You Ain’t Gonna Need It**. This means you should not write code unless it is actually required. Writing unnecessary functionality in advance can lead to wasted effort and future rework.

The most important set of principles is **SOLID**, which is frequently asked in interviews.

SOLID stands for:

* S – Single Responsibility Principle (SRP)
* O – Open/Closed Principle
* L – Liskov Substitution Principle
* I – Interface Segregation Principle
* D – Dependency Inversion Principle

Now let us begin with **Single Responsibility Principle (SRP)**. SRP states that **a class should have only one responsibility**. One class should do only one thing.

The intention behind SRP is to avoid confusion and reduce complexity. Consider a hospital example. There are general physicians and specialists. A general physician handles common illnesses, while specialists handle serious or specific conditions. Each has a clear responsibility.

Similarly, in software design, if a class tries to handle too many responsibilities, it becomes difficult to manage and maintain. A well-designed system clearly separates responsibilities across different classes.

For example, people may own both a car and a boat. A car is meant for driving on roads, and a boat is meant for water. Even though one person may use both, their purposes are different. In the same way, software components should be designed to handle only their specific responsibilities.

Following the Single Responsibility Principle helps create clean, understandable, and maintainable systems that can easily adapt to future changes.

But what if somebody thinks that instead of having two different vehicles, why not have a single vehicle that can run both on roads and on water? At first glance it sounds smart, and technically such vehicles do exist. However, they are not very popular. The reason is tight coupling. When a single system is built to serve multiple functionalities—here, a car and a boat—both functionalities are tightly coupled together. If something goes wrong with the car-related functionality, you will not be able to use the boat-related functionality either, because they are part of the same tightly coupled system. When multiple components are combined into one system and one part fails, the failure spreads and impacts the entire system.

Normally, to avoid this situation, we try to keep components separate. If the car and the boat were two different entities, then even if the car stopped working, you could still use the boat, and if the boat failed, you could still use the car. This separation ensures loose coupling, where failure in one component does not bring down the entire system.

The same idea applies in software and even in daily life examples. Take a mouse and a keyboard. These days everything is USB controlled. From personal experience, there was an option to buy a mouse and a keyboard separately, which would occupy two USB ports. To save a USB port, there was also an option to buy a combo where both mouse and keyboard work with a single USB receiver. It feels like a smart decision, but later if that single USB receiver gets misplaced, neither the mouse nor the keyboard will work. If they had been bought separately, even after losing one USB, at least one device would still work. This happens because both devices were tightly coupled through a single USB. If they were separate, they would be loosely coupled, and failure of one would not impact the other.

Now let us move to a software example. Suppose we have an Employee class with attributes such as id, name, and date of joining. A constructor initializes these values. Inside the same class, we also define behaviors such as calculateSalary, hireEmployee, and evaluateEmployee. In addition, we have getters and setters for id, name, and date of joining. In the main method, we create an Employee object, assign an id, a name, and the current date, and then use getter methods to retrieve these values. We also call methods like hireEmployee, calculateSalary, and evaluateEmployee.

At first glance, this may look fine and may even appear to follow the single responsibility principle. However, the number of methods does not define single responsibility. Single responsibility means that a class should be changed or impacted for only one reason, by only one actor. In this Employee class, calculateSalary belongs to the finance team, hiring belongs to HR, and evaluation belongs to managers. Although everything is placed in a single class, changes are being driven by multiple actors. Finance, HR, and managers may all need to modify this class for their own reasons. Because of this, a change made by one team can unintentionally impact others.

For example, if the finance team changes the tax slab logic, the calculateSalary method changes. Even though HR and managers are not involved, the entire Employee class must be redeployed. During that deployment, HR-related or evaluation-related functionality is also affected, even though no changes were made there. This makes the class tightly coupled and fat, which is bad both for design and maintainability. Single responsibility does not mean one method per class; it means one reason to change. Since this class has multiple reasons to change, it violates the single responsibility principle.

To fix this, the code can be refactored by separating responsibilities into different classes. The Employee class should only contain employee-related data such as id, name, and date of joining. Salary calculation can be moved into a SalaryCalculator class, which is handled by the finance team. Employee evaluation can be moved into an EmployeeEvaluator class, handled by managers. Hiring logic can be moved into an EmployeeHiring class, handled by HR. Now each class has only one actor responsible for changes. If finance changes salary logic, only SalaryCalculator changes. HR and managers are unaffected. This ensures loose coupling and adherence to the single responsibility principle. A class should change only for one reason, even if it contains multiple methods.

Next comes the open–closed principle. This principle says that software entities should be open for extension but closed for modification. In simple terms, we should be able to add new features without changing existing code. For example, suppose we build an AnimalFeeder application that initially feeds dogs. Later, we want to add support for cats. If we modify the existing AnimalFeeder class every time we add a new animal, this approach will not scale. Even though it may work without compile-time or runtime errors, it is a poor design.

To solve this, we use interfaces. We define an Animal interface with a feed method. Then we create separate classes like Dog and Cat that implement this interface and provide their own feed logic. The AnimalFeeder class depends only on the Animal abstraction, not on concrete implementations. When a new animal such as Tiger is added, we simply create a new class that implements Animal. The AnimalFeeder class does not change at all. In this way, the system is open for extension but closed for modification.

The Liskov Substitution Principle builds on this idea. It says that a derived class should be substitutable for its base class without altering the correctness of the program. In other words, wherever a parent class is expected, a child class should be usable without changing behavior. Just satisfying an “is-a” relationship is not enough. The child must fully honor the behavior expected from the parent.

Consider a Cat class with methods like drinkMilk and makeSound. A PetCat can correctly implement both. But a ToyCat, which is mechanical, cannot drink milk. If ToyCat extends Cat and throws an exception in drinkMilk, it violates the Liskov Substitution Principle. Even though ToyCat is a Cat by inheritance, it cannot behave like a real Cat in all situations.

This leads to the Interface Segregation Principle. This principle says that interfaces should be small and focused, and no class should be forced to implement methods it does not use. Instead of having a single fat interface with many methods, we should split it into multiple smaller interfaces. For example, we can have a MechanicalCat interface with only makeSound, and a LivingCat interface that includes both makeSound and drinkMilk. A toy cat implements MechanicalCat, while a real cat implements LivingCat. This avoids forcing classes to implement irrelevant methods and prevents Liskov violations.

Finally, the Dependency Inversion Principle states that high-level modules should not depend on low-level modules. Both should depend on abstractions. Also, abstractions should not depend on details; details should depend on abstractions. When high-level classes directly depend on low-level implementations, the system becomes tightly coupled. Any change in low-level code can break high-level code.

A simple analogy is an organizational hierarchy. A CEO does not directly deal with employees. Communication flows through managers, directors, and VPs. This layered structure reduces dependency and makes the system stable. Similarly, in software, high-level logic should depend on interfaces or abstractions, not concrete classes. This keeps the system loosely coupled, flexible, and easier to extend.

All five SOLID principles are interrelated. Violating one often leads to violations of others. Together, they help us design systems that are flexible, maintainable, scalable, and resilient to change.
