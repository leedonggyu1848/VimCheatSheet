# VimCheatSheet

## 목차

[일반](#1-일반)
[커서이동](#2-커서이동)
[삽입모드](#3-삽입모드)
[편집모드](#4-편집모드)
[선택(visual)모드](#5-선택visual모드)
[선택(visual)모드-명령](#6-선택visual모드-명령)
[레지스터](#7-레지스터)
[마킹](#8-마킹)
[매크로](#9-매크로)
[잘라내기와 붙여넣기](#10-잘라내기와-붙여넣기)
[문단모양](#11-문단모양)
[나가기](#12-나가기)
[검색과 바꾸기](#13-검색과-바꾸기)
[여러 파일 검색](#14-여러-파일-검색)
[탭](#15-탭)
[여러 파일 작업](#16-여러-파일-작업)
[비교](#17-비교)
--

## 1. 일반

key | 설명
:-- | :--
:h[elp] keyword | 도움말 열기
:sav[eas] file | 다른 이름으로 저장
:clo[se] | 현재 창 닫기
:ter[minal] | 터미널 열기
K | 커서가 가리키는 단어의 설명글 열기
[%d]명령어 | %d번 명령어 반복

--

## 2. 커서이동
key | 설명
:-- | :--
s | 왼쪽으로 한 칸 이동
j | 아래로 한 칸 이동
k | 위로 한 칸 이동
l | 오른쪽으로 한 칸 이동
gj | 아래로 한 칸 이동(한 줄이 길 때)
gk | 위로 한 칸 이동(한 줄이 길 때)
H | 현재화면 상단으로 점프
M | 현재화면 중단으로 점프
L | 현재화면 하단으로 점프
w | 다음 단어 시작으로 점프
W | 다음 단어 시작으로 점프 (특수문자 포함)
e | 다음 단어 끝으로 점프
E | 다음 단어 끝으로 점프 (특수문자 포함)
b | 이전 단어 시작으로 점프
B | 이전 단어 시작으로 점프 (특수문자 포함)
ge | 이전 단어 끝으로 점프
gE | 이전 단어 끝으로 점프 (특수문자 포함)
% | 현재 괄호의 짝으로 점프 (:h matchpairs를 통해 더 많은 정보를 얻을 수 있습니다.)
0 | 현재 행 시작으로 점프 (공백 포함)
^ | 현재 행 시작으로 점프
$ | 현재 행 끝으로 점프 (공백 포함)
g_ | 현재 행 끝으로 점프
gg | 문서 첫 줄 시작으로 점프
G | 문서 끝 줄 시작으로 점프
[%d]gg or [%d]G | %d번째 행 시작으로 점프
gd | 지역변수 선언위치로 점프
gD | 전역변수 선언위치로 점프
fx | 다음 검색 문자 x로 점프
tx | 다음 검색 문자 x 앞에 점프
Fx | 이전 검색 문자 x로 점프
Tx | 이전 검색 문자 x 뒤에 점프
; | 최근 f/t/F/T 명령어 실행
, | 최근 F/T/f/t 명령어 실행
} | 다음 단락으로 점프
{ | 이전 단락으로 점프
zz | 화면 위치 중간으로 조정
<C-e> | 한 줄 아래로 화면 조정
<C-y> | 한 줄 위로 화면 조정
<C-b> | 한 화면 위로 조정
<C-f> | 한 화면 아래로 조정
<C-d> | 반 화면 아래로 조정
<C-u> | 반 화면 위로 조정

--

## 3. 삽입모드

key | 설명
:-- | :--
i | 현재 커서 앞에 삽입
I | 현재 커서 행 시작에 삽입
a | 현재 커서 뒤에 삽입
A | 현재 커서 행 끝에 삽입
o | 현재 커서 행 아래에 새 행을 삽입
O | 현재 커서 행 위에 새 행을 삽입
ea | 단어 끝 뒤에 삽입
<C-h> | 이전 문자 제거
<C-w> | 이전 단어 제거
<C-j> | 한 줄 바꿈
<C-t> | 한 탭 들여쓰기
<C-d> | 한 탭 내어쓰기
<C-n> | 다음 단어 탐색 (자동완성)
<C-p> | 이전 단어 탐색 (자동완성)
<C-r> + %c| 레지스터 %c의 내용 삽입
<C-ox> + %c | Temporarily enter normal mode to issue one normal-mode command %c.
<ESC> | 삽입모드 종료

--

## 4. 편집모드

key | 설명
:-- | :--
r | 한 글자 바꾸기
R | 한 글자 이상 바꾸기(ESC 누르면 종료)
J | 현재 행과 다음 행 연결
gJ | 현재 행과 다음 행 연결 (공백무시)
gwip | 단락 리플로우
g~ | 커서 이동으로 대·소문자 전환
gu | 커서 이동으로 소문자 전환
gU | 커서 이동으로 대문자 전환
cc | 한 행 전체 새로 쓰기
c$ or C | 한 행 끝까지 새로 쓰기
ciw | 한 단어 전체 새로 쓰기
cw or ce | 한 단어 끝까지 새로 쓰기
s | 한 문자 새로 쓰기
S | 한 행 전체 새로 쓰기 (cc와 동일)
xp | 잘라내고 붙여넣기
u | 실행취소
U | 최근 수정한 줄 복원(실행취소)
<C-r> | 다시실행(undo)
. | 최근 명령어 반복

--

## 5. 선택(visual)모드

key | 설명
:-- | :--
v | 비주얼 모드
V | 비주얼 라인
o | 선택 영역 반대쪽 끝으로 점프
<C-v> | 비주얼 블록
O | 블록의 반대쪽 모서리로 이동
aw | 단어 선택
ab | 소괄호() 구간 선택
aB | 중괄호{} 구간 선택
at | 태그<> 구간 선택
ib | 소괄호() 내부 선택
iB | 중괄호{} 내부 선택
it | 태그<> 내부 선택
<ESC> | 선택 모드 종료

--

## 6. 선택(visual)모드 명령

key | 설명
:-- | :--
> | 선택 행 들여쓰기
< | 선택 행 내어쓰기
y | 선택 구간 복사
d | 선택 구간 삭제
~ | 대소문자 반전
u | 선택 구간 소문자 전환
U | 선택 구간 대문자 전환

--

## 7. 레지스터

key | 설명
:-- | :--
:reg[isters] | 레지스터 내용 확인
"[%c]y | 레지스터 %c 복사
"[%c]p | 레지스터 %c 붙여넣기
"+y | 클립보드 복사
"+p | 클립보드 붙여넣기

### 7.1 특수 레지스터

reg | 설명
:-- | :--
\0 | 최근 복사 레지스터
\" | 최근 사용 레지스터
\% | 현재 파일명
\# | 대체 파일명
\* | 클립보드 (X11 primary)
\+ | 클립보드 (X11 clipboard)
\/ | 최근 검색 패턴
\: | 최근 Vim 명령줄
. | 최근 삽입 텍스트
\- | 최근 제거 문자
\= | 표현식 레지스터
\_ | 블랙홀 레지스터

--

## 8. 마킹

key | 설명
:-- | :--
:marks | 마킹 항목 표시
ma | 현재 위치를 a로 마킹
`a | 마크 a로 점프
y`a | 마크 a까지 복사
`0 | 종료 전 커서위치로 점프
`" | 최근 편집한 커서 위치로 점프
`. | 최근 변경한 커서 위치로 점프
`` | 최근 점프 전 위치로 점프
:ju[mps] | 점프목록
Ctrl + i | 이전 점프목록 위치로 점프
Ctrl + o | 다음 점프목록 위치로 점프
:changes | 변경목록
g, | 이전 변경목록 위치로 점프
g; | 다음 변경목록 위치로 점프
Ctrl + ] | 커서가 가리키는 태그로 점프

--

## 9. 매크로

key | 설명
:-- | :--
qa | 매크로 a 기록 시작
q | 매크로 기록 중지
@a | 매크로 a 실행
@@ | 최근 매크로 재실행

--

## 10. 잘라내기와 붙여넣기

key | 설명
:-- | :--
yy | 한 행 복사하기
2yy | 2줄 복사하기
yw | 다음 단어까지 복사하기
yiw | 한 단어 복사하기
yaw | 한 단어 복사하기 (공백포함)
y$ or Y | 한 행 끝까지 복사하기
p | 커서 뒤에 붙여넣기
P | 커서 앞에 붙여넣기
gp | 커서 뒤에 붙여넣고 붙여넣은 행 다음으로 커서 옮기기
gP | 커서 앞에 붙여넣고 붙여넣은 행 다음으로 커서 옮기기
dd | 한 행 잘라내기
2dd | 2줄 잘라내기
dw | 다음 단어까지 잘라내기
diw | 한 단어 잘라내기
daw | 한 단어 잘라내기 (공백포함)
d$ or D | 한 행 끝까지 잘라내기
x | 한 문자 잘라내기

--

## 11. 문단모양
key | 설명
:-- | :--
>> | 한 탭 들여쓰기
<< | 한 탭 내어쓰기
>% | 중·소괄호 구간 들여쓰기
>ib | 소괄호 내부 들여쓰기
>at | 태그 구간 들여쓰기
3== | 3줄 자동정렬
=% | 중·소괄호 구간 자동정렬
=iB | 중괄호 내부 자동정렬
gg=G | 전체 버퍼 자동정렬
]p | 붙여쓰고 현재 행 들여쓰기 조

--

## 12. 나가기
key | 설명
:-- | :--
:w | 저장하기
:w !sudo tee % | 관리자로 저장하기
:wq or :x or ZZ | 저장하고 나가기
:q | 나가기 (변경확인)
:q! or ZQ | 나가기 (변경무시)
:wqa | 모든 탭 저장하고 나가기

--

## 13. 검색과 바꾸기
key | 설명
:-- | :--
/pattern | 패턴 검색 (순방향)
?pattern | 패턴 검색 (역방향)
\vpattern | 특수 매직 패턴
n | 다음 검색항목으로 점프
N | 이전 검색항목으로 점프
:%s/old/new/g | 모든 old를 new로 바꾸기
:%s/old/new/gc | 모든 old를 new로 확인하며 바꾸기
:noh[lsearch] | 검색 하이라이트 제거

--

## 14. 여러 파일 검색
key | 설명
:-- | :--
:vim[grep] /pattern/ {`{file}`} | 여러 파일에서 패턴 검색
e.g. :vim[grep] /foo/ **/*
:cn[ext] | 다음 검색항목으로 점프
:cp[revious] | 이전 검색항목으로 점프
:cope[n] | 일치 목록을 새 창으로 열기
:ccl[ose] | 일치 목록 창 닫기

--

## 15. 탭
key | 설명
:-- | :--
:tabnew or :tabnew {page.words.file} | 새 탭에서 파일 열기
Ctrl + wT | 현재 분할 창을 새로운 탭으로 이동
gt or :tabn[ext] | 다음 탭으로 이동
gT or :tabp[revious] | 이전 탭으로 이동
#gt | #번째 탭으로 이동
:tabm[ove] # | 현재 탭을 #번째로 이동
:tabc[lose] | 현재 탭과 그 안의 창들 닫기
:tabo[nly] | 현재 탭 이외의 모든 탭 닫기
:tabdo command | 모든 탭에서 command 실행하기 (예를 들어, :tabdo q - 열린 모든 탭 닫기)

--

## 16. 여러 파일 작업
key | 설명
:-- | :--
:e[dit] file | 새 버퍼에서 파일 편집
:bn[ext] | 다음 버퍼로 이동
:bp[revious] | 이전 버퍼로 이동
:bd[elete] | 버퍼 삭제 (파일 닫기)
:b[uffer]# | #번째 버퍼로 이동
:b[uffer] file | 파일명 버퍼로 이동
:ls or :buffers | 열린 버퍼 모두 나열
:sp[lit] file | 새 버퍼에 파일 열고 상하로 창 분할
:vs[plit] file | 새 버퍼에 파일 열고 좌우로 창 분할
:vert[ical] ba[ll] | 모든 버퍼 열고 좌우로 창 분할
:tab ba[ll] | 모든 버퍼 열고 탭으로 창 분할
Ctrl + ws | 상하로 창 분할
Ctrl + wv | 좌우로 창 분할
Ctrl + ww | 창 전환
Ctrl + wq | 창 닫기
Ctrl + wx | 창 바꾸기
Ctrl + w= | 모든 창 크기 조정
Ctrl + wh | 왼쪽 창으로 이동
Ctrl + wl | 오른쪽 창으로 이동
Ctrl + wj | 아래 창으로 이동
Ctrl + wk | 위 창으로 이동
Ctrl + wH | 현재 창을 최대 높이인 상태로 왼쪽 이동(가장 왼쪽)
Ctrl + wL | 현재 창을 최대 높이인 상태로 오른쪽 이동(가장 오른쪽)
Ctrl + wJ | 현재 창을 최대 너비인 상태로 아래로 이동(가장 아래쪽
Ctrl + wK | 현재 창을 최대 너비인 상태로 위로 이동(가장 위쪽)

--

## 17. 비교
key | 설명
:-- | :--
zf | 폴딩 정의
zd | 폴드 제거
za | 폴드 설정
zo | 폴드 열기
zc | 폴드 닫기
zr | 한 단계씩 폴드 열기
zm | 한 단계씩 폴드 접기
zi | 스마트 폴딩
]c | 다음 수정으로 점프
[c | 이전 수정으로 점프
do or :diffg[et] | 다른 버퍼에서 차이점 얻기
dp or :diffpu[t] | 다른 버퍼로 차이점 보내기
:diffthis | 현재 창 비교모드 열기
:dif[fupdate] | 비교모드 새로고침
:diffo[ff] | 현재 창 비교모드 닫가
