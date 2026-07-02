# CODER PACK — LANDING PAGE SUY TƯỞNG / MARCUS AURELIUS
Version: 1.0 Final
Mode: Vibecode Builder Implementation Pack
Priority: Launch urgent / pre-order page
Owner: Nhã Nam
Main goal: Build a polished landing page for *Suy tưởng* by Marcus Aurelius, visually matching the supplied book cover and interior illustration style.

## 0. Role & Working Protocol

You are Builder. Implement the landing page according to this pack, scan the existing codebase first, follow existing conventions, reuse components/styles where reasonable, and do not change architecture unless necessary. If you find a better implementation path, report it in SUGGESTIONS, but do not silently change the product intent.

After implementation, return a Completion Report with:

STATUS: DONE / PARTIAL / BLOCKED  
FILES CHANGED: list created/modified files  
TEST RESULTS: what was tested  
ISSUES: any remaining issue  
DEVIATIONS: any deviation from this pack and why  
SUGGESTIONS: improvements for later  

## 1. Context

We need a landing page for the 2026 Nhã Nam edition of:

Title: Suy tưởng  
Original title: Meditations  
Author: Marcus Aurelius  
Translator: Đinh Hồng Phúc  
Publisher/Brand: Nhã Nam  

The page should introduce the book, explain its editorial value, show quotes, show interior pages/illustrations, show author section, show translator profile section, and drive users to order on Nhã Nam website.

Important: The page must have only ONE primary order button style and ONE primary CTA label:

**ĐẶT SÁCH TRÊN WEBSITE NHÃ NAM**

All purchase/order links must point to the website URL placeholder:

`{{ORDER_URL}}`

Do not add multiple external marketplace buttons.

## 2. Visual Direction

The page must directly fit the supplied visual assets:

- Cover palette: deep wine red / burgundy, warm ivory, antique gold, black ink.
- Interior illustration style: classical engraving / manuscript-like ornaments, black and gold line art, decorative borders, illuminated initial letters.
- Mood: classical, quiet, dignified, collectible, not modern SaaS, not flashy ecommerce.
- Layout should feel like a premium classic edition landing page, not a generic sales page.

Use design cues from:

- Book cover: burgundy background, gold ornaments, ivory title panel.
- Interior pages: wide margins, serif typography, red chapter headings, black text, gold/black illustration blocks.
- Illustration page: manuscript border, drop cap, antique frame.

Recommended color tokens:

```css
--color-burgundy: #873A3A;
--color-burgundy-dark: #5E2828;
--color-ivory: #F7F0DE;
--color-paper: #FBF8EF;
--color-gold: #C89B53;
--color-ink: #252322;
--color-muted: #7A6A5B;
--color-red-text: #A23E36;
```

Do not use bright pure white as the main background except around product mockups if the source image already has a white/gray background. Prefer ivory/paper.

Typography:

- Headings: elegant serif. Use available project font if present. If not, use CSS fallback:
  `font-family: "Cormorant Garamond", "Libre Baskerville", "Georgia", serif;`
- Body: readable serif or existing site body font. Suggested:
  `font-family: "Source Serif 4", "Noto Serif", Georgia, serif;`
- UI/button: existing site sans if available, otherwise system sans.

Decorative details:

- Use thin double borders.
- Use small gold ornaments/dividers.
- Use drop caps sparingly.
- Quote cards can use a manuscript-like frame.
- Do not overdecorate every section.

## 3. Required Assets

Use these image assets if they are available in the project or supplied in the working directory. If not available, create placeholders and clearly report missing assets.

1. `Suy tuong (bia cung)-01.jpg`  
   Use for hero / cover spread / book cover section.
2. `Minh hoa Suy tuong5.jpg`  
   Use for illustration/quote visual section.
3. `mockup suy tuong tr6.jpg`  
   Use for interior mockup section.
4. `mockup suy tuong tr120.jpg`  
   Use for interior text section.
5. Author image: use provided author portrait if available. If not available, create an author block using cover flap/bio styling and report that no standalone author portrait was provided.
6. Translator image: use provided translator portrait if available. If not available, do not use stock images; use a refined profile card with an ornamental initial/emblem.

Image handling:

