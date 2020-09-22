<div align="center">

## CIRCULATING TEXT


</div>

### Description

This feature circulates text in the top right corner of your web page.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[DOSpoweredGEEK](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dospoweredgeek.md)
**Level**          |Advanced
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |HTML
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__4-9.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dospoweredgeek-circulating-text__4-6792/archive/master.zip)





### Source Code

```
<!-- Paste in head -->
<script language="JavaScript">
if (document.all){
msg="Your message goes here ";
msgColor="00ff00";
msgFont="Verdana";//Some fonts work better than others, Verdana is smoothest!
//Nothing needs altering below!
msg=msg.split('');
n=msg.length;
e=360/n;
yp=0;
xp=0;
yb=40;
xb=60;
sa=0.07;
sb=0;
pa=new Array();
pb=new Array();
for (i=0; i < n; i++){
document.write('<div id="logo" style="position:absolute;top:0;left:0;'
+'height:30;width:30;font-family:'+msgFont+';text-align:center;color:'+msgColor+'">'+msg[i]+'</div>');
}
function ani(){
yp=document.body.scrollTop+50;
xp=document.body.scrollLeft+window.document.body.clientWidth-100;
for (i=0; i < n; i++){
logo[i].style.top =yp+yb*Math.sin(sb+i*e*Math.PI/180);
logo[i].style.left=xp+xb*Math.cos(sb+i*e*Math.PI/180);
pb[i]=logo[i].style.pixelTop-yp;
pa[i]=pb[i]-pb[i]*2;
if (pa[i] < 1){
pa[i]=0;
logo[i].style.visibility='hidden';
}
else logo[i].style.visibility='visible';
logo[i].style.fontSize=pa[i]/2.7;
}
sb-=sa;
setTimeout('ani()',10);
}
window.onload=ani;
}
</script>
```

