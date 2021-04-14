---
description: Un oggetto Graphics fornisce metodi quali DrawLine, DrawImage e DrawString per la visualizzazione di immagini vettoriali, immagini raster e testo.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizzo dei contenitori di grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978906"
---
# <a name="using-graphics-containers"></a>Utilizzo dei contenitori di grafica

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce metodi quali [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) per la visualizzazione di immagini vettoriali, immagini raster e testo. Un oggetto **Graphics** dispone inoltre di diverse proprietà che influenzano la qualità e l'orientamento degli elementi disegnati. Ad esempio, la proprietà modalità di smussamento determina se l'anti-aliasing viene applicato a linee e curve e la proprietà trasformazione globale influisce sulla posizione e sulla rotazione degli elementi disegnati.

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è spesso associato a un particolare dispositivo di visualizzazione. Quando si usa un oggetto **Graphics** per il progetto in una finestra, l'oggetto **Graphics** viene associato anche a tale finestra specifica.

Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) può essere considerato come un contenitore perché include un set di proprietà che influenzano il disegno ed è collegato a informazioni specifiche del dispositivo. È possibile creare un contenitore secondario in un oggetto **Graphics** esistente chiamando il metodo [BeginContainer](/previous-versions//ms535731(v=vs.85)) dell'oggetto **Graphics** .

Gli argomenti seguenti riguardano gli oggetti [**grafici**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e i contenitori annidati in modo più dettagliato:

-   [Stato di un oggetto Graphics](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Contenitori di oggetti Graphics annidati](-gdiplus-nested-graphics-containers-use.md)

 

 
