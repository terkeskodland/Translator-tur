#pgzero
import random

WIDTH = 600
HEIGHT = 500

TITLE = "Uzay Yolculuğu"
FPS = 0

# Değişkanler ve Nesneler
gemi = Actor("uzaygemisi1")
uzay = Actor("uzayresmi1")
dusmanlar = []
gezegenler = [Actor("gezegen1", (random.randint(0, 600), -100)), Actor("gezegen2", (random.randint(0, 600), -100)), Actor("gezegen3", (random.randint(0, 600), -100))]
meteorlar = []
fuzeler = []
mod = "menü"
uzaygemisi1 = Actor("uzaygemisi1")
uzaygemisi2 = Actor("uzaygemisi2")
uzaygemisi3 = Actor("uzaygemisi3")
uzayresmi1 = Actor("uzayresmi1")
uzayresmi2 = Actor("uzayresmi2")
uzayresmi3 = Actor("uzayresmi3")
puan = 0
puan_carpani = 1
carpi = Actor("çarpı", (27, 27))


# Menü modundaki butonlar
oyna_butonu = Actor("buton", (290, 200))
dukkan_butonu = Actor("buton", (290, 300))
aciklama_butonu = Actor("buton", (290, 400))

# Zorluk seviyesi ayarlama modundaki butonlar
kolay_butonu = Actor("buton", (100, 225))
orta_butonu = Actor("buton", (300, 225))
zor_butonu = Actor("buton", (500, 225))

# Dükkan modundaki butonlar
guclendirmeler_butonu = Actor("buton", (200, 225))
gorunumler_butonu = Actor("buton", (400, 225))

# Güçlendirmeler Modundaki Butonlar
ikilifuzeatma_butonu = Actor("buton", (200, 180))
ikilifuzeatma_siniri = 0
uclufuzeatma_izni = 0
uclufuzeatma_butonu = Actor("buton", (200, 280))
uclufuzeatma_siniri = 0
gucarttirma1_butonu = Actor("buton", (400, 125))
gucarttirma1_siniri = 0
gucarttirma2_izni = 0
gucarttirma2_butonu = Actor("buton", (400, 225))
gucarttirma2_siniri = 0
gucarttirma3_izni = 0
gucarttirma3_butonu = Actor("buton", (400, 325))
gucarttirma3_siniri = 0

# Görünümler modundaki butonlar
uzaygemisi1_butonu = Actor("buton", (200, 100))
anatema1_butonu = Actor("buton", (400, 100))
uzaygemisi2_butonu = Actor("buton", (200, 225 ))
anatema2_butonu = Actor("buton", (400, 225))
uzaygemisi3_butonu = Actor("buton", (200, 350))
anatema3_butonu = Actor("buton", (400, 350))

#kaçlı mermi atılır

yan_fuze = 1
fuze_guc = 1
def doldurma():
    # Düşmanlar listesini oluşturmak
    for i in range(5):
        x = random.randint(0, 600)
        y = random.randint(-450, -50)
        dusman = Actor("düşmanuzaygemisi", (x, y))
        dusman.speed = random.randint(2, 8)
        dusmanlar.append(dusman)
        
    # Meteorlar listesini oluşturmak
    for i in range(5):
        x = random.randint(0, 600)
        y = random.randint(-450, -50)
        meteor = Actor("meteor", (x, y))
        meteor.speed = random.randint(2, 8)
        meteorlar.append(meteor)
