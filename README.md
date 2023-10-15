# 우아한테크코스 6기 지원 포트폴리오

## 목차
> [📚 1. 효과적인 학습 방식과 경험](https://github.com/fromitive/woowahan-tech#-1-%ED%9A%A8%EA%B3%BC%EC%A0%81%EC%9D%B8-%ED%95%99%EC%8A%B5-%EB%B0%A9%EC%8B%9D%EA%B3%BC-%EA%B2%BD%ED%97%98)
>
> [💻 2. 성장 중 겪은 실패와 극복](https://github.com/fromitive/woowahan-tech#-2-%EC%84%B1%EC%9E%A5-%EC%A4%91-%EA%B2%AA%EC%9D%80-%EC%8B%A4%ED%8C%A8%EC%99%80-%EA%B7%B9%EB%B3%B5)
>
> [🚣 3. 오랜 시간 몰입했던 경험 그리고 도전](https://github.com/fromitive/woowahan-tech#-3-%EC%98%A4%EB%9E%9C-%EC%8B%9C%EA%B0%84-%EB%AA%B0%EC%9E%85%ED%96%88%EB%8D%98-%EA%B2%BD%ED%97%98-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EB%8F%84%EC%A0%84)
>
> [💡 4. 원하는 프로그래머 모습](https://github.com/fromitive/woowahan-tech#-4-%EC%9B%90%ED%95%98%EB%8A%94-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%A8%B8-%EB%AA%A8%EC%8A%B5)

## 📚 1. 효과적인 학습 방식과 경험

### 🎉 학창시절 노력한 최종 결과물

![학창시절 공부 성과](resource/school.png)

### 🎞️ 발표스터디 발표 슬라이드 쇼

**🔗 슬라이드 쉐어 : https://www.slideshare.net/fromitive/presentations**

### 🎉 케이실드 주니어 학업 우수상과 인증서

![Alt text](resource/k-shield.png)


[🔙 목차로 돌아가기](https://github.com/fromitive/woowahan-tech#%EB%AA%A9%EC%B0%A8)

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

[🔙 목차로 돌아가기](https://github.com/fromitive/woowahan-tech#%EB%AA%A9%EC%B0%A8)

---

## 🚣 3. 오랜 시간 몰입했던 경험 그리고 도전


### 🎬 인프라 취약점 진단 자동화 툴 시연 영상 (영상 길이 - 6분)

**시간이 없으시면 4:00 부터 보시면 됩니다! 감사합니다!**

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/fCxAIZc_xj8/0.jpg)](https://youtu.be/fCxAIZc_xj8)

[🔙 목차로 돌아가기](https://github.com/fromitive/woowahan-tech#%EB%AA%A9%EC%B0%A8)

---

## 💡 4. 원하는 프로그래머 모습

**🔗 블로그 링크 : https://fromitive.github.io/fromitive-blog/**

**🔗 일기 : https://fromitive.github.io/fromitive-diary/**

### 🎬 토이프로젝트 - 백테스팅 툴 (영상 길이 - 2분 34초)

**🔗 레포지토리 : https://github.com/fromitive/news-issuer**

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/8__cC-urP7A/0.jpg)](https://youtu.be/8__cC-urP7A)

[🔙 목차로 돌아가기](https://github.com/fromitive/woowahan-tech#%EB%AA%A9%EC%B0%A8)

---

## End of Document

긴 글 읽어주시고 제 자신을 돌아 볼 기회를 주셔서 감사합니다🙇🏻‍♂️