# calendario
@ECHO off

if not exist "%1" (
    mkdir "%1"
) 
cd "%1"
if not exist "%2" (
    mkdir "%2"
)
cd "%2"

set mes=%2
if %mes%==1 set dias=31
if %mes%==2 set dias=28
if %mes%==3 set dias=31
if %mes%==4 set dias=30
if %mes%==5 set dias=31
if %mes%==6 set dias=30
if %mes%==7 set dias=31
if %mes%==8 set dias=31
if %mes%==9 set dias=30
if %mes%==10 set dias=31
if %mes%==11 set dias=30
if %mes%==12 set dias=31


for /L %%i in (1,1,%dias%) do (
    if not exist %%i (
        mkdir  %%i
    )
)




cd ..
cd ..
mkdir %