doldurma()
# Çizimler
def draw():
    
    # Menü Modu
    if mod == "menü":
        uzay.draw()
        carpi.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        oyna_butonu.draw()
        screen.draw.text("OYNA", center = (290, 200), color = "black", fontsize = 32)
        
        dukkan_butonu.draw()
        screen.draw.text("DÜKKAN", center = (290, 300), color = "black", fontsize = 32)
        
        aciklama_butonu.draw()
        screen.draw.text("AÇIKLAMA", center = (290, 400), color = "black", fontsize = 26)
        
        screen.draw.text("UZAY SAVAŞI", center = (290, 100), color = "white", fontsize = 64)

    # Açıklama Modu
    if mod == "aciklama":
        uzay.draw()
        carpi.draw()
        screen.draw.text("Oyundaki Amacınız Karşınıza Çıkan Uzay Gemilerine", center = (300, 35), color = "white", fontsize = 20)
        screen.draw.text("Farenizin Sol Tuşuna Basarak Füze Göndermek ve Onları", center = (300, 55), color = "white", fontsize = 20)
        screen.draw.text("Patlatmak! Eğer Bir Uzay Gemisi Size Çarparsa Oyun", center = (300, 75), color = "white", fontsize = 20)
        screen.draw.text("Biter ve Tekrar Başlarsınız. Meteorlar ve Diğer Gezegenler", center = (300, 95), color = "white", fontsize = 20)
        screen.draw.text("Size Zarar Vermez. Ne Kadar Çok Gemi Vurursanız O Kadar", center = (300, 115), color = "white", fontsize = 20)
        screen.draw.text("Puan Kazanırsınız. Puanlar Dükkandan Bazı Geliştirmeler", center = (300, 135), color = "white", fontsize = 20)
        screen.draw.text("Alabilmenizi Sağlar. Onları Aldıkça Daha Da Güçlü", center = (300, 155), color = "white", fontsize = 20)
        screen.draw.text("Olursunuz. Ayrıca Dükkandaki Görünümler Kısmından Da", center = (300, 175), color = "white", fontsize = 20)
        screen.draw.text("Uzay Geminize Yeni Bir Görünüş Katabilir veya Uzay", center = (300, 195), color = "white", fontsize = 20)
        screen.draw.text("Temasını Değiştirebilirsiniz. Zevkinize Kalmış!", center = (300, 215), color = "white", fontsize = 20)
        screen.draw.text("Modlar;", center = (300, 265), color = "white", fontsize = 20)
        screen.draw.text("Kolay Oyun Modu: Düşmanlar Daha Yavaş Gelirler", center = (300, 315), color = "white", fontsize = 20)
        screen.draw.text("Fakat Gemi Vurdukça Sadece 1 Puan Kazanırsınız.", center = (300, 335), color = "white", fontsize = 20)
        screen.draw.text("Orta Oyun Modu: Düşmanların Gelişi Hızlanır ve Buna", center = (300, 385), color = "white", fontsize = 20)
        screen.draw.text("Bağlı Olarak Da Gemi Vurdukça 2 Puan Kazanırsınız.", center = (300, 405), color = "white", fontsize = 20)
        screen.draw.text("Zor Oyun Modu: Düşmanlar Çok Hızlı Gelir ve Onları", center = (300, 455), color = "white", fontsize = 20)
        screen.draw.text("Vurmanız Zorlaşır. Fakat Gemi Vurdukça 4 Puan Kazanırsınız!", center = (300, 475), color = "white", fontsize = 20)
        screen.draw.text("İYİ EĞLENCELER !", center = (300, 525), color = "white", fontsize = 20)


    # Zorluk Seviyesi Ayarlama Modu
    if mod == "zorluk":
        uzay.draw()
        carpi.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        kolay_butonu.draw()
        screen.draw.text("KOLAY", center = (100, 225), color = "black", fontsize = 32)
        
        orta_butonu.draw()
        screen.draw.text("ORTA", center = (300, 225), color = "black", fontsize = 32)
        
        zor_butonu.draw()
        screen.draw.text("ZOR", center = (500, 225), color = "black", fontsize = 32)
    
    # Kolay Oyun Modu
    if mod == "kolay_mod":
        uzay.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        for i in gezegenler:
            i.draw()
            
        for i in meteorlar:
            i.draw()
            
        for i in dusmanlar:
            i.draw()
            
        for i in fuzeler:
            i.draw()
            
        
        gemi.draw()   
        
    # Orta Oyun Modu
    if mod == "orta_mod":
        uzay.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        for i in gezegenler:
            i.draw()
        
        for i in meteorlar:
            i.draw()
            
        for i in dusmanlar:
            i.draw()
        
            
        for i in fuzeler:
            i.draw()
            
        
            
        gemi.draw()
    # Zor Oyun Modu
    if mod == "zor_mod":
        uzay.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        
        for i in gezegenler:
            i.draw()
            
        for i in meteorlar:
            i.draw()
        
        for i in dusmanlar:
            i.draw()
            
        for i in fuzeler:
            i.draw()
            
        
        
        gemi.draw()
    # Dükkan Modu    
    if mod == "dükkan":
        uzay.draw()
        carpi.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        guclendirmeler_butonu.draw()
        screen.draw.text("Güçlendirmeler", center = (200, 225), color = "black", fontsize = 22)
        
        gorunumler_butonu.draw()
        screen.draw.text("Görünümler", center = (400, 225), color = "black", fontsize = 22)
        
    # Güçlendirmeler Modu
    if mod == "güçlendirmeler":
        uzay.draw()
        carpi.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        ikilifuzeatma_butonu.draw()
        screen.draw.text("İkili Füze Atma", center = (200, 165), color = "black", fontsize = 22)
        screen.draw.text("50 Puan", center = (200, 195), color = "black", fontsize = 22)
        
        uclufuzeatma_butonu.draw()
        screen.draw.text("Üçlü Füze Atma", center = (200, 265), color = "black", fontsize = 22)
        screen.draw.text("150 Puan", center = (200, 295), color = "black", fontsize = 22)
        
        gucarttirma1_butonu.draw()
        screen.draw.text("Güç Arttırma 1", center = (400, 110), color = "black", fontsize = 22)
        screen.draw.text("25 Puan", center = (400, 140), color = "black", fontsize = 22)
        
        gucarttirma2_butonu.draw()
        screen.draw.text("Güç Arttırma 2", center = (400, 210), color = "black", fontsize = 22)
        screen.draw.text("75 Puan", center = (400, 240), color = "black", fontsize = 22)
        
        gucarttirma3_butonu.draw()
        screen.draw.text("Güç Arttırma 3", center = (400, 310), color = "black", fontsize = 22)
        screen.draw.text("125 Puan", center = (400, 340), color = "black", fontsize = 22)
        
        screen.draw.text("(Not: Güçlendirmeleri Sırayla Almak Zorundasınız)", center = (300, 410), color = "white", fontsize = 22)
        
    # Görünümler Modu
    if mod == "görünümler":
        uzay.draw()
        carpi.draw()
        screen.draw.text(puan, (557, 10), color = "white")
        
        uzaygemisi1_butonu.draw()
        screen.draw.text("Uzay Gemisi1", center = (200, 100), color = "black", fontsize = 23)
        
        anatema1_butonu.draw()
        screen.draw.text("Ana Tema 1", center = (400, 100), color = "black", fontsize = 23)
        
        uzaygemisi2_butonu.draw()
        screen.draw.text("Uzay Gemisi2", center = (200, 225), color = "black", fontsize = 23)
        
        anatema2_butonu.draw()
        screen.draw.text("Ana Tema 2", center = (400, 225), color = "black", fontsize = 23)
        
        uzaygemisi3_butonu.draw()
        screen.draw.text("Uzay Gemisi3", center = (200, 350), color = "black", fontsize = 23)
        
        anatema3_butonu.draw()
        screen.draw.text("Ana Tema 3", center = (400, 350), color = "black", fontsize = 23)
    
    # Oyun Sonu Modu
    elif mod == 'son':
        uzay.draw()
        screen.draw.text("OYUN BİTTİ!", center = (300, 175), color = "white", fontsize = 36)
        screen.draw.text("Devam Etmek İçin Boşluk Tuşuna Bas", center = (300, 225), color = "red", fontsize = 18)
        screen.draw.text(puan, center = (300, 275), color = "white", fontsize = 64)
    
