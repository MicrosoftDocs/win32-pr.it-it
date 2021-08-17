---
title: API del componente del protocollo WebSocket
description: API del componente del protocollo WebSocket
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a712234f55b0270db9da23dc0efa1da823c85907cca92ac3428cb1225fac8a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134214"
---
# <a name="websocket-protocol-component-api"></a>API del componente del protocollo WebSocket

## <a name="purpose"></a>Scopo

L'API del componente del protocollo WebSocket consente canali di comunicazione bidirezionali asincroni su HTTP che funzionano tra intermediari di rete esistenti. Con l'API del componente del protocollo WebSocket, un client usa HTTP per comunicare con un server e quindi entrambi i lati passano all'uso del protocollo sottostante su cui è stato a livelli HTTP (ad esempio TCP o SSL). L'obiettivo è usare prima HTTP per attraversare gli intermediari di rete e quindi usare il canale TCP/SSL sottostante end-to-end stabilito per la comunicazione bidirezionale dell'applicazione. Il protocollo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) è definito in \] IETF, mentre un'API JavaScript \[ [associata W3CAPI](https://dev.w3.org/html5/websockets/) è definita \] nel W3C.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                          | Descrizione                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipi di dati dell'API del componente del protocollo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | L'API del componente del protocollo WebSocket definisce questi tipi di dati.<br/>   |
| [Enumerazioni api del componente del protocollo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | L'API del componente del protocollo WebSocket definisce queste enumerazioni.<br/> |
| [Funzioni API del componente del protocollo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | L'API del componente del protocollo WebSocket definisce queste funzioni.<br/>    |
| [Strutture dell'API del componente del protocollo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | L'API del componente del protocollo WebSocket definisce queste strutture.<br/>   |



 

## <a name="developer-audience"></a>Sviluppatori

L'API del componente del protocollo WebSocket è progettata per l'uso da parte dei programmatori C/C++. È necessaria una certa familiarità con HTTP Windows rete.

> [!Note]  
> Il modo migliore per usare il protocollo WebSocket in Windows è tramite l'API dei servizi [HTTP di Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o l'Windows. [ Spazio dei nomi Networking.Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API del componente del protocollo WebSocket Windows 8 e versioni successive del Windows operativo. Le API possono essere collegate in modo dinamico tramite websocket.dll.

> [!Note]  
> websocket.dll fornisce il supporto per le intestazioni HTTP correlate all'handshake client e server, verifica i dati di handshake ricevuti e analizza il flusso di dati WebSocket. Non gestisce operazioni specifiche di HTTP (reindirizzamento, autenticazione, supporto proxy) né esegue operazioni di I/O (invio o ricezione di byte del flusso WebSocket).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Windows Servizi HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

