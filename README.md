# Pri-stagram
동아리 PRIMITIVE Web 교육 실습 코드 : 인스타그램 느낌의 웹페이지

<img width="1440" alt="스크린샷 2022-05-29 오전 12 21 36" src="https://user-images.githubusercontent.com/79641953/170831781-bd7ff210-85ad-49fd-b421-0ba189813dfa.png">

# 실습 자료
## font 파일
/* 인스타그램 로고 폰트 */
@import url('https://fonts.googleapis.com/css2?family=Cookie&display=swap');
/* font-family: 'Cookie', cursive; */

/* 기본 폰트 */
@import url('https://cdn.rawgit.com/moonspam/NanumSquare/master/nanumsquare.css');
/* font-family: 'NanumSquare'; */

/* 포인트 폰트 - explore 페이지 */
@font-face {
    font-family: 'Cafe24Ssurround';
    src: url('https://2022-01-newyear.s3.ap-northeast-2.amazonaws.com/Cafe24Ssurround.woff') format('woff');
}

@font-face {
    font-family: 'Cafe24Oneprettynight';
    src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_twelve@1.1/Cafe24Oneprettynight.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

## javascript
// jquery 라이브러리 링크

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>


// 자바스크립트

<script lang="javascript">
    var img_loc = './static/images/';

    // heart 이미지 클릭 시 로테이션으로 변경
    $('.heart').on({'click' : function() {
        var src = ($(this).attr('src') == img_loc + 'heart_icon.svg')
            ? img_loc + 'heart_active.svg'
            : img_loc + 'heart_icon.svg';
            $(this).attr('src', src);
        }
    });

    $('.message').on({'click' : function() {
        alert('메시지 보내!');
        }
    });

    $('.bookmark').on({'click' : function() {
        var src = ($(this).attr('src') == img_loc + 'bookmark_icon.svg')
            ? img_loc + 'bookmark_active.svg'
            : img_loc + 'bookmark_icon.svg';
            $(this).attr('src', src);
        }
    });

    function write_comment(n) {
        var textarea = document.querySelectorAll('.comment_txtarea');
        alert('댓글을 달았어요! : ' + textarea[n].value);
    }

    document.querySelector('#notice').addEventListener('click', function() {
        alert('\n1. 반응형 인스타 클론코딩\n2. 하트, 메시지, 북마크 아이콘 클릭 시 이벤트\n3. 댓글 입력 후 게시버튼 클릭 시 이벤트\n4. 상단 home, notice, explore 메뉴 클릭 시 이벤트\n');
    });
</script>
