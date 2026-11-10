# Project proposal

* Name: Benjamin Gerard 
* Project title: Internship Tracker
* Pitch (one sentence): A web application that helps students organise their internship search, save internship offers and track the progress of their applications.
* Target users: University students and computer science students looking for internships.

## Pages

| URL | Content | Dynamic segment? | Rendering strategy and why |
|---|---|---|---|
| / | Homepage introducing the platform and its features | No | Static, because the content does not change often and benefits from SEO. |
| /internships | List of internship offers | No | Static or revalidated, because internship listings do not need to be refreshed on every request. |
| /internships/[id] | Detailed information about a specific internship | Yes, [id] | Dynamic, because each page displays information based on the selected internship. |
| /applications | Dashboard showing all internship applications and their statuses | No | Dynamic, because application information can change frequently. |
| /applications/[id] | Details of an application, including notes and status | Yes, [id] | Dynamic, because users can update application information. |

## Data

Entities (2 to 4), their main fields, and how they are related:

**Internship**
- id
- title
- company
- location
- description
- applicationUrl
- createdAt

**Application**
- id
- internshipId
- status
- appliedAt
- notes
- updatedAt

Relationship: One internship can be linked to multiple applications. Each application belongs to one internship.

## Write actions

Users can:
- Create a new internship offer.
- Edit internship information.
- Delete an internship offer.
- Create an application linked to an internship.
- Update the application status.
- Add or edit notes about an application.
- Delete an application.

## Repository

GitHub URL: https://github.com/BenjaminGERARD2006/Internship-Tracker