Go through this project and the tasks mentioned below from that some tasks I have already done and some tasks I have not done, you will understand the project better. (The task which I have done is to be enhanced by you)
Create a professional AI-powered ATS Resume Analyzer web application with the following specifications:
PROJECT OVERVIEW:
Build an AI Resume Analyzer that evaluates resumes against ATS standards, provides detailed feedback, and generates interview questions. The application should look professionally coded with clean, production-ready code.
UI/UX DESIGN REQUIREMENTS:

Theme & Aesthetics:

Academic/professional theme with subtle animated background (e.g., floating geometric shapes, gradient mesh, or particle effects)
Main title "AI-ATS-Analyzer" in metallic gradient effect (chrome/silver with reflective finish)
Use unique, modern font families: Combination of "Orbitron" or "Rajdhani" for headings and "Inter" or "Space Grotesk" for body text
Implement glassmorphism effects for cards and containers
Add subtle micro-interactions and hover effects


Dark/Light Mode:

Implement seamless toggle switch between dark and light modes
Dark Mode: Deep navy/charcoal backgrounds (#0f172a, #1e293b) with metallic accents
Light Mode: Clean whites/soft grays (#f8fafc, #f1f5f9) with vibrant metallic accents
Smooth transitions between modes (0.3s ease)
Persist mode preference in browser storage


Layout Structure:

Split-screen design: Left 50% for PDF preview, Right 50% for AI analysis results
Responsive design that adapts to mobile, tablet, and desktop
On mobile: Stack vertically with collapsible sections
Fixed header with metallic branding and mode toggle



FUNCTIONAL REQUIREMENTS:

PDF Upload Section:

Drag-and-drop zone with visual feedback
File validation (PDF only, max 5MB)
Loading animation during analysis
Preview uploaded PDF in embedded viewer


AI Analysis Features:

Connect to AI API (provide clear integration points for API key)
Display results in organized sections:

Overall ATS Score (0-100 with visual gauge)
Strengths (highlighted in green)
Issues & Mistakes (highlighted in red with specific line references)
Format Recommendations
Font & Styling Suggestions
Color Scheme Recommendations
Keyword Optimization Score




Interview Questions Generator:

Generate 10-15 relevant interview questions based on resume content
Categorize by: Technical, Behavioral, Role-Specific
Allow export of questions as PDF or copy to clipboard


Performance Optimization:

Lazy loading for PDF viewer
Debounced API calls
Loading states for all async operations
Error handling with user-friendly messages
No lag or jank during mode switching or analysis

AI PROMPT INSTRUCTIONS (To be sent to AI API):
You are an expert ATS (Applicant Tracking System) analyzer and HR professional. Analyze the provided resume PDF with brutal honesty and provide:

1. **ATS Compatibility Score (0-100):** Rate how well this resume will perform in ATS systems.

2. **Critical Issues:** List any formatting errors, parsing problems, or ATS-blocking elements. Be specific about line numbers or sections.

3. **Content Analysis:**
   - Missing essential sections
   - Weak action verbs or passive language
   - Lack of quantifiable achievements
   - Grammar and spelling errors

4. **Format Recommendations:**
   - Font choices (recommend ATS-friendly fonts)
   - Spacing and margins
   - Section organization
   - File formatting issues

5. **Visual Design Feedback:**
   - Color usage (warn if colors will be lost in ATS)
   - Use of graphics, tables, or columns
   - Professional appearance rating

6. **Keyword Optimization:**
   - Missing industry keywords
   - Suggested keywords to add
   - Keyword density analysis

7. **Overall Recommendations:** Prioritized list of improvements for maximum ATS success.

Provide honest, constructive feedback that will genuinely help the candidate improve their resume.

TECHNICAL REQUIREMENTS:

Use React with TypeScript for type safety
Implement proper state management (React Context or Zustand)
Use Tailwind CSS for styling with custom metallic gradient utilities
PDF rendering: Use react-pdf or pdf.js
Animations: Framer Motion for smooth interactions
API integration with proper error boundaries
Clean code architecture: separate components, hooks, and utilities
Add comments only where necessary (code should be self-documenting)
Follow professional naming conventions

ADDITIONAL FEATURES:

Export analysis results as PDF
Save analysis history (optional)
Share results via unique link
Print-friendly version of results

DELIVERABLE:
Provide complete, production-ready code that can be deployed immediately. Include:

All component files
Styling configuration
API integration setup
README with setup instructions

Build this as if you're a senior full-stack developer creating a portfolio piece, not an AI-generated template.
