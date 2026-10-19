SARATHI MEDIA RATE CARD PRO — APK BUILD KIT v1.0

या पॅकेजमधील Customer Dashboard HTML ला Android APK मध्ये पॅक करण्यासाठी GitHub Actions वापरले आहे. Windows वर Android Studio आवश्यक नाही; GitHub क्लाउडवर बिल्ड चालेल.

महत्त्वाची स्पष्टता:
- हे APK build starter kit आहे, आधीपासून तयार APK नाही.
- यात Customer Dashboard v1.6 HTML पॅक केले आहे. HTML मधील ग्राहकनिहाय Draft Library/API integration चे end-to-end परीक्षण झालेले नाही. APK बनणे म्हणजे सर्व feature योग्यरीत्या चालणे याची हमी नाही.
- Admin Hub APK मध्ये समाविष्ट केलेला नाही; Admin Panel फक्त तुमच्याकडे राहावा.
- Production मध्ये वितरित करण्याआधी API URL, customer ID selection, draft loading, live preview, rate calculations, PNG export, network/offline behavior तपासा.

Windows शिवाय build करण्याच्या पायऱ्या:
1. https://github.com वर sign in करा आणि New repository तयार करा. नाव: sarathi-rate-card-apk. Private repository निवडणे चांगले.
2. ZIP extract करा.
3. GitHub repository मध्ये Add file > Upload files वापरून ZIP मधील सर्व files/folders upload करा. ZIP स्वतः upload करू नका; extract केलेल्या files upload करा. Commit करा.
4. Repository > Actions tab > “Build Sarathi APK” workflow > Run workflow क्लिक करा. पहिल्या push वरही workflow चालू होईल.
5. Workflow हिरवा झाल्यावर run उघडा > Artifacts मधील Sarathi-Rate-Card-Pro-debug-apk डाउनलोड करा. ZIP extract केल्यावर app-debug.apk मिळेल.
6. APK Android फोनवर पाठवा. Install करताना Android “Install unknown apps” permission विचारू शकतो. फक्त स्वतःच्या विश्वासार्ह APK साठीच परवानगी द्या.

जर Actions workflow fail झाला तर लाल error log चा screenshot/text पाठवा.

Production note:
- Debug APK चाचणीसाठी आहे; मोठ्या प्रमाणात ग्राहकांना देण्यासाठी signed release APK तयार करणे आवश्यक आहे.
- HTML app ग्राहक ID ला सुरक्षितपणे authenticate करत नसेल तर ID बदलून दुसऱ्या ग्राहकाचे drafts पाहण्याचा धोका असतो. Production launch आधी server-side customer authorization लागू करणे आवश्यक.
