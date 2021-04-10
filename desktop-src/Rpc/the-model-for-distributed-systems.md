---
title: Modello per sistemi distribuiti
description: Tradizionalmente, l'esecuzione di un sistema monolitico su più computer implica la suddivisione del sistema in componenti client e server distinti.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cd1ea3301d68e77562a63c542bc075692e5192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955298"
---
# <a name="the-model-for-distributed-systems"></a>Modello per sistemi distribuiti

Tradizionalmente, l'esecuzione di un sistema monolitico su più computer implica la suddivisione del sistema in componenti client e server distinti. In tali sistemi, il componente client gestisce l'interfaccia utente e l'elaborazione back-end fornita dal server, ad esempio l'accesso al database, la stampa e così via. Con la proliferazione dei computer, la riduzione del costo e la connessione da reti con larghezza di banda sempre più elevata, la suddivisione dei sistemi software in più componenti è diventata più comoda, con ogni componente in esecuzione in un computer diverso ed eseguendo una funzione specializzata. Questo approccio semplifica lo sviluppo, la gestione, l'amministrazione e il miglioramento delle prestazioni e dell'affidabilità, poiché l'errore in un computer non ha necessariamente disabilitato l'intero sistema.

In molti casi il sistema viene visualizzato nel client come cloud opaco che esegue le operazioni necessarie, anche se il sistema distribuito è costituito da singoli nodi, come illustrato nella figura seguente.

![i client accedono ai servizi in un sistema di server RPC che risultano come un cloud opaco ai client esterni](images/indy-nodes.png)

L'opacità del cloud viene mantenuta perché le operazioni di elaborazione vengono richiamate per conto del client. Di conseguenza, i client possono individuare un computer ( *nodo*) all'interno del cloud e richiedere una determinata operazione. durante l'esecuzione dell'operazione, il computer può richiamare la funzionalità su altri computer all'interno del cloud senza esporre i passaggi aggiuntivi o il computer in cui sono stati eseguiti nel client.

Con questo paradigma, i meccanismi di un sistema distribuito di tipo cloud possono essere suddivisi in molti singoli scambi di pacchetti o conversazioni tra i singoli nodi.

I sistemi client-server tradizionali hanno due nodi con responsabilità e ruoli predefiniti. I sistemi distribuiti moderna possono avere più di due nodi e i loro ruoli sono spesso dinamici. In una conversazione un nodo può essere un client, mentre in un'altra conversazione il nodo può essere il server. In molti casi, il consumatore finale della funzionalità esposta è un client con un utente seduto a una tastiera, guardando l'output. In altri casi, le funzioni di sistema distribuite vengono eseguite in modo automatico, eseguendo operazioni in background.

È possibile che il sistema distribuito non disponga di client e server dedicati per ogni scambio di pacchetti specifico, ma è importante ricordare che è presente un chiamante (o initiator) che viene spesso definito client. È anche presente il destinatario della chiamata (spesso definita server). Non è necessario avere scambi di pacchetti bidirezionali nel formato Request/Reply di un sistema distribuito. spesso i messaggi vengono inviati solo unidirezionale.

 

 




