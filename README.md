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

3. Install Python dependencies:
```bash
pip install -r requirements.txt
```

4. Install Mermaid CLI (for workflow diagrams):
```bash
npm install -g @mermaid-js/mermaid-cli
```

5. Create a `.env` file in the project root and add your API keys:
```
GROQ_API_KEY=your_groq_api_key
GEMINI_API_KEY=your_gemini_api_key
UNSPLASH_ACCESS_KEY=your_unsplash_access_key
```

## Usage

1. Basic usage:
```python
from paper_processor import process_paper

process_paper("path/to/your/paper.pdf", "output_video.mp4")
```

2. Running from command line:
```bash
python main.py --pdf_path "path/to/your/paper.pdf" --output "output_video.mp4"
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

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- FFmpeg for video processing
- Mermaid for diagram generation
- Various AI models and APIs used in the project

## Troubleshooting

Common issues and solutions:

1. **FFmpeg not found**
   - Ensure FFmpeg is installed and added to system PATH
   - On Windows: Download from ffmpeg.org and add to PATH
   - On Linux: `sudo apt-get install ffmpeg`

2. **Mermaid CLI errors**
   - Ensure Node.js is installed
   - Try reinstalling Mermaid CLI: `npm install -g @mermaid-js/mermaid-cli`

3. **API Rate Limits**
   - Consider implementing retry logic
   - Check API quotas and limits
