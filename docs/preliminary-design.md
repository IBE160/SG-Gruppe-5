# ibe160 UX Design Specification

_Created on mandag 17. november 2025 by BIP_
_Generated using BMad Method - Create UX Design Workflow v1.0_

---

## Executive Summary

The AI CV & Job Application Assistant is a tool designed to empower students and recent graduates in the competitive job market. By automating the tedious process of tailoring CVs and cover letters, the application saves users significant time, boosts their confidence, and improves the quality of their job applications. The MVP will focus on core features like cover letter generation and CV improvement suggestions, with a long-term vision to become a comprehensive career co-pilot.

---

## 1. Design System Foundation

### 1.1 Design System Choice

**Chosen Design System:** Shadcn UI

**Rationale:** The user prioritizes fast development and recognizes that Shadcn UI, built on Tailwind CSS and designed for Next.js, provides excellent defaults, customizable components, and strong accessibility features. This aligns with the project's need for efficient development while maintaining control over the visual design.

**Key Features Provided by Shadcn UI:**
-   A collection of re-usable, headless UI components (e.g., buttons, forms, dialogs, cards).
-   Seamless integration with Tailwind CSS for styling.
-   Focus on accessibility (WCAG compliance).
-   Customizable to fit specific brand guidelines.

**Customization Needs:** While Shadcn UI offers a robust set of components, specific unique UI elements or highly custom interactions may require bespoke component development or significant customization of existing Shadcn components.

---

## 2. Core User Experience

### 2.1 Defining Experience

**Defining Experience:** "It's like having a personal AI assistant who crafts your perfect job applications."

**Analysis of UX Patterns:**
This defining experience primarily leverages established UX patterns for document management, form input, content display, and feedback mechanisms. Users will interact with:
-   **Document Upload/Management:** Standard drag-and-drop interfaces, file previews.
-   **Form-based Inputs:** Text areas for job descriptions, dropdowns/radio buttons for tone/style selection.
-   **Content Generation & Display:** AI-generated text (cover letters, suggestions) presented in editable fields or clear, scannable formats.
-   **Feedback Mechanisms:** Clear indicators for processing, success, and errors; categorized suggestions.

While the core interactions are familiar, the "personal AI assistant" aspect suggests opportunities for novel *presentation* of the AI's work, such as:
-   **Conversational UI elements:** Guiding the user through the process.
-   **Contextual help and explanations:** Clarifying AI suggestions.
-   **Iterative feedback loops:** Making the "crafting" feel collaborative.

However, no fundamentally novel interaction patterns (like a completely new gesture or interaction model) are immediately apparent. The focus will be on refining existing patterns to make the AI assistance feel seamless, intuitive, and truly assistive.

### 2.2 Novel UX Patterns

No fundamentally novel UX patterns were identified for the core interactions. The focus will be on refining established patterns (document upload, form input, content generation/display, feedback mechanisms) to make the "personal AI assistant" experience seamless, intuitive, and highly assistive. Opportunities exist for novel *presentation* of AI interactions, such as conversational UI elements or contextual help, but these will build upon existing interaction models.

### 2.3 Core Experience Principles

**Speed:** Key actions like uploading documents, generating content, and receiving suggestions should feel instantaneous or very fast. For longer AI processing, clear and engaging progress indicators will manage expectations, reinforcing the goal of saving users time.

**Guidance:** Users will receive proactive, contextual guidance from their "AI assistant" throughout the application process. This guidance will help them interpret AI suggestions, understand the impact of their edits, and navigate the tool efficiently, boosting their productivity and confidence.

**Flexibility:** The system will offer a harmonious balance between AI automation and user control. Users will be empowered to easily accept, modify, or reject AI suggestions, ensuring they maintain full ownership and personalization of their application documents.

**Feedback:** Feedback will be informative, actionable, and immediate. The system will clearly explain AI suggestions, highlight improvements, and confirm successful actions, reinforcing the user's sense of efficiency and progress.

---

## 3. Visual Foundation

### 3.1 Color System

**Brand Personality:** Professional, Trustworthy, Modern, Efficient.

