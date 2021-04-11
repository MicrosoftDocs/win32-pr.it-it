---
description: Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile nel Windows SDK e Windows Driver Kit (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Strumenti di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131823"
---
# <a name="debugging-tools"></a>Strumenti di debug

Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile nel Windows SDK e Windows Driver Kit (WDK). Questi strumenti possono essere usati per testare le funzionalità delle applicazioni personalizzate scritte in WSDAPI o per i dispositivi e i client scritti usando altri profili di dispositivo per gli stack di servizi Web (DPWS).

\_ \_ Per esaminare le caratteristiche dei client o degli host di DPWS, è possibile usare gli strumenti WSD debug host (wsddebughost.exe) e WSD debug client (wsddebugclient.exe). Possono anche essere usati per risolvere i problemi di connettività o configurazione. Per ulteriori informazioni, vedere la [Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md). Questi strumenti sono disponibili solo nell'SDK. Gli strumenti SDK si trovano nella seguente directory: <Windows SDK Install Folder> \\ bin.

Lo [strumento WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) può essere utilizzato per testare l'interoperabilità a livello SOAP o di trasporto, ovvero garantire che i messaggi siano ben formati. Questo strumento è disponibile solo in WDK.

## <a name="the-wsd-debug-client"></a>Client di debug WSD

Il client di debug WSD (wsddebug \_client.exe) fornisce una console interattiva che può essere usata per inviare e ricevere messaggi di WS-Discovery e per ottenere i metadati. Può inoltre essere utilizzato per generare e utilizzare messaggi multicast non elaborati.

Il client di debug WSD funziona in una delle tre modalità seguenti: multicast, individuazione e metadati.



| Mode      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | In modalità multicast il client di debug WSD Invia e riceve messaggi multicast non formattati sulla porta UDP 3702, come definito in WS-Discovery. L'utente può salvare questi messaggi SOAP in un file di testo e può modificare e ritrasmettere i messaggi con il client di debug WSD.                                                                                                                                 |
| Individuazione | In modalità di individuazione, il client di debug WSD Invia e riceve messaggi formattati WS-Discovery. Può visualizzare i messaggi [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) ricevuti. Può inviare messaggi [Probe](probe-message.md) su UDP o http e [risolvere](resolve-message.md) i messaggi tramite UDP. |
| Metadati  | Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità dei metadati tenta anche di recuperare i metadati dai dispositivi.                                                                                                                                                                                                                                                                    |



 

Per ulteriori informazioni, vedere [utilizzo di un host e di un client generico per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [utilizzo del client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>Host di debug WSD

L'host di debug WSD (wsddebug \_host.exe) fornisce una console interattiva utilizzata per annunciare l'host, rispondere alle richieste dei client e stampare le informazioni di diagnostica.

L'host di debug WSD funziona in una delle due modalità seguenti: individuazione e metadati.



| Mode      | Descrizione                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Individuazione | In modalità di individuazione, l'host di debug WSD stampa i messaggi formattati WS-Discovery. Invia anche messaggi [Hello](hello-message.md) e [bye](bye-message.md) e risponde automaticamente al [Probe](probe-message.md) e alla [risoluzione](resolve-message.md) dei messaggi. |
| Metadati  | Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità metadati annuncia un servizio metadati e consente ai client di connettersi ed eseguire lo scambio di metadati.                                                                                       |



 

Per ulteriori informazioni, vedere [utilizzo di un host e di un client generico per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md) e [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni WSD in Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Strumenti di sviluppo WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



