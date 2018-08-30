
<?php
$data = array(1000,1001,1002);
$smarty->assign('custid',$data);
?>


{* この例は $custid 配列のすべての値を表示します *}
{section name=customer loop=$custid}
  id: {$custid[customer]}<br />
{/section}
<hr />
{* $custid 配列のすべての値を逆順に表示します *}
{section name=foo loop=$custid step=-1}
  {$custid[foo]}<br />
{/section}


{section name=foo start=10 loop=20 step=2}
  {$smarty.section.foo.index}
{/section}
<hr />
{section name=bar loop=21 max=6 step=-2}
  {$smarty.section.bar.index}
{/section}

