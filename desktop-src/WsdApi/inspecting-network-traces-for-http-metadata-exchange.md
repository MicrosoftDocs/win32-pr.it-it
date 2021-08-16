---
description: Informazioni sul controllo delle tracce di rete per lo scambio di metadati HTTP. Usare un analizzatore di pacchetti di rete che visualizza i pacchetti non elaborati.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Analisi delle tracce di rete per i metadati HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 076ead8f6ac0cf78699029189f0d34daaf0e17db3dec33d1a41bedfd0167eb2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311600"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Analisi delle tracce di rete per i metadati HTTP Exchange

Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per esaminare le richieste di scambio di metadati HTTP. Microsoft Network Monitor 3 (Netmon) è consigliato. Per altre informazioni su Netmon, vedere [Download di netmon e filtri DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)

Questa procedura di diagnostica potrebbe non essere utile per client e host che usano un canale sicuro per le comunicazioni perché il contenuto del messaggio è crittografato.

**Per esaminare le tracce di rete per lo scambio di metadati HTTP**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Installare l'analizzatore pacchetti (Netmon) nel client o nell'host.
3.  Configurare l'analizzatore pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.
4.  Riprodurre l'errore avviando l'host e il client o premendo F5 nel Esplora rete.
5.  Filtrare i risultati per isolare WS-Discovery traffico di scambio di metadati e dati. Per visualizzare i filtri Netmon di esempio, vedere [Download dei filtri Netmon e DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Questo passaggio è facoltativo.

     

6.  Verificare che i messaggi inviati tra client e host soddisfino i requisiti di traffico di base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verifica che i messaggi soddisfino i requisiti di traffico

I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti. Per informazioni generali sui modelli di messaggio, vedere Individuazione e [metadati Exchange modelli di messaggio](discovery-and-metadata-exchange-message-patterns.md).

-   I messaggi devono soddisfare i requisiti di traffico forniti nell'argomento [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), a meno che non sia assolutamente certo che WS-Discovery non venga usato per lo scambio di metadati.
-   È necessario stabilire una connessione TCP tra il client e il primo indirizzo di trasporto specificato nell'elemento **XAddrs** di [un messaggio ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md) L'elenco seguente mostra un tipico scambio di pacchetti usato per stabilire una connessione TCP.
    -   Il client invia un pacchetto TCP SYN all'host a una porta specificata.
    -   L'host invia un pacchetto TCP SYN/ACK al client.
    -   Il client invia un pacchetto TCP ACK all'host a una porta specificata.

    Dopo che il client ha inviato un pacchetto TCP ACK, viene stabilita la connessione TCP. Si noti che questo scambio di messaggi non si verifica se in precedenza è stata stabilita una connessione TCP.
-   Il client deve inviare una richiesta e un messaggio HTTP [Get](get--metadata-exchange--http-request-and-message.md) validi.
-   L'host deve essere in ascolto sul percorso URL specificato nella [richiesta Get](get--metadata-exchange--http-request-and-message.md) HTTP.
-   **L'elemento To** di [un messaggio di](get--metadata-exchange--http-request-and-message.md) metadati Get deve essere presente e non vuoto. Il valore **dell'elemento To** deve corrispondere a uno degli indirizzi endpoint dell'host. L'indirizzo endpoint di un host viene in genere annunciato in un [messaggio ProbeMatches](probematches-message.md) [o ResolveMatches.](resolvematches-message.md)
-   L'host deve inviare un'intestazione di risposta HTTP valida. Se la richiesta iniziale ha esito positivo, l'intestazione della risposta deve contenere il codice di stato HTTP/1.1 200.
-   L'host deve inviare un [messaggio GetResponse](getresponse--metadata-exchange--message.md) valido.
-   **L'elemento RelatesTo** di [un messaggio GetResponse](getresponse--metadata-exchange--message.md) deve essere presente e non deve essere vuoto. Il valore deve corrispondere al valore **dell'elemento MessageId** del messaggio [Get](get--metadata-exchange--http-request-and-message.md) corrispondente.

Se le richieste HTTP o i messaggi di scambio di metadati inviati dal programma non sono conformi a questi requisiti di traffico, la causa del problema è stata identificata correttamente e non sono necessari altri passaggi per la risoluzione dei problemi. Riscrivere il programma in modo che generi messaggi e richieste conformi e rieseguire il programma.

Se l'origine del problema non è ancora identificata, contattare il supporto tecnico Microsoft per assistenza. Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa radice del problema. Per altre informazioni, vedere [Abilitazione della traccia WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Download di netmon e filtri DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



