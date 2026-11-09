# Limitless Brain Skills

ชุด AI skills 5 ตัวสำหรับ **Limitless Company Brain** สมองบริษัทที่ทั้งทีมและ AI ใช้ร่วมกัน
ทำให้ AI ทุกตัวในทีม (Claude, ChatGPT/Codex, Cursor) ทำงานกับสมองบริษัทแบบเดียวกัน: อ่านหน้า Start here ก่อน ค้นก่อนตอบ ไม่เดาราคา และบันทึกสิ่งใหม่กลับลงโน้ตที่ถูกที่

[English below](#english)

## ติดตั้ง (3 คลิก)
1. เปิดแอป Limitless Company Brain ไปที่ **Vault settings → Skills → Browse marketplace**
2. วาง `jetlauncher/limitless-brain-skills` แล้วกด **Import all**
3. เปิด skill **brain-writeback** แล้วตั้งเป็น **Required** เพื่อให้ทุกคนในทีมได้ตัวนี้อัตโนมัติ (ตัวอื่นเป็น Optional ได้)

จากนั้นเริ่มจาก **brain-setup** ใน vault ใหม่ แล้วแก้โน้ตตัวอย่างให้เป็นข้อมูลจริงของบริษัท

## เชื่อม AI กับสมองบริษัท
ทุก skill ทำงานผ่าน connector Limitless Company Brain (MCP) ที่ `https://brain.jeditrinupab.com/api/mcp`

- **Claude Code:** รัน `claude mcp add --transport http --scope user limitless-brain https://brain.jeditrinupab.com/api/mcp` แล้วพิมพ์ `/mcp` เพื่อล็อกอิน แอปจะติดตั้ง skills ลง `~/.claude/skills` ให้เอง
- **Codex:** รัน `codex mcp add limitless-brain --url https://brain.jeditrinupab.com/api/mcp` แล้วล็อกอินในเบราว์เซอร์ แอปจะติดตั้ง skills ลง `~/.agents/skills` ให้เอง
- **Cursor และแอปอื่น:** ดูคู่มือ brain.jeditrinupab.com/downloads/install ส่วนที่ 4
- **แอป Claude:** เพิ่ม connector ด้วย URL ข้างบน แล้วพิมพ์ เช่น "ใช้ skill brain-setup จากสมองบริษัท" Claude จะอ่าน skill ผ่าน `list_skills`, `get_skill` และ `read_skill_file` เอง

## Skills ทั้ง 5 ตัว
| Skill | ทำอะไร | ลองพิมพ์ |
|---|---|---|
| **brain-setup** | สร้างโฟลเดอร์และโน้ตตั้งต้นใน vault ใหม่ ไม่เขียนทับของเดิม แล้วถามทีละข้อเพื่อกรอกหน้า Start here | "ตั้งค่าสมองบริษัทให้หน่อย" |
| **brain-writeback** | จบงานแล้วบันทึกข้อเท็จจริง การตัดสินใจ และคำตอบใหม่ลงโน้ตที่ถูกที่ แก้โน้ตเดิม ไม่สร้างซ้ำ ใส่วันที่ทุกการตัดสินใจ | "จำไว้นะ ต่อไปส่งของฟรีเมื่อซื้อครบ 1,000 บาท" |
| **meeting-to-brain** | แปลงบันทึกประชุม (Fathom, Plaud, Zoom หรือจดเอง) เป็นโน้ตประชุม การตัดสินใจ งานของแต่ละคน และ FAQ | "นี่คือสรุปประชุมทีมขายเมื่อวาน เก็บเข้าสมองให้หน่อย" |
| **faq-from-chats** | อ่านแชท LINE OA หนึ่งสัปดาห์ เพิ่มและปรับ FAQ แจ้งคำตอบที่ขัดกับราคาหรือ SOP ให้เจ้าของตัดสิน ไม่แก้ราคาเอง | "นี่คือแชท LINE OA สัปดาห์นี้ อัปเดต FAQ ให้หน่อย" |
| **weekly-brain-review** | รีวิวทุกวันศุกร์: โน้ตที่เปลี่ยนสัปดาห์นี้ โน้ตเก่าเกิน 90 วัน โน้ตซ้ำ และราคาที่ขัดกัน เขียนเป็นเช็กลิสต์ 15 นาที | "รีวิวสมองบริษัทประจำสัปดาห์" |

## โครงโฟลเดอร์ที่ brain-setup สร้าง
| โฟลเดอร์ | เก็บอะไร |
|---|---|
| `00 Start here` | ภาพรวมบริษัท ขายอะไร ให้ใคร ราคา น้ำเสียง ใครดูแลอะไร |
| `SOP` | ขั้นตอนการทำงาน เช่น `SOP ขาย & ราคา` |
| `FAQ` | คำถามที่ถามบ่อย แยกเป็นหมวด เช่น `FAQ ราคา & ส่วนลด` |
| `Products & prices` | สินค้า แพ็กเกจ ราคา |
| `Customers` | ข้อมูลลูกค้า |
| `Meetings` | บันทึกประชุม `YYYY-MM-DD หัวข้อ` |
| `Decisions` | การตัดสินใจ `YYYY-MM-DD เรื่อง` |
| `Team` | คนในทีม และงานของแต่ละคน |
| `_AI` | กฎสำหรับ AI (`How to use this brain`) และรีวิวประจำสัปดาห์ |

---

## English

Five AI skills for **Limitless Company Brain**, the shared company brain your team and your AI tools both read and write. They make every AI on the team (Claude, ChatGPT/Codex, Cursor) work the same way: read Start here first, search before answering, never invent prices, and file new facts back in the right note.

### Install (3 clicks)
1. In the Limitless Company Brain app, open **Vault settings → Skills → Browse marketplace**.
2. Paste `jetlauncher/limitless-brain-skills` and click **Import all**.
3. Open **brain-writeback** and set it to **Required** so everyone on the team gets it. The others can stay Optional.

Then run **brain-setup** in a new vault and replace the example notes with your real data.

### Connect your AI
Every skill works through the Limitless Company Brain connector (MCP) at `https://brain.jeditrinupab.com/api/mcp`.

- **Claude Code:** `claude mcp add --transport http --scope user limitless-brain https://brain.jeditrinupab.com/api/mcp`, then `/mcp` to sign in. The desktop app installs the skills into `~/.claude/skills`.
- **Codex:** `codex mcp add limitless-brain --url https://brain.jeditrinupab.com/api/mcp`, then sign in in the browser. The desktop app installs the skills into `~/.agents/skills`.
- **Cursor and other apps:** see brain.jeditrinupab.com/downloads/install?lang=en, Part 4.
- **Claude app:** add the connector with the URL above, then ask, for example, "use the brain-setup skill from the company brain". Claude reads the skill through `list_skills`, `get_skill` and `read_skill_file`.

### The five skills
| Skill | What it does | Try |
|---|---|---|
| **brain-setup** | Builds the starter folders and notes in a new vault without overwriting anything, then interviews the owner one question at a time to fill in Start here. | "Set up my company brain" |
| **brain-writeback** | At the end of a task, saves new facts, decisions and answers into the right note. Updates rather than duplicates, and dates every decision. | "Remember this: free shipping on orders over 1,000 baht" |
| **meeting-to-brain** | Turns a meeting transcript or summary (Fathom, Plaud, Zoom, typed) into a meeting note, dated decisions, per-person action items and FAQ entries. | "Here's yesterday's sales meeting summary, file it" |
| **faq-from-chats** | Reads a week of LINE OA chats, adds and updates FAQ entries, and lists answers that conflict with prices or SOPs for the owner to decide. Never changes a price itself. | "Here are this week's LINE OA chats, update the FAQ" |
| **weekly-brain-review** | Friday check: notes changed this week, notes older than 90 days, likely duplicates and conflicting prices, written as a 15-minute checklist. | "Run the weekly brain review" |

### Repo layout
Each skill is one folder, `skills/<name>/SKILL.md`, plus any files it needs (brain-setup keeps its note templates in `skills/brain-setup/templates/`). The importer treats every folder up to 5 levels deep that holds a `SKILL.md` as one skill. Skill names are lowercase letters, digits and hyphens and match their folder; files and folders starting with `.` are skipped on import.