**Color Palette:**
-   **Primary:** `#136dec` (A vibrant blue, conveying trust and professionalism, used for main actions and key interactive elements).
-   **Background Light:** `#f6f7f8` (A very light gray, providing a clean and spacious canvas).
-   **Background Dark:** `#101822` (A dark charcoal, for a sophisticated dark mode experience).
-   **Text Dark:** `#101822` (Deep charcoal for primary text on light backgrounds).
-   **Text Light:** `white` (For primary text on dark backgrounds).
-   **Secondary Text Dark Mode:** `#92a9c9` (A muted blue-gray for secondary text on dark backgrounds, ensuring readability).

**Typography System:**
-   **Display Font:** 'Manrope', sans-serif (Used for headlines and prominent text, conveying modernity and clarity).
-   **Body Font:** (To be determined, but likely a clean, highly readable sans-serif font that complements Manrope).
-   **Type Scale:** A modular type scale will be established to ensure consistent and hierarchical text sizing (e.g., h1-h6, body, small).
-   **Font Weights:** Use of regular and bold weights for emphasis and hierarchy.

**Spacing and Layout Foundation:**
-   **Base Unit:** An 8px base unit will be used for all spacing and sizing, providing a consistent rhythm.
-   **Spacing Scale:** A proportional spacing scale (e.g., 8px, 16px, 24px, 32px, etc.) will be derived from the base unit for margins, paddings, and component sizing.
-   **Layout Grid:** A flexible, responsive grid system (likely 12-column for desktop, adapting to fewer columns on smaller screens) will be used to ensure content alignment and responsiveness.
-   **Container Widths:** Max-width containers will be defined to ensure optimal readability and visual balance on large screens.

**Interactive Visualizations:**

- Color Theme Explorer: [ux-color-themes.html](./ux-color-themes.html)

---

## 4. Design Direction

### 4.1 Chosen Design Approach



**Chosen Design Direction:** "The Focused Assistant" (Direction 1)



**Rationale:** This direction prioritizes a clear, guided user experience, minimizing distractions and making the application process effortless and confidence-boosting. It aligns with the desired emotional response of "efficient and productive."



**Key Characteristics:**

-   **Layout Approach:** Single-column, centered content with a stepper/wizard-like flow. Content areas are presented in clear, distinct sections, ensuring focus on one task or piece of information at a time.

-   **Visual Hierarchy:** Spacious layout with strong, clear headlines for each step. AI-generated suggestions and feedback will be visually prominent and actionable.

-   **Interaction Patterns:** Direct and intuitive, with dedicated buttons for "Next Step" to guide the user progressively through the process. Emphasis on clear button actions and form-based inputs.

-   **Visual Weight:** Minimalist and balanced, with ample white space. Subtle borders and shadows define elements without adding visual clutter.

-   **Content Approach:** Scannable and concise, presented in digestible chunks within each step of the guided flow.

**Interactive Mockups:**

- Design Direction Showcase: [ux-design-directions.html](./ux-design-directions.html)

---

## 5. User Journey Flows

### 5.1 Critical User Paths

**User Journey: Creating a New Job Application**
**User Goal:** To generate a tailored cover letter and receive CV improvement suggestions for a specific job.
**Approach:** Direct, Focused, and Sequential.

**Flow Steps:**

1.  **Entry Point: Dashboard**
    *   **User sees:** A clean dashboard with a prominent "Start New Application" button.
    *   **User does:** Clicks "Start New Application."
    *   **System responds:** Navigates to the "New Application" screen.

2.  **Input: Upload CV**
    *   **User sees:** A clear drag-and-drop zone labeled "Upload Your CV" with a file picker option.
    *   **User does:** Drags and drops their CV file (PDF, DOC, TXT) or uses the file picker.
    *   **System responds:** Displays visual confirmation of successful upload (file name, green checkmark). If an error occurs, a clear error message is shown.

3.  **Input: Paste Job Description**
    *   **User sees:** A large text area labeled "Paste Job Description Here."
    *   **User does:** Pastes the job description text into the area.
    *   **System responds:** A "Next" or "Analyze" button becomes active.

4.  **Processing: AI Analysis**
    *   **User sees:** A subtle loading indicator (spinner/progress bar) with a message like "Analyzing your CV and Job Description..."
    *   **User does:** Waits for the analysis to complete.
    *   **System responds:** Transitions to the "Review Suggestions" screen once analysis is done.

