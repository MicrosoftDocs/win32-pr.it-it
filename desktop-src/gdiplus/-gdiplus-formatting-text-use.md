---
description: Per applicare una formattazione speciale al testo, inizializzare un oggetto StringFormat e passare l'indirizzo di tale oggetto al metodo DrawString della classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formattazione del testo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b29a56def2d89f9ac3085f494f46a0242889d5ce6bc1a17af086dad96b881e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695813"
---
# <a name="formatting-text-gdi"></a>Formattazione del testo (GDI+)

Per applicare una formattazione speciale al testo, inizializzare un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e passare l'indirizzo di tale oggetto al [metodo DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Per disegnare testo formattato in un rettangolo, sono necessari oggetti [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) [**RectF,**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf) [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)e [**Brush.**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)

-   [Allineamento del testo](#aligning-text)
-   [Impostazione delle tabulazioni](#setting-tab-stops)
-   [Disegno di testo verticale](#drawing-vertical-text)

## <a name="aligning-text"></a>Allineamento del testo

L'esempio seguente disegna testo in un rettangolo. Ogni riga di testo è centrata (da lato a lato) e l'intero blocco di testo è centrato (dall'alto verso il basso) nel rettangolo.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



La figura seguente mostra il rettangolo e il testo centrato.

![Screenshot di una finestra contenente un rettangolo, che contiene sei righe di testo, centrate orizzontalmente](images/fontstext3.png)

Il codice precedente chiama due metodi dell'oggetto [**StringFormat:**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) e [**StringFormat::SetLineAlignment.**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment) La chiamata a **StringFormat::SetAlignment** specifica che ogni riga di testo è centrata nel rettangolo specificato dal terzo argomento passato al [metodo DrawString.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) La chiamata a **StringFormat::SetLineAlignment** specifica che il blocco di testo è centrato (dall'alto verso il basso) nel rettangolo.

Il valore [****StringAlignmentCenter****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) è un elemento dell'enumerazione **StringAlignment,** dichiarato in Gdiplusenums.h.

## <a name="setting-tab-stops"></a>Impostazione delle tabulazioni

È possibile impostare tabulazioni per il testo chiamando il metodo [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) di un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e quindi passando l'indirizzo di tale oggetto **StringFormat** al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Nell'esempio seguente le tabulazioni vengono impostate su 150, 250 e 350. Il codice visualizza quindi un elenco a schede di nomi e punteggi di test.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



La figura seguente mostra il testo a schede.

![illustrazione di un rettangolo contenente quattro colonne di testo; ogni colonna è alligata a sinistra](images/fontstext4.png)

Il codice precedente passa tre argomenti al [**metodo StringFormat::SetTabStops.**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) Il terzo argomento è l'indirizzo di una matrice contenente gli offset di tabulazione. Il secondo argomento indica che la matrice contiene tre offset. Il primo argomento passato a **StringFormat::SetTabStops** è 0, che indica che il primo offset nella matrice viene misurato dalla posizione 0, ovvero il bordo sinistro del rettangolo di delimitazione.

## <a name="drawing-vertical-text"></a>Disegno di testo verticale

È possibile usare un [**oggetto StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) per specificare che il testo deve essere disegnato verticalmente anziché orizzontalmente.

L'esempio seguente passa il valore [****StringFormatFlagsDirectionVertical*** al](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) [**metodo StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) di un [**oggetto StringFormat.**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) L'indirizzo **dell'oggetto StringFormat** viene passato al [metodo DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Il valore [****StringFormatFlagsDirectionVertical****](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) è un elemento dell'enumerazione **StringFormatFlags,** dichiarato in Gdiplusenums.h.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



La figura seguente mostra il testo verticale.

![illustrazione che mostra una finestra che contiene testo ruotato di 90 gradi in senso orario](images/fontstext5.png)

 

 



