# Description

This repo is intended as a starting point for developing new AWS Lambda Functions using Go.

Provided here are 3 things:

1. A simple Makefile for compiling and ZIP'ing your code so that it's ready to send to Lambda for execution.

2. A standard Go boilerplate for Lambda Go functions

3. The code allows for the Lambda library to unmarshal the Event JSON into an empty interface (void) and then uses a simple type assertion to return a usable indexed map which you can explore.  This means you don't have to pre-create a valid struct to marshal the event into and allows for a more iterative development and debugging of events.

It is recommended that you don't overly rely on this and instead properly create a valid struct and methods which can process your event.

# Lambda Screenshot

Here is an example of this code dumping the event passed from an Alexa Session Init event:

!(https://raw.githubusercontent.com/benr/lambda_go_prototype/master/lambda_screenshot.png)