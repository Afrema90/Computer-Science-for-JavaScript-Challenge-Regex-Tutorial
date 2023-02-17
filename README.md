# Regex Tutorial Starter Code
 This week is we where asked to create a tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does. we where giving a template provided in the starter code to create your tutorial.

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines
Acceptance Criteria
GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile
i did this with the help of my study buddy David And my tutor Chris B.
i go my information on https://code.tutsplus.com/tutorials/8-regular-expressions-you-should-know--net-6149

/^(start)
(https?:\/\/)?((optional http:// or https://)
    [\da-z\.-]((digits, letters, dots, hyphens))
    +)\.([a-z\.](extension with letters and dots )
        {2,6})(optional files or directories)
            [\/\w \.-]*)*\/?
            $/(end)
