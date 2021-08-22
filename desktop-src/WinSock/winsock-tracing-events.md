---
description: Dettagli degli eventi di traccia winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventi di traccia winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b2f36991a187d32359694956efcc7b7e3243ac17efd769db454848b5f87e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821985"
---
# <a name="winsock-tracing-events"></a>Eventi di traccia winsock

In questa sezione vengono descritte informazioni dettagliate sugli eventi di traccia di Winsock specifici.

La traccia Winsock è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari di vendita al dettaglio per tracciare determinati eventi Windows socket con sovraccarico minimo. Questa funzionalità consente di migliorare le funzionalità di diagnostica per gli sviluppatori e il supporto tecnico del prodotto. La traccia degli eventi di rete Winsock supporta le operazioni socket di traccia per le applicazioni IPv4 e IPv6. La traccia delle modifiche del catalogo Winsock supporta la traccia delle modifiche apportate al catalogo Winsock dai provider di servizi a più livelli.

> [!Note]  
> I provider di servizi a più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).

 

La traccia Winsock usa Event Tracing for Windows (ETW), una funzionalità di traccia ad alta velocità per utilizzo generico fornita dal sistema operativo. ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel. ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di traccia dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii dell'applicazione. Il supporto per la traccia Winsock con ETW è stato aggiunto Windows Vista e versioni successive. Per informazioni generali su ETW, vedere Migliorare il [debug e l'ottimizzazione delle prestazioni con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

L'elenco seguente fornisce informazioni dettagliate per ogni evento di traccia Winsock. Per altre informazioni su qualsiasi evento, fare clic sul nome dell'evento.



| Nome evento                                                            | Descrizione                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CREAZIONE DI EVENTI AFD \_ \_**](afd-event-create.md)                        | Evento di traccia di rete Winsock per un'operazione di creazione di socket.                            |
| [**AFD \_ EVENT \_ CLOSE**](afd-event-close.md)                          | Evento di traccia di rete Winsock per l'operazione di chiusura del socket.                                 |
| [**INSTALLAZIONE DI WINSOCK \_ WS2HELP \_ \_ LSP**](winsock-ws2help-lsp-install.md) | Evento di modifica del catalogo Winsock per un'operazione di installazione LSP (Layered Service Provider). |
| [**WINSOCK \_ WS2HELP \_ LSP \_ REMOVE**](winsock-ws2help-lsp-remove.md)   | Evento di modifica del catalogo Winsock per un'operazione di rimozione del provider di servizi a più livelli( LSP).      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ DISABLE**](winsock-ws2help-lsp-disable.md) | Evento di modifica del catalogo Winsock per un'operazione di disabilitazione del provider di servizi a più livelli (LSP).      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ RESET**](winsock-ws2help-lsp-reset.md)     | Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Dettagli di traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
