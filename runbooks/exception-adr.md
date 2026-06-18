
# Exception ADR: CVE Vendor Unfix Exception

## Ngày: 2026-06-19

## Trạng thái: Active

## Hết hạn: 2026-09-17

## Bối cảnh

Một số CVE HIGH/CRITICAL trong base image chưa được vendor fix.

Block mãi sẽ làm gián đoạn delivery.

## Quyết định

Cho phép deploy image có CVE chưa fix với điều kiện:

- CVE được ghi nhận và theo dõi

- Có kế hoạch update khi vendor release fix

- Exception có thời hạn 90 ngày

## Rủi ro

- Exposure với CVE đã biết trong thời gian chờ fix

## Hành động

- Review lại sau 90 ngày hoặc khi vendor có fix

