# Lab 5 — Static Code Analysis

**Student Name:** Pruthviraj Ajay Patil  
**SRN:** PES1UG24CS345  
**Assigned Repository:** L5_37_todo_manager

## Issues Identified and Fixes Applied

| Issue | Type | Description | Fix Approach |
|---|---|---|---|
| Unsafe pickle loading | Security | Loading untrusted pickle data can execute malicious code. | Replaced pickle persistence with JSON. |
| Shell command injection risk | Security | Constructing shell commands with user-controlled email data can be unsafe. | Replaced shell execution with the SMTP library and email validation. |
| Mutable default argument | Bug | A shared list can be reused across function calls. | Changed the default to `None` and created a new list per call. |
| Non-standard function names | Style | CamelCase names do not follow the usual Python naming convention. | Renamed functions using snake_case. |
| Missing explicit return | Code quality | A task search without a match did not explicitly return a value. | Added `return None`. |
| Missing file encoding | Portability | File operations relied on the default encoding. | Specified UTF-8 encoding. |
| Empty random selection | Runtime robustness | Selecting from an empty list can raise an exception. | Checked that pending tasks exist before selecting one. |
| Unconditional demonstration execution | Maintainability | Importing the module could execute the demonstration. | Added an `if __name__ == "__main__":` guard. |

## Verification

The fixes must be verified by rerunning Pylint, Bandit, and Flake8 on the updated source. The final results and any remaining findings should be recorded from the actual tool reports.