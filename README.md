-- oracle_Year_Date_Formats
--Simple date forms and year formats
select * from scott.emp where to_char(hiredate, 'YYYY') >= 1981;

select ename || ' Joined in '||to_char(hiredate, 'YYYY') YOJ from scott.emp where to_char(hiredate, 'YYYY') >= 1981;

select e.*, to_char(sysdate, 'Q') from scott.emp e;

select * from scott.emp where to_char(hiredate, 'MON')  between 'JAN' and 'MAY';
select * from scott.emp where to_char(hiredate, 'MM')  between 1 and 4;
select * from scott.emp where trim(to_char(hiredate, 'DAY')) = 'SUNDAY';

select e.*, trim(to_char(hiredate, 'DAY')) dat from scott.emp e;
