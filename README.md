# Mermaid Chart Maker 

A full-featured web editor for creating, editing, and sharing [Mermaid.js](https://mermaid.js.org/) diagrams with live preview and export capabilities.

[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://bjmdevelopers.github.io/Mermaid)

## 🌟 Features

### Diagram Support
- **Flowcharts** (`graph TD`/`graph LR`)
- **Sequence diagrams** (`sequenceDiagram`)
- **Class diagrams** (`classDiagram`)
- **State diagrams** (`stateDiagram-v2`)
- **Gantt charts** (`gantt`)
- **Pie charts** (`pie`)
- **Entity Relationship diagrams** (`erDiagram`)
- **User Journey diagrams** (`journey`)

### Editor Features
- Real-time preview rendering
- Syntax highlighting for Mermaid code
- Code formatting/beautification
- Responsive design (works on all devices)
- Line numbering
- Error highlighting

### Export Options
- Download as SVG (vector)
- Download as PNG (raster)
- Generate shareable URL

### Advanced Functionality
- Custom styling support
- Diagram zoom controls
- Auto-save functionality

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Edge, Safari)
- Internet connection (for CDN resources)

### Using the Web App
1. Visit the [Website](https://bjmdevelopers.github.io/Mermaid)
2. Write or paste your Mermaid code in the editor
3. View the live-rendered diagram
4. Use the toolbar to export or share

### Local Development
3. **Clone the repository**:
   ```bash
   git clone https://github.com/bjmdevelopers/Mermaid.git
   ```
2. **Navigate to project folder**:
   ```bash
   cd Mermaid
   ```
3. **Open in browser**:
   ```bash
   open index.html
   ```
## 📚 Diagram Examples 

### Flowchart
```mermaid
graph TD
    A[Start] --> B{Decision?}
    B -->|Yes| C[Action 1]
    B -->|No| D[Action 2]
    C --> E[End]
    D --> E
    
    style A fill:#4361ee,stroke:#333,color:#fff
    style E fill:#06d6a0,stroke:#333,color:#fff
```

### Sequence Diagram
```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: I'm good thanks!
```

### Class Diagram
```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal: +int age
    Animal: +String gender
    class Duck{
        +String beakColor
        +swim()
    }
```

### State Diagram
```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Processing: Start Event
    Processing --> Success: Success
    Processing --> Error: Failure
    Success --> [*]
    Error --> [*]
```

### Gantt Chart
```mermaid
gantt
    title Project Timeline
    dateFormat  YYYY-MM-DD
    section Phase 1
    Research       :active,    des1, 2023-10-01, 7d
    Design         :           des2, after des1, 5d
    section Phase 2
    Development    :           des3, after des2, 14d
    Testing        :           des4, after des3, 7d
```

### Pie Chart
```mermaid
pie
    title Programming Language Usage
    "JavaScript" : 45.6
    "Python" : 28.3
    "Java" : 15.2
    "Other" : 10.9
```

### Entity Relationship Diagram
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER {
        string name
        string email
    }
    ORDER {
        date orderDate
    }
```

### User Journey Diagram
```mermaid
journey
    title User Journey
    section Sign Up
      Visit Site: 5: User
      Register: 4: User
    section Purchase
      Browse Products: 5: User
      Add to Cart: 4: User
      Checkout: 3: User
```
## 🛠️ Technical Details 

### Core Components
- **Editor**: Vanilla JavaScript text editor with syntax highlighting
- **Renderer**: Mermaid.js integration with live preview
- **Export**: SVG/PNG generation via native browser APIs
- **State**: Lightweight state management using localStorage

### Key Features
- 100% client-side (no backend required)
- Zero build step (runs directly in browser)
- <5kb JavaScript (excluding dependencies)
- Responsive CSS grid layout

### Dependencies
| Library | Purpose | Version |
|---------|---------|---------|
| [Mermaid.js](https://mermaid.js.org/) | Diagram rendering | 10.x |
| [Font Awesome](https://fontawesome.com/) | UI Icons | 6.x |
| html2canvas | PNG export | 1.4.x |

## 📜 License
MIT Licensed - See [LICENSE](LICENSE)

## 🙏 Credits
- Mermaid.js team for the powerful visualization engine
- Font Awesome for the clean icon set
