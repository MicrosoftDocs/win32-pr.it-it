---
description: Una catena di scambio è una raccolta di buffer utilizzati per la visualizzazione di frame all'utente.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: Che cos'è una catena di scambio? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91666ffeb05dd7020a4caad1c11777842d7222cdc4cd6b04cd862edea5fff764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068811"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>Che cos'è una catena di scambio? (Direct3D 9)

Una catena di scambio è una raccolta di buffer utilizzati per la visualizzazione di frame all'utente. Ogni volta che un'applicazione presenta un nuovo frame per la visualizzazione, il primo buffer nella catena di scambio sostituisce il buffer visualizzato. Questo processo è detto scambio o capovolgimento.

Un adattatore grafico contiene un puntatore a una superficie che rappresenta l'immagine visualizzata sul monitor, denominata buffer anteriore. Quando il monitoraggio viene aggiornato, la scheda grafica invia il contenuto del buffer anteriore al monitor da visualizzare. Tuttavia, ciò comporta un problema durante il rendering della grafica in tempo reale. Il problema è che le frequenze di aggiornamento del monitoraggio sono molto lente rispetto al resto del computer. Le frequenze di aggiornamento comuni vanno da 60 Hz (60 volte al secondo) a 100 Hz. Se l'applicazione sta aggiornando il buffer anteriore mentre il monitor è al centro di un aggiornamento, l'immagine visualizzata verrà tagliata a metà con la metà superiore dello schermo contenente l'immagine precedente e la metà inferiore contenente la nuova immagine. Questo problema viene definito rimozione.

Direct3D implementa due opzioni per evitare la rimozione:

-   Opzione che consente solo gli aggiornamenti del monitoraggio nell'operazione di ritrace verticale (o sincronizzazione verticale). Un monitor in genere aggiorna l'immagine spostando un segnaposto chiaro orizzontalmente, zigzing dall'alto a sinistra del monitor e terminando in basso a destra. Quando il segnaposto chiaro raggiunge la parte inferiore, il monitor lo rilibra spostando nuovamente in alto a sinistra in modo che il processo possa essere avviato di nuovo. Questa ricalibrazione è detta sincronizzazione verticale. Durante una sincronizzazione verticale, il monitor non disegna nulla, quindi qualsiasi aggiornamento al buffer anteriore non verrà visualizzato fino a quando il monitor non inizia di nuovo a disegnare. La sincronizzazione verticale è relativamente lenta. tuttavia, non abbastanza lento da eseguire il rendering di una scena complessa durante l'attesa. Ciò che è necessario per evitare la rimozione ed essere in grado di eseguire il rendering di scene complesse è un processo denominato buffering nascosto.
-   Opzione per usare una tecnica denominata buffering nascosto. Il buffering indietro è il processo di disegno di una scena su una superficie esterna dello schermo, denominata buffer nascosto. Si noti che qualsiasi superficie diversa dal buffer anteriore viene chiamata superficie fuori schermo perché non viene mai visualizzata direttamente dal monitor. Usando un buffer nascosto, un'applicazione ha la libertà di eseguire il rendering di una scena ogni volta che il sistema è inattivo (ovvero non sono in attesa messaggi di Windows) senza dover considerare la frequenza di aggiornamento del monitoraggio. Il buffering indietro comporta un'ulteriore complicazione di come e quando spostare il buffer nascosto nel front buffer.

Il processo di spostamento del buffer indietro nel buffer anteriore è detto capovolgimento della superficie. Poiché la scheda grafica usa semplicemente un puntatore a una superficie per rappresentare il buffer anteriore, è sufficiente una semplice modifica del puntatore per impostare il buffer nascosto sul front buffer. Quando un'applicazione chiede a Direct3D di presentare il buffer nascosto nel buffer anteriore, Direct3D semplicemente "capovolge" i due puntatori di superficie. Il risultato è che il buffer nascosto è ora il nuovo front buffer e il buffer anteriore precedente è il nuovo buffer nascosto. Un capovolgimento della superficie viene richiamato ogni volta che un'applicazione chiede al dispositivo Direct3D di presentare il buffer nascosto; È tuttavia possibile configurare Direct3D per accodare le richieste fino a quando non viene eseguita una sincronizzazione verticale. Questa opzione è definita intervallo di presentazione del dispositivo Direct3D. Si noti che i dati nel nuovo buffer nascosto potrebbero non essere riutilizzabili, a seconda di come un'applicazione specifica come Direct3D deve gestire il capovolgimento della superficie. Il capovolgimento della superficie è fondamentale nel software multimediale, di animazione e di gioco; è equivalente al modo in cui è possibile eseguire l'animazione con un riquadro di carta. In ogni pagina l'artista cambia leggermente le figure, in modo che, quando si capovolge rapidamente tra i fogli, il disegno venga animato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Capovolgimento delle superfici (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



