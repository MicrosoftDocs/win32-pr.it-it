---
title: Rendering delle immagini
description: Rendering delle immagini
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, rendering delle immagini
- DrawDib, disegno di DIB
- Funzione DrawDibDraw
- Funzione DrawDibGetBuffer
- Funzione DrawDibUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690751"
---
# <a name="image-rendering"></a>Rendering delle immagini

Dopo aver chiamato [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) per creare un controller di dominio DrawDib (vedere [Operazioni DrawDib](drawdib-operations.md)), è possibile disegnare un DIB sullo schermo usando la [**funzione DrawDibDraw.**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) **DrawDibDraw** esegue il dithering delle bitmap true color quando vengono visualizzate con schede di visualizzazione a 8 bit.

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) supporta anche in modo trasparente i video per la visualizzazione di bitmap compresse. È possibile accedere al buffer che contiene l'immagine decompressa usando la [**funzione DrawDibGetBuffer.**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) **DrawDibGetBuffer** restituisce **NULL quando** si disegna una bitmap non compressa. È necessario preparare l'applicazione per la gestione delle bitmap compresse e non compresse.

È possibile aggiornare un'immagine o una parte di un'immagine visualizzata dall'applicazione usando la macro [**DrawDibUpdate.**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle funzioni DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




