---
description: Il capovolgimento della pagina è fondamentale nel software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con un riquadro di carta.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Capovolgimento pagina e buffering indietro (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f1797300a838e453abf6811ae35b8f576e46c89ca0e929d2326b43ffea274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746931"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Capovolgimento pagina e buffering indietro (Direct3D 9)

Il capovolgimento della pagina è fondamentale nel software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con un riquadro di carta. In ogni pagina l'artista cambia leggermente la figura, in modo che, quando si capovolge rapidamente tra i fogli, il disegno venga animato.

Il capovolgimento della pagina nel software è simile a questo processo. Direct3D implementa la funzionalità di capovolgimento della pagina tramite una catena di scambio, che è una proprietà del dispositivo. Inizialmente, si configura una serie di buffer Direct3D che vengono capovolti sullo schermo nel modo in cui la carta dell'artista capovolge la pagina successiva. Il primo buffer viene definito buffer anteriore dei colori. I buffer dietro di esso sono chiamati buffer back. L'applicazione scrive in un buffer nascosto e quindi capovolge il buffer anteriore dei colori in modo che il buffer nascosto venga visualizzato sullo schermo. Mentre il sistema visualizza l'immagine, il software scrive nuovamente in un buffer nascosto. Il processo continua finché si aggiunge un'animazione, consentendo di animare le immagini in modo efficiente.

Direct3D semplifica la configurazione degli schemi di capovolgimento della pagina, da un semplice schema a doppio buffer (un front buffer a colori con un buffer nascosto) a schemi più sofisticati con buffer nascosto aggiuntivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Che cos'è una catena di scambio? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



