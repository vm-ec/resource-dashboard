# Resource Allocation & Utilization Dashboard

## Overview
The **Resource Allocation & Utilization Dashboard** is a web-based solution designed to provide clear, real-time visibility into employee availability and work assignments across calendar dates.  
It supports structured resource planning through role-based access and an intuitive matrix-style UI.

Employees are displayed as rows, dates as columns, and each intersection is represented by a **circular indicator** showing availability or assignment status.

---

## Key Objectives
- Enable efficient resource planning and allocation
- Provide instant visibility into free and busy resources
- Support multi-resource and multi-date assignments
- Enforce clear role-based responsibilities
- Reduce manual coordination between delivery, architecture, and RMG teams

---

## Personas & Permissions

### 1. User (Viewer)
**Purpose:** Visibility only

**Capabilities:**
- View employee availability across dates
- Identify free vs. busy resources
- Use filters (Availability, Tech Stack, Experience)
- Hover over assignments to view task details

**Restrictions:**
- Read-only access
- Cannot assign or modify work

---

### 2. Architect (Work Allocator)
**Purpose:** Resource planning and assignment

**Capabilities:**
- Select multiple employees
- Select multiple dates
- Assign work via popup modal
- Add task title and detailed description per employee
- Update existing assignments
- Change availability state (Free → Assigned)

**Restrictions:**
- Cannot add or remove employees from the system

---

### 3. RMG Team (Admin)
**Purpose:** Resource governance and administration

**Capabilities:**
- Add new employees
- Remove employees
- Maintain employee metadata:
  - Name
  - Tech stack
  - Experience
- Control the overall resource pool

---

## Visual Indicators (Matrix)

| Indicator | Meaning |
|--------|--------|
| Empty Circle | Employee is free |
| Green Circle | Employee is assigned |
| Tooltip on Hover | Employee name and task details |

---

## Filters & Search

### Availability Filter (Radio Buttons)
- **All** – Show all employees
- **Busy** – Employees assigned on today’s date
- **Free** – Employees free on today’s date

> Availability filtering always starts from **today’s date**.

---

### Tech Stack Filter (Checkboxes)
- Java
- .NET
- React
- Any

Employees may belong to multiple tech stacks.

---

### Experience Filter
- Range slider (e.g., 0–10+ years)
- Helps filter resources by seniority

---

### Search
Search employees by:
- Name
- Tech stack
- Experience

---

## Assignment Workflow (Architect)

1. Select one or more employees
2. Select one or more dates
3. Click **Assign Work**
4. Popup modal opens with selected employees and dates
5. Enter task title and detailed description per employee
6. Confirm assignment
7. Dashboard updates instantly (circle turns green)

---

## Technology Stack

### Frontend
- HTML5
- Tailwind CSS
- JavaScript (Vanilla or React-compatible structure)

### Design Principles
- Component-based UI
- Role-driven UI behavior
- Centralized state management
- Extensible for backend integration

---

## Suggested Folder Structure
