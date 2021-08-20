---
description: La classe PrivateFontCollection eredita dalla classe di base astratta FontCollection. È possibile usare un oggetto PrivateFontCollection per mantenere un set di tipi di carattere specifici per l'applicazione.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Creazione di raccolte private di tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df673273611ed329e933c84e6540ed984088202590dc1d1c644ccdedca2c80c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977591"
---
# <a name="creating-a-private-font-collection"></a>Creazione di raccolte private di tipi di carattere

La [**classe PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) eredita dalla classe di base astratta [**FontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) È possibile usare un **oggetto PrivateFontCollection** per mantenere un set di tipi di carattere specifici per l'applicazione.

Una raccolta di caratteri privati può includere i tipi di carattere di sistema installati e i tipi di carattere che non sono stati installati nel computer. Per aggiungere un file di tipo di carattere a una raccolta di caratteri privata, chiamare il metodo [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) di un [**oggetto PrivateFontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)

> [!Note]  
> Quando si usa l'API GDI+, non è mai necessario consentire all'applicazione di scaricare tipi di carattere arbitrari da origini non attendibili. Il sistema operativo richiede privilegi elevati per garantire che tutti i tipi di carattere installati siano attendibili.

 

Il [**metodo FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) di un [**oggetto PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) restituisce una matrice [**di oggetti FontFamily.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) Prima di chiamare **FontCollection::GetFamilies,** è necessario allocare un buffer sufficientemente grande da contenere tale matrice. Per determinare le dimensioni del buffer richiesto, chiamare il metodo [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e moltiplicare il valore restituito per **sizeof**(**FontFamily**).

Il numero di famiglie di tipi di carattere in una raccolta di tipi di carattere privata non corrisponde necessariamente al numero di file di tipi di carattere aggiunti alla raccolta. Si supponga, ad esempio, di aggiungere i file ArialBd.tff, Times.tff e TimesBd.tff a una raccolta. Nella raccolta saranno presenti tre file, ma solo due famiglie, perché Times.tff e TimesBd.tff appartengono alla stessa famiglia.

L'esempio seguente aggiunge i tre file del tipo di carattere seguenti a un [**oggetto PrivateFontCollection:**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)

-   C: \\ WINNT \\ Fonts \\ Arial.tff (Arial, regular)
-   C: \\ WINNT \\ Fonts \\ CourBI.tff (Courier New, grassetto corsivo)
-   C: \\ WinNT \\ Fonts \\ TimesBd.tff (Times New Roman, bold)

Il codice chiama il metodo [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) dell'oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) per determinare il numero di famiglie nella raccolta privata e quindi chiama [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) per recuperare una matrice [**di oggetti FontFamily.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)

Per ogni oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) nella raccolta, il codice chiama il metodo [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) per determinare se sono disponibili vari stili (normale, grassetto, corsivo, corsivo grassetto, sottolineatura e barrato). Gli argomenti passati al metodo **FontFamily::IsStyleAvailable** sono membri dell'enumerazione [**FontStyle,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) dichiarata in Gdiplusenums.h.

Se è disponibile una particolare combinazione famiglia/stile, viene costruito un [**oggetto Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) usando la famiglia e lo stile. Il primo argomento passato al costruttore **Font** è il nome della famiglia di caratteri (non un [**oggetto FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) come nel caso di altre varianti del costruttore **Font)** e l'argomento finale è l'indirizzo dell'oggetto [**PrivateFontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) Dopo la **costruzione dell'oggetto** Font, il relativo indirizzo viene passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per visualizzare il nome della famiglia insieme al nome dello stile.


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



Nella figura seguente viene illustrato l'output del codice precedente.

![Screenshot di una finestra in cui sono elencati nove nomi di carattere, ognuno dei quali illustra il tipo di carattere denominato](images/fontstext7.png)

Arial.tff (che è stato aggiunto alla raccolta di caratteri privati nell'esempio di codice precedente) è il file del tipo di carattere per lo stile regolare Arial. Si noti, tuttavia, che l'output del programma mostra diversi stili disponibili diversi da quelli normali per la famiglia di caratteri Arial. Ciò è dovuto Windows GDI+ possibile simulare gli stili grassetto, corsivo e corsivo grassetto dello stile normale. GDI+ possono anche produrre sottolineature e barrati dallo stile normale.

Analogamente, GDI+ può simulare lo stile corsivo grassetto dallo stile grassetto o corsivo. L'output del programma mostra che lo stile corsivo grassetto è disponibile per la famiglia Times anche se TimesBd.tff (Times New Roman, bold) è l'unico file Times nella raccolta.

Questa tabella specifica i tipi di carattere non di sistema supportati GDI+ sistema.



|                     | GDI | GDI+ su Windows 7 | GDI+ su Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . Fon                | sì | no                | no                | no          |
| . Fnt                | sì | no                | no                | no          |
| . Ttf                | sì | sì               | sì               | sì         |
| . OTF con TrueType  | sì | sì               | sì               | sì         |
| . OTF con Adobe CFF | sì | no                | sì               | sì         |
| Adobe Type 1        | sì | no                | no                | no          |



 

 

 



