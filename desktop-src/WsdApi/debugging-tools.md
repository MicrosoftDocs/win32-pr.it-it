---
description: Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile in Windows SDK e Windows Driver Kit (WDK).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Strumenti di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e744b37a5376d228ac9023ed7556ce63e26a7a1c20b23fb98aff090e7ae9616f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856781"
---
# <a name="debugging-tools"></a>Strumenti di debug

Un set di strumenti di debug basato su Web Services on Devices API (WSDAPI) è disponibile in Windows SDK e Windows Driver Kit (WDK). Questi strumenti possono essere usati per testare la funzionalità delle applicazioni personalizzate scritte in WSDAPI o di dispositivi e client scritti usando altri stack DPWS (Device Profile for Web Services).

Gli strumenti WSD Debug Host (wsddebughost.exe) e \_ WSD Debug Client (wsddebugclient.exe) possono essere usati per esaminare le caratteristiche di client o host \_ DPWS. Possono anche essere usati per risolvere i problemi di connettività o configurazione. Per altre informazioni, vedere Guida alla risoluzione dei problemi di [WSDAPI.](wsdapi-troubleshooting-guide.md) Questi strumenti sono disponibili solo nell'SDK. Gli strumenti SDK si trovano nella directory seguente: <Windows SDK Install Folder> \\ Bin.

[WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) può essere usato per testare l'interoperabilità a livello DI SOAP o a livello di trasporto, ovvero assicurando che i messaggi siano ben formati. Questo strumento è disponibile solo in WDK.

## <a name="the-wsd-debug-client"></a>Client di debug WSD

WSD Debug Client (wsddebugclient.exe) fornisce una console interattiva che può essere usata per inviare e ricevere WS-Discovery messaggi e per ottenere \_ i metadati. Può anche essere usato per generare e utilizzare messaggi multicast non elaborati.

Il client di debug WSD opera in una delle tre modalità seguenti: multicast, individuazione e metadati.



| Mode      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | In modalità multicast, il client di debug WSD invia e riceve messaggi multicast non formattati sulla porta UDP 3702, come definito in WS-Discovery. L'utente può salvare questi messaggi SOAP in un file di testo e modificare e ritrasinviare nuovamente i messaggi con il client di debug WSD.                                                                                                                                 |
| Individuazione | In modalità di individuazione, il client di debug WSD invia e riceve messaggi WS-Discovery messaggi. Può visualizzare i messaggi [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) ricevuti. Può inviare [messaggi probe](probe-message.md) tramite UDP o HTTP e [risolvere i](resolve-message.md) messaggi tramite UDP. |
| Metadati  | Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità metadati tenta anche di recuperare i metadati dai dispositivi.                                                                                                                                                                                                                                                                    |



 

Per altre informazioni, vedere Using [a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), Using a Generic Host and Client for UDP [WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>Host di debug WSD

L'host di debug WSD (wsddebughost.exe) fornisce una console interattiva usata per annunciare l'host, rispondere alle richieste client e stampare \_ informazioni di diagnostica.

L'host di debug WSD opera in una delle due modalità seguenti: individuazione e metadati.



| Mode      | Descrizione                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Individuazione | In modalità di individuazione, l'host di debug WSD stampa i WS-Discovery messaggi. Invia anche messaggi [Hello](hello-message.md) [e Bye](bye-message.md) e risponde automaticamente ai [messaggi Probe](probe-message.md) [e Resolve.](resolve-message.md) |
| Metadati  | Oltre a implementare tutte le funzionalità della modalità di individuazione, la modalità metadati annuncia un servizio metadati e consente ai client di connettersi ed eseguire lo scambio di metadati.                                                                                       |



 

Per altre informazioni, vedere [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) e Using a Generic Host and Client for UDP [WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni WSD in Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Strumenti di sviluppo WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



