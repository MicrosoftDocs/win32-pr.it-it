---
title: Sovrapposizione, sottoposto e piani principali
description: Nelle applicazioni è possibile usare i piani a livello di hardware, ovvero i piani sovrapposti e quelli sottoposti.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL in Windows, piani livello hardware
- livelli hardware OpenGL
- sovrapposizione di piani OpenGL
- piani di sottofondo OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298204"
---
# <a name="overlay-underlay-and-main-planes"></a>Sovrapposizione, sottoposto e piani principali

Nelle applicazioni è possibile usare i piani a livello di hardware, ovvero i piani sovrapposti e quelli sottoposti. Con Windows, i formati pixel descrivono le configurazioni in pixel di un dispositivo grafico. Ogni formato pixel descrive la profondità e altre caratteristiche dei buffer dei colori principali e descrive i buffer aggiuntivi (ad esempio profondità, accumulo, stencil e ausiliario) usati dal piano principale. I formati pixel sono ora estesi per includere i buffer sovrapposti e di sottofondo.

I piani di livello hanno sempre un buffer di colore in primo piano e possono includere buffer di colore anteriore e posteriore. Ogni piano di livello dispone di un contesto di rendering specifico di cui eseguire il rendering nei buffer del livello. Non è possibile utilizzare le funzioni di disegno GDI nei piani di livello.

Una finestra gestisce i buffer dei colori dei piani di livello in modo analogo al modo in cui gestisce i buffer dei colori del piano principale. È possibile visualizzare più finestre con piani sovrapposti e/o sottoposti allo stesso tempo. Non è possibile avere finestre sovrapposte a virgola mobile gratuite che possono spostarsi in qualsiasi finestra del piano di disegno principale. Inoltre, poiché in ogni momento i piani sottostanti vengono nascosti in una finestra, non è possibile utilizzare i piani popup hardware privi di colore trasparente.

A ogni piano di livello in una finestra è associata una tavolozza. È possibile impostare la tavolozza di un piano del livello di indice colore, ma la tavolozza di un piano di colore RGBA è fissa. È necessario realizzare la tavolozza appropriata quando una finestra è in primo piano. I piani di livello hanno un colore o un indice di pixel trasparente che consente la visualizzazione di tutti i piani di livello sottostante.

È possibile copiare lo stato di un contesto di rendering in un altro contesto di rendering in un piano di livello separato. È anche possibile condividere elenchi di visualizzazione tra contesti di rendering in diversi piani di livello.

Con i piani di livello vengono usate le funzioni seguenti:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




