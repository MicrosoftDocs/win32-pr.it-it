---
description: Windows GDI+ fornisce vari livelli di qualità per il disegno del testo. In genere, un rendering di qualità superiore richiede più tempo di elaborazione rispetto al rendering di qualità inferiore.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Antialiasing con testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249925"
---
# <a name="antialiasing-with-text"></a>Antialiasing con testo

Windows GDI+ fornisce vari livelli di qualità per il disegno del testo. In genere, un rendering di qualità superiore richiede più tempo di elaborazione rispetto al rendering di qualità inferiore.

Il livello di qualità è una proprietà della [**classe**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Graphics. Per impostare il livello di qualità, chiamare il [**metodo Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) di un **oggetto Graphics.** Il **metodo Graphics::SetTextRenderingHint** riceve uno degli elementi dell'enumerazione [**TextRenderingHint,**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) dichiarato in Gdiplusenums.h.

GDI+ fornisce l'antialiasing tradizionale e un nuovo tipo di antialiasing basato sulla tecnologia di visualizzazione Microsoft ClearType disponibile solo in Windows XP e Windows Server 2003 e versioni successive di Windows. Il smoothing ClearType migliora la leggibilità dei monitor LCD a colori con un'interfaccia digitale, ad esempio i monitor nei portatili e i monitor desktop flat di alta qualità. Anche la leggibilità nelle schermate CRT è leggermente migliorata.

ClearType dipende dall'orientamento e dall'ordinamento delle strisce LCD. Attualmente, ClearType viene implementato solo per le strisce verticali ordinate RGB. Questo potrebbe essere un problema se si usa un Tablet PC, in cui lo schermo può essere orientato in qualsiasi direzione o se si usa uno schermo che può essere trasformato da orizzontale a verticale.

L'esempio seguente disegna testo con due diverse impostazioni di qualità:


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



Nella figura seguente viene illustrato l'output del codice precedente.

![Screenshot di una stringa i cui caratteri hanno bordi frastagliati a contrasto con uno con bordi smussati](images/fontstext10.png)

 

 