# Kontroller
def on_mouse_move(pos):
    gemi.pos = pos

# Yeni Düşmanların Eklenmesi
def yeni_dusman(zorluk):
    x = random.randint(0, 400)
    y = -50
    dusman = Actor("düşmanuzaygemisi", (x, y))
    if zorluk == "kolay":
        dusman.speed = random.randint(2, 8)
    elif zorluk == "orta":
        dusman.speed = random.randint(7, 15)
    elif zorluk == "zor":
        dusman.speed = random.randint(11, 20)
    dusmanlar.append(dusman)

# Düşmanların Hareketleri
def dusman_gemisi():
    global mod
    for i in range(len(dusmanlar)):
        if dusmanlar[i].y < 650:
            dusmanlar[i].y = dusmanlar[i].y + dusmanlar[i].speed
        else:
            dusmanlar.pop(i)
            if mod == "kolay_mod":
                yeni_dusman("kolay")
            
            elif mod == "orta_mod":
                yeni_dusman("orta")
                
            elif mod == "zor_mod":
                yeni_dusman("zor")

# Gezegenlerin Hareketleri
def gezegen():
    if gezegenler[0].y < 850:
            gezegenler[0].y = gezegenler[0].y + 1
    else:
        gezegenler[0].y = -100
        gezegenler[0].x = random.randint(0, 600)
        birinci = gezegenler.pop(0)
        gezegenler.append(birinci)

