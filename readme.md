# Axendo back-end developer case

## Introduction

Thanks for deciding to take on the case! 
Below is a brief introduction to help you get started:

- From the moment you receive it, you have 24 hours to complete it.
- The completed case should be a Visual Studio (2019/2022) project with all associated code.
- If you have any questions about the assignment while working on it, feel free to call Gerben at 06-24734869.
- It is OK to have multiple commits. Please send an e-mail gerben.vandiggelen@axendo.nl once your case is ready.
 
## What will the case be evaluated on?
- Demonstrable knowledge level of the used technology (ASP.NET MVC / ASP.NET Core MVC)
- Quality and structure of the code (for example, the DRY principle)
- Correct functioning of the application

We wish you the best of luck in completing the case.



## The Case

An imaginary company stores a list of software products they use. They have stored the name and version of each product. They have asked us to create a simple ASP .NET MVC website where users can type in a version number and receive a list of software products that are greater than the version they entered. The user also has the option to search freely with queries like: "MS Word 13.2.1". If the user enters an invalid version, they should be notified that the version is not valid.

The software versions are stored as a string in a custom version format which has 5 parts stored as the format [major].[minor].[patch].[build].[compilation]. Each version part will always be non-negative integers. You may see versions like “2”, “1.5”, or “2.12.4.0.6”. The period is only used as a separator and does not represent a decimal point – 1.5 does not mean one and a half.

- "2" == "2.0" == "2.0.0" == "2.0.0.0" == "2.0.0.0.0"
- "2" < "2.0.0.0.1"
- "2" < "2.1"
- "2.0.1" < "2.1.0"

The imaginary company stores the software list as a C# object (provided below) that you can simply drop into your code – no need to call a database or REST service. This list of software is just a sample, assume the company will eventually switch to getting list from a database with thousands of softwares.

This site will be publicly available, so user authentication will not be required.

# Software Product List

    public class Software
    {
        public string Name { get; set; }
        public string Version { get; set; }
    }

    public static class SoftwareManager
    {
        public static IEnumerable<Software> GetAllSoftware()
        {
            return new List<Software>
            {
                new Software
                {
                    Name = "MS Word",
                    Version = "13.2.1"
                },
                new Software
                {
                    Name = "AngularJS",
                    Version = "1.7.1"
                },
                new Software
                {
                    Name = "Angular",
                    Version = "13"
                },
                new Software
                {
                    Name = "React",
                    Version = "0.0.5"
                },
                new Software
                {
                    Name = "Vue.js",
                    Version = "2.6"
                },
                new Software
                {
                    Name = "Visual Studio",
                    Version = "17.0.31919.166.0"
                },
                new Software
                {
                    Name = "Visual Studio",
                    Version = "16.11.9.3.55"
                },
                new Software
                {
                    Name = "Visual Studio Code",
                    Version = "1.63"
                },
                new Software
                {
                    Name = "Blazor",
                    Version = "3.2.0"
                }
            };
        }
    }
