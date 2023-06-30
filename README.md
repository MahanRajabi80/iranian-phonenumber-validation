# صحت سنجی شماره تلفن های ایرانی
همیشه صحت سنجی شماره تلفن ها برای ما برنامه نویسا یکم داستان داشته و خب چون بیشتر ما اصلا خودمون رو درگیر این چیزا نمی کنیم و به این فکر می کنیم که خب فوقش طرف شمارشو اشتباه میزنه دیگه و OTP سایت براش نمیره !!!
و همیشه اینجوری از زیر کار در رفتیم. ولی خب من خودم سر یه پروژه ای نیاز داشتم تا با جزئیات اطلاعات مربوط به هر شماره رو دربیارم. این ریجکس ها فقط __فرمت شماره تلفن__ رو پیدا می کنن نه اینکه آیا این شماره واقعا وجود داره یا نه !  




## چرا ریجکس ؟ 
«عبارت‌های منظم» (Regular Expressions) که اصطلاحاً regex یا regexp نامیده می‌شوند در زمان استخراج اطلاعات از هر متنی کاملاً مفید هستند. این عبارت‌ها برای جستجو و یافتن مطابقت یک یا چند الگوی جستجوی خاص مورد استفاده قرار می‌گیرند. بدین ترتیب می‌توان توالی خالصی از کاراکترهای ASCII یا یونیکد را یافت. زمینه‌های کاربرد regex از اعتبارسنجی تا تجزیه/جایگزینی رشته‌ها، ترجمه داده‌ها به قالب‌های دیگر و وب اسکرپینگ متفاوت است.  

## صحت سنجی با ریجکس
توجه کنید که Match کردن با ریجکس توی هر زبان متفاوته و باید داکیومنت های زبانی که دارین باهاش برنامه مینویسن رو بخونید ولی خب بطور عمده یه چیز و اینکه هر زبان برخی از قوانین ریجکس رو کم و زیاد می کنه. استفاده درست از این ها مربوط میشه به زبانی که میخواید از اینا استفاده کنید. گرچه من نمونه هایی از زبان های `#C` و `Java Script` و `Python` و `Type Script`خواهم گذاشت و یک نمونه هم توی github pages انشالله قرار میگیره 💪  




## اوپراتور های کشوری

### تمام شماره های کشور
```regex
/((09)|(\+98))((14)|(13)|(12)|(19)|(18)|(17)|(15)|(16)|(11)|(10)|(90)|(91)|(92)|(93)|(94)|(95)|(96)|(32)|(30)|(33)|(35)|(36)|(37)|(38)|(39)|(00)|(01)|(02)|(03)|(04)|(05)|(41)|(20)|(21)|(22)|(23)|(31)|(34)|(9910)|(9911)|(9913)|(9914)|(9999)|(999)|(990)|(9810)|(9811)|(9812)|(9813)|(9814)|(9815)|(9816)|(9817)|(998)|(94)).?\d{3}.?\d{4}/g
```  

### شماره های همراه اول
```regex
((09)|(\+98))((14)|(13)|(12)|(19)|(18)|(17)|(15)|(16)|(11)|(10)|(90)|(91)|(92)|(93)|(94)|(95)|(96)).?\d{3}.?\d{4}
```  

### شماره های ایرانسل
```regex
/((09)|(\+98))((32)|(30)|(33)|(35)|(36)|(37)|(38)|(39)|(00)|(01)|(02)|(03)|(04)|(05)|(41)).?\d{3}.?\d{4}/g
``` 

### شماره های رایتل
```regex
/((09)|(\+98))((20)|(21)|(22)|(23)).?\d{3}.?\d{4}/g
```  

## اوپراتور های کوچک یا منطقه ای

### تله کیش (TeleKish)
```regex
/((09)|(\+98))(34).?\d{3}.?\d{4}/g
```  

### شماره های تالیا
```regex
/((09)|(\+98))32.?\d{3}.?\d{4}/g
```  

## اپراتورهای مجازی تلفن همراه

### آپتل (Aptel)
```regex
/((09)|(\+98))((9910)|(9911)|(9913)|(9914)).?\d{3}.?\d{4}/g
```  

### سامانتل (SamanTel)
```regex
/((09)|(\+98))((9999)|(999)).?\d{3}.?\d{4}/g
```  

### شاتل موبایل Shatel Mobile
```regex
/((09)|(\+98))((9810)|(9811)|(9812)|(9813)|(9814)|(9815)|(9816)|(9817)).?\d{3}.?\d{4}/g
```  

### انارستان
```regex
/((09)|(\+98))((94)).?\d{3}.?\d{4}/g
```  


