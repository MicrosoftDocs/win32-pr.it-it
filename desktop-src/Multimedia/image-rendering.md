---
title: Rendering di immagini
description: Rendering di immagini
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, rendering di immagini
- DrawDib, disegno di DIB
- DrawDibDraw (funzione)
- DrawDibGetBuffer (funzione)
- DrawDibUpdate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045284"
---
# <a name="image-rendering"></a>Rendering di immagini

Dopo aver chiamato [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) per creare un controller di dominio DrawDib (vedere [operazioni DrawDib](drawdib-operations.md)), è possibile creare una DIB sullo schermo usando la funzione [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) . **DrawDibDraw** presenta le bitmap con colori reali quando vengono visualizzate con adattatori video a 8 bit.

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) supporta anche i compressione video in modo trasparente quando si visualizzano le bitmap compresse. È possibile accedere al buffer che contiene l'immagine decompressa usando la funzione [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) . **DrawDibGetBuffer** restituisce **null** quando si disegna una bitmap non compressa. È necessario preparare l'applicazione per gestire le bitmap compresse e non compresse.

È possibile aggiornare un'immagine o una parte di un'immagine visualizzata dall'applicazione usando la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle funzioni DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




