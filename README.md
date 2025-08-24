# Git Commands Demonstration

โปรเจกต์นี้ทำขึ้นเพื่อแสดงการใช้งานคำสั่ง **Reset**, **Revert**, และ **Checkout** ของ Git

---

## Git Reset
ใช้สำหรับย้อน commit กลับไปยังสถานะก่อนหน้า  
ตัวอย่างที่ทำในงานนี้:

```bash
# ก่อน reset
git log --oneline
32734cd (HEAD -> master, origin/master, origin/HEAD) Merge branch 'thai-lang'
077a7a6 Change label in summit to Thai language in IndexPage.vue
e93f624 Edit waning age
d3a7f6e Edit ladel age eng to thai
5d9902e Add 'Notify'in quasar.comf.js
814ec1f Change label to Thai language in IndexPage.vue
232e0eb Add script part
bef138d Add template part
b1baef7 1st project-quasar

# reset กลับไปที่ commit 814ec1f
git reset --hard 814ec1f
814ec1f (HEAD -> master) Change label to Thai language in IndexPage.vue
232e0eb Add script part
bef138d Add template part
b1baef7 1st project-quasar

# ย้อนกลับมาใหม่อีกครั้ง
git reset --hard 32734cd
32734cd (HEAD -> master, origin/master, origin/HEAD) Merge branch 'thai-lang'
077a7a6 Change label in summit to Thai language in IndexPage.vue
e93f624 Edit waning age
d3a7f6e Edit ladel age eng to thai
5d9902e Add 'Notify'in quasar.comf.js
814ec1f Change label to Thai language in IndexPage.vue
232e0eb Add script part
bef138d Add template part
b1baef7 1st project-quasar

# push 
git push origin master --force
