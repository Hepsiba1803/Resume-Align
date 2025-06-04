## API Contract – Resume–JD Matcher

## Overview

This document defines the API contract for the Resume–JD Matcher project. It specifies all available endpoints, expected request parameters, and response formats to ensure clear communication between backend and frontend systems.

---

## Endpoints

### 1. `/upload_resume`

- **Method:** POST
- **Description:** Upload a resume file.
- **Request:**
  - Content-Type: `multipart/form-data`
  - Field: `resume_file` (required)
    - Type: File (PDF or DOCX only)
- **Responses:**
  - **Success:**  
    ```json
    {
      "status": "success",
      "message": "Resume uploaded successfully."
    }
    ```
  - **Error:**  
    ```json
    {
      "status": "error",
      "message": "Invalid file type. Only PDF or DOCX allowed."
    }
    ```

---

### 2. `/upload_jd`

- **Method:** POST
- **Description:** Upload a job description file.
- **Request:**
  - Content-Type: `multipart/form-data`
  - Field: `jd_file` (required)
    - Type: File (PDF or DOCX only)
- **Responses:**
  - **Success:**  
    ```json
    {
      "status": "success",
      "message": "Job description uploaded successfully."
    }
    ```
  - **Error:**  
    ```json
    {
      "status": "error",
      "message": "Invalid file type. Only PDF or DOCX allowed."
    }
    ```

---

### 3. `/match_score`

- **Method:** POST
- **Description:** Compare resume and JD, return match score and feedback.
- **Request:**
  - Content-Type: `application/json`
  - Body:
    ```json
    {
      "resume_text": "string",
      "jd_text": "string"
    }
    ```
- **Responses:**
  - **Success:**  
    ```json
    {
      "match_score": 0.85,
      "missing_skills": ["Python", "Project Management"],
      "suggestions": [
        "Add Python experience to your resume.",
        "Highlight project management skills."
      ]
    }
    ```
  - **Error:**  
    ```json
    {
      "status": "error",
      "message": "Resume or JD text missing."
    }
    ```

---

## Notes

- All endpoints return JSON responses.
- Only PDF or DOCX files are accepted for file uploads.
- All errors are returned with `"status": "error"` and a descriptive `"message"`.

---

_This contract ensures consistent API communication and should be updated as the API evolves._