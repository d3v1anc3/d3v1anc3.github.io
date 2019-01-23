---
layout: post
title: "The only thing your (ASP.Net Core) WebAPI controller should do"
description: "How to keep your webapi clean."
category: Code
tags: [SRP, Single Responsibility Principle]
---
{% include JB/setup %}

The controller is a class that handles browser requests. It receives input, possibly in the form of model data, and it returns a response. In other words the single responsibility of the Controller is to return a HTTP Response based on the input it is given.

This means, it is not responsible for business logic, nor is it responsible for logging or input validation. 

What not to expect in a controller method:
	- A new modifier
	- A cyclomatic complexity higher than one? (TO CHECK)

What to expect in a controller method:
	- A try catch statement to assure the return of the correct HTTP Error codes.
	- A call to an interactor interface
	- (optionally) a conversion between the input and whatever is required by the interactor interface.

So to get back to the single responsibility. The controller class is responsible to convert the output of the interactor into a Http response message.
