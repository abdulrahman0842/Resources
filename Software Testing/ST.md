# Manual Testing Notes

---

# 1. SDLC (Software Development Life Cycle)

## Definition
SDLC is the complete process of developing software from idea to maintenance.

## Phases

### 1. Requirement Analysis
- Understand client requirements.
- Gather functional and business needs.

**Example**
Client wants an e-commerce website with:
- Login
- Registration
- Product Search
- Cart
- Payment

---

### 2. Planning
- Timeline
- Budget
- Team allocation
- Technology selection
- Risk analysis

---

### 3. Design
Design the system architecture.

Includes:
- UI/UX
- Database design
- APIs
- Architecture

---

### 4. Development
Developers write the application.

Example:
- React Frontend
- Node.js Backend
- MySQL Database

---

### 5. Testing
QA verifies that the application works correctly.

Checks:
- Login
- Registration
- Payment
- Search
- Security

---

### 6. Deployment
Application is released to production.

---

### 7. Maintenance
After deployment:
- Fix bugs
- Improve performance
- Add new features

---

## SDLC Flow

```
Requirement Analysis
        ↓
Planning
        ↓
Design
        ↓
Development
        ↓
Testing
        ↓
Deployment
        ↓
Maintenance
```

---

# 2. STLC (Software Testing Life Cycle)

## Definition
STLC is the testing process followed by the QA team.

## Phases

### 1. Requirement Analysis
QA studies the requirements.

Example:
- Can password be empty?
- Should invalid email show an error?

---

### 2. Test Planning
Decide:
- What to test
- Testing strategy
- Resources
- Timeline
- Tools

---

### 3. Test Case Development
Write test cases.

Example:

| Test Case | Expected Result |
|------------|----------------|
| Valid Login | Login successful |
| Wrong Password | Error message |

---

### 4. Test Environment Setup
Prepare:
- Server
- Database
- Browser
- Test accounts
- APIs

---

### 5. Test Execution
Execute all test cases.

If failure occurs:
- Report bug

---

### 6. Bug Reporting
Report defects with:
- Steps
- Expected Result
- Actual Result
- Severity
- Priority

---

### 7. Test Closure
Prepare:
- Test report
- Passed/Failed count
- Testing summary

---

## STLC Flow

```
Requirement Analysis
        ↓
Test Planning
        ↓
Test Case Development
        ↓
Environment Setup
        ↓
Test Execution
        ↓
Bug Reporting
        ↓
Test Closure
```

---

# SDLC vs STLC

| SDLC | STLC |
|------|------|
| Software Development Life Cycle | Software Testing Life Cycle |
| Covers complete software development | Covers only testing |
| Followed by Developers, Designers, QA, Managers | Mainly followed by QA/Testers |
| Starts with requirement gathering | Starts with requirement analysis for testing |
| Ends with maintenance | Ends with test closure |

**Easy Trick**

- SDLC → Building Software
- STLC → Testing Software

---

# 3. Testing Levels

## 1. Unit Testing

### Definition
Testing an individual function or module.

**Performed By**
Developers

**Example**

```javascript
function add(a,b){
   return a+b;
}
```

Check:
- add(2,3)=5
- add(10,5)=15

---

## 2. Integration Testing

### Definition
Testing interaction between modules.

**Performed By**
Developers / QA

Example

```
Frontend
    ↓
Backend API
    ↓
Database
```

Verify:
- Frontend sends request
- Backend processes request
- Database returns correct data

---

## 3. System Testing

### Definition
Testing the complete application.

**Performed By**
QA

Example:
- Register
- Login
- Search
- Add to Cart
- Checkout
- Payment

Everything should work together.

---

## 4. User Acceptance Testing (UAT)

### Definition
Client verifies that software meets business requirements.

**Performed By**
Client / End User

Example:
Hospital staff verifies:
- Patient Registration
- Appointment Booking
- Prescription Management

---

## Summary

| Testing Level | Performed By | Tests |
|--------------|-------------|-------|
| Unit | Developer | Individual functions |
| Integration | Developer / QA | Module interaction |
| System | QA | Complete application |
| UAT | Client | Business requirements |

---

# 4. Types of Testing

## Functional Testing

### Definition
Verifies that every feature works according to requirements.

Example:
Login:
- Valid credentials → Success
- Invalid password → Error
- Empty fields → Validation message

