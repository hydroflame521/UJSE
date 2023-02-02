# UJSE
Universal JavaScript Editor is a bookmarklet that lets you edit text on most websites. just drag the code into a bookmark and and click the bookmark to turn the editor on. To hide the editing cursor, hit escape.

I did not make this script and i forgot where i got it. I will take it down if the maker of the script requests it.

```
javascript:(function(){  document.designMode='on';  const s=document.createElement('style');  s.innerHTML=`body::before{content:'✏%EF%B8%8F Edit Mode (ESC to end)';z-index:64;padding:1em;background:white;color:black;display:block;margin:1em;font-size:30px;border:5px solid green;}`;  document.body.appendChild(s);  window.scrollTo(0,0);  document.addEventListener('keyup',e => {    if(e.key==='Escape'){      document.designMode='off';      s.remove();      document.removeEventListener('keyup',e);    }  });})();
```
