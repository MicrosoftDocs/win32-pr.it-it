---
description: Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per esaminare i WS-Discovery UDP. Microsoft Network Monitor 3 (Netmon) è consigliato. Per altre informazioni su Netmon, vedere Download di Netmon e filtri DPWS di esempio.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Controllo delle tracce di rete per le WS-Discovery UDP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce21e2943a37640eb091aa03c02eba0886164166b2959e31e897ee788424cd41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920755"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Controllo delle tracce di rete per le WS-Discovery UDP

Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per esaminare i WS-Discovery UDP. Microsoft Network Monitor 3 (Netmon) è consigliato. Per altre informazioni su Netmon, vedere [Download di Netmon e filtri DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)

**Per esaminare le tracce di rete per UDP WS-Discovery**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Installare l'analizzatore pacchetti (Netmon) nel client o nell'host.
3.  Configurare l'analizzatore pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.
4.  Riprodurre l'errore avviando l'host e il client o premendo F5 nel Esplora rete.
5.  Filtrare i risultati per isolare WS-Discovery traffico. Per visualizzare i filtri Netmon di esempio, vedere [Download dei filtri Netmon e DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Questo passaggio è facoltativo.

     

6.  Verificare che i messaggi inviati tra client e host soddisfino i requisiti di traffico di base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verifica che i messaggi soddisfino i requisiti di traffico

I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti. Per informazioni generali sui modelli di messaggio, vedere [Individuazione e metadati Exchange modelli di messaggio.](discovery-and-metadata-exchange-message-patterns.md)

-   [I](probe-message.md) messaggi probe devono essere inviati dal multicast UDP alla porta 3702.
-   **L'elemento** Types di [un messaggio Probe](probe-message.md) deve essere presente e non deve essere vuoto. Deve contenere i tipi a cui risponderà un host.
-   Un [messaggio ProbeMatches](probematches-message.md) deve essere inviato unicast alla porta UDP da cui è [stato](probe-message.md) inviato il probe.
-   **L'elemento RelatesTo** di [un messaggio ProbeMatches](probematches-message.md) deve essere presente e non deve essere vuoto. Il valore deve corrispondere al valore **dell'elemento MessageId** del messaggio [Probe](probe-message.md) corrispondente.
-   Se nel messaggio [ProbeMatches](probematches-message.md) è stato incluso un elemento **XAddrs,** è necessario convalidare gli indirizzi di trasporto forniti. Per altre informazioni, vedere [Regole di convalida XAddr.](xaddr-validation-rules.md)
-   Un [messaggio ProbeMatches](probematches-message.md) deve essere inviato entro 4 secondi dal messaggio [probe](probe-message.md) corrispondente. Il Windows firewall può eliminare un messaggio ProbeMatches inviato più di 4 secondi dopo un messaggio probe.
-   Se non è stato incluso alcun elemento **XAddrs** nel messaggio [ProbeMatches](probematches-message.md) e il client o l'host invierà un messaggio HTTP ,ad esempio una richiesta di scambio di metadati [Get](get--metadata-exchange--http-request-and-message.md) o un messaggio del servizio, il client o l'host deve inviare un messaggio [Resolve](resolve-message.md) tramite multicast UDP alla porta 3702.
-   Se viene [inviato](resolve-message.md) un messaggio Resolve, è necessario inviare un messaggio [ResolveMatches](resolvematches-message.md) unicast alla porta UDP da cui è stato inviato il messaggio Resolve.
-   Un [messaggio ResolveMatches](resolvematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Resolve](resolve-message.md) corrispondente. Il Windows firewall può eliminare un messaggio ResolveMatches inviato più di 4 secondi dopo un messaggio di risoluzione.

Se i messaggi inviati dal programma non sono conformi a questi requisiti, la causa del problema è stata identificata correttamente e non sono necessarie ulteriori procedure di risoluzione dei problemi. Riscrivere il programma in modo che generi messaggi conformi e ripetere il programma.

Se l'origine del problema non può ancora essere identificata, contattare il supporto tecnico Microsoft per assistenza. Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa radice del problema. Per altre informazioni, vedere [Abilitazione della traccia WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Download di Netmon e dei filtri DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



