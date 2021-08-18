---
description: Informazioni sull'analisi delle tracce di rete con l'individuazione diretta. Un analizzatore di pacchetti di rete che visualizza pacchetti non elaborati può esaminare le richieste di scambio di metadati HTTP.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Controllo delle tracce di rete per le applicazioni tramite individuazione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f8e96778b2d75f511c625073ef1d0bbc30dd4c815a327f42432abd0d221756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991731"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a>Controllo delle tracce di rete per le applicazioni tramite individuazione diretta

Qualsiasi analizzatore di pacchetti di rete in grado di visualizzare pacchetti non elaborati può essere usato per esaminare le richieste di scambio di metadati HTTP. Microsoft Network Monitor 3 (Netmon) è consigliato. Per altre informazioni su Netmon, vedere [Download di Netmon e filtri DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)

**Per esaminare le tracce di rete per l'individuazione diretta**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Installare l'analizzatore pacchetti (Netmon) nel client o nell'host.
3.  Configurare l'analizzatore pacchetti per acquisire il traffico sulla scheda di rete che connette l'host e il client.
4.  Riprodurre l'errore avviando l'host e il client o premendo F5 nel Esplora rete.
5.  Filtrare i risultati per isolare WS-Discovery traffico di scambio dei metadati. Per visualizzare i filtri Netmon di esempio, vedere [Download dei filtri Netmon e DPWS di esempio.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Questo passaggio è facoltativo.

     

6.  Verificare che i messaggi inviati tra client e host soddisfino i requisiti di traffico di base.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verifica che i messaggi soddisfino i requisiti di traffico

I client e gli host WSDAPI devono inviare messaggi conformi ai criteri seguenti. Per informazioni generali sui modelli di messaggio, vedere [Individuazione e metadati Exchange modelli di messaggio.](discovery-and-metadata-exchange-message-patterns.md)

-   [I](probe-message.md) messaggi probe devono essere inviati tramite HTTP o HTTPS, in genere alla porta 5357 o 5358.
-   **L'elemento** Types di [un messaggio Probe](probe-message.md) deve essere presente e non deve essere vuoto. Deve contenere i tipi a cui risponderà un host.
-   Un [messaggio ProbeMatches](probematches-message.md) deve essere inviato alla porta HTTP o HTTPS da cui [è](probe-message.md) stato inviato il probe.
-   **L'elemento RelatesTo** di [un messaggio ProbeMatches](probematches-message.md) deve essere presente e non deve essere vuoto. Il valore deve corrispondere al valore **dell'elemento MessageId** del messaggio [Probe](probe-message.md) corrispondente.
-   Se nel messaggio [ProbeMatches](probematches-message.md) è stato incluso un elemento **XAddrs,** è necessario convalidare gli indirizzi di trasporto forniti. Per altre informazioni, vedere [Regole di convalida XAddr.](xaddr-validation-rules.md)
-   Un [messaggio ProbeMatches](probematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Probe](probe-message.md) corrispondente. Il Windows firewall può eliminare un messaggio ProbeMatches inviato più di 4 secondi dopo un messaggio probe.
-   Se non è stato incluso alcun elemento **XAddrs** nel messaggio [ProbeMatches](probematches-message.md) e il client o l'host invierà un messaggio HTTP ,ad esempio una richiesta di scambio di metadati [Get](get--metadata-exchange--http-request-and-message.md) o un messaggio del servizio, il client o l'host deve inviare un messaggio [Resolve](resolve-message.md) tramite HTTP o HTTPS. Questo messaggio viene in genere inviato alla porta 5357 o 5358.
-   Se viene [inviato](resolve-message.md) un messaggio Resolve, è necessario inviare un messaggio [ResolveMatches](resolvematches-message.md) alla porta HTTP o HTTPS da cui è stato inviato il messaggio Resolve.
-   Un [messaggio ResolveMatches](resolvematches-message.md) deve essere inviato entro 4 secondi dal messaggio [Resolve](resolve-message.md) corrispondente. Il Windows firewall può eliminare un messaggio ResolveMatches inviato più di 4 secondi dopo un messaggio di risoluzione.

Se i messaggi inviati dal programma non sono conformi a questi requisiti, la causa del problema è stata identificata correttamente e non sono necessarie ulteriori procedure di risoluzione dei problemi. Riscrivere il programma in modo che generi messaggi conformi e ripetere il programma.

Se l'origine del problema non può ancora essere identificata, contattare il supporto tecnico Microsoft per assistenza. Prima di contattare il supporto tecnico, raccogliere i file di log appropriati per identificare la causa radice del problema. Per altre informazioni, vedere [Abilitazione della traccia WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi relativi alle applicazioni che usano l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Download di Netmon e dei filtri DPWS di esempio](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



