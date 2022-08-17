# sehyun1094's Github Pages

> 블로그 주소  
<https://sehyun1094.github.io>  

<br>  

> Git 초기 설정
- 명령 프롬프트를 통하여 다음 코드를 실행
```
git config --global user.name [사용자 이름]
git config --global user.email [사용자 이메일]
```


> github 블로그 업데이트 방법  
- blog 폴더에서 다음을 실행
```
git clone [repo 주소]
```   

- blog 업데이트 할 폴더 위치로 이동(cd)
- 파일 수정 후 다음을 실행
```
git add .
git commit "메세지"
git push origin main
```

> LF will be replaced by CRLF in 오류  
- 다음 코드를 실행
```python
# Windows, Dos
git config --global core.autocrlf false

# Linux, Mac
git config --global core.autocrlf input
```

---
Powered By [Hydejack-Starter-Kit](https://github.com/hydecorp/hydejack-starter-kit)
