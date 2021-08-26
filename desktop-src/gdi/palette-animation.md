---
description: L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animazione della tavolozza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ea2d557ddd071a8f8e993f3a797fb42c2f4fef9abc68fc13737cded96a18fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965591"
---
# <a name="palette-animation"></a>Animazione della tavolozza

L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori. Un'applicazione può eseguire l'animazione della tavolozza creando una tavolozza logica che contiene voci "riservate" e quindi usando la funzione [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare i colori in tali voci riservate.

Un'applicazione crea una voce riservata in un riquadro logico impostando il membro **peFlags** della struttura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) sul flag PC \_ RESERVED. Dopo aver selezionato e realizzato questo riquadro logico, l'applicazione può chiamare la [**funzione AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare una o più voci riservate. Se la tavolozza specificata è associata alla finestra attiva, il sistema aggiorna immediatamente i colori sullo schermo.

 

 
