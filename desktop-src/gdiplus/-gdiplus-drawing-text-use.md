---
description: È possibile usare il metodo DrawString della classe Graphics per creare testo in una posizione specificata o all'interno di un rettangolo specificato.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Creazione di testo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131347"
---
# <a name="drawing-text-gdi"></a>Creazione di testo (GDI+)

È possibile usare il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare testo in una posizione specificata o all'interno di un rettangolo specificato.

-   [Disegno di testo in una posizione specificata](#drawing-text-at-a-specified-location)
-   [Disegno di testo in un rettangolo](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Disegno di testo in una posizione specificata

Per creare testo in una posizione specifica, sono necessari oggetti [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

Nell'esempio seguente viene disegnata la stringa "Hello" nella posizione (30, 10). La famiglia di caratteri è Times New Roman. Il tipo di carattere, che è un singolo membro della famiglia di caratteri, è Times New Roman, Size 24 pixels, regular Style. Si supponga che **Graphics** sia un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

Nella figura seguente viene illustrato l'output del codice precedente.

![Screenshot di una piccola finestra contenente il testo "Hello"](images/fontstext1.png)

Nell'esempio precedente, il costruttore [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) riceve una stringa che identifica la famiglia di caratteri. L'indirizzo dell'oggetto **FontFamily** viene passato come primo argomento al costruttore del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Il secondo argomento passato al costruttore del **tipo di carattere** specifica la dimensione del tipo di carattere misurato in unità fornite dal quarto argomento. Il terzo argomento specifica lo stile (normale, grassetto, corsivo e così via) del tipo di carattere.

Il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) riceve cinque argomenti. Il primo argomento è la stringa da disegnare e il secondo argomento è la lunghezza (in caratteri, non byte) di tale stringa. Se la stringa è con terminazione null, è possibile passare-1 per la lunghezza. Il terzo argomento è l'indirizzo dell'oggetto del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) creato in precedenza. Il quarto argomento è un oggetto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) che contiene le coordinate dell'angolo superiore sinistro della stringa. Il quinto argomento è l'indirizzo di un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) che verrà utilizzato per inserire i caratteri della stringa.

## <a name="drawing-text-in-a-rectangle"></a>Disegno di testo in un rettangolo

Uno dei metodi [**DrawString**](https://www.bing.com/search?q=**DrawString**) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha un parametro *RectF* . Chiamando il metodo **DrawString** , è possibile creare un testo che esegue il wrapping in un rettangolo specificato. Per creare testo in un rettangolo, sono necessari oggetti **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

Nell'esempio seguente viene creato un rettangolo con angolo superiore sinistro (30, 10), larghezza 100 e altezza 122. Il codice disegna quindi una stringa all'interno del rettangolo. La stringa è limitata al rettangolo e viene eseguito il wrapping in modo tale che le singole parole non vengano interrotte.

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

Nella figura seguente viene illustrato il testo disegnato nel rettangolo.

![Screenshot di una piccola finestra contenente un recangle, all'interno della quale viene visualizzata la prima parte di una frase](images/fontstext2.png)

Nell'esempio precedente, il quarto argomento passato al metodo [**DrawString**](https://www.bing.com/search?q=**DrawString**) è un oggetto [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) che specifica il rettangolo di delimitazione per il testo. Il quinto parametro è di tipo [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), l'argomento è **null** perché non è richiesta alcuna formattazione speciale della stringa.
