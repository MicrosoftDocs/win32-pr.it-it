---
description: Dettagli traccia modifiche catalogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Dettagli traccia modifiche catalogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d949caf94d3b7bbbef32945c97cb3f1db258f798b84280570712ef5299cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051339"
---
# <a name="winsock-catalog-change-tracing-details"></a>Dettagli traccia modifiche catalogo Winsock

> [!Note]  
> I provider di servizi su più livelli sono deprecati. A partire da Windows 8 e Windows Server 2012, usare [Windows Filtering Platform.](../fwp/windows-filtering-platform-start-page.md)

 

La traccia eventi di modifica del catalogo Winsock per provider di servizi a livelli (LSP, Layered Service Provider) è correlata alle operazioni di installazione, rimozione di LSP, disabilitazione LSP e reimpostazione del catalogo Winsock. Tutti gli eventi seguenti vengono scritti nel canale *Microsoft-Windows-Winsock-WS2HELP/Operational,* che è diverso dall'altra traccia eventi di rete Winsock registrata in Windows Vista e versioni successive.

Di seguito viene descritto in dettaglio ogni evento LSP di Winsock che è possibile tracciare e vengono descritti i parametri e le informazioni registrati.

## <a name="lsp-install"></a>Installazione LSP

ID evento = 1

Livello = 4 (informazioni)

Per un'operazione di installazione LSP vengono tracciati gli eventi LSP Winsock seguenti:

-   Nel catalogo Winsock viene installata una voce di protocollo.

Per un evento di installazione LSP vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome dell'LSP ottenuto dal membro **szProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da installare.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Catalogo di Winsock (a 32 bit o a 64 bit) in cui viene installato LSP. Si tratta di un valore intero che è 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Nome del modulo dell'applicazione che effettua la chiamata di installazione LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Valore GUID del provider di trasporto Winsock in cui viene installato l'LSP.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da installare.<br/>                                |



 

## <a name="lsp-uninstall"></a>Disinstallazione di LSP

ID evento = 2

Livello = 4 (informazioni)

Per un'operazione di disinstallazione LSP vengono tracciati gli eventi LSP Winsock seguenti:

-   Una voce di protocollo viene rimossa dal catalogo Winsock.

Per un evento di disinstallazione LSP vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome dell'LSP ottenuto dal membro **szProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da rimuovere.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Catalogo Di Winsock (a 32 bit o a 64 bit) in cui viene rimosso il provider di servizi di rete. Si tratta di un valore intero che è 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Nome del modulo dell'applicazione che effettua la chiamata di rimozione dell'LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Valore GUID del provider di trasporto Winsock da cui viene rimosso l'LSP.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP da rimuovere.<br/>                                |



 

## <a name="lsp-disable"></a>LSP Disable

ID evento = 3

Livello = 4 (informazioni)

Per un'operazione di disabilitazione LSP vengono tracciati gli eventi LSP Winsock seguenti:

-   Una voce di protocollo è disabilitata nel catalogo Winsock.

Per un evento di disabilitazione LSP vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome del provider di servizi di rete ottenuto dal membro **szProtocol** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP disabilitato.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Catalogo Di Winsock (a 32 bit o a 64 bit) in cui viene disabilitato il provider di servizi di rete. Si tratta di un valore intero che è 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Nome del modulo dell'applicazione che effettua la chiamata di disabilitazione LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Valore GUID del provider di trasporto Winsock in cui viene disabilitato l'LSP.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'LSP disabilitato.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Reimpostazione del catalogo Winsock

ID evento = 4

Livello = 4 (informazioni)

Per un'operazione di reimpostazione del catalogo Winsock vengono tracciati gli eventi LSP Winsock seguenti:

-   Il catalogo Winsock viene reimpostato.

Per un evento di reimpostazione del catalogo Winsock vengono registrati i parametri seguenti:



| Parametro                                                                                        | Descrizione                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/> | Catalogo Winsock (a 32 bit o a 64 bit) da reimpostare. Si tratta di un valore intero che è 32 o 64.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della traccia winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia di Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli di Traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
