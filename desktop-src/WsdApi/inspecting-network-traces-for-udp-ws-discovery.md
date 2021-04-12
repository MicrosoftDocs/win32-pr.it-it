---
description: Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per ispezionare i pacchetti WS-Discovery UDP. È consigliabile Microsoft Network Monitor 3 (Netmon). Per ulteriori informazioni su Netmon, vedere Download di Netmon e Sample DPWS filters.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Controllo delle tracce di rete per UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231816"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Controllo delle tracce di rete per UDP WS-Discovery

Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per ispezionare i pacchetti WS-Discovery UDP. È consigliabile Microsoft Network Monitor 3 (Netmon). Per ulteriori informazioni su Netmon, vedere [download di Netmon e Sample DPWS filters](downloading-netmon-and-sample-dpws-filters.md).

**Per esaminare le tracce di rete per UDP WS-Discovery**

1.  Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).
2.  Installare Packet Analyzer (Netmon) nel client o nell'host.
3.  Configurare l'analizzatore di pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.
4.  Riprodurre l'errore avviando l'host e il client o premendo F5 in Network Explorer.
5.  Filtrare i risultati per isolare il traffico WS-Discovery. Per visualizzare i filtri Netmon di esempio, vedere [download di Netmon e Sample DPWS filters](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Questo passaggio è facoltativo.

     

6.  Verificare che i messaggi inviati tra il client e l'host soddisfino i requisiti di traffico di base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verifica per verificare se i messaggi soddisfano i requisiti di traffico

I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti. Per informazioni generali sui modelli di messaggio, vedere [modelli di messaggio di scambio di metadati e individuazione](discovery-and-metadata-exchange-message-patterns.md).

-   I messaggi [Probe](probe-message.md) devono essere inviati dal multicast UDP alla porta 3702.
-   L'elemento **types** di un messaggio [Probe](probe-message.md) deve essere presente e non deve essere vuoto. Deve contenere i tipi a cui un host risponderà.
-   È necessario inviare un messaggio [ProbeMatches](probematches-message.md) unicast alla porta UDP da cui è stato inviato il [Probe](probe-message.md) .
-   L'elemento **Repiù recente** di un messaggio [ProbeMatches](probematches-message.md) deve essere presente e non deve essere vuoto. Il valore deve corrispondere al valore dell'elemento **MessageID** del messaggio [Probe](probe-message.md) corrispondente.
-   Se nel messaggio [ProbeMatches](probematches-message.md) è stato incluso un elemento **XAddrs** , è necessario convalidare gli indirizzi di trasporto specificati. Per altre informazioni, vedere [XAddr validation rules](xaddr-validation-rules.md).
-   Un messaggio [ProbeMatches](probematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Probe](probe-message.md) corrispondente. Il Windows Firewall può rilasciare un messaggio ProbeMatches inviato più di 4 secondi dopo un messaggio Probe.
-   Se non è stato incluso alcun elemento **XAddrs** nel messaggio [ProbeMatches](probematches-message.md) e il client o l'host invierà un messaggio http (ad esempio, una richiesta [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange o un messaggio di servizio), il client o l'host deve inviare un messaggio di [risoluzione](resolve-message.md) tramite multicast UDP alla porta 3702.
-   Se viene inviato un messaggio di [risoluzione](resolve-message.md) , è necessario inviare un messaggio [ResolveMatches](resolvematches-message.md) unicast alla porta UDP dalla quale è stato inviato il messaggio di risoluzione.
-   È necessario inviare un messaggio [ResolveMatches](resolvematches-message.md) entro 4 secondi dal messaggio di [risoluzione](resolve-message.md) corrispondente. Il Windows Firewall può eliminare un ResolveMatchesmessage inviato più di 4 secondi dopo un messaggio di risoluzione.

Se i messaggi inviati dal programma non sono conformi ai requisiti del messaggio, la causa del problema è stata identificata correttamente e non è necessario eseguire ulteriori passaggi per la risoluzione dei problemi. Riscrivere il programma in modo da generare messaggi conformi e testare nuovamente il programma.

Se non è ancora possibile identificare l'origine del problema, contattare il supporto tecnico Microsoft per assistenza. Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa principale del problema. Per ulteriori informazioni, vedere [Abilitazione della traccia WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Download dei filtri Netmon e DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



