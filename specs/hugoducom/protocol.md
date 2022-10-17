# Protocol objectives:

The protocol is a simple client-server protocol.

The client can send a mathematical expression to evaluate in a certain order
(addition, subtraction, division and multiplication) to the server.

It only works with integer numbers.

The server evaluate the expression and send the result back to the client.

The client can close the connection whenever he wants.

# Overall behavior:

| Specifity          | Value           |
|--------------------|-----------------|
| Transport protocol | UDP             |
| Port               | IP_ADDRESS:2727 |

When the client connects to the server, the server prints a help message with
all the commands available.

The client can close the connection by just sending `bye` to the server.

# Messages:

Sequence of the message :
1. `number1`
2. `operation`
3. `number2`

# Specific elements (if useful)

Operations supported:
- `+`
- `-`
- `*`
- `/`

Error handling:
- When an operation is not supported
- When the syntax or the sequence is not respected
- When the provided number is not an integer

Possible improvements:
- Float numbers

# Examples:

```
> nc localhost 3333
Hello welcome to the super calculator machine!
Operations supported : "+", "-", "*", "/".
Only integer numbers are valid.
Example : 11+12

10+19
Answer: 29
bye
Goodbye!
```
