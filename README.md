import segno
qr_text = input("Enter what the qrcode means: ")

while True:
    qr_scale = input("Specify the scale (in numbers) of the QR code: ")
    if qr_scale.isdigit():
        qr_scale = int(qr_scale)
        break
    else:
        print("The scale must be indicated in numbers!")
while True:
    qr_border = input("Specify the border in numbers: ")
    if qr_border.isdigit():
        qr_border = int(qr_border)
        break
    else:
        print("The curb must be indicated in numbers! ")
qr_light = input("Enter a background color name: ")
qr_dark = input("Enter qr color name: ")
qr_zone = input("Enter the border color name: ")



qrcode = segno.make_qr(qr_text)
qrcode.save(f"QR.png",scale=qr_scale,border=qr_border,light=qr_light,dark=qr_dark,quiet_zone=qr_zone)
