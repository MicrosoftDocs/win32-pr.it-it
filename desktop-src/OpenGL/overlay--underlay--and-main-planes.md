---
title: Piani sovrapposti, sottostanti e principali
description: È possibile usare piani di livello hardware (piani sovrapposti e sottostanti) nelle applicazioni.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL su Windows,piani di livello hardware
- Piani di livello hardware OpenGL
- Piani di sovrimpressione OpenGL
- underlay planes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936490"
---
# <a name="overlay-underlay-and-main-planes"></a>Piani sovrapposti, sottostanti e principali

È possibile usare piani di livello hardware (piani sovrapposti e sottostanti) nelle applicazioni. Con Windows, i formati pixel descrivono le configurazioni pixel di un dispositivo grafico. Ogni formato pixel descrive la profondità e altre caratteristiche dei buffer di colore principali e descrive buffer aggiuntivi (ad esempio profondità, accumulo, stencil e ausiliario) utilizzati dal piano principale. I formati pixel sono ora estesi per includere buffer sovrapposti e sottostanti.

I piani di livello hanno sempre un buffer di colore anteriore sinistro e possono anche includere buffer di colore anteriore destro e posteriore. Ogni piano livello ha un contesto di rendering specifico per il rendering nei buffer del livello. Non è possibile usare le funzioni di disegno GDI nei piani di livello.

Una finestra gestisce i buffer di colore dei piani di livello in modo analogo al modo in cui gestisce i buffer di colore del piano principale. È possibile visualizzare contemporaneamente più finestre con piani sovrapposti e/o sottostanti. Non è possibile avere finestre sovrapposte mobili che possono essere spostate su qualsiasi finestra nel piano di disegno principale. Inoltre, poiché nasconde i piani sottostanti in una finestra in qualsiasi momento, non è possibile usare piani popup hardware senza colore trasparente.

A ogni piano di livello in una finestra è associata una tavolozza. È possibile impostare la tavolozza di un piano livello indice colori, ma la tavolozza di un piano colori RGBA è fissa. È necessario realizzare la tavolozza appropriata quando una finestra è in primo piano. I piani livello hanno un colore o un indice in pixel trasparente che consente la visualizzazione di tutti i piani di livello sottostanti.

È possibile copiare lo stato di un contesto di rendering in un altro contesto di rendering in un piano livello separato. È anche possibile condividere gli elenchi di visualizzazione tra contesti di rendering in piani di livello diversi.

Con i piani di livello vengono usate le funzioni seguenti:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




