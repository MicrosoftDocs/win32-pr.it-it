---
title: Funzioni API dei componenti del protocollo WebSocket
description: L'API Componente del protocollo WebSocket definisce queste funzioni.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d88a4ef8eb9caa0e409d0ded60b6dffd2717dc74d1b2cdddeb08ee6d9de08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330339"
---
# <a name="websocket-protocol-component-api-functions"></a>Funzioni API dei componenti del protocollo WebSocket

L'API Componente del protocollo WebSocket definisce queste funzioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | interrompe un handle di sessione WebSocket creato [**da WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | avvia l'handshake sul lato client.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | avvia l'handshake sul lato server.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | completa un'azione avviata [**da WebSocketGetAction.**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction)<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | crea un handle di sessione WebSocket sul lato client.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | crea un handle di sessione WebSocket sul lato server.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | elimina un handle di sessione WebSocket creato [**da WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | completa l'handshake sul lato client.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | completa l'handshake sul lato server.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | restituisce un'azione da una chiamata a [**WebSocketSend,**](/windows/desktop/api/websocket/nf-websocket-websocketsend) [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) [**o WebSocketCompleteAction.**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction)<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | ottiene una singola proprietà WebSocket.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | aggiunge un'operazione di ricezione alla coda delle operazioni del componente del protocollo.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | aggiunge un'operazione di invio alla coda delle operazioni del componente del protocollo.<br/>                                                                                                                                 |



 

 

