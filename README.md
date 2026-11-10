# Việt hóa Batman: Arkham Asylum – Game of the Year Edition

Bản Việt hóa cho **Batman: Arkham Asylum GOTY (bản Steam, tiếng Anh)**.

## Bao gồm

- Toàn bộ menu, hướng dẫn, mục tiêu, hồ sơ nhân vật, câu đố Riddler, mẹo màn hình chờ, phụ đề cắt cảnh (~4.600 dòng văn bản).
- Phụ đề hội thoại trong game (~3.800 câu), gồm lời Joker qua loa, bọn côn đồ, băng ghi âm Spirit of Arkham.
- Font chữ đã được bổ sung đầy đủ dấu tiếng Việt (menu, HUD và phụ đề).

## Yêu cầu

- Batman: Arkham Asylum **Game of the Year Edition** bản **Steam**, ngôn ngữ tiếng Anh, đã cập nhật mới nhất.
- Windows. Không cần cài thêm phần mềm.

> Bản Epic, GOG, bản đĩa hoặc bản thường (không phải GOTY) có thể không khớp. Trình cài đặt sẽ báo lỗi và không sửa file nào nếu phiên bản không đúng.

## Tải về

Tải file **[VietHoa_BatmanAA_v1.0.zip](../../raw/main/VietHoa_BatmanAA_v1.0.zip)** (bấm vào tên file → nút **Download raw file**).

## Cài đặt

1. **Tìm thư mục game:** trong Steam, chuột phải *Batman: Arkham Asylum GOTY* → **Manage** → **Browse local files**.
   Thư mục này có chứa `BmGame` và `Binaries`, thường là:
   `C:\Program Files (x86)\Steam\steamapps\common\Batman Arkham Asylum GOTY`
2. **Giải nén** file zip, rồi chép cả thư mục `VietHoa_BatmanAA` vào **bên trong** thư mục game ở bước 1:
   ```
   Batman Arkham Asylum GOTY\
   ├── Binaries\
   ├── BmGame\
   └── VietHoa_BatmanAA\     <-- chép vào đây
       ├── CAI_DAT.bat
       └── ...
   ```
3. **Tắt game**, mở thư mục `VietHoa_BatmanAA` và chạy **`CAI_DAT.bat`**.
   Nếu game nằm trong `Program Files`, hãy chuột phải → **Run as administrator**.
4. Chờ đến khi hiện **CAI DAT THANH CONG** (khoảng 1–3 phút).
5. Vào game → **Options** → bật **Subtitles** để xem phụ đề tiếng Việt.

## Gỡ cài đặt

Chọn một trong hai cách:

- Chạy `GO_CAI_DAT.bat` trong thư mục `VietHoa_BatmanAA`. File gốc sẽ được chép lại từ thư mục `VietHoa_Backup`.
- Hoặc trong Steam: chuột phải game → **Properties** → **Installed Files** → **Verify integrity of game files**.

## Câu hỏi thường gặp

**Cài xong vẫn là tiếng Anh?** Kiểm tra lại xem thư mục `VietHoa_BatmanAA` có nằm đúng bên trong thư mục game không, và trình cài đặt có báo "Loi: 0 file" không.

**Trình cài đặt báo lỗi một số file?** Phiên bản game không khớp, hoặc file đã bị bản mod khác sửa. Hãy chạy *Verify integrity of game files* trên Steam, xóa thư mục `VietHoa_Backup` trong thư mục game, rồi chạy lại `CAI_DAT.bat`.

**Steam cập nhật game làm mất Việt hóa?** Chạy lại `CAI_DAT.bat`.

**Phát hiện lỗi dịch hoặc lỗi font?** Hãy mở một [Issue](../../issues), ghi rõ vị trí trong game và đính kèm ảnh chụp màn hình.

## Cách hoạt động

Gói này không chứa file game. Nó chỉ chứa các bản vá (`.xdelta`) và các file văn bản tiếng Việt. Khi cài đặt:

1. File gốc được sao lưu vào `VietHoa_Backup`.
2. Bản vá được áp lên file gốc bằng [xdelta3](https://github.com/jmacd/xdelta-gpl). Xdelta tự kiểm tra checksum, nên nếu phiên bản không khớp thì file sẽ không bị sửa.

Danh sách file và mã MD5 (gốc và Việt hóa) nằm trong `md5.txt`.

## Ghi chú

- Đây là dự án phi thương mại do người hâm mộ thực hiện, không liên quan tới Rocksteady Studios, Warner Bros. Games hay DC.
- Bạn cần sở hữu bản quyền game để sử dụng.
- `tools/xdelta3.exe` là xdelta 3.1.0 (GPL v2), mã nguồn tại https://github.com/jmacd/xdelta-gpl.
