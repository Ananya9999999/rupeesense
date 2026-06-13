# 💸 RupeeSense — Your AI Financial Mirror

**Financial clarity through personality-driven spending analysis.**

An AI-powered personal finance app that analyzes your spending habits and delivers honest, character-driven feedback. Add transactions, get instant reactions, and track your financial health.

---

## ✨ Core Features

### 💬 **Personality-Driven Feedback**
Every transaction gets an instant, character-driven response based on merchant and amount.


### 🏥 **Money Health Score**
Get a dynamic 0–100 score based on your weekly spending patterns:
- High food/entertainment spending → Lower score
- Responsible transport/utilities → Boosts score
- Real-time updates as you add transactions

### 📊 **Category Breakdown**
Visual representation of spending across:
- 🍔 Food
- 🛍️ Shopping  
- 🎬 Entertainment
- 🚕 Transport
- 💡 Utilities

See exact amounts and percentage distribution.

### 📋 **Bulk Import**
Add multiple transactions at once with CSV format:
```
450, Swiggy, Food, 2024-01-10
1200, Amazon, Shopping, 2024-01-10
340, Starbucks, Food, 2024-01-09
```

---

## 🎨 Design

**Glassmorphism Aesthetic:**
- Dark gradient background with animated blob animations
- Frosted glass cards with backdrop blur
- Semi-transparent UI elements with glowing borders
- Smooth transitions and responsive design
- Category-specific color coding

**Tech Stack:**
- React 19 with TypeScript
- TanStack Start (full-stack framework)
- TanStack Router for navigation
- Tailwind CSS + Radix UI components
- Vite for fast builds
- Cloudflare Workers for deployment

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or bun

### Installation

```bash
# Clone the repository
git clone https://github.com/Ananya9999999/RS.git
cd RS

# Install dependencies
npm install

# Start dev server
npm run dev
```

The app will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

---

## 📱 How to Use

### **Add a Transaction**
1. Enter amount (₹)
2. Enter merchant name (Swiggy, Amazon, Netflix, etc.)
3. Select category (Food, Shopping, Entertainment, Transport, Utilities)
4. Pick date (defaults to today)
5. Click **+ Add Transaction**

### **See Instant Feedback**
- Click any transaction in the list
- Wait for AI processing (100-300ms)
- Read the personality-driven response

### **Track Your Health**
- View Money Health Score at the top
- See category breakdown with percentages
- Watch progress bars update in real-time

### **Bulk Import** (Optional)
- Paste multiple transactions in CSV format
- Click **📋 Import**
- All transactions load instantly

---

## 🏗️ Project Structure

```
RS/
├── src/
│   ├── routes/              # TanStack Router pages
│   ├── components/          # Reusable UI components
│   ├── lib/                 # Utilities & helpers
│   ├── server.ts            # Cloudflare Worker handler
│   └── app.tsx              # Main app component
├── dist/
│   ├── public/              # Static files
│   └── server/server.js     # Built server
├── package.json
├── tsconfig.json
├── vite.config.ts
├── tailwind.config.js
├── wrangler.toml            # Cloudflare config
└── README.md
```

### Key Logic

**Spending Analysis:**
- Merchant pattern matching (Swiggy, Amazon, Netflix, etc.)
- Amount-based decision trees
- Category-specific personality responses

**Health Score Calculation:**
- Food ratio: -40 points (highest impact)
- Entertainment ratio: -30 points
- Shopping ratio: -20 points
- Transport/Utilities: Neutral/Positive

---

## 💾 State Management

Uses React `useState` for:
- `transactions` - List of spending entries
- Form inputs: `amount`, `merchant`, `category`, `date`, `pasteText`

**All data is stored in browser** — nothing is sent to external servers.

---

## 🎯 Built in 24 Hours

Hackathon-optimized design:
- ✅ Zero external API calls (hardcoded logic)
- ✅ Instant responses (no network latency)
- ✅ Minimal dependencies
- ✅ Full functionality in modular code
- ✅ Modern glassmorphism UI
- ✅ Mobile-responsive design

---

## 🔧 Customization

### Change Personality Responses
Edit response logic in your components:

```typescript
if (merchant.includes('Swiggy')) {
  if (amount > 500) return '₹' + amount + ' Swiggy? [YOUR MESSAGE]';
}
```

### Adjust Health Score Formula
Modify category weights in score calculation:

```typescript
const score = Math.max(0, 100 - (
  foodRatio * 40 +              // Adjust weight
  entertainmentRatio * 30 +
  shoppingRatio * 20
));
```

### Add New Categories
1. Add to category select dropdown
2. Add corresponding response logic
3. Update health score weights

---

## 📊 Tech Stack Details

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 19, TypeScript |
| **Framework** | TanStack Start, TanStack Router |
| **Styling** | Tailwind CSS, Radix UI |
| **Build** | Vite |
| **Deployment** | Cloudflare Workers |
| **State** | React hooks (useState) |

---

## 🚀 Deployment

### **Cloudflare Workers** (Current)

```bash
# Install Wrangler
npm install -D wrangler

# Login
npx wrangler login

# Deploy
npm run build
npx wrangler deploy
```


### Build for Other Platforms

```bash
npm run build
# Output in dist/ folder
```

---

## 🎓 Future Enhancements

Potential additions (not currently implemented):
- [ ] Claude API for dynamic AI responses
- [ ] Cloud storage (Supabase/Firebase)
- [ ] Real UPI SMS parsing
- [ ] Fraud detection
- [ ] Historical trends & analytics
- [ ] Export reports (PDF)
- [ ] Dark/light mode
- [ ] Multi-language support
- [ ] Mobile app (React Native)

---

## 👤 Author

**Ctrl+Slay** — VIT Chennai, ArcNight

Built during 24-hour hackathon. Designed for Indian fintech market.

---

## 📝 License

MIT — Use, modify, and share freely.

---

## 📞 Support

**Issues?** Open a GitHub issue.

**Want to contribute?** Fork and send a PR.

---

**Start tracking. Get honest feedback. Take control. 💪**

*"Financial clarity through AI-powered personality."*