5.  **Feedback: Review CV Improvement Suggestions**
    *   **User sees:** Categorized CV improvement suggestions in a dedicated, scrollable panel. Each suggestion has clear "Accept," "Edit," or "Dismiss" actions.
    *   **User does:** Reviews suggestions, accepts/edits/dismisses them.
    *   **System responds:** Updates the internal CV representation based on user actions. A "Generate Cover Letter" button becomes active.

6.  **Action: Generate Cover Letter**
    *   **User sees:** A "Generate Cover Letter" button.
    *   **User does:** Clicks "Generate Cover Letter."
    *   **System responds:** Displays a loading indicator ("Generating Cover Letter...") then presents the tailored cover letter in an editable text area.

7.  **Success: Review and Download Cover Letter**
    *   **User sees:** The generated cover letter, an "Edit" option, and a "Download" button.
    *   **User does:** Reviews the cover letter, makes any final edits, and clicks "Download."
    *   **System responds:** Downloads the cover letter file. Displays a success message ("Application Ready!") and options to save the session or start a new one.

```mermaid
graph TD
    A[User Logs In / Dashboard] --> B{Start New Application};
    B --> C[New Application Screen];
    C --> D[Upload CV (Drag & Drop / File Picker)];
    D -- CV Uploaded --> E[Paste Job Description];
    E -- Job Description Pasted --> F[Click "Analyze"];
    F --> G{AI Analyzing CV & Job Description};
    G -- Analysis Complete --> H[Review CV Improvement Suggestions];
    H -- User Actions on Suggestions --> I[Click "Generate Cover Letter"];
    I --> J{AI Generating Cover Letter};
    J -- Generation Complete --> K[Review & Download Cover Letter];
    K -- User Downloads --> L[Application Complete / Options];
```

---

## 6. Component Library

### 6.1 Component Strategy

**Design System Integration:**
The project will primarily leverage **Shadcn UI** as its foundational component library. This choice aligns with the goal of fast development, providing a robust set of accessible, customizable, and well-documented UI components that integrate seamlessly with Next.js and Tailwind CSS.

**Required Components and Shadcn UI Coverage:**
Most standard UI elements required for the application, such as buttons, text inputs, text areas, dialogs, toast notifications, cards, and progress indicators, are well-covered by Shadcn UI's existing component set or can be easily composed using its primitives.

**Custom Components and Customization Needs:**
While Shadcn UI provides a strong base, certain core features of the "AI CV & Job Application Assistant" will require custom development or significant customization of Shadcn UI components to deliver the unique user experience:

-   **Enhanced Drag-and-Drop File Upload Zone:** A visually distinct and highly interactive drag-and-drop area for CV uploads, complete with real-time file previews, clear validation feedback, and various states (e.g., idle, dragging, uploading, error), will be built as a custom component leveraging Shadcn UI primitives for styling and basic input handling.
-   **Categorized AI Suggestion Panel:** This critical component will display AI-generated CV improvement suggestions in a categorized, actionable format. It will require custom composition and logic to present suggestions clearly, allow for "Accept," "Edit," or "Dismiss" actions per suggestion, and potentially highlight relevant sections of the CV. This will be built using Shadcn UI's `Card`, `Button`, and `Badge` components as building blocks.
-   **Editable AI-Generated Content Display:** For the generated cover letter and potentially for refining CV suggestions, an advanced editable text area will be needed. This component will allow for inline modifications, potentially track changes, and clearly distinguish between AI-generated and user-edited content. This may involve integrating a third-party rich text editor or building a custom solution on top of basic Shadcn UI `Textarea` components.

This strategy ensures that development can proceed efficiently with established patterns while allowing for the creation of unique, high-impact components where the core value of the AI assistant is delivered.

---

## 7. UX Pattern Decisions

### 7.1 Consistency Rules

**Approach:** Efficiently established defaults, with the understanding that specific contexts may require overrides.

**1. Button Hierarchy:**
-   **Primary Action:** Prominent, solid fill (using the primary blue from the palette), used for the single most important action on a screen (e.g., "Start New Application," "Generate Cover Letter").
-   **Secondary Action:** Outline or ghost button style, used for important but not primary actions (e.g., "Edit CV," "Save Draft").
-   **Tertiary Action:** Text-only button, used for less prominent actions or navigation within a flow (e.g., "Cancel," "Learn More").
-   **Destructive Action:** Red color, used sparingly for irreversible actions (e.g., "Delete Application").

