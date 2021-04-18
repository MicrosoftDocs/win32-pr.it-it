---
description: Il capovolgimento della pagina è fondamentale per il software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con una carta da tastiera.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Capovolgimento della pagina e buffering indietro (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303844"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Capovolgimento della pagina e buffering indietro (Direct3D 9)

Il capovolgimento della pagina è fondamentale per il software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con una carta da tastiera. In ogni pagina, l'artista modifica leggermente la figura, in modo che, quando si scorre rapidamente tra i fogli, il disegno appaia animato.

Il capovolgimento della pagina nel software è simile a questo processo. Direct3D implementa la funzionalità di capovolgimento della pagina tramite una catena di scambio, che è una proprietà del dispositivo. Inizialmente, viene configurata una serie di buffer Direct3D che passano sullo schermo nel modo in cui il documento dell'artista passa alla pagina successiva. Il primo buffer viene definito buffer anteriore del colore. I buffer sottostanti vengono richiamati buffer. L'applicazione scrive in un buffer nascosto e quindi capovolge il buffer anteriore del colore in modo che il buffer nascosto venga visualizzato sullo schermo. Mentre il sistema Visualizza l'immagine, il software sta scrivendo nuovamente in un buffer nascosto. Il processo continua fino a quando si sta aggiungendo un'animazione, consentendo di animare le immagini in modo efficiente.

Direct3D semplifica la configurazione degli schemi di capovolgimento della pagina, da un semplice schema con doppio buffer (un buffer anteriore a un colore con un buffer nascosto) a schemi più sofisticati con buffer back aggiuntivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Che cos'è una catena di scambio? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