- Optimize loading with lazy loading below hero.
- Use responsive images if the project supports it.
- Add meaningful alt text.
- Ensure images do not distort.
- On mobile, images should stack naturally and remain legible.

## 4. Page Structure

Implement the page with these sections, in this order:

1. Hero
2. Intro: A book not written for publication
3. Why read Suy tưởng today
4. Quote section
5. Translation and translator profile section
6. Edition / production value section
7. Two editions comparison
8. Marcus Aurelius author section
9. How to read this book
10. Who it is for
11. Final CTA

Use anchor navigation only if existing site has a pattern for it. Do not add sticky ecommerce bar unless it fits existing site UX.

## 5. Landing Page Copy

Use the following Vietnamese copy. Preserve tone. Minor line-break adjustments are allowed for layout.

### HERO

SUY TƯỞNG  
Marcus Aurelius

Meditations

Bản dịch mới của Đinh Hồng Phúc  
Dựa theo bản tiếng Anh của George Long, có tham khảo nguyên bản Hy Lạp.

Một văn bản gần 2.000 năm tuổi, nay trở lại trong ấn bản Nhã Nam 2026, để đọc chậm, gạch chân và giữ lâu.

Marcus Aurelius không viết những dòng này để trở thành tác giả. Ông viết cho chính mình: giữa chiến trận, chính sự, bệnh tật, bổn phận và ý nghĩ thường trực về cái chết. Ở giữa quyền lực lớn nhất La Mã, ông quay lại một câu hỏi rất nhỏ mà cũng rất khó: làm sao giữ mình không bị kéo lệch khỏi điều đúng?

Bản thường để đọc hằng ngày.  
Bản đặc biệt để giữ như một ấn bản sưu tầm.

CTA button:
ĐẶT SÁCH TRÊN WEBSITE NHÃ NAM

Secondary CTA:
XEM HAI PHIÊN BẢN

### SECTION 1 — MỘT CUỐN SÁCH KHÔNG ĐƯỢC VIẾT ĐỂ XUẤT BẢN

Có những cuốn sách được viết để giảng giải. Có những cuốn được viết để thuyết phục. Suy tưởng thuộc về một trường hợp hiếm hơn: những ghi chép riêng tư của một người đang tự rèn mình.

Marcus Aurelius là hoàng đế La Mã, nhưng trong những trang viết này, điều hiện ra trước hết không phải một người cai trị, mà là một con người liên tục đối diện với chính mình. Ông tự nhắc mình về giận dữ, danh vọng, khoái lạc, cái chết, sự bấp bênh của thân xác, bổn phận trước cộng đồng và cách giữ cho linh hồn không bị kéo lệch bởi những thứ nằm ngoài quyền kiểm soát.

Gần 2.000 năm sau, Suy tưởng vẫn còn được đọc vì nó không chiều chuộng người đọc. Cuốn sách không hứa hẹn đời sống nhẹ hơn. Nó nhắc ta sống tỉnh táo hơn.

### SECTION 2 — VÌ SAO ĐỌC SUY TƯỞNG HÔM NAY?

Vì có những điều con người hiện đại tưởng là mới, nhưng Marcus đã nhìn thấy từ rất lâu.

Nỗi sợ bị quên lãng. Cơn giận trước sự ngu dốt của người khác. Áp lực phải chứng minh bản thân. Sự mong manh của danh tiếng. Cảm giác bị kéo đi bởi những việc không nằm trong tay mình. Suy tưởng không đưa ra công thức giải quyết nhanh, nhưng nó đặt người đọc vào một cuộc đối thoại nghiêm khắc: nếu không thể kiểm soát tất cả những gì xảy đến, ta còn có thể kiểm soát điều gì?

Đây là cuốn sách để đọc từng đoạn, gạch chân, đặt xuống, rồi quay lại. Có những câu chỉ mở ra sau vài năm. Có những đoạn đọc ở tuổi hai mươi là một lời khuyên, đến tuổi ba mươi lại thành một lời cảnh tỉnh.

### SECTION 3 — NHỮNG CÂU NÊN DỪNG LẠI

