---
description: 'Altre informazioni su: macro API cabinet'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macro API cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522866"
---
# <a name="cabinet-api-macros"></a>Macro API cabinet

Questa sezione illustra in dettaglio le macro usate dall'API CAB:

## <a name="fci-macros"></a>Macro FCI

Le macro seguenti vengono usate dall'istanza FCI:



| Macro                                              | Descrizione                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Usato per allocare memoria in un contesto dell'istanza del cluster di failover.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Utilizzato per chiudere un file.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Utilizzato per eliminare un file.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Utilizzato per notificare quando un file viene inserito nell'archivio.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Utilizzato per liberare la memoria allocata in precedenza in un contesto dell'istanza FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Utilizzato per richiedere informazioni per il file CAB successivo.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Utilizzato per aprire un file e recuperare la data, l'ora e gli attributi del file.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Utilizzato per ottenere un nome di file temporaneo.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Utilizzato per aprire un file in un contesto dell'istanza del cluster di failover.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Utilizzato per leggere i dati da un file.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Utilizzato per spostare un puntatore di file in una posizione specificata.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Utilizzato per aggiornare l'utente.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Utilizzato per scrivere i dati in un file.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Converte le dimensioni di Windows in un valore LXZ TCOMP per [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).<br/> |



 

## <a name="fdi-macros"></a>Macro IDE

Le macro seguenti vengono usate da IDE:



| Macro                              | Descrizione                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Usato per allocare memoria in un contesto IDE.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Usato per chiudere un file in un contesto IDE.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Utilizzato per aggiornare l'applicazione sullo stato del decodificatore.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Usato per liberare la memoria allocata in precedenza in un contesto IDE.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Utilizzato per aprire un file in un contesto IDE.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Usato per leggere i dati da un file in un contesto IDE.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Usato per spostare un puntatore di file nella posizione specificata in un contesto IDE.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Usato per scrivere i dati in un file in un contesto IDE.<br/>                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'API cabinet](cabinet-api-reference.md)
</dt> <dt>

[Uso dell'API cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




