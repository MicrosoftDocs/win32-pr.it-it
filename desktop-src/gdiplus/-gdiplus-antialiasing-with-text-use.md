---
description: Windows GDI+ offre diversi livelli di qualità per il disegno di testo. In genere, il rendering di qualità superiore impiega più tempo di elaborazione rispetto al rendering di qualità inferiore.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anti-aliasing con testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994461"
---
# <a name="antialiasing-with-text"></a>Anti-aliasing con testo

Windows GDI+ offre diversi livelli di qualità per il disegno di testo. In genere, il rendering di qualità superiore impiega più tempo di elaborazione rispetto al rendering di qualità inferiore.

Il livello di qualità è una proprietà della classe [**grafica**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Per impostare il livello di qualità, chiamare il metodo [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) di un oggetto **Graphics** . Il metodo **Graphics:: SetTextRenderingHint** riceve uno degli elementi dell'enumerazione [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , dichiarata in Gdiplusenums. h.

GDI+ fornisce l'anti-aliasing tradizionale e un nuovo tipo di anti-aliasing basato sulla tecnologia di visualizzazione di Microsoft ClearType disponibile solo in Windows XP e Windows Server 2003 e versioni successive di Windows. ClearType smoothing migliora la leggibilità dei monitor LCD a colori che dispongono di un'interfaccia digitale, ad esempio i monitoraggi in computer portatili e schermi desktop flat di alta qualità. Anche la leggibilità sulle schermate CRT è stata migliorata.

ClearType dipende dall'orientamento e dall'ordinamento dei nastri LCD. Attualmente ClearType viene implementato solo per le strisce verticali ordinate RGB. Questo potrebbe costituire un problema se si utilizza un Tablet PC, in cui la visualizzazione può essere orientata in qualsiasi direzione o se si utilizza una schermata che può essere trasformata dall'orizzontale al verticale.

Nell'esempio seguente viene disegnato un testo con due impostazioni di qualità diverse:


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

![Screenshot di una stringa i cui caratteri hanno bordi frastagliati contrapposti a uno con bordi smussati](images/fontstext10.png)

 

 



