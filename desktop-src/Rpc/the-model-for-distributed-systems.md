---
title: Modello per sistemi distribuiti
description: In genere, l'esecuzione di un sistema monolitico tra più computer comportava la suddivisione del sistema in componenti client e server separati.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859b2a0a83e7f12bd7caf372e60acf2736a114a0cdf46893830032a47a548019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924174"
---
# <a name="the-model-for-distributed-systems"></a>Modello per sistemi distribuiti

In genere, l'esecuzione di un sistema monolitico tra più computer comportava la suddivisione del sistema in componenti client e server separati. In questi sistemi, il componente client ha gestito l'interfaccia utente e il server ha fornito l'elaborazione back-end, ad esempio l'accesso al database, la stampa e così via. Con la proliferazione, la riduzione dei costi e la connessione dei computer da parte di reti con larghezza di banda sempre più elevata, la suddivisione dei sistemi software in più componenti è diventata più semplice, con ogni componente in esecuzione in un computer diverso ed eseguendo una funzione specializzata. Questo approccio ha semplificato lo sviluppo, la gestione, l'amministrazione e spesso ha migliorato le prestazioni e l'affidabilità, poiché l'errore in un computer non ha necessariamente disabilitato l'intero sistema.

In molti casi il sistema appare al client come un cloud opaco che esegue le operazioni necessarie, anche se il sistema distribuito è costituito da singoli nodi, come illustrato nella figura seguente.

![i client accedono ai servizi in un sistema di server RPC che viene visualizzato come cloud opaco ai client esterni](images/indy-nodes.png)

L'opacità del cloud viene mantenuta perché le operazioni di calcolo vengono richiamate per conto del client. Di conseguenza, i client possono individuare un computer (un *nodo*) nel cloud e richiedere una determinata operazione. nell'esecuzione dell'operazione, tale computer può richiamare la funzionalità in altri computer all'interno del cloud senza esporre al client i passaggi aggiuntivi o il computer in cui sono stati eseguiti.

Con questo paradigma, i meccanismi di un sistema distribuito simile al cloud possono essere suddivisi in molti scambi di pacchetti singoli o conversazioni tra singoli nodi.

I sistemi client-server tradizionali hanno due nodi con ruoli e responsabilità predefiniti. I sistemi con distribuzione moderna possono avere più di due nodi e i relativi ruoli sono spesso dinamici. In una conversazione un nodo può essere un client, mentre in un'altra conversazione il nodo può essere il server. In molti casi, l'utente finale della funzionalità esposta è un client con un utente che siede su una tastiera e guarda l'output. In altri casi il sistema distribuito funziona in modo automatico, eseguendo operazioni in background.

Il sistema distribuito potrebbe non avere client e server dedicati per ogni scambio di pacchetti specifico, ma è importante ricordare che è presente un chiamante o un iniziatore, uno dei quali viene spesso definito client. È presente anche il destinatario della chiamata (spesso indicato come server). Non è necessario avere scambi di pacchetti bidireci nel formato richiesta-risposta di un sistema distribuito. spesso i messaggi vengono inviati solo in un modo.

 

 