Quote 1:
Nếu một việc khó tự mình hoàn thành, đừng cho rằng nó là điều bất khả đối với con người. Nhưng điều gì khả thi đối với con người và phù hợp với bản tính của y, hãy nghĩ rằng ngươi cũng có thể đạt được nó.

Quote 2:
Nghệ thuật sống giống với nghệ thuật của một đô vật hơn là của một vũ công, ở chỗ nó phải sẵn sàng và vững vàng để đối mặt với những đòn tấn công bất ngờ và không lường trước.

Quote 3:
Và nếu thiên hạ không tin rằng anh ta đang sống một đời giản dị, khiêm nhường và biết đủ, anh ta cũng chẳng tức giận với ai trong số họ, cũng không rời xa con đường dẫn đến điểm cuối cuộc đời - nơi con người phải bước đến một cách thanh sạch, an nhiên, sẵn sàng rời đi, không chút ép buộc, hoàn toàn hòa giải với số phận của mình.

Quote 4:
Mỗi khi ngươi làm bất cứ điều gì, hãy dừng lại và tự hỏi: liệu cái chết có thực sự đáng sợ chỉ vì nó lấy đi điều này khỏi ngươi?

### SECTION 4 — BẢN DỊCH MỚI CỦA ĐINH HỒNG PHÚC

Với một văn bản kinh điển, bản dịch không phải chi tiết phụ.

Suy tưởng bản Nhã Nam 2026 được dịch giả Đinh Hồng Phúc thực hiện, dựa theo bản tiếng Anh của George Long, có tham khảo nguyên bản Hy Lạp. Lựa chọn này giúp bản dịch giữ được tinh thần cổ điển của văn bản, đồng thời đưa những suy tưởng của Marcus Aurelius đến gần hơn với người đọc Việt Nam hôm nay.

Đinh Hồng Phúc hiện là giảng viên Trường Đại học Thủ Dầu Một, từng là nghiên cứu viên tại Viện Khoa học Xã hội vùng Nam Bộ, tốt nghiệp Thạc sĩ Triết học tại Trường Đại học Khoa học Xã hội và Nhân văn, ĐHQG-HCM. Anh là dịch giả và đồng dịch giả của nhiều đầu sách thuộc lĩnh vực triết học, tư tưởng, khoa học xã hội và lịch sử, trong đó có Tư duy phản biện dành cho sinh viên, Thuyết hiện sinh là một thuyết nhân bản, Nhập môn Marx, Đế chế La Mã, Nhập môn xã hội học, Lý thuyết nhân loại học – giới thiệu lịch sử, Từ điển Kant, Các quy tắc của phương pháp xã hội học.

Anh cũng là người sáng lập và quản lý website triết học triethoc.edu.vn, đồng thời là Giám đốc Chương trình Tư duy biện luận và Phương pháp nghiên cứu khoa học tại Đại học Thủ Dầu Một.

Không nên đọc Suy tưởng như một cuốn sổ trích dẫn. Đây là một văn bản có nhịp điệu riêng: lúc ngắn gọn, lúc nghiêm khắc, lúc gần như một lời tự vấn. Bản dịch lần này hướng đến việc giữ lại cảm giác ấy: một người đang nói với chính mình, không lên bục giảng, không trình diễn sự thông thái.

#### Translator profile card content

Name:
Đinh Hồng Phúc

Role:
Dịch giả / Giảng viên Trường Đại học Thủ Dầu Một

Credentials:
- Từng là nghiên cứu viên tại Viện Khoa học Xã hội vùng Nam Bộ.
- Thạc sĩ Triết học, Trường Đại học Khoa học Xã hội và Nhân văn, ĐHQG-HCM.
- Dịch giả và đồng dịch giả của nhiều sách triết học, tư tưởng, khoa học xã hội và lịch sử.
- Sáng lập và quản lý website triết học triethoc.edu.vn.
- Giám đốc Chương trình Tư duy biện luận và Phương pháp nghiên cứu khoa học, Đại học Thủ Dầu Một.

Translated / co-translated works:
Tư duy phản biện dành cho sinh viên; Thuyết hiện sinh là một thuyết nhân bản; Nhập môn Marx; Đế chế La Mã; Nhập môn xã hội học; Lý thuyết nhân loại học – giới thiệu lịch sử; Từ điển Kant; Các quy tắc của phương pháp xã hội học.

