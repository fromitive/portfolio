# 우아한테크코스 6기 지원 포트폴리오


## 📚 1. 효과적인 학습 방식과 경험

### 🎉 학창시절 노력한 최종 결과물

![학창시절 공부 성과](resource/school.png)

### 🎉 케이실드 주니어 학업 우수상과 인증서

![Alt text](resource/k-shield.png)

---

## 💻 2. 성장 중 겪은 실패와 극복

### 첨부 방식으로 변경한 코드

**🔗 레포지토리 : https://github.com/fromitive/news-issuer**
``` python
...
## 파일 위치: mailsender/mailbuild.py 51line
def setContent(self, contentsDir):
    # 1. 크롤링한 html 파일을 읽어옵니다.
    with open(os.path.join(contentsDir, "main.html"), "r", encoding="utf-8") as fcontent:  
        content = fcontent.read()
        soup = BeautifulSoup(content, features="html.parser")

        # 2. img 테그의 첨부된 이메일 경로를 추출합니다.
        imgTags = soup.select("img")
        for img in imgTags:
            srcBefore = img.attrs["src"]
            htmlCid, attachCid = self._generateCid()

            img.attrs["src"] = htmlCid

            # 이미지를 메일에 첨부합니다.
            with open(os.path.join(contentsDir, srcBefore), "rb") as fimgContent:
                imgContent = fimgContent.read()
                imgAttach = MIMEImage(imgContent)
                imgAttach.add_header("Content-ID", attachCid)
                self.ImgContents.append(imgAttach)
        self.strMailContent = str(soup)
...
```

> [!IMPORTANT]
> 피싱메일 시스템은 회사 자산이어서 이를 응용한 보안 뉴스레터 발송 시스템으로 증적을 대체합니다 🙏

### 🎬 보안 뉴스레터 발송 시스템 시연 영상 (영상 길이 - 1분 50초)

**시간이 없으시면 1:16 부터 보시면 됩니다! 감사합니다!**

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/EqdP1rJLXiI/0.jpg)](https://youtu.be/EqdP1rJLXiI)

---

## 🚣 3. 오랜 시간 몰입했던 경험 그리고 도전

### 🎬 인프라 취약점 진단 자동화 툴 시연 영상 (영상 길이 - 6분)

**시간이 없으시면 4:00 부터 보시면 됩니다! 감사합니다!**

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/fCxAIZc_xj8/0.jpg)](https://youtu.be/fCxAIZc_xj8)

---

## 💡 4. 원하는 프로그래머 모습

**🔗 블로그 링크 : https://fromitive.github.io/fromitive-blog/**

**🔗 일기 : https://fromitive.github.io/fromitive-diary/**

### 🎬 토이프로젝트 - 백테스팅 툴 (영상 길이 - 2분 34초)

**🔗 레포지토리 : https://github.com/fromitive/news-issuer**

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/8__cC-urP7A/0.jpg)](https://youtu.be/8__cC-urP7A)

---

## End of Document

긴 글 읽어주시고 제 자신을 돌아 볼 기회를 주셔서 감사합니다🙇🏻‍♂️