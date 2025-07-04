# Branching Strategy

## Long-Lived Branch

- The only long-lived branch in the repository will be: **`main`**

---

## Branch Naming Convention

All new branches must be created from the `main` branch and follow the format:


### 🔹 Components of the Naming Convention

| Component     | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `type`        | Purpose of the branch (see accepted values below)                          |
| `ticket-id`   | Corresponding Jira ticket ID                                               |
| `short-description` | A brief, hyphenated summary of the change                          |

---

### ✅ Accepted `type` Values

- **`feature`** – Functional changes to application, infrastructure, or data pipelines  
- **`docs`** – Documentation updates  
- **`bug`** – Bug or defect fixes  
- **`poc`** – Proof of concept or experimental testing (not for long-term use)

---

### Note

> This naming convention must be followed in `atlas` repositories.
