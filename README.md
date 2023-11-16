<h1>LangChain - Build Large Language Model to chat to your data</h1>



<h2>Overview</h2>

ChatWithYourData_Bot is a conversational chatbot powered by LangChain's framework and integrated with OpenAI's API. It facilitates interactive discussions with a focus on leveraging information stored in documents. The bot is designed to engage in meaningful conversations based on a loaded document database, providing users with answers and relevant source documents.

<h2>Features</h2
              
Document Loading: Load PDF documents into the system for chatbot interaction.
Conversation History: Track and display the chat history between the user and the bot.
Database Query: Retrieve information from the loaded document database based on user queries.
Source Document Display: View the documents that contribute to the bot's responses.
Configurability: Easily configure and clear the chat history to start a new topic.
<h2>Usage</h2
           
Load a PDF document using the provided interface.
Initiate conversations by entering queries in the input box.
Explore database queries and view source documents for each interaction.
Clear the chat history when needed to start fresh conversations.
<h2>Components</h2
                
Conversation Tab: Enter queries and engage in interactive conversations with the bot.
Database Tab: Review database queries and explore source documents.
Chat History Tab: View the history of conversations with the bot.
Configure Tab: Manage document loading, clear chat history, and configure the chatbot.
<h2>Dependencies</h2
                  
LangChain Framework
OpenAI API
<h2>Getting Started</h2
                     
load_db Function
- This function loads a PDF document specified by the 'file' parameter.
- It uses LangChain's RecursiveCharacterTextSplitter to break the document into chunks for processing.
- Text embeddings are generated using OpenAI's embeddings.
- The document chunks are then converted into a vector database using LangChain's DocArrayInMemorySearch.
- A retriever is defined to search for similar documents in the database based on user queries.
- Finally, a conversational retrieval chain is created using LangChain's ConversationalRetrievalChain, incorporating an OpenAI language model (ChatOpenAI).

cbfs Class
- This class, using Param and Panel, manages the user interface components and interactions.
- The __init__ method initializes class attributes, including setting up the initial document and chatbot.
- call_load_db is a method triggered by a button click to load a new document and update the chatbot accordingly.
- convchain processes user queries, interacts with the chatbot, and updates the UI with the conversation history.
- get_lquest and get_sources are methods to display information about the last database query and source documents, respectively.
- get_chats displays the chat history.
- clr_history clears the chat history

Panel Configuration
- This section configures the user interface using Panel.
- Tabs are created for different aspects of the application: Conversation, Database, Chat History, and Configuration.
- Each tab contains specific UI components, such as input boxes, buttons, and panels displaying chat history, database queries, and source documents

Running the Dashboard
- An instance of the cbfs class is created.
- File input, buttons, and text input components are initialized.
- Callbacks are set up to handle button clicks and user input.
- The final dashboard is constructed by arranging the UI components into tabs.

<br />



</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