---

## Regression Testing

### Definition
Ensures existing functionality still works after code changes.

Example:
Added Google Login.

Now test:
- Normal Login
- Registration
- Forgot Password

---

## Smoke Testing

### Definition
Quick testing of major functionalities after a new build.

Example:
- App opens
- Login works
- Dashboard loads
- Logout works

If Login fails → Reject build.

---

## Sanity Testing

### Definition
Checks only the affected functionality after a bug fix.

Example:
Bug:
Login button not clickable.

Developer fixes it.

Tester verifies:
- Login button works.

---

## Retesting

### Definition
Testing the exact bug after it has been fixed.

Example:
Bug:
Payment failed.

Developer fixes.

Tester performs payment again.

---

## Exploratory Testing

### Definition
Testing without predefined test cases.

Tester explores application freely.

Examples:
- Random clicks
- Large file upload
- Emojis in input
- Refresh during payment
- Multiple tabs

Purpose:
Find unexpected bugs.

---

## Acceptance Testing

### Definition
Client verifies application before release.

Example:
Pharmacy owner checks:
- Medicine Sales
- Purchase
- Reports
- Stock Management

If satisfied → Approves software.

---

## Smoke vs Sanity

| Smoke Testing | Sanity Testing |
|---------------|----------------|
| New Build | Bug Fix |
| Broad Testing | Narrow Testing |
| Major Features | Specific Feature |

---

## Regression vs Retesting

| Regression | Retesting |
|------------|-----------|
| Test old features | Test fixed bug only |
| Done after changes | Done after bug fix |
| Wide scope | Narrow scope |

---

# 5. Severity vs Priority

## Severity

### Definition
Measures how serious the bug is technically.

Usually decided by QA.

Examples:
- App Crash → High
- Data Loss → High
- Typo → Low

---

## Priority

### Definition
Measures how urgently the bug should be fixed.

Usually decided by Product Manager or Business Team.

Examples:
- Company logo missing before release → High
- Typo in Settings page → Low

---

## Examples

### High Severity + High Priority
- Login not working

Fix immediately.

---

### High Severity + Low Priority
- PDF Export crashes
- Rarely used feature

---

### Low Severity + High Priority
- Company name misspelled on Homepage before launch

---

### Low Severity + Low Priority
- Extra spacing between buttons

---

## Easy Trick

**Severity = Technical Impact**

**Priority = Business Urgency**

---

# 6. Bug Life Cycle

## Definition
The stages a bug goes through from discovery to closure.

```
New
 ↓
Assigned
 ↓
Open
 ↓
Fixed
 ↓
Retest
 ↓
Closed
```

If bug still exists:

```
Retest
 ↓
Reopened
```

---

## Stages

### 1. New
Tester discovers and reports bug.

---

### 2. Assigned
Bug assigned to developer.

---

### 3. Open
Developer starts working.

---

### 4. Fixed
Developer fixes bug.

---

### 5. Retest
Tester verifies fix.

---

### 6. Closed
Bug successfully fixed.

---

### 7. Reopened
Bug still exists after fix.

Sent back to developer.

---

## Example

Bug:
Uploading PDF larger than 20MB crashes server.

Lifecycle:
- New
- Assigned
- Open
- Fixed
- Retest
- Closed

---

# Interview Questions

### Difference between SDLC and STLC?

- SDLC → Complete Software Development
- STLC → Software Testing Process

---

### Difference between Smoke and Sanity Testing?

Smoke:
- New build
- Major functionality

Sanity:
- Bug fix
- Specific functionality

---

### Difference between Regression and Retesting?

Regression:
- Test existing features after changes

Retesting:
- Test only the fixed bug

---

### Difference between Severity and Priority?

Severity:
- Technical impact

Priority:
- Business urgency

---

# Quick Revision

## SDLC
Requirement → Planning → Design → Development → Testing → Deployment → Maintenance

## STLC
Requirement Analysis → Test Planning → Test Case Development → Environment Setup → Test Execution → Bug Reporting → Test Closure

## Testing Levels
- Unit
- Integration
- System
- UAT

## Types of Testing
- Functional
- Regression
- Smoke
- Sanity
- Retesting
- Exploratory
- Acceptance

## Severity
Technical impact

## Priority
Business urgency

## Bug Life Cycle
New → Assigned → Open → Fixed → Retest → Closed