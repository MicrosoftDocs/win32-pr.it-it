---
description: L'argomento Disegno di una linea illustra come scrivere un'applicazione Windows che usa Windows GDI+ per disegnare una linea.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Disegno di una stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9f9384631a0f3505e0bfd20a5e9b23ef3969432cd4ec82737ecf6f962062ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067504"
---
# <a name="drawing-a-string"></a>Disegno di una stringa

[L'argomento Disegno di una](-gdiplus-drawing-a-line-use.md) linea illustra come scrivere un'applicazione Windows che usa Windows GDI+ per disegnare una linea. Per disegnare una stringa, sostituire la **funzione OnPaint** illustrata in tale argomento con la funzione **OnPaint** seguente:


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



Il codice precedente crea diversi GDI+ oggetti . [**L'oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce il [metodo DrawString,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) che esegue il disegno effettivo. [**L'oggetto SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) specifica il colore della stringa.

Il [**costruttore FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) riceve un singolo argomento stringa che identifica la famiglia di caratteri. L'indirizzo **dell'oggetto FontFamily** è il primo argomento passato al [**costruttore Font.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Il secondo argomento passato al costruttore [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) specifica la dimensione del carattere e il terzo argomento specifica lo stile. Il valore **FontStyleRegular** è un membro [**dell'enumerazione FontStyle,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) dichiarato in Gdiplusenums.h. L'ultimo argomento del **costruttore Font** indica che le dimensioni del carattere (24 in questo caso) sono misurate in pixel. Il valore **UnitPixel** è un membro [**dell'enumerazione Unit.**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit)

Il primo argomento passato al [metodo DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) è l'indirizzo di una stringa di caratteri wide. Il secondo argomento, –1, specifica che la stringa è con terminazione Null. Se la stringa non è con terminazione Null, il secondo argomento deve specificare il numero di caratteri wide nella stringa. Il terzo argomento è l'indirizzo [**dell'oggetto Font.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Il quarto argomento è un riferimento a un [**oggetto PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) che specifica la posizione in cui verrà disegnata la stringa. L'ultimo argomento è l'indirizzo [**dell'oggetto Brush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) che specifica il colore della stringa.

 

 
