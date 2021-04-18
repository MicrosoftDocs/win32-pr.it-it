---
description: Alcune tecniche di programmazione si verificano in problemi di prestazioni collegati all'implementazione di TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemi specifici di TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313231"
---
# <a name="tcpip-specific-issues"></a>Problemi specifici di TCP/IP

Alcune tecniche di programmazione si verificano in problemi di prestazioni collegati all'implementazione di TCP/IP. Tali problemi di prestazioni non indicano che TCP/IP è inefficiente o un collo di bottiglia delle prestazioni. questi problemi si verificano invece quando le operazioni TCP/IP non vengono riconosciute.

I problemi seguenti identificano scenari comuni in cui la combinazione di opzioni per lo sviluppo di applicazioni di rete e di operazioni TCP/IP comporta una riduzione delle prestazioni.

-   Applicazioni con utilizzo intensivo della connessione.

    Alcune applicazioni creano un'istanza di una nuova connessione TCP per ogni transazione. La creazione della connessione TCP richiede tempo, contribuisce a RTTs aggiuntivi ed è soggetta a un avvio lento. Inoltre, le connessioni chiuse sono soggette a tempo di attesa, che utilizza le risorse di sistema.

    Le applicazioni con un elevato numero di connessioni sono molto comuni perché sono facili da creare; la gestione dei test e degli errori è molto semplice. Il rilevamento degli errori in una connessione permanente può richiedere un codice e un impegno considerevoli e, pertanto, a volte non viene completato.

    Risolvere questa situazione riutilizzando la connessione TCP. Questa operazione può causare la serializzazione sulla connessione TCP, a meno che le transazioni non siano multiplexate su più connessioni. Se si adotta questo approccio, il numero di connessioni deve essere limitato a due e l'inquadramento a livello di applicazione e la gestione avanzata degli errori sono obbligatori.

-   Buffer di invio a lunghezza zero e invii di blocco.

    La disattivazione del buffer tramite la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare il buffer di invio (in modo che \_ sndbuf) su zero è simile alla disattivazione della memorizzazione nella cache del disco. Quando si imposta il buffer di invio su zero e si emette un blocco inviato, un'applicazione ha una probabilità del 50% di raggiungere un riconoscimento ritardato di 200 millisecondi.

    Non disattivare il buffer di invio, a meno che l'utente non abbia preso in considerazione l'effetto in tutti gli ambienti di rete. Un'eccezione: i dati di streaming con I/O sovrapposti devono impostare il buffer di invio su zero.

-   Modello di programmazione Send-Send-Receive.

    La strutturazione di un'applicazione per l'esecuzione di Send-Send-Receive consente di aumentare le probabilità di riscontrare l'algoritmo Nagle, che causa un ritardo di RTT + 200 ms. L'algoritmo Nagle può essere rilevato se l'ultimo invio è inferiore alle dimensioni del segmento massimo TCP (MSS, i dati massimi in un singolo datagramma). MSS può essere un valore di grandi dimensioni (64K in IPv4 e anche più grande in IPv6), quindi non contare su un MSS di solito piccolo. Un'opzione migliore consiste nel combinare i due invii in una singola trasmissione usando la funzione [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o **memcpy** .

-   Un numero elevato di connessioni simultanee.

    Le connessioni simultanee non devono superare due, ad eccezione delle applicazioni per scopi specifici. Il superamento di due connessioni simultanee comporta una perdita di risorse. Una regola efficace consiste nel disporre di un massimo di quattro connessioni di breve durata o di due connessioni permanenti per destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comportamento dell'applicazione](application-behavior-2.md)
</dt> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



