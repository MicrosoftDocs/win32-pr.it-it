---
description: Un inserimento/espulsione è un pseudofile che risiede in memoria e si usano funzioni file standard per accedervi.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Informazioni su mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319617"
---
# <a name="about-mailslots"></a>Informazioni su mailslot

Un inserimento/espulsione è un pseudofile che risiede in memoria e si usano funzioni file standard per accedervi. I dati in un messaggio inserimento/espulsione possono essere in qualsiasi formato, ma non possono essere più grandi di 424 byte se inviati tra computer. A differenza dei file su disco, mailslot sono temporanei. Quando tutti gli handle di un inserimento/espulsione vengono chiusi, il inserimento/espulsione e tutti i dati in esso contenuti vengono eliminati.

Un *Server inserimento/espulsione* è un processo che crea e possiede un inserimento/espulsione. Quando il server crea un inserimento/espulsione, riceve un handle inserimento/espulsione. Questo handle deve essere usato quando un processo legge i messaggi dal inserimento/espulsione. Solo il processo che crea un inserimento/espulsione o ha ottenuto l'handle da un altro meccanismo, ad esempio l'ereditarietà, può leggere da inserimento/espulsione. Tutte le mailslot sono locali per il processo che le crea. Un processo non è in grado di creare un inserimento/espulsione remoto.

Un *client inserimento/espulsione* è un processo che scrive un messaggio in un inserimento/espulsione. Tutti i processi che hanno il nome di un inserimento/espulsione possono inserire un messaggio. I nuovi messaggi seguono tutti i messaggi esistenti in inserimento/espulsione.

Mailslot è in grado di trasmettere messaggi all'interno di un dominio. Se più processi in un dominio creano un inserimento/espulsione con lo stesso nome, ogni messaggio indirizzato a tale inserimento/espulsione e inviato al dominio viene ricevuto dai processi partecipanti. Poiché un processo può controllare sia un handle inserimento/espulsione server che l'handle client recuperato quando viene aperto il inserimento/espulsione per un'operazione di scrittura, le applicazioni possono implementare facilmente una semplice funzione di passaggio dei messaggi all'interno di un dominio.

Per inviare messaggi di dimensioni superiori a 424 byte tra computer, utilizzare [Named Pipes](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Nomi inserimento/espulsione](mailslot-names.md)
</dt> <dt>

[Operazioni inserimento/espulsione](mailslot-operations.md)
</dt> </dl>

 

 
