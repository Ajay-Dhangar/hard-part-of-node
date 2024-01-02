# Node Js Learning

## Node Overview (client-server)

Will diagrams client-server interactions in a web application to highlight the area where Node operates.

```mermaid
sequenceDiagram
    participant Client as Client
    participant Server as Server

    Client->>Server: Request
    Server->>Server: Processing (Node.js)
    Server-->>Client: Response
```

<h2 align="center"> OR</h2>

```mermaid
graph TD
  subgraph Client
    A(Web Browser)
  end

  subgraph Server
    B(Node.js)
  end

  A -->|Request| B
  B -->|Response| A
```

**In this Mermaid flowchart:**

- The client (browser) sends a request to the server.

- Node.js on the server processes the request.
- The server sends a response back to the client.
- Node.js is a JavaScript runtime environment that allows JavaScript to run on the server.
- Node.js is designed for asynchronous, non-blocking operations and building scalable servers.
- Node.js is event-driven, which means that everything that happens in Node is in reaction to an event.
- Node.js is single-threaded, which means that everything that happens in Node is run in a single thread.

---

## JavaScript, Node, and Computers

Will explains the role of JavaScript and Node within a server and differentiates between the two roles.
    
```mermaid
graph LR
subgraph Client
    A(Web Browser)
end
subgraph Server
    B[(Node.js)]
end
A -->|Request| B
B -->|Response| A
```

**Role of JavaScript on the Server**

```mermaid
graph TD
  subgraph Client
    C(Client - Browser)
  end

  subgraph Server
    JS(Server-Side JavaScript)
    C -->|Request| JS
    JS -->|Processing| JS
    JS -->|Response| C
  end

```

**In this Mermaid flowchart:**

- The client (browser) sends a request to the server.
- JavaScript on the server processes the request.
- The server sends a response back to the client.

### Role of Node.js on the Server:

```mermaid
graph TD
  subgraph Client
    C(Client - Browser)
  end

  subgraph Server
    Node(Node.js)
    C -->|Request| Node
    Node -->|Processing| Node
    Node -->|Response| C
  end

```

**In this Mermaid flowchart:**

- The client (browser) sends a request to the server.
- Node.js on the server processes the request.
- The server sends a response back to the client.

### Differentiation:

```mermaid
graph TD
  subgraph Client
    C(Client - Browser)
  end

  subgraph Server
    JS(Server-Side JavaScript)
    Node(Node.js)
    C -->|Request| JS
    JS -->|Processing| JS
    JS -->|Response| C
    C -->|Request| Node
    Node -->|Processing| Node
    Node -->|Response| C
  end

```

<h2 align="center"> OR</h2>

```mermaid
graph LR
  subgraph JavaScript
    JS(Server-Side JavaScript)
  end

  subgraph Node.js
    Node(Node.js)
  end

  JS -->|Server-Side Logic| JS
  JS -->|Handling Requests and Responses| JS

  Node -->|Event-Driven and Asynchronous| Node
  Node -->|Building Scalable Servers| Node
  Node -->|Use Cases| Node

```

<h2 align="center"> OR</h2>

```mermaid
graph TD
  subgraph JavaScript
    JS(JavaScript)
  end

  subgraph Node.js
    Node(Node.js)
  end

  JS -->|Can run on server| Node
  Node -->|Specific runtime| Node
  Node -->|Asynchronous| Node
  Node -->|Scalable servers| Node

```

**In this Mermaid flowchart:**

- JavaScript can run in various environments, including servers.
- Node.js is a specific runtime environment for server-side JavaScript.
- Node.js is designed for asynchronous, non-blocking operations and building scalable servers.

---

## Executing JavaScript code review

Will demonstrates how to execute JavaScript code in the terminal using the Node REPL (Read-Eval-Print-Loop).

```mermaid
sequenceDiagram
    participant Terminal as Terminal
    participant NodeREPL as NodeREPL

    Terminal->>NodeREPL: Open terminal
    Terminal->>NodeREPL: Type 'node' and press Enter
    Terminal->>NodeREPL: Node REPL starts
    Terminal->>NodeREPL: Enter JavaScript code
    NodeREPL->>NodeREPL: Evaluate and print result
    Terminal->>NodeREPL: Repeat as needed
    Terminal->>NodeREPL: Type '.exit' to exit REPL

```

