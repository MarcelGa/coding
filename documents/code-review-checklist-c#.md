1. Make sure that there shouldn’t be any project warnings, treat warning as errors
2. It will be much better if Code Analysis is performed on a project (with all Microsoft Rules enabled) and then remove the warnings.
3. Use asynchronous programming using C# async await where application, as it tremendously improves the performance. [more](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/)
4. Use C# new language features, for example use nameof operator to get the property/method names instead of hard coding it
if (IsNullOrWhiteSpace(lastName))
throw new ArgumentException(message: “Cannot be blank”, paramName: nameof(lastName));
5. All unused usings need to be removed. Code cleanup for unnecessary code is always a good practice.
6. ‘null’ check needs to be performed wherever applicable to avoid the Null Reference Exception at runtime, use C# 6.0 new feature “Null-conditional operators” for this, one example as given below
var first = person?.FirstName;
[more](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-6)
7. Follow best practices while writing code by following [SOLID](https://www.c-sharpcorner.com/UploadFile/damubetha/solid-principles-in-C-Sharp/) principle and software [design patterns](https://www.dofactory.com/net/design-patterns)
8. Write loosely coupled components, follow dependency injection concept, extremely important, helps while doing unit testing as well. [more](https://www.dotnetcurry.com/software-gardening/1284/dependency-injection-solid-principles)
9. Code Reusability: Extract a method if the same piece of code is being used more than once or you expect it to be used in future. Make some generic methods for repetitive task and put them in a related class so that other developers start using them once you intimate them. Develop user controls for common functionality so that they can be reused across the project. [more](http://msdn.microsoft.com/en-us/library/office/aa140806(v=office.10).aspx)
10. Code Consistency: Let’s say that an Int32 type is coded as int and String type is coded as string, then they should be coded in that same fashion across the application. But not like sometimes int and sometimes as Int32.
11. Code Readability: Should be maintained so that other developers understand your code easily. [more](http://msdn.microsoft.com/en-IN/library/aa291591(v=vs.100).aspx)
12. Disposing of Unmanaged Resources like File I/O, Network resources, etc. They have to be disposed of once their usage is completed. Use usings block for unmanaged code, if you want to automatically handle the disposing of objects once they are out of scope. [more](http://msdn.microsoft.com/en-us/library/498928w2.aspx)
Use new feature of deallocating unmanaged resources. [more](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8#using-declarations)
13. Proper implementation of Exception Handling (try/catch and finally blocks) and logging of exceptions. [more](http://msdn.microsoft.com/en-us/library/vstudio/ms229005(v=vs.100).aspx)
14. Naming conventions to be followed always. Generally for variables/parameters, follow Camel casing and for method names and class names, follow Pascal casing. [more](http://msdn.microsoft.com/en-us/library/ms229043.aspx)
15. Making sure that methods have less number of lines of code. Not more than 20 to 30 lines
16. Timely check-in/check-out of files/pages at source control (like TFS). [more](http://www.codeproject.com/Tips/593014/Steps-Check-in-Check-Out-Mechanism-for-TFS-To-avoi)
17. Peer code reviews. Swap your code files/pages with your colleagues to perform internal code reviews.
18. Unit Testing. Write developer test cases and perform unit testing to make sure that basic level of testing is done before it goes to QA testing. [more](https://msdn.microsoft.com/en-us/library/hh694602.aspx)
19. Avoid nested for/foreach loops and nested if conditions as much as possible.
20. Use anonymous types if code is going to be used only once. [more](http://msdn.microsoft.com/en-us/library/vstudio/bb397696.aspx)
21. Try using LINQ queries and Lambda expressions to improve Readability. [more](http://msdn.microsoft.com/en-us/library/bb308959.aspx)
22. Use PLINQ wherever applicable, as it makes parallel operation within LINQ query and improves the performance [more](https://docs.microsoft.com/en-us/dotnet/standard/parallel-programming/introduction-to-plinq)
23. Proper usage of var, object, and dynamic keywords. They have some similarities due to which most of the developers are confused or don’t know much about them and hence they use them interchangeably, which shouldn't be the case. [more](http://blogs.msdn.com/b/csharpfaq/archive/2010/01/25/what-is-the-difference-between-dynamic-and-object-keywords.aspx)
24. Use access specifiers (private, public, protected, internal, protected internal) as per the scope need of a method, a class, or a variable. Let’s say if a class is meant to be used only within the assembly, then it is enough to mark the class as internal only. [more](http://msdn.microsoft.com/en-us/library/kktasw36.aspx)
25. Use interfaces wherever needed to maintain decoupling. Some design patterns came into existence due to the usage of interfaces. [more](http://msdn.microsoft.com/en-IN/library/3b5b8ezk(v=vs.100).aspx)
26. Mark a class as sealed or static or abstract as per its usage and your need. [more](http://msdn.microsoft.com/en-us/library/ms173150(v=vs.100).aspx)
27. Use a Stringbuilder instead of string if multiple concatenations are required, to save heap memory.
28. Check whether any unreachable code exists and modify the code if it exists.
29. Write comments on top of all methods to describe their usage and expected input types and return type information.
30. Use fiddler/Postman tool to check the HTTP/network traffic and bandwidth information to trace the performance of web application and services.
31. Use [constants](http://msdn.microsoft.com/en-us/library/e6w8fe1b(v=vs.100).aspx) and [readonly](http://msdn.microsoft.com/en-us/library/acdd6hb7(v=vs.100).aspx) wherever applicable.
32. Avoid type casting and type conversions as much as possible; because it is a performance penalty.[more](http://msdn.microsoft.com/en-us/library/ms173105.aspx)
33. Override ToString (from Object class) method for the types which you want to provide with custom information. [more](http://msdn.microsoft.com/en-us/library/ms173154(v=vs.100).aspx)
34. Avoid straightaway copy/pasting of code from other sources. It is always recommended to hand write the code even though if you are referring to the code from some sources. By this, you will get good practice of writing the code yourself and also you will understand the proper usage of that code; finally you will never forget it.
35. Always make it a practice to read books/articles, upgrade and follow the Best Practices and Guidelines by industry experts like Microsoft experts and well-known authors like Martin Fowler, Kent Beck, Jeffrey Ritcher, Ward Cunningham, Scott Hanselman, Scott Guthrie, Donald E Knuth.
36. Verify whether your code have any memory leakages. If yes, make sure that they have been fixed. [more](http://blogs.msdn.com/b/davidklinems/archive/2005/11/16/493580.aspx)
37. Try attending technical seminars by experts to be in touch with the latest software trends and technologies and best practices.
38. Understand thoroughly the OOPs concepts and try implementing it in your code.
39. Get to know about your project design and architecture to better understand the flow of your application as a whole.
40. Take necessary steps to block and avoid any cross scripting attacks, SQL injection, and other security holes, follow all OWASP top 10 security rules [more](https://owasp.org/www-project-top-ten/)
41. Always encrypt (by using good encryption algorithms) secret/sensitive information like passwords while saving to database and connection strings stored in web.config file(s) to avoid manipulation by unauthorized users.
42. Avoid using default keyword for the known types (primitive types) like int, decimal, bool, etc. Most of the times, it should be used in case of Generic types (T) as we may not be sure whether the type is a value type or reference type. [more]( http://msdn.microsoft.com/en-us/library/xwth0h0d(v=vs.100).aspx)
43. Usage of ‘out' and 'ref' keywords be avoided as recommended by Microsoft (in the Code analysis Rules and guidelines). These keywords are used to pass parameters by reference. Note that 'ref' parameter should be initialized in the calling method before passing to the called method but for 'out' parameter this is not mandatory.
44. C# language has tremendously improved over a period of time, always use new features while writing programs, below are the latest C# msdn links
> - [c#-6](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-6)
> - [c#-7](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-7)
> - [c#-8](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-8)
> - [c#-9](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9)
> - [c#-10](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-10)
