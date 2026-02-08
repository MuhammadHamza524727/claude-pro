# Claude Pro + Claude Code CLI Setup Guide (Urdu/Hindi Explanation)

Yeh repo mera YouTube video ke saath hai jisme main step-by-step batata hoon ki **Claude AI ka paid Pro version** kaise lete hain (mobile se card add karke), aur phir **terminal (CLI) mein Claude Code** kaise chalate hain — bilkul free extra credits ke baghair (sirf Pro subscription se).

**Video Link:** []  
(Video mein full demo hai: payment, login fix, error solve "Credit balance too low", project mein use.)

## Requirements
- Computer (Windows WSL/Linux/macOS)
- Node.js installed (https://nodejs.org)
- Claude Pro subscription ($20/month ya sell Link $10/month )
- Discount link is here💕
- https://claude.ai/upgrade/pro?interval=monthly

## Step-by-Step Setup (Video Follow Karo)

Note:
yad rhe google or chrome pr same gmail se login rho jise ai use krte ho ya proejct krte ho

1. **Claude Pro Subscribe Karo**
   - Jaao: https://claude.ai/upgrade/pro?interval=monthly
   - Mobile se card details enter karo (Visa/Mastercard jo international ho).
   - Payment complete → Billing page pe check karo (Pro active, invoice paid).

2. **Claude Code CLI Install Karo**
   Terminal kholo aur run karo:
   ```
   npm install -g @anthropic-ai/claude-code
   ```
   Verify:
   ```
   claude --version
   ```

3. **Important: API Key Conflict Fix (Error "Credit balance too low")**
   - Check karo koi old API key set hai:
     ```
     echo $ANTHROPIC_API_KEY
     ```
   - Agar output aaye to remove:
     ```
     unset ANTHROPIC_API_KEY
     ```
     (Permanent remove ~/.bashrc ya .profile se)

4. **Login with Pro Subscription**
   Project folder mein jao (jaise tumhara todo-cli-app):
   ```
   cd /path/to/your/project
   ```
   Start karo:
   ```
   claude
   ```
   - Browser khulega → claude.ai pe login (Pro account).
   - Subscription mode select karo.
   - Status check:
     ```
     /status
     ```
     (Pro show hona chahiye)

5. **Use Karo**
   - Prompt likho: "Explain my codebase ya simple hi" ya "Add a new feature to add todo item"
   - Files add: `@src/app.js`
   - Commands: `/plan`, `/init`, `/exit`

## Common Errors & Fixes
- **Credit balance too low**: API key remove karo + /logout → /login with Pro.
- Rate limit hit: Pro ke 5x higher limits hain, wait karo ya simple prompts use.
- Update CLI: `npm update -g @anthropic-ai/claude-code`

## Why This is Awesome
- Pro se terminal mein full agentic coding (files read/edit automatically).
- No extra API bills — sirf $10/month.


Agar video pasand aaye to like, subscribe, comment kar dena! Questions ho to GitHub issues mein pooch lo ya video comments mein.

Made with ❤️ by Muhammad Hamza (https://linktr.ee/muhammadhamza524727) - Karachi, Pakistan
```