<h2 align="center"> OR</h2>

```mermaid
graph TD;
    A[Open Terminal];
    B[Type node and press Enter];
    C[Enter REPL];
    D[Type JavaScript code];
    E[Press Enter to execute];
    F[See output];
    G[Exit REPL];

    A -->|step-1| B;
    B -->|step-2| C;
    C -->|step-3| D;
    D -->|step-4| E;
    E -->|step-5| F;
    F -->|step-6| G;
    G -->|step-7| A;

```

Explanation:

1. **Open Terminal**: Open your terminal or command prompt.

2. **Type "node" and press Enter**: Launch the Node.js environment in the terminal by typing "node" and pressing Enter.

3. **Enter REPL**: You will enter the Node REPL (Read-Eval-Print-Loop), indicated by the continuation of the flow.

4. **Type JavaScript code**: Input your JavaScript code directly into the REPL.

5. **Press Enter to execute**: Execute the entered JavaScript code by pressing Enter.

6. **See output**: View the output generated by the executed code.

7. **Exit REPL**: If you want to exit the Node REPL, type `.exit` or press `Ctrl + C` twice.

This flowchart provides a step-by-step guide for executing JavaScript code in the Node REPL in the terminal. Adjustments can be made based on specific needs or additional details.


---

Will walks line by line through the execution of code in JavaScript to demonstrate what is going on under the hood.

```mermaid
sequenceDiagram
    participant C as Client
    participant JS as JavaScript

    C->>JS: Function Definition<br/><br/>function addNumbers(a, b)
    C->>JS: Function Invocation<br/><br/>let result = addNumbers(3, 5)
    JS-->>JS: Function Execution
    JS->>JS: Variable Declaration<br/>let sum = a + b;
    JS-->>JS: Return<br/><br/>return sum;
    JS->>C: Store Result<br/><br/>let result = 8
    C->>JS: Logging<br/><br/>console.log(result)
    JS-->>C: Log Result<br/><br/>Prints: 8
```

**The diagram shows the flow of execution:**

1. The client sends a function definition to JavaScript.
2. The client invokes the function with arguments.
3. JavaScript executes the function, involving variable declaration, addition operation, and return statement.
4. The result is stored in the client.
5. The client logs the result to the console.

---

## Executing Node.js code

Will discusses how Node is able to talk with the inner features of the server computer to enable network communication.

```mermaid
sequenceDiagram
    participant Terminal as Terminal
    participant Node as Node
    participant Server as Server

    Terminal->>Node: Open terminal
    Terminal->>Node: Type 'node' and press Enter
    Terminal->>Node: Node REPL starts
    Terminal->>Node: Enter Node.js code
    Node->>Server: Send request
    Server->>Node: Send response
    Node->>Terminal: Print response
    Terminal->>Node: Repeat as needed
    Terminal->>Node: Type '.exit' to exit REPL
```


<h2 align="center"> OR</h2>

```mermaid
graph TD
  subgraph ServerComputer
    A[Node.js Application] -->|Uses APIs| B[Inner Features of the Server]
  end

  subgraph Network
    B -->|Network Communication| C[External Systems or Clients]
  end
```

**Explanation:**

- **Node.js Application** communicates with the `Inner Features of the Server using APIs`. This represents how Node.js interacts with the underlying system resources and features.

- The interaction with the inner features of the server enables `Network Communication` with external systems or clients. This is where Node.js leverages its event-driven, non-blocking I/O model to efficiently handle multiple network requests.

- The arrows in the flowchart indicate the flow of communication from the Node.js application to the inner features of the server and, subsequently, to external systems or clients.


<h2 align="center"> OR</h2>

```mermaid
sequenceDiagram
    participant Server as Server
    participant InnerFeatures as InnerFeatures

    Node->>Server: Initiates Network Communication
    Server->>InnerFeatures: Accesses Inner Features
    InnerFeatures-->>Server: Processes and Responds
    Server-->>Node: Sends Response

```

**Explanation:**

- **Initiation:** Node initiates network communication with the server.

- **Access Inner Features:** The server (S) utilizes its inner features to handle the incoming network communication.

- **Processing and Response:** The inner features process the request, and the server sends a response.

- **Response to Node.js:** The server sends the processed response back to Node, completing the communication.

---

