---
description: Una catena di scambio è una raccolta di buffer usati per visualizzare i frame all'utente.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: Che cos'è una catena di scambio? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8fc1fd2d313c70a680d9b276a3aabedc6d8cff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225349"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>Che cos'è una catena di scambio? (Direct3D 9)

Una catena di scambio è una raccolta di buffer usati per visualizzare i frame all'utente. Ogni volta che un'applicazione presenta un nuovo frame per la visualizzazione, il primo buffer nella catena di scambio sostituisce il buffer visualizzato. Questo processo è detto scambio o capovolgimento.

Una scheda grafica include un puntatore a una superficie che rappresenta l'immagine visualizzata sul monitor, denominata buffer anteriore. Quando il monitoraggio viene aggiornato, la scheda grafica invia il contenuto del buffer anteriore al monitor da visualizzare. Tuttavia, questo causa un problema durante il rendering della grafica in tempo reale. Il fulcro del problema è che le frequenze di aggiornamento del monitoraggio sono molto lente rispetto al resto del computer. Le frequenze di aggiornamento comuni sono comprese tra 60 Hz (60 volte al secondo) e 100 Hz. Se l'applicazione sta aggiornando il buffer anteriore mentre il monitor si trova al centro di un aggiornamento, l'immagine visualizzata verrà tagliata a metà con la metà superiore della visualizzazione che contiene l'immagine precedente e la metà inferiore contenente la nuova immagine. Questo problema viene definito strappo.

Direct3D implementa due opzioni per evitare lo strappo:

-   Opzione che consente di consentire solo gli aggiornamenti del monitoraggio sull'operazione di ritraccia verticale (o sincronizzazione verticale). Un monitoraggio consente in genere di aggiornare l'immagine spostando un pin chiaro orizzontalmente, zigzagando dalla parte superiore sinistra del monitoraggio e terminando in basso a destra. Quando il PIN della luce raggiunge la fine, il monitoraggio ricalibra il pin chiaro spostando il pin in alto a sinistra, in modo che il processo possa riavviarsi. Questa ritaratura è detta sincronizzazione verticale. Durante una sincronizzazione verticale, il monitoraggio non esegue alcuna operazione, pertanto qualsiasi aggiornamento del buffer anteriore non viene visualizzato fino a quando non viene riavviato il disegno del monitoraggio. La sincronizzazione verticale è relativamente lenta; Tuttavia, non sufficientemente lento da eseguire il rendering di una scena complessa in attesa. Gli elementi necessari per evitare lacerazioni ed essere in grado di eseguire il rendering di scene complesse sono un processo denominato buffering.
-   Opzione per utilizzare una tecnica chiamata buffering. Il buffering indietro è il processo di disegno di una scena in una superficie esterna, denominata buffer nascosto. Si noti che qualsiasi superficie diversa dal buffer anteriore viene chiamata superficie fuori schermo perché non viene mai visualizzata direttamente dal monitoraggio. Utilizzando un buffer nascosto, un'applicazione è in grado di eseguire il rendering di una scena ogni volta che il sistema è inattivo (ovvero, nessun messaggio di Windows è in attesa) senza dover considerare la frequenza di aggiornamento del monitoraggio. Il buffering nascosto comporta una complicazione aggiuntiva di come e quando spostare il buffer indietro nel buffer anteriore.

Il processo di trasferimento del buffer indietro nel buffer anteriore è denominato capovolgimento della superficie. Poiché la scheda grafica usa semplicemente un puntatore a una superficie per rappresentare il buffer anteriore, una semplice modifica del puntatore è sufficiente per impostare il buffer nascosto sul buffer anteriore. Quando un'applicazione chiede a Direct3D di presentare il buffer nascosto al buffer anteriore, Direct3D semplicemente "capovolge" i due puntatori della superficie. Il risultato è che il buffer nascosto è ora il nuovo buffer anteriore e il buffer anteriore precedente è il nuovo buffer nascosto. Un flip di superficie viene richiamato ogni volta che un'applicazione chiede al dispositivo Direct3D di presentare il buffer nascosto; Tuttavia, Direct3D può essere configurato per accodare le richieste fino a quando non si verifica una sincronizzazione verticale. Questa opzione è definita intervallo di presentazione del dispositivo Direct3D. Si noti che i dati nel nuovo buffer nascosto potrebbero non essere riutilizzabili, a seconda del modo in cui un'applicazione specifica il modo in cui Direct3D deve gestire il capovolgimento della superficie. Il capovolgimento della superficie è fondamentale nei programmi multimediali, di animazione e di gioco; equivale al modo in cui è possibile eseguire l'animazione con un riquadro di carta. In ogni pagina, l'autore modifica leggermente le cifre, in modo che quando si esegue rapidamente il capovolgimento tra i fogli, il disegno viene visualizzato animato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Capovolgimento di superfici (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



