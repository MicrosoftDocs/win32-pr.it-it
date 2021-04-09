---
title: API del componente del protocollo WebSocket
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118071"
---
# <a name="websocket-protocol-component-api"></a>API del componente del protocollo WebSocket

## <a name="purpose"></a>Scopo

L'API del componente del protocollo WebSocket consente canali di comunicazione bidirezionali asincroni su HTTP che funzionano tra gli intermediari di rete esistenti. Con l'API del componente del protocollo WebSocket, un client usa HTTP per comunicare con un server e quindi entrambi i lati passano all'uso del protocollo sottostante su cui HTTP è stato sovrapposto (ad esempio TCP o SSL). L'obiettivo è quello di usare il protocollo HTTP per attraversare gli intermediari di rete e quindi usare il canale TCP/SSL sottostante end-to-end per la comunicazione di applicazioni bidirezionali. Il protocollo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] viene definito in IETF, mentre un W3CAPI dell'API JavaScript associato \[ [](https://dev.w3.org/html5/websockets/) \] viene definito in W3C.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                          | Descrizione                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Tipi di dati dell'API del componente del protocollo WebSocket**](web-socket-protocol-component-api-data-types.md)<br/> | L'API del componente del protocollo WebSocket definisce questi tipi di dati.<br/>   |
| [Enumerazioni API del componente del protocollo WebSocket](web-socket-protocol-component-api-enumerations.md)<br/> | L'API del componente del protocollo WebSocket definisce queste enumerazioni.<br/> |
| [Funzioni API del componente del protocollo WebSocket](web-socket-protocol-component-api-functions.md)<br/>       | L'API del componente del protocollo WebSocket definisce queste funzioni.<br/>    |
| [Strutture API del componente del protocollo WebSocket](web-socket-protocol-component-api-structures.md)<br/>     | L'API del componente del protocollo WebSocket definisce queste strutture.<br/>   |



 

## <a name="developer-audience"></a>Sviluppatori

L'API del componente del protocollo WebSocket è progettata per l'uso da parte dei programmatori C/C++. È necessaria una certa familiarità con le funzionalità di rete HTTP e Windows.

> [!Note]  
> Il modo migliore per usare il protocollo WebSocket in Windows è tramite l' [API servizi HTTP Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o lo [spazio dei nomi Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).

 

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API del componente del protocollo WebSocket richiede Windows 8 e versioni successive del sistema operativo Windows. Le API possono essere collegate in modo dinamico tramite websocket.dll.

> [!Note]  
> websocket.dll fornisce il supporto per intestazioni HTTP correlate all'handshake client e server, verifica i dati di handshake ricevuti e analizza il flusso di dati WebSocket. Non gestisce operazioni specifiche di HTTP (Reindirizzamento, autenticazione, supporto del proxy) né eseguire operazioni di I/O (invio o ricezione di byte di flusso WebSocket).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HTTP](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[Servizi HTTP di Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

