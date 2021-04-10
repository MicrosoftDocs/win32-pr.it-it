---
description: Dettagli della traccia delle modifiche del catalogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Dettagli della traccia delle modifiche del catalogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130403"
---
# <a name="winsock-catalog-change-tracing-details"></a>Dettagli della traccia delle modifiche del catalogo Winsock

> [!Note]  
> I provider di servizi sovrapposti sono deprecati. A partire da Windows 8 e Windows Server 2012, usare la [piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md).

 

La traccia eventi di modifica del catalogo Winsock per i provider di servizi su più livelli (LSP) è correlata all'installazione di LSP, alla rimozione di LSP, alla disabilitazione di LSP e alla reimpostazione del catalogo Winsock Tutti gli eventi seguenti vengono scritti nel canale *Microsoft-Windows-Winsock-ws2help/Operational* , che è diverso dall'altra traccia degli eventi di rete Winsock registrata in Windows Vista e versioni successive.

Di seguito vengono descritti in dettaglio tutti gli eventi del LSP Winsock che possono essere tracciati e vengono descritti i parametri e le informazioni registrate.

## <a name="lsp-install"></a>Installazione LSP

ID evento = 1

Livello = 4 (informazioni)

Per un'operazione di installazione di LSP vengono tracciati gli eventi LSP seguenti:

-   Una voce di protocollo viene installata nel catalogo Winsock.

Per un evento di installazione LSP vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Il catalogo Winsock (32 bit o 64 bit) in cui viene installato lo LSP. Si tratta di un valore intero che può essere 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione<br/> | Il nome file del modulo dell'applicazione che effettua la chiamata di installazione di LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valore GUID del provider di trasporto Winsock in cui viene installato il LSP.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da installare.<br/>                                |



 

## <a name="lsp-uninstall"></a>Disinstallazione di LSP

ID evento = 2

Livello = 4 (informazioni)

Per un'operazione di disinstallazione di LSP vengono tracciati gli eventi LSP seguenti:

-   Una voce di protocollo viene rimossa dal catalogo Winsock.

Per un evento di disinstallazione LSP vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome dell'oggetto LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Il catalogo Winsock (32 bit o 64 bit) in cui viene rimosso lo LSP. Si tratta di un valore intero che può essere 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione<br/> | Il nome file del modulo dell'applicazione che effettua la chiamata di rimozione LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valore GUID del provider di trasporto Winsock da cui viene rimosso il LSP.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP da rimuovere.<br/>                                |



 

## <a name="lsp-disable"></a>Disabilitazione LSP

ID evento = 3

Livello = 4 (informazioni)

Per un'operazione di disabilitazione di LSP sono tracciati gli eventi LSP seguenti:

-   Una voce di protocollo è disabilitata nel catalogo Winsock.

I parametri seguenti vengono registrati per un evento di disabilitazione LSP:



| Parametro                                                                                                | Descrizione                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | Nome dello LSP ottenuto dal membro **szProtocol** della struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/>         | Il catalogo Winsock (32 bit o 64 bit) in cui lo LSP viene disabilitato. Si tratta di un valore intero che può essere 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installazione<br/> | Il nome file del modulo dell'applicazione che effettua la chiamata di disabilitazione di LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valore GUID del provider di trasporto Winsock in cui lo LSP viene disabilitato.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | Membro **dwCatalogEntryId** della struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per l'oggetto LSP disabilitato.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Reimpostazione del catalogo Winsock

ID evento = 4

Livello = 4 (informazioni)

Per un'operazione di reimpostazione del catalogo Winsock vengono tracciati gli eventi LSP seguenti:

-   Il catalogo Winsock è stato reimpostato.

Per un evento di reimpostazione del catalogo Winsock vengono registrati i parametri seguenti:



| Parametro                                                                                        | Descrizione                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogo<br/> | Il catalogo Winsock (32 bit o 64 bit) che viene reimpostato. Si tratta di un valore intero che può essere 32 o 64.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Dettagli traccia eventi di rete Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
