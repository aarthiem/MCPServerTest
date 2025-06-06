# Build your MCP Server using C# SDK

This repo is for educational purposes to explore how to create your own MCP server using C# SDK.

![image](https://github.com/user-attachments/assets/69dc3fb9-6d09-47f9-89eb-7aae3c18da5e)

[Official MSFT blog](https://devblogs.microsoft.com/blog/microsoft-partners-with-anthropic-to-create-official-c-sdk-for-model-context-protocol) 

## Steps to build
This is a simple .NET console application that builds a MCP server with 3 simple methods namely to return echo, reverse, length of the input string. This project is based on the sample explained in (Introduction to the C# SDK for Model Context Protocol (MCP))[https://www.youtube.com/watch?v=krB1aA9xpts]

To build MCP server using c# SDK, follow the below steps
- Create a .NET console application
- Add Nuget packages Microsoft.Extensions.Hosting and ModelContextProtocol
- To expose your method as MCP tool decorate it with attribute [McpServerToolType] and provide clear description so the LLM can decide which tool to invoke
- Build the project
- Add mcp.json under .vscode folder to add new server. Add the server with the project location to run the dotnet command
- Run your server now
- Open GH Copilot Chat window and run it under Agent mode
- Once the app is running, you can click on the Tools icon on the GH Copilot chat window.
- Now you will see the three tools available
  
![image](https://github.com/user-attachments/assets/bc194aac-5090-4c89-bf0a-891344c36f83)
- Use the GH copilot chat as the client and ask it to reverse a given string as below. This will invoke the reverse tool from the MCP server and return the result
<img width="274" alt="image" src="https://github.com/user-attachments/assets/0c70cfb9-8bab-4961-97e8-7685dd80521c" />




