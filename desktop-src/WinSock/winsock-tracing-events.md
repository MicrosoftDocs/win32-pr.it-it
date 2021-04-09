---
description: Dettagli degli eventi di traccia Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventi di traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129103"
---
# <a name="winsock-tracing-events"></a>Eventi di traccia Winsock

In questa sezione vengono descritte le informazioni dettagliate sui dettagli specifici degli eventi di traccia di Winsock.

La traccia Winsock è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari finali per tracciare alcuni eventi socket di Windows con un sovraccarico minimo. Questa funzionalità consente di migliorare le funzionalità di diagnostica per gli sviluppatori e il supporto tecnico. La traccia eventi di rete Winsock supporta la traccia di operazioni socket per le applicazioni IPv4 e IPv6. La traccia delle modifiche del catalogo Winsock supporta la traccia delle modifiche apportate al catalogo Winsock dai provider di servizi a più livelli (LSP).

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

La traccia Winsock utilizza Event Tracing for Windows (ETW), una funzionalità di traccia a utilizzo generale e ad alta velocità fornita dal sistema operativo. ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel. ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii di applicazioni. Il supporto per la traccia Winsock mediante ETW è stato aggiunto in Windows Vista e versioni successive. Per informazioni generali su ETW, vedere [migliorare il debug e l'ottimizzazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Nell'elenco seguente vengono fornite informazioni dettagliate per ogni evento di traccia Winsock. Per ulteriori informazioni su qualsiasi evento, fare clic sul nome dell'evento.



| Nome evento                                                            | Descrizione                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_creazione evento \_ AFD**](afd-event-create.md)                        | Evento di traccia di rete Winsock per un'operazione di creazione del socket.                            |
| [**\_chiusura evento \_ AFD**](afd-event-close.md)                          | Evento di traccia di rete Winsock per l'operazione di chiusura del socket.                                 |
| [**Installazione di WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-install.md) | Evento di modifica del catalogo Winsock per un'operazione di installazione di un provider di servizi a più livelli (LSP). |
| [**Rimozione di WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-remove.md)   | Evento di modifica del catalogo Winsock per un'operazione di rimozione di un provider di servizi a più livelli (LSP).      |
| [**\_Disabilitare ws2help \_ LSP di Winsock \_**](winsock-ws2help-lsp-disable.md) | Evento di modifica del catalogo Winsock per un'operazione di disabilitazione di un provider di servizi a più livelli (LSP).      |
| [**Reimpostazione di WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-reset.md)     | Evento di modifica del catalogo Winsock per un'operazione di reimpostazione del catalogo Winsock.                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
