---
description: 'La classe FontFamily fornisce i metodi seguenti che recuperano varie metriche per una particolare combinazione famiglia/stile:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Recupero della metrica dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049469"
---
# <a name="obtaining-font-metrics"></a>Recupero della metrica dei tipi di carattere

La classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fornisce i metodi seguenti che recuperano varie metriche per una particolare combinazione famiglia/stile:

-   [**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

I numeri restituiti da questi metodi sono in unità di progettazione dei tipi di carattere, quindi sono indipendenti dalle dimensioni e dalle unità di un particolare oggetto [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .

Nella figura seguente vengono mostrati i valori di ascesa, discesa e interlinea.

![diagramma di due caratteri nelle righe adiacenti, che mostra l'ascesa delle celle, la discesa della cella e l'interlinea](images/fontstext7a.png)

Nell'esempio seguente vengono visualizzate le metriche per lo stile regolare della famiglia di caratteri Arial. Il codice crea anche un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basato sulla famiglia Arial) con dimensioni pari a 16 pixel e visualizza le metriche (in pixel) per quel particolare oggetto **tipo di carattere** .


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



Nella figura seguente viene illustrato l'output del codice precedente.

![Screenshot di una finestra con testo che indica le dimensioni e l'altezza del carattere e l'ascesa, la discesa e l'interlinea](images/fontstext8.png)

Prendere nota delle prime due righe di output nell'illustrazione precedente. L'oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) restituisce una dimensione di 16 e l'oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) restituisce un'altezza em di 2.048. Questi due numeri (16 e 2.048) rappresentano la chiave per la conversione tra le unità di progettazione dei tipi di carattere e le unità (in questo caso pixel) dell'oggetto **tipo di carattere** .

Ad esempio, è possibile convertire l'ascesa da unità di progettazione a pixel come indicato di seguito:

![equazione che moltiplica 1854 unità di progettazione per 16 pixel divise per 2048 unità di progettazione, equivalenti a 14,484375 pixel](images/fontstext9.png)

Il codice precedente posiziona il testo verticalmente impostando il membro dati *y* di un oggetto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) . La coordinata y viene aumentata da `font.GetHeight(0.0f)` per ogni nuova riga di testo. Il metodo [**font:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) di un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) restituisce l'interlinea (in pixel) per quel particolare oggetto **tipo di carattere** . In questo esempio, il numero restituito da **font:: GetHeight** è 18,398438. Si noti che si tratta dello stesso numero ottenuto convertendo la metrica di interlinea in pixel.

 

 
