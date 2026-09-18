# TUM-HOME KKU (ตุ้มโฮม มข.) — Lifestyle & Activity Matching Platform
### 📱 Mobile UI/UX Design System: Wireframe (Low-Fi) & Prototype (High-Fi)

<div align="center">

[![Figma Prototype](https://img.shields.io/badge/Figma-Prototype%20Interactive-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/design/Ptycb6IgYbPVFfCblgiy9g/G16-TUM-HOME-KKU-Prototype?node-id=0-1&t=XAHtU2DpT5ir8qFX-1)
[![Khon Kaen University](https://img.shields.io/badge/KKU-Khon%20Kaen%20University-A73B24?style=for-the-badge&logo=google-scholar&logoColor=white)](https://www.kku.ac.th/)
[![Group](https://img.shields.io/badge/Team-Group%2016%20(G16)-00897B?style=for-the-badge)](https://github.com/chaiyawat19/TUM-HOME-KKU-Prototype)
[![Status](https://img.shields.io/badge/Design%20Status-Complete%20Showcase-success?style=for-the-badge)]()

<br/>

**🔗 [เปิดดู Interactive Prototype บน Figma (คลิกที่นี่)](https://www.figma.com/design/Ptycb6IgYbPVFfCblgiy9g/G16-TUM-HOME-KKU-Prototype?node-id=0-1&t=XAHtU2DpT5ir8qFX-1)**

<p align="center">
  <b>“ตุ้มโฮม (TUM-HOME)”</b> แพลตฟอร์มค้นหาเพื่อนร่วมกิจกรรม ไลฟ์สไตล์ และคอมมูนิตี้สำหรับนักศึกษามหาวิทยาลัยขอนแก่น<br/>
  พร้อมระบบสะสมแต้ม Gamification และแลกสิทธิพิเศษคูปองส่วนลดร้านค้าชั้นนำรอบรั้ว มข.
</p>

</div>

---

## 📑 สารบัญ (Table of Contents)
1. [เกี่ยวกับโครงการ (About TUM-HOME KKU)](#-เกี่ยวกับโครงการ-about-tum-home-kku)
2. [ภาพรวมโฟลว์การทำงาน (System Architecture & User Flow)](#-ภาพรวมโฟลว์การทำงาน-system-architecture--user-flow)
3. [ตารางเปรียบเทียบ Wireframe (Low-Fi) vs Prototype (High-Fi)](#-ตารางเปรียบเทียบ-wireframe-low-fi-vs-prototype-high-fi)
   - [01. Authentication & Onboarding](#01-authentication--onboarding-ระบบเข้าสู่ระบบและสมัครสมาชิก)
   - [02. Home Feed & Discovery](#02-home-feed--discovery-หน้าหลักและระบบค้นหา)
   - [03. Activity Creation Flow](#03-activity-creation-flow-ขั้นตอนการสร้างโพสต์หากิจกรรมทำร่วมกัน)
   - [04. Post Detail, Join & Completion](#04-post-detail-join--completion-รายละเอียดโพสต์-เข้าร่วม-และรับแต้ม)
   - [05. Chat & Community Hub](#05-chat--community-hub-ห้องแชทกลุ่มและกล่องข้อความ)
   - [06. Smart Q&A Assistant ("โกโก้ยอดนักตอบ")](#06-smart-qa-assistant-โกโก้ยอดนักตอบ-ai-chatbot)
   - [07. Gamification & Rewards Redemption](#07-gamification--rewards-redemption-ระบบสะสมแต้มและแลกคูปองส่วนลด)
   - [08. User Profile & Membership](#08-user-profile--membership-โปรไฟล์และระบบสมาชิก-tum-home-club)
   - [09. Notifications, Settings & Help Center](#09-notifications-settings--help-center-การแจ้งเตือน-ตั้งค่า-และศูนย์ช่วยเหลือ)
4. [Design System & UI Identity](#-design-system--ui-identity)
5. [โครงสร้างไดเรกทอรีที่จัดระเบียบใหม่ (Directory Structure)](#-โครงสร้างไดเรกทอรีที่จัดระเบียบใหม่-directory-structure)
6. [ตาราง Mapping ไฟล์เดิม ➔ ไฟล์ใหม่ (File Mapping Manifest)](#-ตาราง-mapping-ไฟล์เดิม--ไฟล์ใหม่-file-mapping-manifest)

---

## 💡 เกี่ยวกับโครงการ (About TUM-HOME KKU)

### 📌 ที่มาและปัญหา (Problem Statement)
ชีวิตนักศึกษาในมหาวิทยาลัยขอนแก่น (KKU) มักพบเจอปัญหา:
- อยากหาเพื่อนไปกินข้าวที่คอมเพล็กซ์ หรือร้านอาหารรอบ มข. แต่เพื่อนในกลุ่มติดธุระ
- อยากไปวิ่งออกกำลังกายตอนเช้า/เย็นที่บึงสีฐาน แต่ไม่อยากวิ่งคนเดียว
- อยากเล่นบอร์ดเกม ตีแบดมินตัน หรืออ่านหนังสือติวสอบ แต่ยังขาดคนร่วมตี้
- ขาดพื้นที่ส่วนกลางที่ปลอดภัย ตรวจสอบตัวตนได้เฉพาะนักศึกษา มข. ในการนัดเจอกันอย่างสร้างสรรค์

### 🚀 โซลูชันของ "TUM-HOME"
**TUM-HOME** เข้ามาตอบโจทย์ด้วยการเป็นแอปพลิเคชัน Matching กิจกรรมแบบ On-Demand:
- **Smart Category Matching**: แยกหมวดหมู่กิจกรรมชัดเจน (หาเพื่อนกินข้าว, ผับและบาร์, ทำกิจกรรม, ร้านคาเฟ่, กีฬา, บอร์ดเกม)
- **Built-in Group Chat**: เข้าร่วมโพสต์แล้วเข้ากลุ่มแชทพูดคุยเพื่อนัดหมายสถานที่และเวลาได้ทันที
- **Location & Distance Tracking**: บอกระยะทางและพิกัดจุดนัดพบใน มข. อย่างแม่นยำ
- **Gamification Points**: ทุกครั้งที่สร้างโพสต์หรือเข้าร่วมกิจกรรมสำเร็จ รับแต้มสะสมทันที 50 แต้ม
- **Privilege & Discount Exchange**: นำแต้มที่สะสมได้ไปแลกสิทธิพิเศษคูปองส่วนลด เช่น Super Sports, SF Cinema, Cafe Amazon, Auntie Anne's
- **AI Assistant ("โกโก้ยอดนักตอบ")**: บอตช่วยเหลือตอบข้อสงสัยและแนะนำการใช้งานตลอด 24 ชม.

---

## 🗺️ ภาพรวมโฟลว์การทำงาน (System Architecture & User Flow)

```mermaid
flowchart TD
    Start([เปิดแอปพลิเคชัน]) --> Loading[01. Splash & Loading]
    Loading --> Auth{เข้าสู่ระบบ?}
    Auth -->|ยังไม่มีบัญชี| SignUp[Sign up สมัครสมาชิก]
    Auth -->|มีบัญชีแล้ว| Login[Login เข้าสู่ระบบ]
    
    SignUp --> Home[02. Home Feed หน้าหลัก]
    Login --> Home
    
    Home --> Search[ค้นหากิจกรรม / กรองหมวดหมู่]
    Home --> CreatePost[03. สร้างโพสต์นัดเพื่อน]
    Home --> ViewPost[04. ดูรายละเอียดโพสต์]
    Home --> ChatTab[05. แชทข้อความ]
    Home --> RewardTab[07. ร้านค้าแลกแต้มสะสม]
    Home --> ProfileTab[08. โปรไฟล์ & สมาชิก]
    
    CreatePost --> StepCategory[เลือกประเภทกิจกรรม]
    StepCategory --> StepForm[กรอกข้อมูล: ชื่อ/สถานที่/รูป/วันเวลา/จำนวนคน]
    StepForm --> PublishPost[โพสต์สำเร็จ ➔ สร้างห้องแชทกลุ่ม]
    PublishPost --> ChatRoom[ห้องแชทกลุ่ม รอสมาชิก]
    
    ViewPost --> JoinPost[กดยืนยันเข้าร่วมกิจกรรม]
    JoinPost --> InGroupChat[พูดคุยในแชทกลุ่ม]
    InGroupChat --> Meetup[ทำกิจกรรมร่วมกัน]
    Meetup --> ReviewLoc[รีวิวและให้คะแนนสถานที่]
    ReviewLoc --> EarnPoints[รับแต้มสะสม +50 แต้ม!]
    
    EarnPoints --> RewardTab
    RewardTab --> RedeemCoupon[แลกคูปองส่วนลด SF / Amazon / Super Sports]
    
    ProfileTab --> EditProfile[แก้ไขข้อมูลส่วนตัว]
    ProfileTab --> Membership[สมัครสมาชิก TUM-HOME รายเดือน/รายปี x2 แต้ม]
    
    Home --> HelpCenter[09. ศูนย์ช่วยเหลือ FAQ]
    HelpCenter --> AskKoko[06. ถามโกโก้ยอดนักตอบ AI]
```

---

## 🖼️ ตารางเปรียบเทียบ Wireframe (Low-Fi) vs Prototype (High-Fi)

### 01. Authentication & Onboarding (ระบบเข้าสู่ระบบและสมัครสมาชิก)
การเตรียมพร้อมเข้าสู่แอปพลิเคชัน รองรับการเข้าสู่ระบบและลงทะเบียนของนักศึกษา มข.

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **Loading / Splash** | <img src="tumhome/wire-frame/01_auth/01_loading.png" width="180"/> | <img src="tumhome/prototype/01_auth/01_loading.png" width="180"/> | หน้าโหลดเริ่มต้น แสดงตราสัญลักษณ์ TUM-HOME KKU พร้อมแอนิเมชันเปิดตัว |
| **Login** | <img src="tumhome/wire-frame/01_auth/02_login.png" width="180"/> | <img src="tumhome/prototype/01_auth/02_login.png" width="180"/> | เข้าสู่ระบบด้วยอีเมล/รหัสผ่าน หรือ Single Sign-On |
| **Sign Up** | <img src="tumhome/wire-frame/01_auth/03_signup.png" width="180"/> | <img src="tumhome/prototype/01_auth/03_signup.png" width="180"/> | ลงทะเบียนบัญชีใหม่ ระบุข้อมูลส่วนตัวและยืนยันตัวตน |

---

### 02. Home Feed & Discovery (หน้าหลักและระบบค้นหา)
ฟีดกิจกรรมที่แนะนำแบบ Personalized พร้อมระบบคำนวณระยะทางแบบ Real-time และฟังก์ชันค้นหาตามประเภท

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **Home Feed** | <img src="tumhome/wire-frame/02_home_feed/01_home_feed.png" width="180"/> | <img src="tumhome/prototype/02_home_feed/01_home_feed.png" width="180"/> | ฟีดแท็บ: แนะนำ, ใกล้เคียง, ใหม่ พร้อมระยะทาง (km), วันเวลา, จำนวนผู้เข้าร่วม และปุ่มลอยสร้างโพสต์ |
| **Search & Filter** | <img src="tumhome/wire-frame/02_home_feed/02_search.png" width="180"/> | <img src="tumhome/prototype/02_home_feed/02_search.png" width="180"/> | ค้นหาด้วยคีย์เวิร์ด ตัวกรองสถานที่ และประเภทกิจกรรมตามความสนใจ |

---

### 03. Activity Creation Flow (ขั้นตอนการสร้างโพสต์หากิจกรรมทำร่วมกัน)
กระบวนการ Step-by-Step ที่เป็นมิตร ใช้งานง่าย และครอบคลุมรายละเอียดกิจกรรมครบถ้วน

| ขั้นตอน | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | คำอธิบายฟังก์ชัน |
| :--- | :---: | :---: | :--- |
| **1. เลือกหมวดหมู่** | <img src="tumhome/wire-frame/03_create_post/01_category_select.png" width="180"/> | <img src="tumhome/prototype/03_create_post/01_category_select.png" width="180"/> | Modal "อยากทำอะไร?": หาเพื่อนกินข้าว, ผับและบาร์, ทำกิจกรรม, ร้านคาเฟ่, กีฬา, บอร์ดเกม |
| **2. ฟอร์มตั้งต้น** | <img src="tumhome/wire-frame/03_create_post/02_form_blank.png" width="180"/> | <img src="tumhome/prototype/03_create_post/02_form_blank.png" width="180"/> | แบบฟอร์มสร้างโพสต์ มีช่องระบุข้อมูลครบถ้วน |
| **3. ตั้งชื่อโพสต์** | <img src="tumhome/wire-frame/03_create_post/03_input_title.png" width="180"/> | <img src="tumhome/prototype/03_create_post/03_input_title.png" width="180"/> | ใส่หัวข้อกิจกรรม เช่น *"หาเพื่อนกินข้าวที่คอมเพล็กซ์"* |
| **4. เลือกสถานที่** | <img src="tumhome/wire-frame/03_create_post/11_choose_location_modal.png" width="180"/> | <img src="tumhome/prototype/03_create_post/05_choose_location_modal.png" width="180"/> | ป็อปอัปแผนที่และจุดแลนด์มาร์กใน มข. เช่น ศูนย์อาหารคอมเพล็กซ์ |
| **5. อัปโหลดรูปภาพ** | <img src="tumhome/wire-frame/03_create_post/12_choose_pictures_modal.png" width="180"/> | <img src="tumhome/prototype/03_create_post/06_choose_pictures_modal.png" width="180"/> | แนบรูปบรรยากาศร้านหรือสถานที่นัดหมายได้สูงสุด 3 รูป |
| **6. เลือกวันและเวลา** | <img src="tumhome/wire-frame/03_create_post/13_choose_date_modal.png" width="180"/> | <img src="tumhome/prototype/03_create_post/08_choose_date_modal.png" width="180"/> | ปฏิทินและตัวเลือกเวลา (Date/Time Picker) ชัดเจน |
| **7. จำนวนคนสูงสุด** | <img src="tumhome/wire-frame/03_create_post/15_choose_max_participants_expanded.png" width="180"/> | <img src="tumhome/prototype/03_create_post/11_choose_max_participants_modal.png" width="180"/> | กำหนดจำนวนสมาชิกร่วมตี้ (3–15 คน) เพื่อความพอดีของโต๊ะและกลุ่ม |
| **8. ตรวจสอบ & โพสต์** | <img src="tumhome/wire-frame/03_create_post/10_step_ready.png" width="180"/> | <img src="tumhome/prototype/03_create_post/13_form_submit_ready.png" width="180"/> | หน้าฟอร์มที่กรอกครบทุกฟิลด์ พร้อมปุ่มฟ้าไฮไลต์ *"สร้างโพสต์"* เพื่อเผยแพร่ |

---

### 04. Post Detail, Join & Completion (รายละเอียดโพสต์, เข้าร่วม, และรับแต้ม)
ผู้ใช้สามารถกดดูรายละเอียด ตรวจสอบรายชื่อสมาชิก เข้าร่วมกลุ่ม รีวิว และรับแต้มรางวัล

| ขั้นตอน | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **หน้ารายละเอียดโพสต์** | <img src="tumhome/wire-frame/04_post_detail_join/01_post_detail.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/02_post_detail.png" width="180"/> | รูปภาพสไลด์, วันเวลา, สถานที่, ผู้สร้าง, สมาชิกที่เข้าร่วมแล้ว (X/X คน) |
| **แชร์โพสต์ (Share)** | <img src="tumhome/wire-frame/04_post_detail_join/03_share_post_modal_a.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/01_share_post_modal.png" width="180"/> | Bottom Sheet แชร์ลิงก์กิจกรรมไปยัง Social Media หรือส่งให้เพื่อน |
| **กดยืนยันเข้าร่วม** | <img src="tumhome/wire-frame/04_post_detail_join/05_join_chat_action.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/04_join_activity.png" width="180"/> | ปุ่ม *"เข้าร่วมแชท"* ดึงผู้ใช้เข้าสู่ระบบแชทกลุ่มทันที |
| **รายชื่อผู้เข้าร่วม** | <img src="tumhome/wire-frame/08_profile_membership/06_membership_benefits.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/05_member_list.png" width="180"/> | ดูรายชื่อเพื่อนร่วมตี้และโปรไฟล์ของแต่ละคน |
| **รีวิวสถานที่** | <img src="tumhome/wire-frame/04_post_detail_join/07_review_location_modal.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/07_review_location.png" width="180"/> | กิจกรรมเสร็จสิ้น ให้คะแนนดาว (1-5 ดาว) พร้อมรีวิวเพื่อสร้างคอมมูนิตี้ที่ดี |
| **รับแต้มสะสม +50 แต้ม** | <img src="tumhome/wire-frame/04_post_detail_join/06_reward_points_popup.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/08_reward_50_points.png" width="180"/> | Pop-up ยินดีด้วย *"คุณได้รับแต้ม 50 แต้ม"* เพิ่มเข้ากระเป๋าทันที |

---

### 05. Chat & Community Hub (ห้องแชทกลุ่มและกล่องข้อความ)
ระบบแชทแบบกลุ่มที่ถูกสร้างขึ้นโดยอัตโนมัติตามกิจกรรม ช่วยให้นัดหมายราบรื่น

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **กล่องข้อความ (Inbox)** | <img src="tumhome/wire-frame/05_chat/01_chat_inbox.png" width="180"/> | <img src="tumhome/prototype/05_chat/01_chat_inbox.png" width="180"/> | รายการห้องแชทของกิจกรรมทั้งหมด พร้อมแสดงจำนวนแต้มสะสมมุมขวาบน |
| **ห้องแชทที่มีการพูดคุย** | <img src="tumhome/wire-frame/05_chat/02_chat_room_active.png" width="180"/> | <img src="tumhome/prototype/05_chat/02_chat_room_active.png" width="180"/> | ห้องแชทกลุ่ม เช่น *"หาเพื่อนไปวิ่งที่บึงสีฐาน เช้านี้!!"* มีระบบแจ้งคนเข้ากลุ่ม |
| **ห้องแชทโพสต์ใหม่** | <img src="tumhome/wire-frame/05_chat/03_chat_room_waiting.png" width="180"/> | <img src="tumhome/prototype/05_chat/03_chat_room_waiting.png" width="180"/> | สถานะ *"รอคนเข้าร่วม"* สำหรับโพสต์ที่เพิ่งสร้างใหม่ |
| **กล่องข้อความอัปเดต** | <img src="tumhome/wire-frame/05_chat/04_chat_inbox_updated.png" width="180"/> | <img src="tumhome/prototype/05_chat/04_chat_inbox_updated.png" width="180"/> | แสดงห้องแชทที่อัปเดต และยอดเหรียญสะสมที่เพิ่มขึ้น (50 แต้ม) |

---

### 06. Smart Q&A Assistant ("โกโก้ยอดนักตอบ" AI Chatbot)
ผู้ช่วยอัจฉริยะประจำแอปพลิเคชัน TUM-HOME ให้คำแนะนำวิธีการใช้งานแก่นักศึกษา

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **ถามมาตอบไป (โกโก้)** | <img src="tumhome/wire-frame/06_qa_assistant/01_koko_qa_chat.png" width="180"/> | <img src="tumhome/prototype/06_qa_assistant/01_koko_qa_chat.png" width="180"/> | แชทกับ **"โกโก้ยอดนักตอบ"** เช่น ถามวิธีสร้างโพสต์ชวนเพื่อนว่ายน้ำ แชตบอตจะอธิบายทีละขั้นตอนอย่างละเอียด |

---

### 07. Gamification & Rewards Redemption (ระบบสะสมแต้มและแลกคูปองส่วนลด)
เปลี่ยนการเข้าร่วมกิจกรรมเป็นรางวัลจริง แลกรับคูปองร้านค้ายอดนิยมในขอนแก่น

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **หน้าร้านค้าแลกคะแนน** | <img src="tumhome/wire-frame/07_rewards/01_rewards_list.png" width="180"/> | <img src="tumhome/prototype/07_rewards/01_rewards_list.png" width="180"/> | คูปอง Super Sports 30% (50 แต้ม), ตั๋วหนัง SF 2 ใบ (500 แต้ม), ส่วนลด Cafe Amazon (50 แต้ม), ชุด Lemonade Auntie Anne's (25 แต้ม) |
| **หมวดหมู่แคตตาล็อก** | <img src="tumhome/wire-frame/07_rewards/01_rewards_list.png" width="180"/> | <img src="tumhome/prototype/07_rewards/02_rewards_catalog.png" width="180"/> | จัดหมวดหมู่อาหาร เครื่องดื่ม กีฬา และบันเทิง |
| **รายละเอียดคูปอง** | <img src="tumhome/wire-frame/07_rewards/02_coupon_detail.png" width="180"/> | <img src="tumhome/prototype/07_rewards/03_coupon_detail.png" width="180"/> | เงื่อนไขการใช้งาน, วันหมดอายุ (1 ม.ค. - 30 ก.ค. 2567), สาขาที่ร่วมรายการ และปุ่ม *"รับสิทธิ์"* |
| **ยืนยันการใช้แต้ม** | <img src="tumhome/wire-frame/07_rewards/03_confirm_redeem_modal.png" width="180"/> | <img src="tumhome/prototype/07_rewards/04_confirm_redeem_modal.png" width="180"/> | Dialog สรุปการใช้แต้ม ยืนยัน/ยกเลิก ป้องกันการกดผิด |

---

### 08. User Profile & Membership (โปรไฟล์และระบบสมาชิก TUM-HOME Club)
หน้าข้อมูลส่วนตัว แท็กความสนใจ และสิทธิพิเศษของสมาชิกคลับ

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **หน้าโปรไฟล์ผู้ใช้** | <img src="tumhome/wire-frame/08_profile_membership/01_profile_overview.png" width="180"/> | <img src="tumhome/prototype/08_profile_membership/01_profile_overview.png" width="180"/> | รูปโปรไฟล์, ไบโอ, แท็กความสนใจ, ยอดแต้มสะสม และแท็บ: เข้าร่วมแล้ว / โพสต์ที่สร้าง / ประวัติแลกของ |
| **แก้ไขโปรไฟล์** | <img src="tumhome/wire-frame/08_profile_membership/03_edit_profile.png" width="180"/> | <img src="tumhome/prototype/08_profile_membership/04_edit_profile_form.png" width="180"/> | แก้ไขชื่อแสดง, ชื่อผู้ใช้งาน, คำอธิบายตนเอง, เพศ และสิ่งที่สนใจ |
| **สิทธิประโยชน์สมาชิก** | <img src="tumhome/wire-frame/08_profile_membership/06_membership_benefits.png" width="180"/> | <img src="tumhome/prototype/04_post_detail_join/05_member_list.png" width="180"/> | สิทธิพิเศษ: รับแต้มเพิ่ม 2 เท่า, สร้างโพสต์ได้ไม่จำกัด, ลดราคาคูปองมากกว่าสมาชิกปกติ |
| **สมัครสมาชิก (Subscription)**| <img src="tumhome/wire-frame/08_profile_membership/07_membership_checkout_monthly.png" width="180"/> | <img src="tumhome/prototype/08_profile_membership/03_update_profile_status.png" width="180"/> | แพ็กเกจรายเดือน (฿199/เดือน) และรายปี (฿959/ปี เฉลี่ย ฿79.92/เดือน) ชำระผ่านระบบ Store |

---

### 09. Notifications, Settings & Help Center (การแจ้งเตือน, ตั้งค่า, และศูนย์ช่วยเหลือ)

| หน้าจอ | Wireframe (Low-Fidelity) | Prototype (High-Fidelity) | รายละเอียด |
| :--- | :---: | :---: | :--- |
| **การแจ้งเตือน (Noti)** | <img src="tumhome/wire-frame/09_settings_help/01_notifications.png" width="180"/> | <img src="tumhome/prototype/09_settings_help/01_notifications.png" width="180"/> | แจ้งเตือนเมื่อมีคนเริ่มติดตาม, แจ้งเตือนเวลาใกล้ถึงนัดหมาย และการอัปเดตกิจกรรม |
| **การตั้งค่า (Setting)** | <img src="tumhome/wire-frame/09_settings_help/02_settings.png" width="180"/> | <img src="tumhome/prototype/09_settings_help/02_settings.png" width="180"/> | เมนูจัดการบัญชี (ความปลอดภัย, ความเป็นส่วนตัว), ศูนย์ช่วยเหลือ, รายงานปัญหา และออกจากระบบ |
| **ศูนย์ช่วยเหลือ & FAQ** | <img src="tumhome/wire-frame/09_settings_help/03_help_faq.png" width="180"/> | <img src="tumhome/prototype/09_settings_help/03_help_faq.png" width="180"/> | คำถามที่พบบ่อย: แต้มได้จากอะไร?, แต้มเอาไปทำอะไร?, จะแลกแต้มต้องทำยังไง? พร้อมปุ่มไปถามโกโก้ |

---

## 🎨 Design System & UI Identity

### Color Palette (ชุดสีหลัก)
- **Primary Cyan/Aqua**: `#4DD0E1` / `#80DEEA` — สื่อถึงความสดใส ความเป็นมิตร และการเชื่อมโยงถึงกัน
- **Gamification Gold**: `#FFD54F` / `#FFA000` — สีเหรียญทองและแต้มคะแนน ให้ความรู้สึกมีคุณค่าและจูงใจ
- **Accent Yellow**: `#FFF59D` / `#FFEE58` — สีไฮไลต์ปุ่ม CTA รับสิทธิ์ และแท็กหมวดหมู่
- **Dark Elements**: `#1E1E1E` / `#2D3748` — สีปุ่มหลักและข้อความความคมชัดสูง อ่านง่ายสบายตา
- **Neutral Light**: `#F8F9FA` / `#FFFFFF` — พื้นหลังสไตล์ Card Elevation สะอาดตา ทันสมัย

### Typography & Iconography
- **Font**: บุคลิกแบบ Modern Sans-Serif อ่านง่าย เข้ากับภาษาไทยและอังกฤษ
- **Icons**: สไตล์ Minimalist Outline พร้อมไอคอนสีตามหมวดหมู่กิจกรรม
- **Form Factors**: ออกแบบสำหรับหน้าจอสมาร์ตโฟนสมัยใหม่ (iOS Safe Area 428 x 926 px)

---

## 📁 โครงสร้างไดเรกทอรีที่จัดระเบียบใหม่ (Directory Structure)

ไฟล์ภาพทั้งหมดถูกแบ่งหมวดหมู่อย่างเป็นระเบียบตาม Feature Module:

```
tumhome/
├── wire-frame/                    # ภาพโครงร่าง Low-Fidelity (51 ไฟล์)
│   ├── 01_auth/                   # ระบบยืนยันตัวตน (Loading, Login, Signup)
│   ├── 02_home_feed/              # หน้าฟีดหลัก และค้นหา
│   ├── 03_create_post/            # โฟลว์สร้างโพสต์และตัวเลือก Picker
│   ├── 04_post_detail_join/       # หน้ารายละเอียด, เข้าร่วม, รีวิว และรับแต้ม
│   ├── 05_chat/                   # ห้องแชทกลุ่มและกล่องข้อความ
│   ├── 06_qa_assistant/           # แชตบอตโกโก้ยอดนักตอบ
│   ├── 07_rewards/                # รายการแลกแต้มและคูปอง
│   ├── 08_profile_membership/     # โปรไฟล์ผู้ใช้และแพ็กเกจสมาชิก
│   └── 09_settings_help/          # แจ้งเตือน, การตั้งค่า และ FAQ
│
├── prototype/                     # ภาพดีไซน์เสมือนจริง High-Fidelity (43 ไฟล์)
│   ├── 01_auth/                   # หน้าจอสีสันสมบูรณ์ระบบ Auth
│   ├── 02_home_feed/              # หน้า Home Feed & Search พร้อมรูปภาพจริง
│   ├── 03_create_post/            # ลำดับขั้นตอนสร้างโพสต์แบบสมบูรณ์
│   ├── 04_post_detail_join/       # หน้าโพสต์, แชร์, สมาชิก, รีวิว, แต้ม 50 เหรียญ
│   ├── 05_chat/                   # หน้าจอแชทกลุ่มพร้อมคีย์บอร์ดเสมือน
│   ├── 06_qa_assistant/           # แชตบอตโกโก้สีสันเต็มรูปแบบ
│   ├── 07_rewards/                # คูปอง Super Sports, SF, Amazon, Auntie Anne's
│   ├── 08_profile_membership/     # โปรไฟล์และหน้าอัปเดตข้อมูล
│   └── 09_settings_help/          # หน้าตั้งค่าและการแจ้งเตือน
│
└── _raw_backup/                   # ข้อมูลสำรองต้นฉบับดั้งเดิม (ความปลอดภัย 100%)
    ├── wire-frame/
    └── prototype/
```

---

## 📋 ตาราง Mapping ไฟล์เดิม ➔ ไฟล์ใหม่ (File Mapping Manifest)

### 1. Prototype (High-Fidelity: รวม 43 ไฟล์)
| ชื่อไฟล์เดิม (Original Name) | หมวดหมู่ & ชื่อไฟล์ใหม่ (Organized Path) | คำอธิบายหน้าจอ |
| :--- | :--- | :--- |
| `Loading.png` | `01_auth/01_loading.png` | หน้าสแปลช/กำลังโหลด |
| `Login.png` | `01_auth/02_login.png` | หน้าเข้าสู่ระบบ |
| `Sign up.png` | `01_auth/03_signup.png` | หน้าสมัครสมาชิก |
| `Home.png` | `02_home_feed/01_home_feed.png` | หน้าหลักฟีดกิจกรรม |
| `Search.png` | `02_home_feed/02_search.png` | หน้าค้นหากิจกรรม |
| `ComboBox.png` | `03_create_post/01_category_select.png` | ตัวเลือกหมวดหมู่กิจกรรม |
| `CHANGE PAGE-1.png` | `03_create_post/02_form_blank.png` | ฟอร์มสร้างโพสต์ว่าง |
| `CHANGE PAGE.png` | `03_create_post/03_input_title.png` | กรอกชื่อโพสต์ |
| `CHANGE PAGE-2.png` | `03_create_post/04_input_location_note.png` | กรอกสถานที่และหมายเหตุ |
| `Chose location.png` | `03_create_post/05_choose_location_modal.png` | โมดอลเลือกพิกัดสถานที่ |
| `Chose picture.png` | `03_create_post/06_choose_pictures_modal.png` | โมดอลเลือกรูปภาพ |
| `CHANGE PAGE-3.png` | `03_create_post/07_form_with_photos.png` | ฟอร์มที่เพิ่มรูปภาพแล้ว |
| `Chose date.png` | `03_create_post/08_choose_date_modal.png` | โมดอลเลือกวัน |
| `Chose time.png` | `03_create_post/09_choose_time_modal.png` | โมดอลเลือกเวลา |
| `CHANGE PAGE-4.png` | `03_create_post/10_form_with_datetime.png` | ฟอร์มที่ระบุวันเวลาแล้ว |
| `Chose max participant.png` | `03_create_post/11_choose_max_participants_modal.png` | โมดอลเลือกจำนวนคนสูงสุด |
| `CHANGE PAGE-6.png` | `03_create_post/12_form_with_participants.png` | ฟอร์มระบุจำนวนคนครบถ้วน |
| `CHANGE PAGE-5.png` | `03_create_post/13_form_submit_ready.png` | ปุ่ม "สร้างโพสต์" แสดงพร้อมส่ง |
| `Share Post.png` | `04_post_detail_join/01_share_post_modal.png` | ป็อปอัปแชร์โพสต์ |
| `Detail.png` | `04_post_detail_join/02_post_detail.png` | หน้ารายละเอียดโพสต์ |
| `Post Detail.png` | `04_post_detail_join/03_post_detail_overview.png` | หน้ารายละเอียดโพสต์ภาพใหญ่ |
| `Join.png` | `04_post_detail_join/04_join_activity.png` | หน้าเข้าร่วมกิจกรรมสำเร็จ |
| `Member.png` | `04_post_detail_join/05_member_list.png` | รายชื่อสมาชิกในกิจกรรม |
| `Member-1.png` | `04_post_detail_join/06_member_list_expanded.png` | รายชื่อสมาชิกเพิ่มเติม |
| `Review location.png` | `04_post_detail_join/07_review_location.png` | ให้คะแนนรีวิวสถานที่ |
| `Get point.png` | `04_post_detail_join/08_reward_50_points.png` | ป็อปอัปได้รับ 50 แต้ม |
| `Get point-1.png` | `04_post_detail_join/09_reward_points_confirmed.png` | ยืนยันการรับแต้ม |
| `Chat all.png` | `05_chat/01_chat_inbox.png` | กล่องรวมแชท (เริ่มต้น 1 ห้อง) |
| `Chat.png` | `05_chat/02_chat_room_active.png` | ห้องแชทกลุ่มพร้อมคีย์บอร์ด |
| `Chat 2.png` | `05_chat/03_chat_room_waiting.png` | ห้องแชทใหม่รอคนเข้าร่วม |
| `Chat all 2.png` | `05_chat/04_chat_inbox_updated.png` | กล่องรวมแชทอัปเดต (2 ห้อง + 50 เหรียญ) |
| `ถามมาตอบไป.png` | `06_qa_assistant/01_koko_qa_chat.png` | โกโก้ยอดนักตอบ AI Chatbot |
| `แลกของ.png` | `07_rewards/01_rewards_list.png` | หน้ารายการคูปองแลกแต้ม |
| `Catalogs.png` | `07_rewards/02_rewards_catalog.png` | แคตตาล็อกหมวดหมู่สินค้า |
| `แกลของ.png` | `07_rewards/03_coupon_detail.png` | รายละเอียดคูปอง Super Sports |
| `Use point 2.png` | `07_rewards/04_confirm_redeem_modal.png` | ยืนยันการแลกคะแนน |
| `Profile.png` | `08_profile_membership/01_profile_overview.png` | หน้าโปรไฟล์หลักของผู้ใช้ |
| `Profile Update.png` | `08_profile_membership/02_profile_update_view.png` | หน้าตรวจสอบอัปเดตโปรไฟล์ |
| `Update profile.png` | `08_profile_membership/03_update_profile_status.png` | สถานะการแก้ไขโปรไฟล์ |
| `Edit Profile.png` | `08_profile_membership/04_edit_profile_form.png` | แบบฟอร์มแก้ไขข้อมูลส่วนตัว |
| `Noti.png` | `09_settings_help/01_notifications.png` | ศูนย์แจ้งเตือนกิจกรรม |
| `Setting.png` | `09_settings_help/02_settings.png` | หน้าการตั้งค่าบัญชี |
| `Help.png` | `09_settings_help/03_help_faq.png` | ศูนย์ช่วยเหลือและคำถามที่พบบ่อย |

---

### 2. Wire-frame (Low-Fidelity: รวม 51 ไฟล์)
| ชื่อไฟล์เดิม (Original Name) | หมวดหมู่ & ชื่อไฟล์ใหม่ (Organized Path) | คำอธิบายหน้าจอ |
| :--- | :--- | :--- |
| `Loading (MU).png` | `01_auth/01_loading.png` | Wireframe หน้าโหลดเริ่มต้น |
| `Login (MU).png` | `01_auth/02_login.png` | Wireframe เข้าสู่ระบบ |
| `Sign up (MU).png` | `01_auth/03_signup.png` | Wireframe สมัครสมาชิก |
| `Home (MU).png` | `02_home_feed/01_home_feed.png` | Wireframe หน้าหลักฟีดกิจกรรม |
| `Search (MU).png` | `02_home_feed/02_search.png` | Wireframe ค้นหากิจกรรม |
| `da.png` | `03_create_post/01_category_select.png` | Wireframe เลือกหมวดหมู่กิจกรรม |
| `Detail post.png` | `03_create_post/02_form_blank.png` | Wireframe ฟอร์มสร้างโพสต์ว่าง |
| `CHANGE PAGE.png` | `03_create_post/03_input_title.png` | Wireframe กรอกชื่อโพสต์ |
| `CHANGE PAGE-1.png` | `03_create_post/04_step_location.png` | Wireframe ขั้นตอนระบุสถานที่ |
| `CHANGE PAGE-2.png` | `03_create_post/05_step_photos.png` | Wireframe ขั้นตอนแนบรูปถ่าย |
| `CHANGE PAGE-3.png` | `03_create_post/06_step_datetime.png` | Wireframe ขั้นตอนเลือกวันเวลา |
| `CHANGE PAGE-4.png` | `03_create_post/07_step_members.png` | Wireframe ขั้นตอนระบุผู้เข้าร่วม |
| `CHANGE PAGE-5.png` | `03_create_post/08_step_tags.png` | Wireframe ขั้นตอนใส่แท็ก |
| `CHANGE PAGE-6.png` | `03_create_post/09_step_notes.png` | Wireframe ขั้นตอนใส่หมายเหตุ |
| `CHANGE PAGE-7.png` | `03_create_post/10_step_ready.png` | Wireframe ฟอร์มพร้อมกดส่ง |
| `Chose location.png` | `03_create_post/11_choose_location_modal.png` | Wireframe โมดอลเลือกสถานที่ |
| `Chose picture.png` | `03_create_post/12_choose_pictures_modal.png` | Wireframe โมดอลเลือกรูปถ่าย |
| `Chose date.png` | `03_create_post/13_choose_date_modal.png` | Wireframe โมดอลเลือกวัน |
| `Chose time.png` | `03_create_post/14_choose_time_modal.png` | Wireframe โมดอลเลือกเวลา |
| `Home-8.png` | `03_create_post/15_choose_max_participants_expanded.png` | Wireframe เลือกจำนวนคน (เปิด Dropdown) |
| `Home-9.png` | `03_create_post/16_choose_max_participants_collapsed.png` | Wireframe เลือกจำนวนคน (ปิด Dropdown) |
| `Home-2.png` | `03_create_post/17_form_state_a.png` | Wireframe สถานะฟอร์ม A |
| `Home-3.png` | `03_create_post/18_form_state_b.png` | Wireframe สถานะฟอร์ม B |
| `Home-10.png` | `03_create_post/19_form_state_c.png` | Wireframe สถานะฟอร์ม C |
| `Post2.png` | `04_post_detail_join/01_post_detail.png` | Wireframe หน้ารายละเอียดโพสต์ |
| `Post2-2.png` | `04_post_detail_join/02_post_detail_view.png` | Wireframe รายละเอียดโพสต์มุมมองที่ 2 |
| `Post2-1.png` | `04_post_detail_join/03_share_post_modal_a.png` | Wireframe แชร์โพสต์ แบบ A |
| `Post2-3.png` | `04_post_detail_join/04_share_post_modal_b.png` | Wireframe แชร์โพสต์ แบบ B |
| `Join.png` | `04_post_detail_join/05_join_chat_action.png` | Wireframe ปุ่มเข้าร่วมแชท |
| `Join-1.png` | `04_post_detail_join/06_reward_points_popup.png` | Wireframe จบกิจกรรมรับ 50 แต้ม |
| `Join-2.png` | `04_post_detail_join/07_review_location_modal.png` | Wireframe รีวิวสถานที่ให้คะแนนดาว |
| `Home-12.png` | `04_post_detail_join/08_reward_50_points_confirm.png` | Wireframe ป็อปอัปยืนยันรับแต้ม |
| `Ch.png` | `05_chat/01_chat_inbox.png` | Wireframe กล่องรวมแชท |
| `Chat1.png` | `05_chat/02_chat_room_active.png` | Wireframe ห้องแชทกลุ่ม |
| `Chat 3.png` | `05_chat/03_chat_room_waiting.png` | Wireframe ห้องแชทใหม่รอสมาชิก |
| `Chat all 3.png` | `05_chat/04_chat_inbox_updated.png` | Wireframe กล่องแชทอัปเดต 2 ห้อง |
| `ถามมาตอบไป.png` | `06_qa_assistant/01_koko_qa_chat.png` | Wireframe แชทบอตโกโก้ยอดนักตอบ |
| `แกลของ-1.png` | `07_rewards/01_rewards_list.png` | Wireframe หน้ารายการแลกคะแนน |
| `แกลของ-2.png` | `07_rewards/02_coupon_detail.png` | Wireframe หน้ารายละเอียดคูปอง |
| `แกลของ.png` | `07_rewards/03_confirm_redeem_modal.png` | Wireframe ยืนยันการแลกคูปอง |
| `Home-4.png` | `08_profile_membership/01_profile_overview.png` | Wireframe หน้าโปรไฟล์ผู้ใช้ |
| `Home-11.png` | `08_profile_membership/02_profile_joined_tabs.png` | Wireframe แท็บประวัติที่เข้าร่วมแล้ว |
| `Home-7.png` | `08_profile_membership/03_edit_profile.png` | Wireframe หน้าแก้ไขโปรไฟล์ |
| `Update profile.png` | `08_profile_membership/04_update_profile_status.png` | Wireframe สถานะอัปเดตโปรไฟล์ |
| `Home.png` | `08_profile_membership/05_membership_plans.png` | Wireframe ตัวเลือกแพ็กเกจสมาชิก |
| `Member.png` | `08_profile_membership/06_membership_benefits.png` | Wireframe สิทธิประโยชน์ของสมาชิก |
| `Home-5.png` | `08_profile_membership/07_membership_checkout_monthly.png` | Wireframe สมัครสมาชิกรายเดือน |
| `Member-1.png` | `08_profile_membership/08_membership_checkout_confirm.png` | Wireframe ยืนยันการสมัครสมาชิก |
| `Home-1.png` | `09_settings_help/01_notifications.png` | Wireframe หน้าการแจ้งเตือน |
| `Setting.png` | `09_settings_help/02_settings.png` | Wireframe หน้าการตั้งค่า |
| `Home-6.png` | `09_settings_help/03_help_faq.png` | Wireframe หน้าช่วยเหลือ FAQ |

---

## 👥 ข้อมูลโครงการ (Project Information)
- **สถาบันการศึกษา**: มหาวิทยาลัยขอนแก่น (Khon Kaen University)
- **กลุ่มผู้พัฒนา**: Group 16 (G16)
- **หัวข้อโครงงาน**: TUM-HOME KKU Mobile Application Prototype
- **Figma File**: [G16-TUM-HOME-KKU-Prototype](https://www.figma.com/design/Ptycb6IgYbPVFfCblgiy9g/G16-TUM-HOME-KKU-Prototype?node-id=0-1&t=XAHtU2DpT5ir8qFX-1)