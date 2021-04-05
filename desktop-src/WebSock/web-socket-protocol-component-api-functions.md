---
title: Funzioni API del componente del protocollo WebSocket
description: L'API del componente del protocollo WebSocket definisce queste funzioni.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d778fef6680112007b0f4a459787a51eb20bfe0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728783"
---
# <a name="websocket-protocol-component-api-functions"></a>Funzioni API del componente del protocollo WebSocket

L'API del componente del protocollo WebSocket definisce queste funzioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | interrompe un handle di sessione WebSocket creato da [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | inizia l'handshake lato client.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | inizia l'handshake lato server.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | completa un'azione avviata da [**WebSocketGetAction**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction).<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | Crea un handle di sessione WebSocket lato client.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | Crea un handle di sessione WebSocket sul lato server.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | Elimina un handle di sessione WebSocket creato da [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | completa l'handshake lato client.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | completa l'handshake lato server.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | Restituisce un'azione da una chiamata a [**WebSocketSend**](/windows/desktop/api/websocket/nf-websocket-websocketsend), [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) o [**WebSocketCompleteAction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction).<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | Ottiene una singola Proprietà WebSocket.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | aggiunge un'operazione di ricezione alla coda dell'operazione del componente del protocollo.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | aggiunge un'operazione di invio alla coda dell'operazione del componente del protocollo.<br/>                                                                                                                                 |



 

 

