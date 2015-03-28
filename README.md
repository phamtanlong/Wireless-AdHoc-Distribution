# Wireless-AdHoc-Distribution
[Enlish source: http://gknops.github.io/adHocGenerate]

Khi cần deploy ứng dụng iOS lên nhiều thiết bị của tester, thì thường ta dùng TestFlight của Apple hay Diawi.
TestFlight thì có nhược điểm là cần phải có thời gian review.
Diawi thì có vấn đề là file ipa trên 150M thì sẽ không thể up lên được.
Vậy cần phải có 1 cách nào đó để giải quyết vấn đề này.
Tìm hiểu trên mạng, mình tìm được 1 cách làm một trang web có dịch vụ tương tự Diawi như sau:

Ta cần có 3 file:
1- File HTML
2- File Plist
3- File .IPA

1/ File HTML là trang web chứa đường dẫn để install lên thiết bị.
Cấu trúc file tuỳ ý, chỉ cần có 1 đoạn chứa đường dẫn download như sau:
<a href="itms-services://?action=download-manifest&amp;
    url=http://www.bitart.com/WirelessAdHocDemo/WirelessAdHocDemo.plist">
    click this link to install
</a>

