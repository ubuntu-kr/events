[![Deploy Website](https://github.com/ubuntu-kr/events/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/ubuntu-kr/events/actions/workflows/deploy.yml)
# event.ubuntu-kr.org

> This website and source codes are no longer maintained and has been replaced with ["Schedules & Events" category on Forum.](https://discourse.ubuntu-kr.org/c/scheds-and-events)
> 이 웹사이트 및 소스코드는 더이상 유지보수 되지 않으며, [포럼의 "일정 및 행사" 카테고리로 대체 되었습니다.](https://discourse.ubuntu-kr.org/c/scheds-and-events)

The new Event list website of Ubuntu Korea Community. Built with [Hugo](https://gohugo.io) and vanillaframework.io

## License
MIT License (See `LICENSE`)

## 새 포스팅 추가하기
 [Hugo CLI](https://gohugo.io/getting-started/installing/) 를 설치하고, 이 명령줄 프로그램으로 새 포스팅을 생성합니다.

아래와 같은 명령으로 새 포스팅을 추가합니다. 명령으로 생성된 새 Markdown 파일을 수정하여 글을 작성합니다.
사진 등 첨부파일을 추가하려면, 글 본문인 담긴 `index.md` 와 동일한 디렉터리에 넣고 사용합니다.
```bash
# 포스팅 추가
hugo new --kind post post/<session-name>/index.md
# 예시: "UbuCon Asia 2021 후기" 라는 제목의 글 추가
hugo new --kind post post/ubucon-asia-2021-review/index.md

```

게시물에 대한 영문 번역을 추가하려면, `index.md` 가 있는 디렉터리에 `index.en.md` 파일을 생성하고, 생성된 파일에 번역된 내용을 작성하면 됩니다.