**2. Feedback Patterns:**
-   **Success:** Brief, non-intrusive "toast" notifications (small, temporary messages at the top/bottom of the screen) for quick confirmations (e.g., "CV Uploaded Successfully!").
-   **Error:** Inline error messages directly next to the problematic input field for validation errors. For system-level errors, a clear, actionable modal dialog.
-   **Loading:** Subtle spinners or progress bars directly within the component or button that triggered the action (e.g., on the "Generate" button while AI processes).
-   **Info/Guidance:** Contextual tooltips or small info icons that reveal more details on hover/click.

**3. Form Patterns:**
-   **Label Position:** Labels placed **above** the input field for clarity and better responsiveness.
-   **Required Field Indicator:** A small **asterisk (\*)** next to the label.
-   **Validation Timing:** Validate **on blur** (when the user leaves the field) and **on submit**.
-   **Error Display:** Inline error messages directly below the problematic field.
-   **Help Text:** Concise help text below the label or as a tooltip for more complex inputs.

**4. Empty State Patterns:**
-   **First Use/No Content:** A friendly, illustrative message explaining what the section is for, combined with a clear call-to-action button to get started (e.g., "No applications yet. Start your first one!").
-   **No Results (e.g., search):** A clear message indicating "No results found," with suggestions for refining the search or starting over.

**5. Confirmation Patterns:**
-   **Irreversible Actions (e.g., deleting an application):** A **modal dialog** requiring explicit confirmation from the user, clearly stating the impact of the action.
-   **Leaving Unsaved Changes:** A browser-level or custom modal warning the user about unsaved changes before navigating away.

**6. Modal Patterns:**
-   **Dismiss Behavior:** Users can close modals by clicking a close (X) button, pressing the Escape key, or clicking the background overlay.
-   **Focus Management:** Focus will be trapped within the modal to guide the user.
-   **Stacking:** Avoid stacking modals to maintain a clean, simple interface.

**7. Navigation Patterns:**
-   **Active State:** The active navigation item will be indicated with a bold font and a subtle background color.
-   **Back Button:** The browser's back button will function as expected, taking the user to their previous view.

**8. Notification Patterns:**
-   **Placement:** Notifications will appear in the top-right corner.
-   **Duration:** Informational messages will auto-dismiss after 5 seconds; errors will require manual dismissal.

**9. Search Patterns:**
-   **Trigger:** A simple search bar in the header.
-   **Results Display:** Instant results as the user types.
-   **Filters:** Not applicable for the current design.
-   **No Results:** Display a "No results found" message.

**10. Date/Time Patterns:**
-   **Format:** Use relative time for recent items (e.g., "2 hours ago") and absolute dates for older items (e.g., "Nov 19, 2025").
-   **Timezone:** All times will be displayed in the user's local timezone.

---

## 8. Responsive Design & Accessibility

### 8.1 Responsive Strategy

**Responsive Design Strategy:**
The application will implement a fluid and adaptive responsive design, ensuring optimal usability and visual presentation across a range of devices:

-   **Desktop (Large Screens):** Content areas will expand to an optimal readable width, maintaining generous white space. Multi-column layouts will be utilized for displaying related information side-by-side (e.g., CV preview and job description input). Primary navigation will be a top navigation bar, with secondary actions potentially in a subtle left-aligned menu.
-   **Tablet (Medium Screens):** Layouts will adapt by collapsing multi-column sections into single or two-column arrangements. Interactive elements will be touch-optimized with adequate touch target sizes. The design will gracefully adapt to both portrait and landscape orientations, prioritizing content flow.
-   **Mobile (Small Screens):** Navigation will transition to a hamburger menu or a bottom navigation bar. All multi-column layouts will collapse into a single, scrollable column. Touch target sizes will be a critical focus to ensure all interactive elements are easily tappable.

**Breakpoint Strategy (Example, to be refined during implementation):**
-   **Mobile:** Max-width 767px (single-column layout, hamburger/bottom navigation)
-   **Tablet:** 768px - 1023px (single or two-column layout, adapted navigation)
-   **Desktop:** Min-width 1024px (multi-column layout, top navigation)

