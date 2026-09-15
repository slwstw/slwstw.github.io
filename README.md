# Sustainable Land-Water Systems Lab by Prof. Wei Weng
Public Website of **Sustainable Land-Water Systems Lab** (by Prof. Wei Weng) in **Dept. of Geography, National Taiwan Unversity (NTU)**.

## Data-driven maintenance

This project keeps most content in structured JSON files instead of writing members or project details directly into HTML.

### Important folders
- `data/members.json` — all member records
- `data/research.json` — research sections and project lists
- `images/members/` — member photos
- `images/events/` — event/news photos

## Add a new member

1. Open `data/members.json`.
2. Add one new object to the array.
3. Use the template below.
4. Save the photo into `images/members/` and set the `photo` path to the correct relative path.

### Member template

```json
{
  "name": "Student Name",
  "role": "Master Student",
  "photo": "images/members/student-name.jpg",
  "projects": [
    "Project title 1",
    "Project title 2"
  ]
}
```

### Role ordering

The page sorts members by role through the `roleOrder` map in `members.html`.

Current order is:
1. Master Student
2. Research Assistant
3. Bachelor Student
4. Alumni

This means any member with `role: "Alumni"` appears at the bottom of the display automatically.

### Example

```json
{
  "name": "Kai-Yuan Cheng (Carrie)",
  "role": "Bachelor Student",
  "photo": "images/members/kai-yuan-cheng.jpeg",
  "projects": [
    "Climate change economics"
  ]
}
```

## Add a new research section

1. Open `data/research.json`.
2. Add a string item to one of the arrays:
   - `ongoingProjects`
   - `mastersProjects`
   - `bachelorsProjects`

### Research template

```json
{
  "ongoingProjects": [
    "Project A",
    "Project B"
  ],
  "mastersProjects": [
    "Master project A"
  ],
  "bachelorsProjects": [
    "Bachelor project A"
  ]
}
```

## How the page reads the data

- `members.html` loads `data/members.json` and renders the member cards.
- `research.html` loads `data/research.json` and renders the project lists.
- HTML files stay as layout templates; the actual content is stored in JSON.

## Quick maintenance checklist

- Add or edit a member in `data/members.json`
- Add or edit research entries in `data/research.json`
- Put new images in `images/members/` or `images/events/`
- Refresh the page in the browser to see the update