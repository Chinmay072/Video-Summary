# Research Paper Video Generator

An AI-powered tool that automatically converts research papers (PDF) into engaging video presentations. The tool analyzes the paper's content, extracts key information, and creates a professional video summary complete with visuals, narration, and dynamic transitions.

## Features

- 🎥 Generates complete video presentations from research papers
- 🤖 Uses multiple AI models for content analysis and generation
- 🎨 Creates dynamic visualizations including workflow diagrams
- 🗣️ Automatic text-to-speech narration
- 📊 Extracts and explains figures from the paper
- 🖼️ Integrates thematically relevant background images
- 📝 Generates paper summaries and key insights

![image](https://github.com/user-attachments/assets/727eeecd-6be8-458a-bef4-3665797b8771)
![image](https://github.com/user-attachments/assets/f14c3fa9-0377-467a-ad34-c3cc67d7cba7)
![image](https://github.com/user-attachments/assets/e02d95c0-0dd4-467f-a420-430dfa452e49)
![image](https://github.com/user-attachments/assets/76ff1b56-ad3d-4b49-8035-8910191fbf37)


## Prerequisites

- Python 3.8+
- Node.js (for Mermaid CLI)
- FFmpeg (for video processing)

### API Keys Required
You'll need to obtain API keys for the following services:
- Groq API
- Google AI (Gemini)
- (Optional) Unsplash API

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/research-paper-video-generator.git
cd research-paper-video-generator
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install Mermaid CLI (for workflow diagrams):
```bash
npm install -g @mermaid-js/mermaid-cli
```
```

## Usage

1. Running from command line (mention the path of research paper and where you want to store the video in python code):
```bash
python simplegen.py
```

## How It Works

1. **Text Extraction**
   - Extracts full text, abstract, and conclusion from the PDF
   - Generates a concise summary using Gemini AI

2. **Image Processing**
   - Extracts figures and diagrams from the PDF
   - Analyzes images using LLaMA Vision API
   - Downloads relevant background images based on paper content

3. **Content Generation**
   - Creates workflow diagrams using Mermaid
   - Generates explanations for figures and diagrams
   - Converts text to speech for narration

4. **Video Creation**
   - Combines all elements into a cohesive video
   - Adds dynamic transitions and overlays
   - Synchronizes audio narration with visuals

## Video Structure

The generated video includes:
1. Title and introduction
2. Paper overview
3. Abstract summary
4. Workflow diagram with explanation
5. Key figures and their analysis
6. Conclusion

## Configuration

You can customize various aspects of the video generation by modifying the following parameters in the code:

- Video dimensions (default: 800x600)
- Font sizes and styles
- Background image count
- Audio speed and language
- Video quality settings

## Acknowledgments

- FFmpeg for video processing
- Mermaid for diagram generation
- Various AI models and APIs used in the project

## Troubleshooting

Common issues and solutions:

1. **Mermaid CLI errors**
   - Ensure Node.js is installed
   - Try reinstalling Mermaid CLI: `npm install -g @mermaid-js/mermaid-cli`

2. **API Rate Limits**
   - Consider implementing retry logic
   - Check API quotas and limits