### SECTION 5 — MỘT ẤN BẢN ĐƯỢC LÀM ĐỂ GIỮ LÂU

Suy tưởng bản Nhã Nam 2026 được thiết kế như một ấn bản kinh điển có thể đặt trên bàn đọc, đọc chậm và quay lại nhiều lần.

Điểm đặc sắc của ấn bản:

- Bản dịch mới của Đinh Hồng Phúc.
- Dựa theo bản tiếng Anh của George Long, có tham khảo nguyên bản Hy Lạp.
- Sách dày 368 trang.
- Ruột sách in màu.
- Có 13 tranh minh họa mới do họa sĩ trẻ Phạm Viết Nam thực hiện.
- Mỹ thuật lấy tinh thần cổ điển, với bảng màu đỏ rượu vang, ngà, đen và vàng kim.
- Bố cục trang trong thoáng, phù hợp với kiểu đọc chậm, gạch chân, quay lại.

### SECTION 6 — HAI PHIÊN BẢN

BẢN THƯỜNG  
220.000đ

Dành cho người muốn đọc một bản Suy tưởng mới, đẹp, in màu, có minh họa, phù hợp để đọc và quay lại nhiều lần.

Thông tin chính:
- 368 trang.
- In màu.
- 13 tranh minh họa mới do họa sĩ trẻ Phạm Viết Nam thực hiện.
- Bìa mềm.
- Phù hợp với người đọc muốn có một bản Suy tưởng đẹp, dễ đọc, dễ mang theo.

BẢN ĐẶC BIỆT  
490.000đ

Dành cho người sưu tầm và những bạn thích sách đẹp.

Giới hạn 333 bản.

Mỗi bản đặc biệt đều có:
- Bìa cứng carton nhập ngoại.
- Ruột in giấy ngà định lượng 100gsm.
- Bụng sách mạ nhũ vàng.
- Đánh số từ 1 đến 333.
- Đóng triện Nhã Nam.
- Có chữ ký dịch giả Đinh Hồng Phúc.

Bản thường để đọc. Bản đặc biệt để giữ.

CTA:
ĐẶT SÁCH TRÊN WEBSITE NHÃ NAM

### SECTION 7 — MARCUS AURELIUS

Marcus Aurelius  
121–180

Marcus Aurelius là một trong những hoàng đế vĩ đại nhất của Đế quốc La Mã, đồng thời là một trong những gương mặt quan trọng của chủ nghĩa Khắc kỷ. Ông cai trị trong một thời kỳ đầy chiến tranh, dịch bệnh, biến động chính trị và những áp lực không ngừng của quyền lực.

Nhưng Suy tưởng không ghi lại hình ảnh một hoàng đế đang ra lệnh. Cuốn sách cho thấy một con người đang tự nhắc mình sống đúng: khiêm nhường hơn trước danh tiếng, vững vàng hơn trước biến cố, tỉnh táo hơn trước cơn giận, và sẵn sàng hơn trước cái chết.

### SECTION 8 — ĐỌC CUỐN SÁCH NÀY NHƯ THẾ NÀO?

Đừng đọc Suy tưởng như một cuốn sách cần đọc liền mạch để “xong”. Cũng đừng chỉ đọc nó như một kho quote để lưu lại vài câu hay.

Có thể đọc mỗi ngày một đoạn. Có thể mở sách vào những lúc thấy mình bị kéo đi bởi giận dữ, lo âu, tự ái, tham vọng hoặc mệt mỏi. Có thể đọc một quyển, dừng lại, rồi quay lại sau vài tuần. Suy tưởng hợp với nhịp đọc chậm, vì nhiều đoạn trong sách không cần ta đồng ý ngay; chúng cần ta sống thêm một chút, rồi đọc lại.

### SECTION 9 — DÀNH CHO AI?

Cuốn sách này dành cho người muốn đọc Marcus Aurelius trực tiếp, không chỉ qua những câu trích dẫn trên mạng. Dành cho người quan tâm đến triết học Khắc kỷ, nhưng không muốn dừng lại ở các diễn giải quá đơn giản. Dành cho người thích những cuốn sách có thể ở lại lâu trên bàn đọc. Dành cho người muốn tặng một cuốn sách nghiêm túc, đẹp và có trọng lượng.

