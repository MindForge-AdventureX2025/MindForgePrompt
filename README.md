# Prompt-Agents-Collection

A comprehensive collection of prompt templates and agent definitions for building intelligent systems through prompt engineering.

## 🌟 Overview

This repository serves as a centralized hub for organizing and sharing prompt templates used in various AI agents and systems. It provides standardized JSON schemas for different agent types, making it easier to integrate and utilize them in your projects.

## 🤖 Available Agents

### 1. Summarization Agent (`summarize_agent`)
An intelligent agent designed to generate concise summaries of provided content.

**Capabilities:**
- Condenses lengthy text while preserving key information
- Identifies main themes and important points
- Works with various content types including journal entries, articles, and reports

**Input:** Content title and body text  
**Output:** Condensed summary maintaining critical information

### 2. Report Generator Agent (`report_agent`)
Specialized in creating comprehensive reports from data files, especially visulization tables and graphs.

**Capabilities:**
- Generates structured reports with proper formatting
- Analyzes trends and patterns in data
- Creates visualizations through markdown tables
- Offers actionable insights and recommendations

**Input:** Report type and data files to analyze  
**Output:** Formatted report with sections, insights, and visualization

### 3. Search Agent (`search_agent`)
A research-focused agent that retrieves relevant information based on queries.

**Capabilities:**
- Conducts targeted web searches
- Returns structured results with titles, URLs and snippets
- Customizable number of results

**Input:** Search query and desired number of results  
**Output:** Array of search results with metadata

### 4. Supervisor Agent (`supervisor_agent`)
Meta-agent that orchestrates workflows by coordinating multiple specialized agents.

**Capabilities:**
- Analyzes user requests to determine required sub-tasks
- Delegates work to appropriate specialized agents
- Manages complex multi-step processes
- Handles parameter passing between agents

**Input:** High-level user request  
**Output:** Structured task assignments for worker agents

## 🔧 Usage

Each agent is defined in a standardized JSON format specifying:
- Unique identifier name
- Input parameters and their types
- Output structure
- Working examples

To use these agents in your application:

```javascript
// Example of using the summarize agent
const result = await invokeAgent("summarize", {
  title: "Meeting Notes - July 15",
  content: "During our quarterly planning meeting, we discussed..."
});

console.log(result); // Returns a concise summary
```

## 🔄 Integration Examples

The agents can work together to solve complex tasks:

```javascript
// Example: Research and report generation workflow
const supervisorResult = await invokeAgent("supervisor_agent", {
  user_request: "Create a report about meditation techniques for anxiety management"
});

// Supervisor will delegate to search_agent and report_agent as needed
```


*This repository is actively maintained. For questions or suggestions, please open an issue.*
