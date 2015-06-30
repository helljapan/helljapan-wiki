[헬일본 위키]에 기여하는 법 (위키미정)
===================

헬일본 위키의 내용은 git로 보관되도록 설계되었습니다. 아래의 순서에 따라 기여하시면 됩니다. 

윈도우에서는 https://github.com/git-for-windows/git/releases 에서 편리한 버전을 활용하실 수 있습니다.

헬일본 위키를 편집하기 위해서는 **Github 계정이 있어야 합니다. 먼저 가입하세요~~**

## 일반인용

### 문서 생성 제안하기

위키 접속 후 없는 문서 페이지 URL을 임의로 입력하시면 위키 페이지를 생성할 수 있는 URL을 안내해드립니다. 해당 링크를 따라 들어가서 편집하신 후 등록 신청(pull)하시면 됩니다.

파일 이름은 폴더 구조를 갖춘 후 **폴더/구조/구성후/최종문서명.wiki** (확장자 md 포함)와 같이 구성해주셔야 합니다.

Github 웹에서 사용하시는 에디터 화면에 Edit New File 옆에 Preview 탭이 있습니다. 눌러보시면서 페이지의 모양을 예상하시면서 작업하시면 편리합니다.

위키미정

### 문서 편집 제안하기

문서 편집 제안은 각 위키 문서에 들어가신 후 연필모양의 Edit This File 아이콘을 누르시거나 위키 본문에 편집 아이콘을 포함시킬 예정입니다. 링크를 따라가 동일하게 진행하시면 됩니다.


## 덕후용

### 저장소를 Fork 하신 후 내 계정 이름으로 Clone합니다. (여기에서 내 계정 이름은 hellbari이라고 가정합니다.)

ex) https://github.com/hellbari/helljapan-wiki.git


### 새로운 패치셋을 전송할 때

> git checkout -b localwiki

주어진 폴더에서 수정을 마치신 후

> git add . --all

> git commit -m "{이 커밋과 관련한 이유/사항 등 입력}"

> git push origin localnotes

로 전송하신 후 성공하시면 Fork 해두신 본인의 저장소에, Create Pull Request라는 녹색 버튼이 생기면 신청서를 작성하시면 됩니다. 


### 패치셋에 문제가 있어서 변경할 때

패치셋에 문제가 생겼거나 분쟁 발생시 기본적으로 수정하신 후 추가 commit들을 squash 하시는 것이 서버 부담을 줄게 하기 위한 대책입니다. 

이를 위해서 추가 커밋을 일단 수행하신 후

> git rebase --interactive HEAD~2 (여기에서 2는 후퇴할 커밋 수입니다.)

> 텍스트 나올시에 맨 처음 것만 pick 하시고 모두 squash로 바꾸십니다. (기본 에디터에서는 :wq를 입력하여 저장후 나오십니다.)

> 이후 커밋 편집을 하시면 커밋이 합쳐지며, 

> git push origin localnotes --force

를 통하여 다시 전송하시면 수정되며, Pull 요청서도 자동으로 수정이 된다곤 하는데 아직 해본적은 없습니다.

자세한 사항은 https://dogfeet.github.io/articles/2011/git-merge.html 를 참고하세요


## 기타

이 밖에도 별도 문의사항이나 건의사항이 있으시다면 티켓을 생성하시거나 http://ask.fm/hellchosun 으로 문의주시면 됩니다.

파일 이름은 폴더 구조를 갖춘 후 최종문서명.wiki 와 같이 구성해주셔야 합니다.

기타 내용은 [Using pull requests - Github Help](https://help.github.com/articles/using-pull-requests/)도 참고하세요!

저도 git 허접입니다. 고수분들이 보시기에 문제가 있는 부분이 있으면 이 문서도 수정해서 pull하시면 됩니다!
