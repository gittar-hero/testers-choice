<p align="center">
  <img src="logo.png" width="100">
</p>

<h1 align="center"> Testers Choice </h1>

<p align="center">
  A web app that cleans answer marks from multiple-choice question PDFs written in Hebrew, creating clean exams for efficient learning.
</p>
<p align="center">
  <!-- ⚠️ Update this link once your app is deployed! -->
  <a href="https://your-streamlit-app-url.streamlit.app"><strong>✨ Try the Live App ✨</strong></a>
</p>

---

###  The Purpose: Efficient Learning

This tool solves a common problem for students: **How do you practice on an old exam when the correct answers are already marked?**

This app takes a PDF file of multiple-choice questions (like the one you uploaded from your physics course) where the answers are highlighted, and automatically removes those markings. The result is a "clean" PDF that feels like a new exam, allowing for effective practice and repeated study sessions.

###  How It Works

This app uses a smart hybrid approach:

1.  **Pre-check (YOLO):** A trained YOLO model first scans the document. If it detects a highlighter mark on any page, it flags the entire document as "marked."
2.  **Deep Clean (OpenCV):** Once flagged, the system performs a "brute-force" color-threshold clean on *every page*.
3.  **Text Preservation:** This cleaning logic identifies dark pixels (the text) and ignores them. It only paints over the colorful highlighter pixels, leaving the original text readable and intact.
4.  **User Feedback:** If the model scans the file and finds no supported markings, it notifies the user that the file is either clean or the markings are not a supported type.

###  Features

* **Study-Focused:** Turns "burned" exam files into reusable practice tests.
* **Simple UI:** Upload a marked PDF, get a clean PDF back.
* **Smart Detection:** Uses YOLO to avoid processing clean files unnecessarily.
* **High-Quality Cleaning:** Removes the highlighter color without deleting the text underneath.

* **Built with Python:** The entire stack is built with Streamlit, OpenCV, and Ultralytics.
