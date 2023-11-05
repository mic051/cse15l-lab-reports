# Lab 2

## Part 1

![Image](Screenshot 2023-10-22 123624.png)

![Image](Screenshot 2023-10-22 123630.png)

![Image](image.png)

![Image](image(1).png)

Starting with the second screenshot, `main()`, `Server.start(port, new Handler())` is called. Port is the port number of the server passed in from the program call. If a different integer is passed to the program call, then a server will get opened on the new, different port. A new handler is passed to the server so it can receive and handle incoming events before starting it. The second screenshot defines the handler with the variable `storedStrings` of type `ArrayList<String>`. This variable holds the strings added to the server.  `handleRequest(URI url)` handles requests sent to the server. `url` is the url of the request. On line 11, the code checks to see if the url contains the path "/add-message". If it does, it adds the argument to `storedStrings`. If the query contains an s, it stores the passed string in the server and calls `printArrayList(ArrayList<String>)` and returns the results. `printArrayList(ArrayList<String>` formats the contents of the ArrayList<String> into the format "<position>. <string>". If the path does not "/add-message", an error is returned.

## Part 2

![image](https://github.com/mic051/cse15l-lab-reports/assets/146787706/ce64971f-070f-4ec6-b359-f00b8c9b6a4a)

![Image](Screenshot 2023-10-22 131902.png)

## Part 3

This week I learned that ssh keys can be generated with `ssh-keygen`. I also learned that the private key is stored in "~/.ssh" on the connecting machine and the public key is stored in "~/.ssh/authorized_keys" on the connected machine.