Suy tưởng có thể không hợp với người tìm một cuốn sách dễ đọc theo kiểu hướng dẫn từng bước. Marcus Aurelius không viết công thức. Ông để lại một cuộc tự vấn. Và chính vì thế, cuốn sách này vẫn còn được đọc.

### FINAL CTA

Một ấn bản Suy tưởng để đọc chậm, gạch chân và quay lại.

Bản thường dành cho người muốn đọc.  
Bản đặc biệt 333 bản dành cho người muốn giữ.

CTA:
ĐẶT SÁCH TRÊN WEBSITE NHÃ NAM

## 6. Functional Requirements

REQ-001: Create a responsive landing page for Suy tưởng.  
REQ-002: Use only one primary CTA label: "ĐẶT SÁCH TRÊN WEBSITE NHÃ NAM".  
REQ-003: All CTA buttons must link to `{{ORDER_URL}}`.  
REQ-004: Page must include hero, intro, why read, quotes, translation, translator profile, edition details, two-version comparison, author, reading guide, audience, final CTA.  
REQ-005: Page must display the 4 supplied quotes exactly as provided in the copy section.  
REQ-006: Page must show supplied visual assets: cover/spread, illustration, interior mockups.  
REQ-007: Page must include one author section for Marcus Aurelius.  
REQ-008: Page must be mobile responsive.  
REQ-009: Page must use visual language matching the book: burgundy, ivory, antique gold, black ink, manuscript borders, serif typography.  
REQ-010: Page must avoid generic ecommerce design, neon colors, excessive animations, modern SaaS aesthetic.  
REQ-011: Page must have good accessibility: alt text, sufficient contrast, semantic headings, keyboard-focusable CTA.  
REQ-012: Page must not include unverified claims such as "bản dịch chuẩn nhất", "giúp hết lo âu", "thay đổi cuộc đời".  
REQ-013: Page must include a translator profile section for Đinh Hồng Phúc.  
REQ-014: Translator profile must mention his current role at Trường Đại học Thủ Dầu Một.  
REQ-015: Translator profile must mention his philosophy background and selected translated/co-translated works.  
REQ-016: Translator profile must not look like a long academic CV; it should support trust in the translation while keeping the landing page readable.  
REQ-017: Do not add unverified superlative claims such as "dịch giả hàng đầu", "bản dịch uy tín nhất", "chuyên gia số một".

## 7. Suggested Layout Blueprint

### 7.1 Hero

Desktop:
- Full-width burgundy background.
- Left: title, subtitle, translator info, intro paragraph, CTA.
- Right: cover image or book spread visual.
- Add subtle gold ornamental divider.
- Add small label: "Bản Nhã Nam 2026".

Mobile:
- Title first, cover image second, CTA visible without excessive scrolling.

### 7.2 Intro section

- Ivory background.
- Two-column layout if desktop.
- Text on one side, illustration detail or ornamental frame on other side.
- Use a large drop cap for the first paragraph if visually consistent.

### 7.3 Why read today

- Paper background.
- Use 3 short visual callouts:
  1. Danh vọng
  2. Giận dữ
  3. Cái chết
- Each callout should feel like a marginal note, not a modern card.

### 7.4 Quote section

- Burgundy or dark ink background.
- Quote cards in ivory with thin gold/black border.
- 2x2 grid desktop, 1 column mobile.
- Each quote should be readable; do not use tiny text.
- Long quote may span 2 columns if needed.

### 7.5 Translation and translator profile section

- Use a sober text section.
- Add a metadata card:
  - Dịch giả: Đinh Hồng Phúc
  - Căn cứ: bản tiếng Anh của George Long
  - Có tham khảo: nguyên bản Hy Lạp
- Add a refined translator profile card, not a dense résumé block.
- Card background: ivory or paper.
- Border: thin gold/black double border.
- Small heading: "Dịch giả".
- Name should be prominent but not larger than the book title.
- Credentials may be displayed as short bullets or compact rows.
- If a translator portrait is available, place it in a circular or framed classical portrait container.
- If no portrait is available, do not use stock images. Use ornamental initials or a small manuscript-style emblem instead.
- Link triethoc.edu.vn only if existing project allows external links; otherwise render as text.

