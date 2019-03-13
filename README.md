# GoodGoodStudy
DayDayUp
1、BeanUtil.substringByte(masterFile.getHhanyoMoji1(), 0, 4) 按字节截 
2、subString（）使用时进行长度判断预防空指针
	if (tmpStr.length() > 4) {
	tmpStr = tmpStr.substring(0, 4);
			}
3、日时转化
ApplDateFormat.convertIgnoreV2M(getUser(),masterFile.getEntryDatet(), "yyyyMMddHHmmss", "HHmmss")
4、 
create cast ( numeric as text) with INOUT as implicit; 
create cast ( varchar as timestamp) with INOUT as implicit;   
create cast ( integer as text) with INOUT as implicit; 
create cast ( varchar as integer ) with INOUT as implicit;

5　rs.getString（1）；不要这么编码，不利于后期维护。
6 隐藏变量如果设置多个值，可能会导致空指针异常。具体情况时，要具体分析，查找具体是哪个隐藏变量重复设置值。有可能在当前jsp里隐含有别的jsp（ListHiddenItem.jsp）,而该jsp可能已经设置过隐藏变量。常见可能设置重复的隐藏变量有
<html:hidden property="action"></html:hidden>
<html:hidden property="conditionKey"></html:hidden>
<html:hidden property="lastConditionKey"></html:hidden>
<html:hidden property="pageNo"></html:hidden>
7 　SQL语句执行的时候，比较隐蔽的问题注意：
　and（（A）or（B）or（C））和and  A or B or C 结果是不一样的
8　在全选的时候如果初始化里面有disabled的chebox,在添加全选的时候，需要加上（选择器）.not(':disabled').prop("checked", v);
9　postgre 修改表结构
ALTER TABLE sisxv00010.rekjkp1 ADD wzkgidnm character varying(40);
ALTER TABLE sisyt.RCUSTP1 DROP  COLUMN whn11ig;
alter table sisxv00010.eevhdp1 alter column wevusup type character varying(15);
