---
description: "Altre informazioni su: Macro dell'API Cabinet"
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macro dell'API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525ec84e3e857c4819b1689cade2ed0f7267dffbd8a0e0da02251a03f8d4a36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668269"
---
# <a name="cabinet-api-macros"></a>Macro dell'API Cabinet

In questa sezione vengono fornite informazioni dettagliate sulle macro usate dall'API Cabinet:

## <a name="fci-macros"></a>Macro FCI

Le macro seguenti vengono usate dall'FCI:



| Macro                                              | Descrizione                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Usato per allocare memoria in un contesto FCI.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Usato per chiudere un file.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Usato per eliminare un file.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Utilizzato per inviare una notifica quando un file viene inserito nell'archivio.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Usato per liberare memoria allocata in precedenza in un contesto FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Usato per richiedere informazioni per l'archivio successivo.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Usato per aprire un file e recuperare la data, l'ora e gli attributi del file.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Usato per ottenere un nome di file temporaneo.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Usato per aprire un file in un contesto FCI.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Usato per leggere i dati da un file.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Usato per spostare un puntatore di file in un percorso specificato.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Usato per aggiornare l'utente.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Usato per scrivere dati in un file.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Converte le dimensioni delle finestre in un valore TCOMP LXZ per [**FCIAddFile.**](/windows/desktop/api/Fci/nf-fci-fciaddfile)<br/> |



 

## <a name="fdi-macros"></a>Macro FDI

Le macro seguenti vengono usate da FDI:



| Macro                              | Descrizione                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Usato per allocare memoria in un contesto FDI.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Utilizzato per chiudere un file in un contesto FDI.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Usato per aggiornare l'applicazione sullo stato del decodificatore.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Usato per liberare memoria allocata in precedenza in un contesto FDI.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Usato per aprire un file in un contesto FDI.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Usato per leggere dati da un file in un contesto FDI.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Utilizzato per spostare un puntatore di file nel percorso specificato in un contesto FDI.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Usato per scrivere dati in un file in un contesto FDI.<br/>                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API cabinet](cabinet-api-reference.md)
</dt> <dt>

[Uso dell'API Cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




