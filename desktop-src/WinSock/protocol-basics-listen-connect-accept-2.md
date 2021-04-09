---
description: Nozioni di base sui protocolli di WSPListen, WSPAccept e WSPConnect per stabilire una connessione socket con Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Nozioni fondamentali sui protocolli: ascolto, connessione, accettazione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62ef290d71e571154b4d022c24c7e21f8fffa1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129134"
---
# <a name="protocol-basics-listen-connect-accept"></a>Nozioni fondamentali sui protocolli: ascolto, connessione, accettazione

Le operazioni di base necessarie per stabilire una connessione socket possono essere descritte più facilmente in termini di paradigma client-server.

Il lato server creerà prima di tutto un socket, lo associerà a un indirizzo locale noto (in modo che il client possa trovarlo) e inserirà il socket in modalità di ascolto, tramite [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), per preparare le richieste di connessione in ingresso e per specificare la lunghezza della coda di backlog della connessione. I provider di servizi contengono richieste di connessione in sospeso in una coda di backlog fino a quando non vengono eseguite dal server o non vengono ritirate (a causa di un timeout) da parte del client. Un provider di servizi può ignorare automaticamente le richieste per estendere le dimensioni della coda di backlog oltre un limite superiore definito dal provider.

A questo punto, se viene utilizzato un socket di blocco, il lato server può chiamare immediatamente [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) che si bloccherà fino a quando una richiesta di connessione non è in sospeso. Viceversa, il server può utilizzare anche uno dei meccanismi di indicazione degli eventi di rete descritti in precedenza per disporre la notifica delle richieste di connessione in ingresso. A seconda del meccanismo di notifica selezionato, il provider emetterà un messaggio di Windows o segnalerà un oggetto evento all'arrivo delle richieste di connessione. Vedere [notifica degli eventi di rete](notification-of-network-events-2.md) per informazioni su come eseguire la registrazione per l' \_ evento di rete di accettazione FD.

Il lato client creerà un socket appropriato e avvierà la connessione chiamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), specificando l'indirizzo del server noto. I client in genere non eseguono un'operazione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) esplicita prima di avviare una connessione, consentendo al provider di servizi di eseguire un'associazione implicita per loro conto. Se il socket è in modalità di blocco, **WSPConnect** si bloccherà fino a quando il server non ha ricevuto e agito sulla richiesta di connessione (o fino a quando non si verifica un timeout). In caso contrario, il client deve usare uno dei meccanismi di indicazione degli eventi di rete descritti in precedenza per organizzare la notifica di una nuova connessione stabilita. A seconda del meccanismo di notifica selezionato, il provider indicherà questa impostazione tramite un messaggio di Windows o segnalando un oggetto evento.

Quando il lato server richiama [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept), il provider di servizi chiama la funzione di condizione fornita dall'applicazione, usando i parametri della funzione per passare le informazioni sul server dalla voce superiore della coda di backlog della richiesta di connessione. Queste informazioni includono elementi come indirizzo di connessione host, eventuali dati utente disponibili ed eventuali informazioni QoS disponibili. Utilizzando queste informazioni, la funzione di condizione del server determina se accettare la richiesta, rifiutare la richiesta o posticipare la decisione fino a un momento successivo. Questa decisione viene indicata tramite il valore restituito della funzione Condition. Per informazioni su come eseguire la registrazione per l'evento di rete FD Connect, vedere [notifica degli eventi di rete](notification-of-network-events-2.md) \_ .

Se il server decide di accettare la richiesta, il provider deve creare un nuovo socket con tutti gli stessi attributi e registrazioni di eventi del socket in ascolto. Il socket originale rimane nello stato di ascolto, in modo che possano essere ricevute le richieste di connessione successive. Tramite i parametri di output della funzione condition, il server può anche fornire qualsiasi dato utente di risposta e assegnare parametri QoS (presupponendo che queste operazioni siano supportate dal provider di servizi).

 

 
