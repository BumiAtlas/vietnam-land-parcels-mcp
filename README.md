# Vietnam Land Parcels & Zoning MCP (Thửa đất và quy hoạch)

[Tiếng Việt](#tiếng-việt)

Connect your AI assistant to [BumiAtlas](https://bumiatlas.com) for Vietnamese land research through the Model Context Protocol.

This listing is a focused entry point for:

- Land parcels (thửa đất) nationwide: parcel code (mã thửa đất), map sheet (tờ bản đồ) and parcel number (thửa), cadastral land-use codes with English names, stated and mapped area, and boundary
- Lookups the way a land-use certificate (sổ đỏ / sổ hồng) writes them: *"tờ 32 thửa 91, Hương Sơn"*, by commune, district or province, old or new names, with or without diacritics
- Both the new administrative units (after the July 2025 merger: 34 provinces, communes, no districts) and the old commune, district and province that older certificates use
- Planning zones (quy hoạch) in Ho Chi Minh City and Đà Nẵng: general, zoning and detailed plans, with land use and, in HCMC, building density, floor area ratio, floors and height
- The zoning over a parcel, with each zone's share of it
- Map images of a parcel and its neighbours on satellite or street maps, each parcel labelled with its number

Not every parcel is covered: the data is what the source portals publish. There are no owners, certificate numbers or prices.

## Connect

```
https://bumiatlas.com/mcp/vietnam
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/vietnam](https://bumiatlas.com/mcp-docs/vietnam).

## Tools

| Tool | Description |
|---|---|
| `VN_parcel_search` | Parcels by code (104890320091), sheet and parcel number with a place (`tờ 32 thửa 91 Hương Sơn`), or at `latitude, longitude` |
| `VN_parcel_get` | One parcel: land use, area, new and old address, and the planning zones covering it; boundary as GeoJSON |
| `VN_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its number |
| `VN_zoning_get` | Planning zones at a point in HCMC or Đà Nẵng, or by id: plan level, land use, and HCMC's density, FAR, floors and height limits |

## By city

**Ho Chi Minh City (TP. Hồ Chí Minh).** Parcels plus zoning plans (quy hoạch phân khu) with building rules per block: coverage, FAR, floors and height.

- *"What is the zoning at 10.7769, 106.7009 in District 1? What FAR and height are allowed?"*
- *"Find tờ 14 thửa 5, Bến Nghé, Quận 1 and tell me its land use."*

**Hà Nội.** Parcels with land use and both the new ward and the old district address.

- *"Which parcel is at 21.0285, 105.8542 near Hoàn Kiếm Lake, and what is it used for?"*
- *"Look up tờ 30 thửa 3, Lý Thái Tổ, Hoàn Kiếm."*

**Đà Nẵng.** Parcels from the city's planning portal, plus its general, zoning and detailed (1/500) plans.

- *"Which planning zones cover the parcel at 16.0544, 108.2022? Is there a detailed plan?"*
- *"Show me a satellite image of this parcel in Hải Châu with its neighbours labelled."*

**Other cities.** Parcels with land use, area and both addresses. Old place names still work, so a Vũng Tàu or Thủ Dầu Một certificate can be looked up as written, though both are now part of Ho Chi Minh City.

- *"Find tờ 15 thửa 21, Thắng Tam, Vũng Tàu. What is its land use and area?"*
- *"Which parcel is at 10.9804, 106.6519 in Thủ Dầu Một, Bình Dương?"*
- *"What is the land use of the parcel at 12.2388, 109.1967 in Nha Trang?"*
- *"How big is the parcel at 10.2270, 103.9640 on Phú Quốc, and what is it used for?"*
- *"Is the parcel at 10.0452, 105.7469 in Cần Thơ rice land or residential?"*
- *"Find thửa 208 tờ 2 in Hàng Kênh, Lê Chân, Hải Phòng. How big is it?"*

## Coverage

Provinces by their pre-2025 names, which searches accept as well as the new ones.

**Most communes covered**

- South: Ho Chi Minh City, Bình Dương, Bà Rịa–Vũng Tàu, Đồng Nai, Bình Phước, Long An, Tây Ninh, Tiền Giang, Đồng Tháp, Bến Tre, Vĩnh Long, Hậu Giang, Bạc Liêu
- Central coast and Highlands: Đà Nẵng, Quảng Bình, Quảng Ngãi, Bình Định, Phú Yên, Khánh Hòa, Bình Thuận, Đắk Lắk, Lâm Đồng
- North: Hà Nội, Bắc Ninh, Bắc Giang, Bắc Kạn

**Partly covered:** Cần Thơ, Cà Mau, An Giang, Kiên Giang (Phú Quốc), Trà Vinh, Huế, Quảng Nam, Gia Lai, Kon Tum, Đắk Nông, Hà Tĩnh, Nghệ An, Thanh Hóa, Hải Phòng, Thái Bình, Hòa Bình, Phú Thọ, Cao Bằng, Lạng Sơn

**Little or none yet:** Quảng Ninh, Hải Dương, Hưng Yên, Hà Nam, Nam Định, Ninh Bình, Vĩnh Phúc, Thái Nguyên, Tuyên Quang, Hà Giang, Lào Cai, Yên Bái, Sơn La, Điện Biên, Lai Châu, Quảng Trị, Ninh Thuận, Sóc Trăng

## Compared with Vietnamese land apps

If you check plots with Meey Map or batdongsan.com.vn's *Soi quy hoạch*, or on official portals such as Ho Chi Minh City's Thông tin quy hoạch (TTQH), Hà Nội's planning map or Đà Nẵng's construction planning portal, this covers the same kind of lookup for an AI assistant. You can look up a tờ/thửa from a sổ đỏ, read its land-use code, and check the plan at a point (tra cứu quy hoạch, check quy hoạch). Ask in plain language, and the assistant runs the searches, explains codes like ODT, CLN or LUC, and compares neighbouring parcels.

What it doesn't have: road-widening lines (lộ giới), prices, owners, or a check that a certificate is genuine. Zoning is loaded for Ho Chi Minh City and Đà Nẵng only. BumiAtlas is not affiliated with any of these apps or portals.

## Data sources

Parcels from Vietnamese provincial land and planning portals (such as Đà Nẵng's and Cần Thơ's) and guland.vn; each parcel names the site it came from. Zoning © Sở Xây dựng Đà Nẵng and Ho Chi Minh City's planning portal (quyhoach.hochiminhcity.gov.vn).

## Tiếng Việt

Kết nối trợ lý AI của bạn với [BumiAtlas](https://bumiatlas.com) để tra cứu thông tin đất đai tại Việt Nam qua Model Context Protocol (MCP).

- Thửa đất trên cả nước: mã thửa đất, số tờ bản đồ và số thửa, mục đích sử dụng đất (ODT, ONT, LUC, CLN…), diện tích và ranh giới thửa
- Tra cứu theo cách ghi trên sổ đỏ, sổ hồng: *"tờ 32 thửa 91, Hương Sơn"*, theo xã, phường, huyện hoặc tỉnh, tên cũ hay tên mới, có dấu hoặc không dấu
- Địa chỉ theo đơn vị hành chính mới (sau sáp nhập tháng 7/2025) và địa chỉ cũ (xã, huyện, tỉnh) như trên các giấy chứng nhận trước đây
- Quy hoạch tại TP. Hồ Chí Minh và Đà Nẵng: quy hoạch chung, phân khu và chi tiết; tại TP. Hồ Chí Minh có mật độ xây dựng, hệ số sử dụng đất, tầng cao và chiều cao
- Ảnh vệ tinh hoặc bản đồ của thửa đất và các thửa lân cận, có ghi số thửa

Dữ liệu là những gì các cổng thông tin công bố, nên chưa có đủ mọi thửa đất. Phủ gần hết các xã, phường tại TP. Hồ Chí Minh, Bình Dương, Bà Rịa – Vũng Tàu, Đồng Nai, Bình Phước, Long An, Tây Ninh, Tiền Giang, Đồng Tháp, Bến Tre, Vĩnh Long, Hậu Giang, Bạc Liêu, Đà Nẵng, Quảng Bình, Quảng Ngãi, Bình Định, Phú Yên, Khánh Hòa, Bình Thuận, Đắk Lắk, Lâm Đồng, Hà Nội, Bắc Ninh, Bắc Giang và Bắc Kạn (tên tỉnh trước sáp nhập); một phần tại nhiều tỉnh khác. Không có tên chủ sở hữu, số giấy chứng nhận hay giá đất.

**Tra cứu quy hoạch bằng AI.** Nếu bạn quen check quy hoạch, soi quy hoạch hay tra cứu thửa đất online trên Meey Map, Soi quy hoạch của batdongsan.com.vn, ứng dụng Thông tin quy hoạch (TTQH) TP. Hồ Chí Minh, bản đồ quy hoạch Hà Nội hay cổng thông tin quy hoạch Đà Nẵng, thì đây là cách tra cứu tương tự qua trợ lý AI. Bạn có thể tra cứu tờ thửa theo sổ đỏ, sổ hồng, xem bản đồ địa chính, ký hiệu loại đất và quy hoạch sử dụng đất tại một vị trí. Chỉ cần hỏi bằng lời thường: trợ lý tự tìm, giải thích ký hiệu (ODT, CLN, LUC…) và so sánh với các thửa xung quanh.

Chưa có lộ giới, giá đất hay tên chủ sở hữu, và không kiểm tra được sổ đỏ thật hay giả. Quy hoạch mới có tại TP. Hồ Chí Minh và Đà Nẵng. BumiAtlas không liên kết với các ứng dụng, cổng thông tin nói trên.

**Kết nối:** thêm `https://bumiatlas.com/mcp/vietnam` làm custom connector trong ứng dụng hỗ trợ MCP và đăng nhập bằng Google. Trợ lý có thể trả lời bằng tiếng Việt, dù tên công cụ bằng tiếng Anh.

Ví dụ câu hỏi:

- *"Quy hoạch tại 10.7769, 106.7009 ở Quận 1 là gì? Hệ số sử dụng đất và chiều cao tối đa bao nhiêu?"*
- *"Tìm tờ 30 thửa 3, phường Lý Thái Tổ, Hoàn Kiếm, Hà Nội."*
- *"Thửa đất tại 16.0544, 108.2022 ở Đà Nẵng nằm trong những khu quy hoạch nào?"*
- *"Tìm tờ 15 thửa 21, phường Thắng Tam, Vũng Tàu."*
- *"Thửa đất tại 12.2388, 109.1967 ở Nha Trang có mục đích sử dụng gì?"*
- *"Thửa đất tại 10.0452, 105.7469 ở Cần Thơ là đất lúa hay đất ở?"*