### 7.6 Edition section

- Use interior mockups.
- Use image + text alternating layout.
- Show "in màu", "13 tranh minh họa mới do họa sĩ trẻ Phạm Viết Nam thực hiện", "368 trang" as refined stat blocks.

### 7.7 Two editions comparison

- Two cards.
- Standard card for "Bản thường".
- Highlighted card for "Bản đặc biệt" with badge "333 bản".
- Do not make "Bản thường" look cheap.
- CTA after cards.

### 7.8 Author section

- Use author portrait if available.
- If not, use a classical framed author bio block.
- Include "Marcus Aurelius / 121–180".

### 7.9 Reading guide

- Use a calm, text-forward section.
- Maybe 3-step reading suggestion:
  1. Đọc từng đoạn
  2. Dừng lại
  3. Quay lại

### 7.10 Audience section

- Use three audience blocks:
  1. Người đọc Marcus trực tiếp
  2. Người thích sách kinh điển
  3. Người muốn tặng sách đẹp
- Include a short "Không hợp nếu..." paragraph.

### 7.11 Final CTA

- Burgundy background.
- Big line: "Bản thường để đọc. Bản đặc biệt để giữ."
- Single CTA button.

## 8. Component Requirements

Use existing components if project has them. If not, create minimal reusable components:

- LandingContainer
- HeroSection
- OrnamentDivider
- QuoteCard
- EditionCard
- ImagePanel
- CTAButton
- StatBlock
- TranslatorProfileCard

Keep component names aligned with existing project naming conventions.

## 9. CSS / Styling Requirements

Use existing styling system if present. If project uses Tailwind, use Tailwind classes plus CSS variables if appropriate. If project uses SCSS/CSS modules, follow that.

Required responsive breakpoints:

- Mobile: 360px+
- Tablet: 768px+
- Desktop: 1024px+
- Wide: 1280px+

Spacing:

- Generous vertical rhythm.
- Desktop section padding: approx 80–120px.
- Mobile section padding: approx 48–72px.
- Max text width: 680–760px.
- Avoid overly wide body text.

Buttons:

- Primary CTA background: antique gold or ivory depending on section.
- Button text must have strong contrast.
- Hover: subtle darkening or border change.
- No bouncing, flashing, aggressive animation.

Animation:

- Optional subtle fade-in only if project already uses animation.
- No parallax unless existing system supports it well.
- Respect prefers-reduced-motion.

## 10. SEO Requirements

Page title:
Suy tưởng - Marcus Aurelius | Bản Nhã Nam 2026

Meta description:
Suy tưởng của Marcus Aurelius, bản dịch mới của Đinh Hồng Phúc, in màu, 13 tranh minh họa mới do họa sĩ trẻ Phạm Viết Nam thực hiện. Bản thường 220.000đ và bản đặc biệt giới hạn 333 bản dành cho người sưu tầm.

Open Graph:

- og:title = Suy tưởng - Marcus Aurelius
- og:description = Một ấn bản Suy tưởng để đọc chậm và giữ lâu. Bản dịch mới của Đinh Hồng Phúc, có bản đặc biệt giới hạn 333 bản.
- og:image = use cover image if available.

Structured data:
If project supports Product schema, add Product JSON-LD with two offers:

- Bản thường: 220000 VND
- Bản đặc biệt: 490000 VND

If not supported, skip and report.

## 11. Accessibility Requirements

- Use semantic h1, h2, h3 structure.
- Only one h1.
- All images must have alt text.
- Button must be keyboard focusable.
- Contrast must pass readable standards.
- Quote text must not be embedded only inside images.
- Do not rely on color alone to distinguish editions.

Suggested alt texts:

- Cover image: "Bìa sách Suy tưởng của Marcus Aurelius bản Nhã Nam 2026"
- Illustration: "Tranh minh họa in màu của họa sĩ Phạm Viết Nam trong sách Suy tưởng"
- Interior mockup 1: "Trang trong minh họa của sách Suy tưởng"
- Interior mockup 2: "Trang ruột in màu của sách Suy tưởng"
- Author image: "Marcus Aurelius"
- Translator image: "Dịch giả Đinh Hồng Phúc"

