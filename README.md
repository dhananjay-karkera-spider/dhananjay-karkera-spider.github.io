Microservices on Azure - Part I

The Story reader app 
Main Components
	A drop down listing the Story Titles available with the application
	A reading section to display the content. This section takes up most of the area of the page.
	A dictionary section to displays dictionary results for words selected from the reading section. This section is displayed in a collapisble pane.
	
Implementation: 
	The UI consumes three services
		1. Get the list of titles available in the online library
		2. Get the content for the title selected
		3. A DictionaryService to lookup the word meaning
		
UI implementation - Html Page + javascript + css (Azure Storage)

As a minimal implementation I choose to go with Azure functions. Scope of each service is limited to a single task without dependency on the other.

1. Trigger based (HttpTrigger, GitHub Webhook, Blob and Queue Triggers....)
2. Nuget package integration - so you can still use any third party libraries 
3. Reference dlls for code sharing
4. Swagger
5. Cost effective - consumption plan
6. Scalable
8. Multiple language support (C#, Java, Python, Javascript)
11. Security - token based
12. Each function can be developed, tested and deployed separately.
9. Deployment Slot
4. .NET Core 2.0 support
10. CI integration

Each Azure function could be used in a standalone mode or as building blocks for workflows (Azure Logic Apps)

Consider an Expense Reimbursement App used by Users with different roles. The Expense approval workflow is triggered by a user raising an request for a reimbursement, request going the review process and getting approved/rejected, approver eith

 
	