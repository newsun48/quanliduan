# Fix Blank Page localhost:5173 (Babel ESM Parse Error)

**Root Cause:** Corrupted @babel/parser in node_modules causing 'Cannot use import statement outside a module' in main.jsx.

**Status:** In progress

### Steps:
- [x] Delete node_modules (Remove-Item PS)
- [x] Delete package-lock.json
- [x] npm install (completed successfully)
- [ ] Kill any old vite dev server (Ctrl+C)
- [x] cd client-app ; npm run dev (running on 5174)
- [x] Verify esbuild fixed, no parse error (GroupChatPanel.jsx syntax cleaned), Login page shows at localhost:5174
- [x] Made group chat input taller/wider (height 50px, font 16px, padding) for better typing
- [ ] Start backend: mvnw spring-boot:run (MongoDB required)
- [ ] Test login: admin@example.com / admin123

**Optional Stability:**
- Downgrade React to ^18.3.1 (React 19 beta unstable)
- react-router-dom to ^6.26.2

**Test Command:** http://localhost:5173