## 12. Analytics Events

If analytics event system exists, add events:

- suy_tuong_cta_click
- suy_tuong_edition_view
- suy_tuong_quote_section_view
- suy_tuong_special_edition_view
- suy_tuong_translator_profile_view

If no event system exists, do not add a new analytics dependency. Report skipped analytics.

## 13. Acceptance Criteria

AC-001: Given a user lands on the page, when the hero loads, then the user sees title "Suy tưởng", author "Marcus Aurelius", translator "Đinh Hồng Phúc", and the primary CTA.

AC-002: Given a user scrolls through the page, when they reach the quote section, then all 4 supplied quotes are displayed as selectable HTML text, not only image text.

AC-003: Given a user views the editions section, when they compare the two versions, then they can clearly distinguish Bản thường 220.000đ and Bản đặc biệt 490.000đ.

AC-004: Given a user views the special edition card, then they see all details: 333 bản, bìa cứng carton nhập ngoại, giấy ngà 100gsm, bụng sách mạ nhũ vàng, đánh số 1–333, triện Nhã Nam, chữ ký dịch giả.

AC-005: Given a user clicks any CTA, then the link goes to `{{ORDER_URL}}`.

AC-006: Given a mobile user opens the page, then the layout is readable, no horizontal scroll appears, CTA buttons are tappable, and images scale correctly.

AC-007: Given an accessibility scan, then the page has one h1, semantic sections, alt text for all images, and readable contrast.

AC-008: Given visual review, then the page should feel visually connected to the book cover and illustrations through burgundy, ivory, gold, serif type, thin borders, and classical ornaments.

AC-009: Given a content review, then the page must not contain claims like "bản dịch chuẩn nhất", "giúp hết lo âu", "thay đổi cuộc đời", or any comparison that attacks other editions.

AC-010: Given the page is implemented, then Builder returns a Completion Report with files changed, test results, issues, deviations, and suggestions.

AC-011: Given a user views the translation section, then they see Đinh Hồng Phúc’s name, academic background, institutional affiliation, selected translated works, and triethoc.edu.vn reference.

AC-012: Given the translator section is reviewed visually, then it should feel like an editorial trust block, not a dense résumé.

AC-013: Given content review, then the translator profile must not contain exaggerated claims beyond the provided facts.

## 14. Implementation Notes

- If this is a Next.js project, implement as a route such as `/suy-tuong` or appropriate existing route convention.
- If this is a static/CMS template, implement as a standalone template/section file consistent with the project.
- Keep copy editable in a data object if the project pattern supports it.
- Avoid hardcoding image dimensions that break responsive layout.
- Do not introduce large new dependencies for simple layout.
- Do not import external fonts if project policy disallows it. Use fallback serif stack.
- Keep the page performant; optimize above-the-fold image.
- Replace `{{ORDER_URL}}` with the real Nhã Nam website order URL when available.

## 15. QA Checklist Before Completion Report

- [ ] Page renders without console errors.
- [ ] Mobile 360px tested.
- [ ] Tablet 768px tested.
- [ ] Desktop 1440px tested.
- [ ] All images load or missing assets are reported.
- [ ] All CTA buttons link to `{{ORDER_URL}}`.
- [ ] No extra marketplace buttons added.
- [ ] Copy is Vietnamese and correctly accented.
- [ ] Four quotes are exact.
- [ ] Translator profile is present and readable.
- [ ] Special edition details are complete.
- [ ] Visual direction matches cover and illustration.
- [ ] Accessibility basics checked.
- [ ] SEO metadata added if project supports it.
- [ ] Completion Report returned.

## 16. Completion Report Template

STATUS:
DONE / PARTIAL / BLOCKED

FILES CHANGED:
- path/to/file

TEST RESULTS:
- Build:
- Lint:
- Mobile:
- Desktop:
- CTA links:
- Accessibility:

ISSUES:
- None / list issues

DEVIATIONS:
- None / list deviations

SUGGESTIONS:
- Suggested future improvements, if any
