---
description: Un mailslot è uno pseudofile che risiede in memoria e si usano funzioni di file standard per accedervi.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Informazioni su Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756519"
---
# <a name="about-mailslots"></a>Informazioni su Mailslot

Un mailslot è uno pseudofile che risiede in memoria e si usano funzioni di file standard per accedervi. I dati in un messaggio mailslot possono essere in qualsiasi formato, ma non possono essere maggiori di 424 byte se inviati tra computer. A differenza dei file su disco, i mailslot sono temporanei. Quando tutti gli handle di un mailslot vengono chiusi, il mailslot e tutti i dati in esso contenuti vengono eliminati.

Un *server mailslot* è un processo che crea e possiede un mailslot. Quando il server crea un mailslot, riceve un handle mailslot. Questo handle deve essere usato quando un processo legge i messaggi dal mailslot. Solo il processo che crea un mailslot o ha ottenuto l'handle da un altro meccanismo (ad esempio l'ereditarietà) può leggere da mailslot. Tutti i mailslot sono locali per il processo che li crea. Un processo non può creare un mailslot remoto.

Un *client mailslot* è un processo che scrive un messaggio in un mailslot. Qualsiasi processo con il nome di un mailslot può inserire un messaggio. I nuovi messaggi seguono tutti i messaggi esistenti in mailslot.

I mailslot possono trasmettere messaggi all'interno di un dominio. Se diversi processi in un dominio creano ognuno un mailslot con lo stesso nome, ogni messaggio indirizzato a tale mailslot e inviato al dominio viene ricevuto dai processi partecipanti. Poiché un processo può controllare sia un handle mailslot del server che l'handle del client recuperato quando il mailslot viene aperto per un'operazione di scrittura, le applicazioni possono implementare facilmente una semplice funzionalità di passaggio dei messaggi all'interno di un dominio.

Per inviare messaggi di dimensioni superiori a 424 byte tra computer, usare [named pipe](named-pipes.md) o Windows [Socket.](/windows/desktop/WinSock/windows-sockets-start-page-2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Nomi di Mailslot](mailslot-names.md)
</dt> <dt>

[Operazioni di Mailslot](mailslot-operations.md)
</dt> </dl>

 

 
