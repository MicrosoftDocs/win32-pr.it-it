---
description: Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere utilizzato per controllare le richieste di scambio di metadati HTTP. È consigliabile Microsoft Network Monitor 3 (Netmon). Per ulteriori informazioni su Netmon, vedere Download di Netmon e Sample DPWS filters.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Controllo delle tracce di rete per lo scambio di metadati HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9993c542789b7f11eb35344dd6b0b03bfbafc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226923"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Controllo delle tracce di rete per lo scambio di metadati HTTP

Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere utilizzato per controllare le richieste di scambio di metadati HTTP. È consigliabile Microsoft Network Monitor 3 (Netmon). Per ulteriori informazioni su Netmon, vedere [download di Netmon e Sample DPWS filters](downloading-netmon-and-sample-dpws-filters.md).

Questa procedura di diagnostica potrebbe non essere utile per i client e gli host che utilizzano un canale sicuro per le comunicazioni perché il contenuto del messaggio è crittografato.

**Per esaminare le tracce di rete per lo scambio di metadati HTTP**

1.  Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).
2.  Installare Packet Analyzer (Netmon) nel client o nell'host.
3.  Configurare l'analizzatore di pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.
4.  Riprodurre l'errore avviando l'host e il client o premendo F5 in Network Explorer.
5.  Filtrare i risultati per isolare il traffico di WS-Discovery e di scambio dei metadati. Per visualizzare i filtri Netmon di esempio, vedere [download di Netmon e Sample DPWS filters](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Questo passaggio è facoltativo.

     

6.  Verificare che i messaggi inviati tra il client e l'host soddisfino i requisiti di traffico di base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verifica per verificare se i messaggi soddisfano i requisiti di traffico

I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti. Per informazioni generali sui modelli di messaggio, vedere [modelli di messaggio di scambio di metadati e individuazione](discovery-and-metadata-exchange-message-patterns.md).

-   I messaggi devono soddisfare i requisiti di traffico forniti nell'argomento [controllo delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), a meno che non sia assolutamente certo che WS-Discovery non venga utilizzato per lo scambio di metadati.
-   È necessario stabilire una connessione TCP tra il client e il primo indirizzo di trasporto fornito nell'elemento **XAddrs** di un messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) . Nell'elenco seguente viene illustrato un tipico scambio di pacchetti utilizzato per stabilire una connessione TCP.
    -   Il client invia un pacchetto SYN TCP all'host su una porta specificata.
    -   L'host invia al client un pacchetto SYN/ACK TCP.
    -   Il client invia un pacchetto ACK TCP all'host in una porta specificata.

    Una volta che il client ha inviato un pacchetto ACK TCP, viene stabilita la connessione TCP. Si noti che questo scambio di messaggi non verrà eseguito se è già stata stabilita una connessione TCP.
-   Il client deve inviare una richiesta HTTP [Get](get--metadata-exchange--http-request-and-message.md) e un messaggio validi.
-   L'host deve essere in ascolto sul percorso URL specificato nella richiesta HTTP [Get](get--metadata-exchange--http-request-and-message.md) .
-   L'elemento **to** di un messaggio [Get](get--metadata-exchange--http-request-and-message.md) Metadata deve essere presente e non vuoto. Il valore dell'elemento **to** deve corrispondere a uno degli indirizzi endpoint dell'host. L'indirizzo endpoint di un host viene in genere annunciato in un messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .
-   L'host deve inviare un'intestazione di risposta HTTP valida. Se la richiesta iniziale ha avuto esito positivo, l'intestazione della risposta deve contenere il codice di stato HTTP/1.1 200.
-   L'host deve inviare un messaggio [GetResponse](getresponse--metadata-exchange--message.md) valido.
-   L'elemento **Repiù recente** di un messaggio [GetResponse](getresponse--metadata-exchange--message.md) deve essere presente e non deve essere vuoto. Il valore deve corrispondere al valore dell'elemento **MessageID** del messaggio [Get](get--metadata-exchange--http-request-and-message.md) corrispondente.

Se le richieste HTTP o i messaggi di scambio di metadati inviati dal programma non sono conformi a questi requisiti di traffico, la causa del problema è stata identificata e non sono necessarie ulteriori passaggi per la risoluzione dei problemi. Riscrivere il programma in modo da generare messaggi e richieste conformi e testare nuovamente il programma.

Se non è ancora possibile identificare l'origine del problema, contattare il supporto tecnico Microsoft per assistenza. Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa principale del problema. Per ulteriori informazioni, vedere [Abilitazione della traccia WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Download dei filtri Netmon e DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



