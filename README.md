# Multiple Choice Question Generator

## Overview

The Multiple Choice Question Generator is a comprehensive text processing application designed to automatically generate multiple choice questions from educational content. The system leverages natural language processing techniques to extract factual information from input text and creates well-structured questions with plausible distractors.

## Features

### Core Functionality
- **Automatic Question Generation**: Converts textual content into multiple choice questions with four options each
- **Intelligent Entity Recognition**: Identifies and categorizes key information including persons, organizations, locations, dates, and objects
- **Smart Distractor Creation**: Generates contextually appropriate incorrect options using semantic analysis and WordNet relationships
- **Interactive Web Interface**: Provides a user-friendly interface with customizable styling for Google Colab environments

### Text Processing Capabilities
- **Dual NLP Support**: Compatible with both spaCy and NLTK libraries for maximum flexibility
- **Context-Aware Analysis**: Maintains contextual relationships between sentences for better question quality
- **Semantic Grouping**: Utilizes predefined semantic categories for generating relevant alternative answers
- **Question Type Optimization**: Employs different question starters based on entity types for natural question formation

## Technical Architecture

### Dependencies
- **Natural Language Processing**: spaCy (en_core_web_sm model), NLTK
- **Interface Components**: ipywidgets, IPython.display
- **Core Libraries**: random, re, collections

### Key Components

#### TextProcessor Class
The primary processing engine that handles:
- Text analysis and entity extraction
- Question generation logic
- Distractor creation and ranking
- Context analysis and fact extraction

#### Question Generation Pipeline
1. **Text Analysis**: Input text is processed to identify key facts and entities
2. **Entity Classification**: Extracted information is categorized by type (PERSON, ORG, GPE, etc.)
3. **Fact Prioritization**: Facts are ranked based on entity type importance and context relevance
4. **Distractor Generation**: Alternative answers are created using multiple strategies
5. **Question Assembly**: Final questions are constructed with appropriate question starters

#### Distractor Creation Strategies
- **WordNet Integration**: Utilizes synonyms, antonyms, hypernyms, and hyponyms
- **Semantic Categorization**: Draws alternatives from predefined semantic groups
- **Contextual Extraction**: Identifies relevant entities from the source text
- **Type-Specific Alternatives**: Provides category-appropriate distractors

## Installation and Setup

### Prerequisites
Ensure the following packages are installed in your Google Colab environment:

```python
!pip install spacy nltk ipywidgets
!python -m spacy download en_core_web_sm
```

### Initial Setup
The application automatically handles NLTK data downloads and spaCy model loading during first run.

## Usage Instructions

### Basic Operation
1. **Launch the Interface**: Execute the main function to display the interactive widget interface
2. **Select Input Method**: Choose between sample text or custom text input
3. **Enter Content**: For custom text, paste your educational material in the text area
4. **Configure Parameters**: Set the desired number of questions using the slider control
5. **Generate Questions**: Click the generate button to process the text and create questions

### Input Requirements
- **Minimum Text Length**: Provide substantial text content for optimal question generation
- **Content Type**: Educational or informational text works best
- **Text Structure**: Well-structured paragraphs with clear factual statements produce better results

### Output Format
Generated questions include:
- Clear question text with contextual information
- Four multiple choice options (A, B, C, D)
- Correct answer identification
- Professional formatting with visual styling

## Technical Specifications

### Question Types Supported
- **Entity-Based Questions**: Person, organization, location identification
- **Temporal Questions**: Date and time-related queries
- **Factual Questions**: Object and concept identification
- **Descriptive Questions**: Characteristic and attribute-based queries

### Quality Assurance Features
- **Duplicate Prevention**: Ensures unique questions without repetition
- **Similarity Analysis**: Ranks distractors by semantic similarity to correct answers
- **Context Preservation**: Maintains original text context in question formation
- **Answer Validation**: Verifies distractor quality and relevance

### Performance Characteristics
- **Processing Speed**: Optimized for real-time question generation
- **Scalability**: Handles varying text lengths efficiently
- **Memory Management**: Efficient resource utilization for large text processing

## Interface Design

### Visual Elements
- **Modern Styling**: Professional gradient backgrounds and card-based layouts
- **Responsive Design**: Adapts to different screen sizes and orientations
- **Interactive Components**: Hover effects and smooth transitions
- **Clear Typography**: Readable fonts with appropriate sizing and spacing

### User Experience Features
- **Intuitive Controls**: Simple toggle buttons and sliders for easy configuration
- **Real-time Feedback**: Progress indicators and status messages
- **Error Handling**: Graceful handling of edge cases and user errors
- **Accessibility**: Proper contrast ratios and semantic HTML structure

## Limitations and Considerations

### Text Requirements
- **Content Depth**: Requires substantial factual content for effective question generation
- **Language Support**: Currently optimized for English language text
- **Domain Specificity**: Performance may vary based on subject matter complexity

### Technical Constraints
- **Processing Time**: Complex texts may require additional processing time
- **Memory Usage**: Large texts consume proportional system resources
- **Model Dependencies**: Requires stable internet connection for initial model downloads

## Future Enhancements

### Planned Features
- **Multi-language Support**: Extension to additional language models
- **Advanced Question Types**: True/false and fill-in-the-blank question formats
- **Difficulty Grading**: Automatic assessment of question complexity levels
- **Export Functionality**: Options to save questions in various formats

### Technical Improvements
- **Performance Optimization**: Enhanced processing speed for large documents
- **Advanced NLP Integration**: Incorporation of transformer-based models
- **Quality Metrics**: Automated assessment of question and distractor quality

## Support and Maintenance

### Troubleshooting
Common issues and solutions are addressed through proper error handling and user feedback mechanisms. The system provides clear error messages and suggestions for resolution.

### Updates and Versioning
The application is designed for easy updates and modifications. Core functionality is modular, allowing for incremental improvements without system-wide changes.

## License and Attribution

This project utilizes open-source libraries and follows standard software development practices. Proper attribution is maintained for all third-party components and dependencies.

---

**Note**: This application is optimized for Google Colab environments and educational use cases. For production deployment, additional security and performance considerations may be required.
