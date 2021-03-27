---
description: La classe PrivateFontCollection eredita dalla classe base astratta FontCollection. È possibile usare un oggetto PrivateFontCollection per mantenere un set di tipi di carattere specifici per l'applicazione.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Creazione di raccolte private di tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227085"
---
# <a name="creating-a-private-font-collection"></a>Creazione di raccolte private di tipi di carattere

La classe [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) eredita dalla classe base astratta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . È possibile usare un oggetto **PrivateFontCollection** per mantenere un set di tipi di carattere specifici per l'applicazione.

Una raccolta di tipi di carattere privata può includere i tipi di carattere del sistema installato e i tipi di carattere che non sono stati installati nel computer. Per aggiungere un file del tipo di carattere a una raccolta di tipi di carattere privata, chiamare il metodo [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) di un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .

> [!Note]  
> Quando si usa l'API GDI+, non è mai necessario consentire all'applicazione di scaricare tipi di carattere arbitrari da origini non attendibili. Il sistema operativo richiede privilegi elevati per assicurarsi che tutti i tipi di carattere installati siano attendibili.

 

Il metodo [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) di un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) restituisce una matrice di oggetti [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Prima di chiamare **FontCollection:: GetFamilies**, è necessario allocare un buffer sufficientemente grande da mantenere tale matrice. Per determinare le dimensioni del buffer richiesto, chiamare il metodo [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e moltiplicare il valore restituito da **sizeof**(**FontFamily**).

Il numero di famiglie di caratteri in una raccolta di tipi di carattere privata non è necessariamente uguale al numero di file del tipo di carattere aggiunti alla raccolta. Si supponga, ad esempio, di aggiungere i file ArialBd. TFF, Times. tff e TimesBd. TFF a una raccolta. Saranno presenti tre file, ma solo due famiglie della raccolta, poiché Times. tff e TimesBd. tff appartengono alla stessa famiglia.

Nell'esempio seguente vengono aggiunti i tre file del tipo di carattere seguenti a un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :

-   C: \\ WinNT \\ fonts \\ Arial. tff (Arial, Regular)
-   C: \\ WinNT \\ fonts \\ Courbi. tff (Courier New, Bold Italic)
-   C: \\ WinNT \\ fonts \\ TimesBd. tff (Times New Roman, Bold)

Il codice chiama il metodo [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) dell'oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) per determinare il numero di famiglie nella raccolta privata, quindi chiama [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) per recuperare una matrice di oggetti [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .

Per ogni oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) della raccolta, il codice chiama il metodo [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) per determinare se sono disponibili diversi stili (Regular, Bold, Italic, Bold Italic, Underline e Strike). Gli argomenti passati al metodo **FontFamily:: IsStyleAvailable** sono membri dell'enumerazione [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , dichiarata in Gdiplusenums. h.

Se è disponibile una particolare combinazione di famiglia/stile, viene creato un oggetto del [**tipo di carattere**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) usando tale famiglia e stile. Il primo argomento passato al costruttore del **tipo di carattere** è il nome della famiglia di caratteri (non un oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) come nel caso di altre varianti del costruttore del **tipo di carattere** ) e l'argomento finale è l'indirizzo dell'oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) . Dopo la creazione dell'oggetto **font** , il relativo indirizzo viene passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per visualizzare il nome della famiglia insieme al nome dello stile.


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

![Screenshot di una finestra in cui sono elencati nove nomi di caratteri, ognuno dei quali illustra il tipo di carattere denominato](images/fontstext7.png)

Arial. TFF, che è stato aggiunto alla raccolta di tipi di carattere privati nell'esempio di codice precedente, è il file del tipo di carattere per lo stile normale Arial. Si noti, tuttavia, che l'output del programma mostra diversi stili disponibili diversi da Regular per la famiglia di caratteri Arial. Ciò è dovuto al fatto che Windows GDI+ è in grado di simulare gli stili in grassetto, corsivo e corsivo in grassetto dallo stile normale. GDI+ può inoltre produrre sottolineature e strikeouts dallo stile normale.

Analogamente, GDI+ è in grado di simulare lo stile corsivo grassetto dallo stile grassetto o corsivo. L'output del programma mostra che lo stile corsivo in grassetto è disponibile per la famiglia Times anche se TimesBd. tff (Times New Roman, Bold) è l'unico file di volte nella raccolta.

Questa tabella specifica i tipi di carattere non di sistema supportati da GDI+.



|                     | GDI | GDI+ in Windows 7 | GDI+ in Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . FON                | sì | no                | no                | no          |
| . FNT                | sì | no                | no                | no          |
| . TTF                | sì | sì               | sì               | sì         |
| . OTF con TrueType  | sì | sì               | sì               | sì         |
| . OTF con Adobe CFF | sì | no                | sì               | sì         |
| Adobe Type 1        | sì | no                | no                | no          |



 

 

 



