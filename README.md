# پرداخت‌یاری

## کتابخانه ها و مستندات مربوط به روال **پرداخت‌یاری شاپرک** - طبق [مستندات رسمی شاپرک](https://shaparak.ir/tips/%D9%85%D8%B3%D8%AA%D9%86%D8%AF%D8%A7%D8%AA)

این مخزن برای ارائه کتابخانه پرداخت‌یاری شاپرک طبق مستندات رسمی این شرکت به زبان سی شارپ و پلت فرم دات نت ایجاد شده است. در اینجا شما می‌توانید مدل ها، کلاس ها و مستندات مربوط به وب سرویس شاپرک را پیدا کنید. کُدهای ارائه شده در این مخزن طبق [مستندات رسمی شاپرک که در وب سایت این شرکت در دسترس عموم قرار گرفته](https://shaparak.ir/tips/%D9%85%D8%B3%D8%AA%D9%86%D8%AF%D8%A7%D8%AA)، نوشته شده و به جز این مورد، **هیچ ارتباطی بین این مخزن و شرکت شاپرک وجود ندارد.**

<p dir="rtl" align="right">
هدف از ایجاد این مخزن، سهولت استفاده توسعه دهندگان دات نت از وب سرویس های ایجاد شده توسط شرکت شاپرک برای انجام روال های پرداخت‌یاری و ارائه راهنمایی های لازم برای انجام آزمون‌های شرکت شاپرک، دریافت مجوز پرداخت‌یاری و استفاده از این سرویس ها در اپلیکیشن های عملیاتی است.
  </p>

# نحوه استفاده
<p dir="rtl" align="right">
آخرین نسخه از این کتابخانه روی .NET Standard 2.1 کامپایل شده و از طریق نیوگت میتوانید آن را نصب کنید.
</p>

`Install-Package Shaparak.PaymentFacilitation`

<p dir="rtl" align="right">
بعد از نصب پکیج کافیست در فایل Startup سرویس مربوط به پرداخت یاری را اضافه نمایید.
 </p>

`services.AddPaymentFacilitation(options => {
options.BaseUrl = "https://mms.shaparak.ir/merchant";
options.Username = "username";
options.Password = "password";
});`
<p dir="rtl" align="right">
تنظیمات مربوط به سرویس را میتونید از appsetting در یک section بخوانید
</p>

`services.AddPaymentFacilitation(options => Configuration.GetSection("shaparak").Bind(options));`

# اطلاعات بیشتر
<p dir="rtl" align="right">
برای کسب اطلاعات بیشتر می تونید این مقاله رو بخونید. در [این مقاله](https://virgool.io/@imun/pardakhtyari-nnnvvxpnyyay) من کامل در مورد روال پرداخت‌یاری و چگونگی انجام تست اند-تو-اند شرکت شاپرک توضیح دادم.
اگر به زبان های دیگه مسلط هستید، می تونید با مطالعه سورس کد، معادل این کتابخانه را به زبان های دیگه برای پلت فرم های مختلف بنویسید. اگر این کارو انجام دادید به من اطلاع بدین تا لینک پروژه تون رار مقاله ام بذارم.
 </p>
