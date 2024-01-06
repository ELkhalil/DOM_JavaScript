# Introduction to the DOM
    The Document Object Model (DOM) is the data representation of the objects that comprise the structure 
    and content of a document on the web. This guide will introduce the DOM, look at how the DOM represents 
    an HTML document in memory and how to use APIs to create web content and applications.

# What is the DOM?
    The Document Object Model (DOM) is a programming interface for web documents. It represents the page so 
    that programs can change the document structure, style, and content. The DOM represents the document as 
    nodes and objects; that way, programming languages can interact with the page.

# How does the process work (understand the process)
    window document is just an object that lives in the window we can check it's content:
    console:
        console.dir(window.document);

    REMEMBER:
        those are just API that are inside the browser that will help us manipulate it...
        but the difference is DOM will give us API to our HTML && CSS code and BOM will be responsible for the
        browser components.
            DOM:
                lives in the document
                document is inside a global object (window)
                window global object:
            BOM:
                Browser Object Model
                it is from the global object (window) but it gives us only the browser details
                in simple words the BOM will give us access to the browser and it's component like:
                    console : window.navigator // it will give you the details of the browser window
                              window.screen; // it will gives us the details and the quality of the screen
            JavaScript Code:
                Interesting but window global object also have the javascrip code we passed to out HTML
                meaning we can access that code from the window
                example:
                    window.variable;  //variable is created inside our script file linked to our index.html

# How to use event listeners to access a DOM Element (DOMContentLoaded)
    -> we can run a script only if the DOM is loaded and finished 
       so we can know the HTML is finished loading... 
        <script>
            window.addEventListner(
                "DOMContentLoaded",
                () => {
                    console.log(
                        document.getElementById("wrapper"),
                    );
                },
            );
        </script>
    -> you can use anything to listen to until it finish everything (it is bad and consume a lot of time)
     <script>
            window.addEventListner(
                "load",
                () => {
                    console.log(
                        document.getElementById("wrapper"),
                    );
                },
            );
        </script>
    -> be sure that the DOM is finished and run your script that uses those nodes because if the tree is not finished it will not
       be available (null)

# HTML Script Tag (Inline vs. Async vs. Defer) 
    the HTML parsing go line by line until it fin a script tag it stops there and download the script 
    after that it execute it...
    - we can add an attribute to our script tag to change it's behavior (how it will be downloaded/executed)
    # all of the 3 do the same thing witch is Download and Execute they all share the same goal but they have a major different
        Flow.
    -> Inline
        <script src="./js/main.js"></script>
        in this the browser froze until it download the script and wait for it until it is downloaded and executed but the issue is the
        parsing of the HTML is paused... it is called blocking because of this behavior.
    -> Async
        <script src="./js/main.js" async></script>
        the browser start parsing but if it encounter a script tag it start downloading but it did not stop the HTML parse they go in\
        parallel, the issue rise in the script execution phase where it stops the browser until the script is executed.
    -> Defer
        <script src="./js/main.js" defer></script>
        same as the Async + it does not stop the HTML parsing and defer meaning do not execute it now wait until the parser finishes
        it's job...
    
# DOM Nodes Demystified
    -> the goal is to understand how things work and how does the node content is added
        workflow: how an object is filled

            HTML Parsing -> Select a Node -> Define the Node Type -> Set The Interfaces (Prototype Chain) -> Fill The Object
                                <html>          ELEMENT_NODE                                                     document.documentElement

# 
    Frontend Path:
    1️⃣ HTML
    2️⃣ CSS
    3️⃣ Make small projects using the basics (Convert UIs to HTML / CSS)

    ---------
    4️⃣ JavaScript Basics
    5️⃣ JavaScript Prototype
    6️⃣ JavaScript DOM
    🟩 Make Small Projects

    ---------
    7️⃣ JavaScript ES6
    8️⃣ ReactJS or VueJS
    8️⃣ TypeScript if you'll choose Angular as a Framework
    9️⃣ Angular
    🟩 Make Small Projects

    ----------
    🟩 Make Large Projects



















































