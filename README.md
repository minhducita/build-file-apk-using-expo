# Build file apk using Expo
Bình thường, với IOS, bạn phải tải có Xcode mới build được app, sau đó có thể build ra file .ipa hoặc dùng Xcode/Application Loader push thẳng app lên ItunesConnect để submit app.

Android thì dễ hơn chỉ cần build ra file .apk là được.

Với Expo, bạn chỉ cần chạy vài command line là có thể build được dễ dàng.

### Bước 1: Login vào tài khoản Expo của bạn

- **Chạy câu lệnh sau**: 

```sh
expo login -u [user] -p [password]
```
### Bước 2: Sau khi login thành công bạn chạy lệnh sau để tiên hành buld file apk

```sh
expo build:ios
expo build:android
```

Với IOS thì Expo tự tạo certificates and provisioning profiles cho bạn luôn. Đương nhiên phải nhập Apple developer account rồi.

Mọi việc diễn ra tự động, bạn ngồi đợi một xíu là có file để submit lên store rồi.

Điều này sẽ rất hữu ích vì một số bạn không có máy Mac hoặc không quen với việc build app từ Xcode. Nhất là khi bạn mới chuyển từ web qua

Cập nhật app Over the Air (OTA)
Ví dụ bạn muốn chỉnh sửa vài thứ nhỏ nhặt trong app như đổi tên placeholder của text filed, đổi text trong welcome screen thì cũng phải build ra phiên bản mới rồi upload lên store lại, rồi phải đợi người ta duyệt mới cập nhật được( Với Apple Store thôi nha ), như vậy rất mất công và tốn thời gian.

Khi deploy ứng dụng React Native với Expo, mọi chuyện dễ dàng hơn. Bạn chỉ cần sửa code và nhấn nút publish là xong. Khi người dùng mở ứng dụng lên, nó sẽ tự động cập nhật thay đổi mới nhất từ bạn.

Tính năng này như CodePush của Microsoft nhưng dùng Expo thì không cần cài đặt gì cả.
