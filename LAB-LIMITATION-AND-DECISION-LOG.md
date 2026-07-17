# Lab Limitation Decision Log (Update)

### 1. Objective & Progress 
I tried to configure billing administration and assign administrative roles in Microsoft Entra ID. 
I was able to create users, assign the billing administrator role to new user "Alwin Storm". I was able to also confirm new
user to the Entra ID free tier. Check audit logs for confirmation.
### 2. Roadblock Encountered
Was attempting to activate the licensing required to continue the lab, but the checkout process required signing a
licensing agreement subject to a review period of up to 2 days. During checkout, I encountered an error that stopped the
transaction from completing. In 2026 Microsoft also retired their free learn sandbox. That was my no-cost path.
### 3. Options Evaluated 
- Retried paid license and wait out 2 day agreement. After checkout retry is blocked by an error which caused a delay
  outside of my control
- Entra ID P2 free trial required.
- Microsoft 365 Developer E5 sandbox requires a qualifying subscription.
- The $200 Azure credit is available to me but only covers VMs storage not Entra ID P1/P2 licensing so it doesn't unblock
  the roadblock encountered.
### 4. Decision & Rationale
I chose to refocus my effort on my available $200 Azure credit. This will pivot learning to cloud security labs. 
This choice can reinforce using azure and combine it with Wazuh as a SIEM tool. 
Will revisit Entra P1/P2 scenarios like Conditional Access and PIM if a specific role requires them.
