# Tasarim-Calismasi
Python dilinde görünüm / tasarım oluşturma kodları.
from tkinter import *

def factor (sayi): # sayi = değer
    sayi=1
    for i in range(2,sayi+1):
          sayi=sayi*i
    return sayi
def hesapla():
    cikis=str(factor(int(giris)))
    cikis.insert(END,())


pencere = Tk()
pencere.geometry("500x400+0+0")  # Formun en - boy ekran ... - ekrana uzaklığı

pencere.title("Merhaba ilk formum")  # Formumuza isism atadığımız kod
pencere.resizable(width=False,height=False) # Formun genişliği ve yüksekliğini ayarlamamızı sağlar.

etiket= Label(text="Merhaba iyi akşamlar",fg="blue",font="Times 15 italic")  # Formun içine yazı yazmamızı sağlar , Label (Etiketin) form içindeki konumuna ayarlar , font yazı tipi
etiket.place(x=10,y=10)  # Nerede yayınlanacağına karar veririz

giris=Entry(borderwidth=20,width=50,insertwidth=3)  # Metin kutusu oluştur , insertwidth imleç sayı girdikçe kalınlaşıyor
giris.place(x=60,y=60)

onay=Checkbutton(text="Merhaba")   # Kutucuk ekler
onay.place(x=60,y=100)

#dugme = Button(text="Giriş",command= pencere.quit, width=7 , height=3) # Buton ekleme  width= genişlik
dugme = Button(text="Giriş",command= hesapla, width=7 , height=3)
dugme.place(x=60,y=100)  # Giriş kutusunu (buttonunu) yerini belirliyor.
dugme.pack()  # Giriş'i ( Button'u) hep ortada tutar.
#dugme.pack(expand=YES)  # Kaymayı engeller
#dugme.grid() # Sol üstten başlatıyor
#dugme.grid(column=20)

cikis=Entry(borderwidth=20,width=50,insertwidth=3)  # Metin kutusu oluştur , insertwidth imleç sayı girdikçe kalınlaşıyor
cikis.place(x=60,y=60)

mainloop()
