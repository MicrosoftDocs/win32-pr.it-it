---
description: Un oggetto Graphics fornisce metodi come DrawLine, DrawImage e DrawString per la visualizzazione di immagini vettoriali, immagini raster e testo.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizzo dei contenitori di grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96292395113b80ec79f8b59d4ac7f203c3d1f2d892c2da62ce4957e49b81860d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036289"
---
# <a name="using-graphics-containers"></a>Utilizzo dei contenitori di grafica

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce metodi come [DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) per la visualizzazione di immagini vettoriali, immagini raster e testo. Un **oggetto Graphics** ha anche diverse proprietà che influenzano la qualità e l'orientamento degli elementi disegnati. Ad esempio, la proprietà smoothing mode determina se l'antialiasing viene applicato a linee e curve e la proprietà di trasformazione world influisce sulla posizione e sulla rotazione degli elementi disegnati.

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è spesso associato a un particolare dispositivo di visualizzazione. Quando si usa un **oggetto Graphics** per disegnare in una finestra, anche l'oggetto **Graphics** viene associato a tale finestra specifica.

Un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) può essere pensato come un contenitore perché contiene un set di proprietà che influiscono sul disegno ed è collegato a informazioni specifiche del dispositivo. È possibile creare un contenitore secondario all'interno **di un oggetto Graphics** esistente chiamando il metodo [BeginContainer](/previous-versions//ms535731(v=vs.85)) dell'oggetto **Graphics.**

Gli argomenti seguenti descrivono [**in**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) modo più dettagliato gli oggetti Graphics e i contenitori annidati:

-   [Stato di un oggetto Graphics](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contenitori di oggetti Graphics annidati](-gdiplus-nested-graphics-containers-use.md)

 

 