# Meteorların Hareketleri
def meteorlar_hareket():
    for i in range(len(meteorlar)):
        if meteorlar[i].y < 850:
            meteorlar[i].y = meteorlar[i].y + meteorlar[i].speed
        else:
            meteorlar[i].x = random.randint(0, 600)
            meteorlar[i].y = -20
            meteorlar[i].speed = random.randint(2, 10)

# Çarpışmalar
def carpismalar():
    global mod
    global puan
    for i in range(len(dusmanlar)):
        if gemi.colliderect(dusmanlar[i]):
            mod = "son"
            
        # Füzelerin Çarpışması
        for j in range(len(fuzeler)):
            if fuzeler[j].colliderect(dusmanlar[i]):
                puan = puan + puan_carpani
                dusmanlar.pop(i)
                fuzeler[j].can -= 1
                if fuzeler[j].can == 0:
                    fuzeler.pop(j)
                if mod == "kolay_mod":
                    yeni_dusman("kolay")
                elif mod == "orta_mod":
                    yeni_dusman("orta")
                elif mod == "zor_mod":
                    yeni_dusman("zor")
                break
            
def kolayoyunmodu():
    
    dusman_gemisi()
    carpismalar()
    gezegen()
    meteorlar_hareket()
    
    # Füzelerin Hareketleri
    for i in range(len(fuzeler)):
        if fuzeler[i].y < 0:
            fuzeler.pop(i)
            break
        else:
            fuzeler[i].y = fuzeler[i].y - 10
            
def normaloyunmodu():
    dusman_gemisi()
    carpismalar()
    gezegen()
    meteorlar_hareket()
    
    # Füzelerin Hareketleri
    for i in range(len(fuzeler)):
        if fuzeler[i].y < 0:
            fuzeler.pop(i)
            break
        else:
            fuzeler[i].y = fuzeler[i].y - 10
                
def zoroyunmodu():
    dusman_gemisi()
    carpismalar()
    gezegen()
    meteorlar_hareket()
    
    # Füzelerin Hareketleri
    for i in range(len(fuzeler)):
        if fuzeler[i].y < 0:
            fuzeler.pop(i)
            break
        else:
            fuzeler[i].y = fuzeler[i].y - 10 
                
def update(dt):
    global puan, mod, dusmanlar, gezegenler, meteorlar, fuzeler
    
    if mod == "kolay_mod":
        kolayoyunmodu()
        
    elif mod == "orta_mod":
        normaloyunmodu()
        
    elif mod == "zor_mod":
        zoroyunmodu()
        
    if mod == 'son' and keyboard.space:
        mod = 'menü'
        dusmanlar = []
        gezegenler = [Actor("gezegen1", (random.randint(0, 600), -100)), Actor("gezegen2", (random.randint(0, 600), -100)), Actor("gezegen3", (random.randint(0, 600), -100))   ]
        meteorlar = []
        fuzeler = []
        doldurma()
        

    
        
