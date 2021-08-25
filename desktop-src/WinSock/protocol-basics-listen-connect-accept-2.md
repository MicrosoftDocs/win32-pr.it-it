---
description: Nozioni di base sul protocollo di WSPListen, WSPAccept e WSPConnect per stabilire una connessione socket con Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Nozioni di base sul protocollo: Listen, Connessione, Accept'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db73ea4bca5a709ff6d030fcbb44661c6181e552955d02b67d8eb2bcf680bf92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857921"
---
# <a name="protocol-basics-listen-connect-accept"></a>Nozioni di base sul protocollo: Listen, Connessione, Accept

Le operazioni di base coinvolte nella definizione di una connessione socket possono essere spiegate in modo più pratico in termini di paradigma client-server.

Il lato server creerà prima un socket, lo associerà a un indirizzo locale noto (in modo che il client possa trovarlo) e metterà il socket in modalità di ascolto, tramite [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), per preparare le richieste di connessione in ingresso e per specificare la lunghezza della coda di backlog della connessione. I provider di servizi mandono le richieste di connessione in sospeso in una coda di backlog fino a quando non vengono agite dal server o non vengono ritirate (a causa di un timeout) dal client. Un provider di servizi può ignorare in modo invisibile all'utente le richieste per estendere le dimensioni della coda di backlog oltre un limite superiore definito dal provider.

A questo punto, se viene usato un socket di blocco, il lato server può chiamare [**immediatamente WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) che verrà bloccato fino a quando una richiesta di connessione non è in sospeso. Al contrario, il server può anche usare uno dei meccanismi di indicazione degli eventi di rete descritti in precedenza per organizzare la notifica delle richieste di connessione in ingresso. A seconda del meccanismo di notifica selezionato, il provider emettere un messaggio Windows o segnalare un oggetto evento all'arrivo delle richieste di connessione. Per [informazioni su come eseguire](notification-of-network-events-2.md) la registrazione per l'evento di rete FD ACCEPT, vedere Notifica degli eventi di \_ rete.

Il lato client creerà un socket appropriato e avvierà la connessione chiamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), specificando l'indirizzo del server noto. I client in genere [](/windows/desktop/api/winsock/nf-winsock-bind) non eseguono un'operazione di associazione esplicita prima di avviare una connessione, consentendo al provider di servizi di eseguire un'associazione implicita per loro conto. Se il socket è in modalità di blocco, **WSPConnect** verrà bloccato fino a quando il server non riceverà e agirà in base alla richiesta di connessione (o fino a quando non si verifica un timeout). In caso contrario, il client deve usare uno dei meccanismi di indicazione degli eventi di rete descritti in precedenza per organizzare la notifica di una nuova connessione stabilita. A seconda del meccanismo di notifica selezionato, il provider indicherà questa operazione tramite un messaggio Windows o segnalando un oggetto evento.

Quando il lato server richiama [**WSPAccept,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)il provider di servizi chiama la funzione condizione fornita dall'applicazione, usando i parametri della funzione per passare le informazioni sul server dalla voce principale nella coda di backlog della richiesta di connessione. Queste informazioni includono, ad esempio, l'indirizzo dell'host di connessione, tutti i dati utente disponibili e le informazioni QoS disponibili. Usando queste informazioni, la funzione della condizione del server determina se accettare la richiesta, rifiutarla o posticipare la decisione fino a un secondo momento. Questa decisione viene indicata tramite il valore restituito della funzione della condizione. Per [informazioni su come eseguire](notification-of-network-events-2.md) la registrazione per l'evento di rete FD CONNECT, vedere Notifica degli eventi di \_ rete.

Se il server decide di accettare la richiesta, il provider deve creare un nuovo socket con tutti gli stessi attributi e registrazioni di eventi del socket di ascolto. Il socket originale rimane in ascolto in modo da poter ricevere le richieste di connessione successive. Tramite i parametri di output della funzione condition, il server può anche fornire dati utente di risposta e assegnare parametri QoS (presupponendo che queste operazioni siano supportate dal provider di servizi).

 

 