**Accessibility Strategy:**
The project will target **WCAG 2.1 Level AA compliance**. This commitment ensures the application is usable by the widest possible audience, including individuals with disabilities, and aligns with best practices for public-facing and educational tools.

**Key Accessibility Requirements:**
-   **Keyboard Navigation:** All interactive elements will be fully navigable and operable using only a keyboard.
-   **Screen Reader Compatibility:** Semantic HTML will be used, along with appropriate ARIA attributes, to ensure content and interactive elements are clearly understood by screen readers.
-   **Color Contrast:** All text and essential graphical elements will meet WCAG 2.1 AA contrast ratios to ensure readability for users with low vision or color blindness.
-   **Focus Indicators:** Clear and visible focus indicators will be provided for all interactive elements.
-   **Alternative Text:** All meaningful images will have descriptive alternative text.
-   **Form Labels:** All form inputs will have properly associated and descriptive labels.
-   **Error Identification:** Error messages will be clear, descriptive, and programmatically associated with their respective input fields.
-   **Touch Target Size:** Interactive elements, especially on touch devices, will have sufficiently large touch target areas.

**Testing Strategy:**
Accessibility will be integrated into the development and testing process, utilizing both automated tools (e.g., Lighthouse, axe DevTools) and manual testing (e.g., keyboard-only navigation, screen reader testing).

---

## 9. Implementation Guidance

### 9.1 Completion Summary

Excellent work! Your UX Design Specification is complete.

**What we created together:**

-   **Design System:** Shadcn UI with identified custom components for upload, suggestions, and editable content.
-   **Visual Foundation:** Professional, Trustworthy, Modern, Efficient brand personality. Primary blue color (`#136dec`), Manrope font, 8px spacing system.
-   **Design Direction:** "Clean & Focused Assistant" - minimalist, clear calls to action, direct interactions.
-   **User Journeys:** One critical user journey ("Creating a New Job Application") designed with a direct, focused, and sequential approach.
-   **UX Patterns:** Established defaults for button hierarchy, feedback, forms, empty states, and confirmations.
-   **Responsive Strategy:** Adaptive design for desktop, tablet, and mobile, with specific breakpoint considerations.
-   **Accessibility:** WCAG 2.1 Level AA compliance targeted.

**Your Deliverables:**
-   UX Design Document: `docs/ux-design-specification.md`

**What happens next:**
-   Designers can create high-fidelity mockups from this foundation.
-   Developers can implement with clear UX guidance and rationale.
-   All your design decisions are documented with reasoning for future reference.

You've made thoughtful choices through visual collaboration that will create a great user experience. Ready for design refinement and implementation!

---

## Appendix

### Related Documents

- Product Requirements: `{{prd_file}}`
- Product Brief: `{{brief_file}}`
- Brainstorming: `{{brainstorm_file}}`

### Core Interactive Deliverables

This UX Design Specification was created through visual collaboration:

- **Color Theme Visualizer**: {{color_themes_html}}
  - Interactive HTML showing all color theme options explored
  - Live UI component examples in each theme
  - Side-by-side comparison and semantic color usage

- **Design Direction Mockups**: {{design_directions_html}}
  - Interactive HTML with 6-8 complete design approaches
  - Full-screen mockups of key screens
  - Design philosophy and rationale for each direction

### Optional Enhancement Deliverables

_This section will be populated if additional UX artifacts are generated through follow-up workflows._

<!-- Additional deliverables added here by other workflows -->

### Next Steps & Follow-Up Workflows

This UX Design Specification can serve as input to:

- **Wireframe Generation Workflow** - Create detailed wireframes from user flows
- **Figma Design Workflow** - Generate Figma files via MCP integration
- **Interactive Prototype Workflow** - Build clickable HTML prototypes
- **Component Showcase Workflow** - Create interactive component library
- **AI Frontend Prompt Workflow** - Generate prompts for v0, Lovable, Bolt, etc.
- **Solution Architecture Workflow** - Define technical architecture with UX context

### Version History

| Date     | Version | Changes                         | Author        |
| -------- | ------- | ------------------------------- | ------------- |
| mandag 17. november 2025 | 1.0     | Initial UX Design Specification | BIP |

---

_This UX Design Specification was created through collaborative design facilitation, not template generation. All decisions were made with user input and are documented with rationale._