def on_mouse_down(button, pos):
    global puan
    global mod
    global uclufuzeatma_izni
    global gucarttirma2_izni
    global gucarttirma3_izni
    global ikilifuzeatma_siniri
    global uclufuzeatma_siniri
    global gucarttirma1_siniri
    global gucarttirma2_siniri
    global gucarttirma3_siniri
    global gemi
    global uzay
    global yan_fuze
    global fuze_guc
    global puan_carpani
    
    
# Menü Modu
    if button == mouse.LEFT and mod != "menü":
        if carpi.collidepoint(pos):
            mod = "menü"

# Zorluk Modu
    if button == mouse.LEFT and mod == "menü":
        if oyna_butonu.collidepoint(pos):
            mod = "zorluk"
   
# Zorluk Modu > Kolay Oyun Modu
    elif button == mouse.LEFT and mod == "zorluk":
        if kolay_butonu.collidepoint(pos):
            mod = "kolay_mod"
            puan_carpani = 1

# Zorluk Modu > Orta Oyun Modu
    
        elif orta_butonu.collidepoint(pos):
            mod = "orta_mod"
            puan_carpani = 2
# Zorluk Modu > Zor Oyun Modu
    
        elif zor_butonu.collidepoint(pos):
            mod = "zor_mod"
            puan_carpani = 4
# Dükkan Modu            
    if button == mouse.LEFT and mod == "menü":
        if dukkan_butonu.collidepoint(pos):
            mod = "dükkan"
            
# Güçlendirmeler Modu            
    if button == mouse.LEFT and mod == "dükkan":
        if guclendirmeler_butonu.collidepoint(pos):
            mod = "güçlendirmeler"
            
            
# Güçlendirmeler Modu > İkili Füze Atma Butonu            
    if button == mouse.LEFT and mod == "güçlendirmeler":
        if ikilifuzeatma_butonu.collidepoint(pos) and puan >= 50 and ikilifuzeatma_siniri != 1:
            puan = puan - 50
            uclufuzeatma_izni = 1
            ikilifuzeatma_siniri = 1
            yan_fuze = 2
            

# Güçlendirmeler Modu > Üçlü Füze Atma Butonu    
    if button == mouse.LEFT and mod == "güçlendirmeler" and uclufuzeatma_izni == 1 and uclufuzeatma_siniri != 1:
        if uclufuzeatma_butonu.collidepoint(pos) and puan >= 150:
            puan = puan - 150
            uclufuzeatma_siniri = 1
            yan_fuze = 3
            
            
# Güçlendirmeler Modu > Güç Arttırma 1 Butonu
    if button == mouse.LEFT and mod == "güçlendirmeler":
        if gucarttirma1_butonu.collidepoint(pos) and puan >= 25 and gucarttirma1_siniri != 1:
            puan = puan - 25
            gucarttirma2_izni = 1
            gucarttirma1_siniri = 1
            fuze_guc = 2
            
            
# Güçlendirmeler Modu > Güç Arttırma 2 Butonu
    if button == mouse.LEFT and mod == "güçlendirmeler" and gucarttirma2_izni == 1 and gucarttirma2_siniri != 1:
        if gucarttirma2_butonu.collidepoint(pos) and puan >= 75:
            puan = puan - 75
            gucarttirma3_izni = 1
            gucarttirma2_siniri = 1 
            fuze_guc = 3
            
            
# Güçlendirmeler Modu > Güç Arttırma 3 Butonu
    if button == mouse.LEFT and mod == "güçlendirmeler" and gucarttirma3_izni == 1 and gucarttirma3_siniri != 1:
        if gucarttirma3_butonu.collidepoint(pos) and puan >= 125:
            puan = puan - 125
            gucarttirma3_siniri = 1
            fuze_guc = 4
            
# Görünümler Modu
    if button == mouse.LEFT and mod == "dükkan":
        if gorunumler_butonu.collidepoint(pos):
            mod = "görünümler"


# Görünümler Modu > Uzay Gemisi 1 Butonu
    elif button == mouse.LEFT and mod == "görünümler":
        if uzaygemisi1_butonu.collidepoint(pos):
            gemi = uzaygemisi1
            
