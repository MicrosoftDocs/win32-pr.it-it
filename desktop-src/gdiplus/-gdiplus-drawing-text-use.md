---
description: È possibile usare il metodo DrawString della classe Graphics per disegnare testo in una posizione specificata o all'interno di un rettangolo specificato.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Creazione di testo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31591d62198bc6ff72cdd7cce0d8ab515dc0e96011457b5bccd601a59ee0293f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115041"
---
# <a name="drawing-text-gdi"></a>Creazione di testo (GDI+)

È possibile usare il [metodo DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per disegnare testo in una posizione specificata o all'interno di un rettangolo specificato.

-   [Disegno di testo in una posizione specificata](#drawing-text-at-a-specified-location)
-   [Disegno di testo in un rettangolo](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Disegno di testo in una posizione specificata

Per disegnare testo in una posizione specificata, sono necessari [**oggetti Graphics,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) [**FontFamily,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)e [**Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

Nell'esempio seguente viene disegnata la stringa "Hello" nella posizione (30, 10). La famiglia di caratteri è Times New Roman. Il tipo di carattere, che è un singolo membro della famiglia di caratteri, è Times New Roman, dimensioni 24 pixel, stile normale. Si supponga **che la grafica** sia un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

Nella figura seguente viene illustrato l'output del codice precedente.

![Screenshot di una piccola finestra contenente il testo "hello"](images/fontstext1.png)

Nell'esempio precedente il costruttore [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) riceve una stringa che identifica la famiglia di caratteri. L'indirizzo **dell'oggetto FontFamily** viene passato come primo argomento al [**costruttore Font.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Il secondo argomento passato al **costruttore Font** specifica le dimensioni del tipo di carattere misurate in unità specificate dal quarto argomento. Il terzo argomento specifica lo stile (normale, grassetto, corsivo e così via) del tipo di carattere.

Il [metodo DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) riceve cinque argomenti. Il primo argomento è la stringa da disegnare e il secondo argomento è la lunghezza (in caratteri, non in byte) di tale stringa. Se la stringa ha terminazione Null, è possibile passare –1 per la lunghezza. Il terzo argomento è l'indirizzo [**dell'oggetto Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) costruito in precedenza. Il quarto argomento è un [**oggetto PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) che contiene le coordinate dell'angolo superiore sinistro della stringa. Il quinto argomento è l'indirizzo di [**un oggetto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) che verrà usato per riempire i caratteri della stringa.

## <a name="drawing-text-in-a-rectangle"></a>Disegno di testo in un rettangolo

Uno dei metodi [**DrawString**](https://www.bing.com/search?q=**DrawString**) della [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha un *parametro RectF.* Chiamando il metodo **DrawString,** è possibile disegnare testo che va a capo in un rettangolo specificato. Per disegnare testo in un rettangolo, sono necessari **oggetti Graphics,** [**FontFamily,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)e [**Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

Nell'esempio seguente viene creato un rettangolo con angolo superiore sinistro (30, 10), larghezza 100 e altezza 122. Il codice disegna quindi una stringa all'interno del rettangolo. La stringa è limitata al rettangolo ed esegue il wrapping in modo che le singole parole non siano interrotte.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

La figura seguente mostra il testo disegnato nel rettangolo.

![Screenshot di una piccola finestra contenente una ricangola, all'interno della quale viene visualizzata la prima parte di una frase](images/fontstext2.png)

Nell'esempio precedente, il quarto argomento passato al metodo [**DrawString**](https://www.bing.com/search?q=**DrawString**) è un [**oggetto RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) che specifica il rettangolo di delimitazione per il testo. Il quinto parametro è di tipo [**StringFormat. L'argomento**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)è **NULL** perché non è necessaria alcuna formattazione di stringa speciale.
