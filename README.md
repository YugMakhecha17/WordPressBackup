### Social Media Content Tool - n8n Workflow
A powerful n8n automation workflow that generates visually compelling social media posters and advertising content using AI. This tool combines creative text generation with image creation to produce professional-grade marketing materials.
Features

Interactive Form Interface: User-friendly web form for content specifications
AI-Powered Content Generation: Creates engaging post ideas and catchy headlines
Automated Image Generation: Produces high-quality advertising posters using Google Gemini
Customizable Contact Information: Includes your contact details in generated posters
Professional Output: Creates print-ready advertising posters and social media graphics

### Workflow Components
1. Form Trigger (On form submission)

Captures user input through a web form
Collects content specifications and contact information
Triggers the entire automation workflow

2. AI Agent (AI Agent)

Processes user input using GLM-4.5-Air model via OpenRouter
Generates creative and engaging post ideas
Creates catchy titles and descriptions suitable for visual content

3. Image Generation (Generate an image)

Uses Google Gemini 2.0 Flash Exp Image Generation model
Creates professional advertising posters
Incorporates generated content and contact information
Produces print-ready and social media-ready graphics

### Prerequisites
Required Credentials

Google Gemini API: For image generation

Create a Google AI Studio account
Generate API key for Gemini models


OpenRouter API: For text generation

Sign up at OpenRouter.ai
Obtain API key for GLM-4.5-Air model access

### n8n Requirements

n8n version 1.0+ (recommended)
Internet connection for API calls
Webhook functionality enabled