# Görünümler Modu > Uzay Gemisi 2 Butonu
    
        elif uzaygemisi2_butonu.collidepoint(pos):
            gemi = uzaygemisi2
            
# Görünümler Modu > Uzay Gemisi 3 Butonu
    
        elif uzaygemisi3_butonu.collidepoint(pos):
            gemi = uzaygemisi3
            
# Görünümler Modu > Ana Tema 1 Butonu
    
        elif anatema1_butonu.collidepoint(pos):
            uzay.image  = "uzayresmi1"
            
# Görünümler Modu > Ana Tema 2 Butonu
    
        elif anatema2_butonu.collidepoint(pos):
            uzay.image = "uzayresmi2"
            
# Görünümler Modu > Ana Tema 3 Butonu
    
        elif anatema3_butonu.collidepoint(pos):
            uzay.image = "uzayresmi3"
            
# Açıklama Modu
    if button == mouse.LEFT and mod == "menü":
        if aciklama_butonu.collidepoint(pos):
            mod = "aciklama"
            
    # Ateş Etmek
    elif (mod == 'kolay_mod' or mod == "orta_mod" or mod == "zor_mod") and button == mouse.LEFT:
        
        if yan_fuze == 1:
            fuze = Actor("füze1")
            if fuze_guc == 1:
                fuze.can = 1
            elif fuze_guc == 2:
                fuze.can = 2
                
            elif fuze_guc == 3:
                fuze.can = 3
                
            elif fuze_guc == 4:
                fuze.can = 4
            
            fuze.pos = gemi.pos
            fuzeler.append(fuze)
        elif yan_fuze == 2:
            
            
            
            if fuze_guc == 1:
                fuze1 = Actor("füze1")
                fuze2 = Actor("füze1")
                fuze1.can = 1
                fuze2.can = 1
                
            elif fuze_guc == 2:
                fuze1 = Actor("füze1")
                fuze2 = Actor("füze1")
                fuze1.can = 2
                fuze2.can = 2
                
            elif fuze_guc == 3:
                fuze1 = Actor("füze2")
                fuze2 = Actor("füze2")
                fuze1.can = 3
                fuze2.can = 3
            
            elif fuze_guc == 4:
                fuze1 = Actor("füze3")
                fuze2 = Actor("füze3")
                fuze1.can = 4
                fuze2.can = 4
            
                
            fuze1.pos = gemi.pos
            fuze2.pos = gemi.pos
            fuze1.x -= 10
            fuze2.x += 10
            
            fuzeler.append(fuze1)
            fuzeler.append(fuze2)
            
        elif yan_fuze == 3:
            
            
            if fuze_guc == 1:
                fuze1 = Actor("füze1")
                fuze2 = Actor("füze1")
                fuze3 = Actor("füze1")
                fuze1.can = 1
                fuze2.can = 1
                fuze3.can = 1
                
            elif fuze_guc == 2:
                fuze1 = Actor("füze1")
                fuze2 = Actor("füze1")
                fuze3 = Actor("füze1")
                fuze1.can = 2
                fuze2.can = 2
                fuze3.can = 2
                
            elif fuze_guc == 3:
                fuze1 = Actor("füze2")
                fuze2 = Actor("füze2")
                fuze3 = Actor("füze2")
                fuze1.can = 3
                fuze2.can = 3
                fuze3.can = 3
                
            elif fuze_guc == 4:
                fuze1 = Actor("füze3")
                fuze2 = Actor("füze3")
                fuze3 = Actor("füze3")
                fuze1.can = 4
                fuze2.can = 4
                fuze3.can = 4
                
            fuze1.pos = gemi.pos
            fuze2.pos = gemi.pos
            fuze3.pos = gemi.pos
            
            fuze1.x -= 15
            fuze3.x += 15
            
            fuzeler.append(fuze1)
            fuzeler.append(fuze2)
            fuzeler.append(fuze3)
        
# HAZIRLAYAN : ASRIN EFE TERKEŞ






