# รวมมิจ

[![All Contributors](https://img.shields.io/github/all-contributors/akexorcist/ruam-mij-android?color=ee8449&style=flat-square)](#contributors)

## รวมสารพัดข้อมูลเพื่อช่วยให้คุณพ้นภัยจากมิจฉาชีพ

![cover.png](image%2Fcover.png)

แอปสำหรับตรวจสอบแอปที่น่าสงสัยภายในเครื่องที่สุ่มเสี่ยงต่อความปลอดภัยของผู้ใช้ในด้านต่าง ๆ เช่น แอปที่ถูกติดตั้งจากช่องทางที่ไม่ปลอดภัย หรือการใช้ Accessibility Services ในทางที่ไม่ถูกต้อง เป็นต้น

## การติดตั้ง
[![ดาวน์โหลดเวอร์ชันล่าสุด](image%2Fbutton.png)](https://github.com/akexorcist/ruam-mij-android/releases/download/1.0.2/app-release.apk)

ดาวน์โหลดแอปและติดตั้งผ่านไฟล์ APK ในแต่ละเวอร์ชันได้จากหน้า [Release บน GitHub ของ Repository นี้](https://github.com/akexorcist/ruam-mij-android/releases)

แน่นอนว่าวิธีในการติดตั้งแอปแบบนี้จะไม่ต่างอะไรกับการโหลดไฟล์ APK ของแอปอื่นมาติดตั้งด้วยตัวเอง ซึ่งเป็นหนึ่งในช่องทางสำหรับผู้ที่ไม่ประสงค์ดีและหวังจะใช้ประโยชน์จากการหลอกให้ติดตั้งแอปที่ไม่ปลอดภัยด้วยวิธีแบบนี้

## คำแนะนำก่อนใช้งาน
* ถ้าคุณกังวลในการใช้งานแอปนี้เนื่องจากต้องดาวน์โหลดเป็นไฟล์ APK มาติดตั้งในเครื่องด้วยตัวเอง ไม่แนะนำให้ดาวน์โหลดแอปนี้
* ถ้าคุณไม่เข้าใจเนื้อหาที่แสดงในแอปนี้ แนะนำให้ปรึกษาคนรอบตัวที่มีความรู้เกี่ยวกับระบบแอนดรอยด์ เพราะแอปนี้แสดงข้อมูลเชิงลึกสำหรับผู้ใช้ที่มีความรู้ความเชี่ยวชาญในระบบแอนดรอยด์
* แอปนี้ช่วยในการตรวจสอบแอปที่ติดตั้งอยู่ภายในเครื่องเท่านั้น ไม่สามารถป้องกันหรือขัดขวางการทำงานของแอปที่ไม่ปลอดภัยได้

![highlight.png](image%2Fhighlight.png)

## ฟีเจอร์ที่มีให้ใช้งาน
* ตรวจสอบแอปที่ถูกติดตั้งจากช่องทางที่ไม่ปลอดภัย พร้อมกับแสดงข้อมูลสำคัญของแอปเพื่อช่วยให้ผู้ใช้ตรวจสอบแอปภายในเครื่องตัวเองได้ง่ายขึ้น
* ตรวจสอบแอปที่มีการใช้งานการเชื่อเหลือพิเศษหรือ Accessibility Service ภายในเครื่อง
* ตรวจสอบแอปที่กำลังจับภาพหน้าจออยู่ในขณะนั้น (Screen Sharing หรือ Media Projection)

## ความเป็นส่วนตัวของผู้ใช้
* แอปทำงานแบบออฟไลน์ ไม่ได้ขอสิทธิ์เข้าถึง Internet ตั้งแต่แรกเพื่อให้ผู้ใช้มั่นใจได้ว่าข้อมูลส่วนตัวของผู้ใช้จะไม่ถูกส่งออกไปที่อื่น [ตรวจสอบโค้ดได้ที่ [AndroidManifest.xml](app%2Fsrc%2Fmain%2FAndroidManifest.xml)]
* แอปขอสิทธิ์ (Permission) ที่เรียกว่า `QUERY_ALL_PACKAGES` ซึ่งเป็นสิทธิ์ในการขอค้นหาแอปที่ติดตั้งอยูภายในเครื่องเท่านั้น และเป็นแค่เพียงสิทธิ์เดียวเท่านั้นที่แอปที่ขอเข้าถึง และนั่นก็เป็นเหตุผลที่ทำให้แอปนี้ไม่สามารถอยู่บน Google Play ได้ เนื่องจากแอปนี้ไม่เข้าข่ายแอปที่จะใช้งานงานสิทธิ์ดังกล่าวได้
* ไม่มีการทำงานเบื้องหลังใด ๆ แอปจะทำงานในตอนที่ผู้ใช้เปิดใช้งานเท่านั้น
* ไม่มีการเก็บข้อมูลใด ๆ ของผู้ใช้ รวมไปถึงข้อมูลแอปที่ติดตั้งในเครื่องที่เราจะตรวจสอบใหม่ทุกครั้งเมื่อคุณเปิดแอปขึ้นมา
* ถ้าคุณรู้สึกว่าแอปดูเรียบง่าย และทำอะไรได้ไม่เยอะ นั่นสิ่งที่ทีมพัฒนาตั้งใจให้เป็นเช่นนั้น เพราะเราไม่อยากให้คุณต้องรู้สึกเสี่ยงอันตรายจากการติดตั้งแอปของเราเช่นกัน (เพราะคุณก็ต้องโหลด APK ของแอปนี้ไปติดตั้งด้วยตัวเองเช่นกัน) ดังนั้นการทำงานของแอปนี้จึงเป็นแบบออฟไลน์และรบกวนผู้ใช้ให้น้อยที่สุดเท่าที่จะทำได้

## ถ้ามีคำถามหรือข้อสงสัย
* สามารถตั้งคำถามได้ผ่านหน้า [Issue บน GitHub ของ Repository นี้](https://github.com/akexorcist/ruam-mij-android/issues)

## อยากมีส่วนรวมในการพัฒนาโปรเจคนี้?
ดูรายละเอียดได้ที่ [Contributing](CONTRIBUTING.md)

## คำแนะนำสำหรับการ Build Debug APK จาก Source Code โดยตรง (สำหรับทดสอบแบบ Nightly ในกรณีที่โค้ดมีการอัปเดตแต่ยังไม่ Release)
ตรวจสอบให้แน่ใจว่าตั้งค่า Environment Variable `ANDROID_HOME` ให้ชี้ไปยัง Android SDK ที่ถูกต้อง
และควรตั้งค่า `JAVA_HOME` ให้ชี้ไปยัง JDK ที่ต้องการใช้งานด้วย

```bash
echo $ANDROID_HOME
echo $JAVA_HOME
```
หลังจาก Run Command ข้างต้น หากเห็น Path ชี้ไปยัง SDK และ JDK ที่ต้องการแล้ว ให้ Run Command ด้านล่างต่อไปนี้เพื่อ Build Debug APK สำหรับทดสอบ

```bash
git clone https://github.com/akexorcist/ruam-mij-android.git
cd ruam-mij-android

# List all task from gradlew
./gradlew task

# Build a debug apk
./gradlew assembleDebug
```

## License
ดูได้ที่ [LICENSE](LICENSE)

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/dheerapat"><img src="https://avatars.githubusercontent.com/u/61280196?v=4?s=100" width="100px;" alt="dheerapat"/><br /><sub><b>dheerapat</b></sub></a><br /><a href="#doc-dheerapat" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/Judrummer"><img src="https://avatars.githubusercontent.com/u/12605075?v=4?s=100" width="100px;" alt="Tipatai Puthanukunkit"/><br /><sub><b>Tipatai Puthanukunkit</b></sub></a><br /><a href="#code-Judrummer" title="Code">💻</a> <a href="#infra-Judrummer" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://kajornsakp.dev"><img src="https://avatars.githubusercontent.com/u/10228783?v=4?s=100" width="100px;" alt="Kajornsak Peerapathananont"/><br /><sub><b>Kajornsak Peerapathananont</b></sub></a><br /><a href="#code-kajornsakp" title="Code">💻</a> <a href="#infra-kajornsakp" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://farzai.com"><img src="https://avatars.githubusercontent.com/u/4928451?v=4?s=100" width="100px;" alt="parsilver"/><br /><sub><b>parsilver</b></sub></a><br /><a href="#code-parsilver" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/popeyee27"><img src="https://avatars.githubusercontent.com/u/8433930?v=4?s=100" width="100px;" alt="Suttichan Paenchan"/><br /><sub><b>Suttichan Paenchan</b></sub></a><br /><a href="#code-popeyee27" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://nayuki.cyou"><img src="https://avatars.githubusercontent.com/u/69802296?v=4?s=100" width="100px;" alt="Nayuki"/><br /><sub><b>Nayuki</b></sub></a><br /><a href="#code-Kuuuuuuuu" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/azygous13"><img src="https://avatars.githubusercontent.com/u/3615979?v=4?s=100" width="100px;" alt="Teerapong Chantakard"/><br /><sub><b>Teerapong Chantakard</b></sub></a><br /><a href="#code-azygous13" title="Code">💻</a></td>
    </tr>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://www.mikkipastel.com"><img src="https://avatars.githubusercontent.com/u/17794661?v=4?s=100" width="100px;" alt="Monthira Chayabanjonglerd"/><br /><sub><b>Monthira Chayabanjonglerd</b></sub></a><br /><a href="#code-mikkipastel" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/iamwee"><img src="https://avatars.githubusercontent.com/u/10849396?v=4?s=100" width="100px;" alt="Wathin Sonnukij"/><br /><sub><b>Wathin Sonnukij</b></sub></a><br /><a href="#code-iamwee" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/kittinunf"><img src="https://avatars.githubusercontent.com/u/4669517?v=4?s=100" width="100px;" alt="Kittinun Vantasin"/><br /><sub><b>Kittinun Vantasin</b></sub></a><br /><a href="#code-kittinunf" title="Code">💻</a> <a href="#infra-kittinunf" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/FatCatCode"><img src="https://avatars.githubusercontent.com/u/2326355?v=4?s=100" width="100px;" alt="CatCode"/><br /><sub><b>CatCode</b></sub></a><br /><a href="#code-FatCatCode" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://siriwatk.dev"><img src="https://avatars.githubusercontent.com/u/18292247?v=4?s=100" width="100px;" alt="Siriwat K"/><br /><sub><b>Siriwat K</b></sub></a><br /><a href="#doc-siriwatknp" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/validcube"><img src="https://avatars.githubusercontent.com/u/93124920?v=4?s=100" width="100px;" alt="Pun Butrach"/><br /><sub><b>Pun Butrach</b></sub></a><br /><a href="#code-validcube" title="Code">💻</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/ultimagz"><img src="https://avatars.githubusercontent.com/u/1924593?v=4?s=100" width="100px;" alt="Pitsanu Kittipittayakorn"/><br /><sub><b>Pitsanu Kittipittayakorn</b></sub></a><br /><a href="#code-ultimagz" title="Code">💻</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->