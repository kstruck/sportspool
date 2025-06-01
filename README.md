## 1. Objective
To create a monetizable sports pool website that allows users to host, manage, and participate in private pools. Competitor examples: [officepools.com](https://www.officepools.com), [runyourpool.com](https://www.runyourpool.com).

## 2. Platform & Tech Stack
- Host Environment: PHP 8.2, MariaDB 11.4, cPanel & WHM v124.0.10
- CMS: WordPress 6.7
- Required: Responsive, mobile-first design and accessibility compliance (WCAG 2.1)

## 3. User Roles
- **Site Owner**: Full platform access and pool oversight
- **Pool Manager (Commissioner)**: Creates and manages individual pools
- **Participants**: Invited users who join and play in pools

## 4. Registration & Login
- Fields: First Name, Last Name, Email, Password
- Password must be strong (≥8 characters, upper/lowercase, number, special character)
- Google Login option
- Email verification required (link-based)
- Redirect verified users to "Create Your Pool" screen

## 5. Pool Creation Example
*Jane creates an NFL Pick-em Pool called "Gridiron Gurus," selects "Against the Spread" scoring, sets $25 per entry, and chooses to limit picks to the Top 10 weekly games with confidence values.*

## 6. Pool Setup Options
- **Pool Name**
- **Entry Cost** (whole dollar only, e.g., $50)

### Game Format:
- **Pick Type**: 
  - *Straight Up* = predict the winner
  - *Against the Spread* = pick winner considering point spread
- **Confidence Ranking**: Assign values 1–N to picks; each number can be used once per week
- **Pick Subsets**: Choose all games or top 5, 10, etc.
- **Supported Leagues**: NFL, NCAA, or both

## 7. Pool Access & Security
- Each pool has a unique, secure URL
- Managers can optionally allow members to invite others
- Pool access is restricted to accepted/invited users

## 8. Invitation System
- Email-based invites
- Manager can allow member-to-member invitations
- Backend must track:
  - Total invites sent
  - Invite-to-join conversion
  - Account data for accepted users

## 9. Admin Dashboards
### Site Owner:
- Active/inactive pools
- User and pool analytics (charts, graphs)
- Suspend/delete pool
- Feature toggles
- Pool templates

### Pool Manager:
- Control all pool settings
- View stats, picks, and invite performance
- Manage pool members and permissions

## 10. AI Integration (Planned Use)
- Analyze historical picks for trends
- Highlight upsets and unexpected outcomes
- Suggest weekly picks (optional toggle per user)
- Alert admins of suspicious behavior
- Can be run as batch processes (weekly) or real-time if performance permits

## 11. Technical Requirements
Please provide full documentation and code deliverables for development, including:

- File list with purpose
- Suggested folder structure
- Key API integrations:
  - Google Auth
  - Email (SendGrid, Mailgun, etc.)
  - Sports data (e.g., Sportradar, TheOddsAPI)
  - Optional: AI API/tool (Loveable, OpenAI, etc.)
- Recommended WordPress plugins or custom module strategies
- Frontend Pages:
  - Registration / Login
  - Email Verification
  - Dashboard (admin and user views)
  - Pool Creation
  - Invite Screen
  - Pick Submission Interface
  - Email Templates (Invite, Verification, etc.)
- Sample data models/schema (users, pools, games, picks)
- Error flows:
  - Failed login
  - Invalid token
  - Expired verification
  - Duplicate entry
- Notes on deployment and hosting setup
