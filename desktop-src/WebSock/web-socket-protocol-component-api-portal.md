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
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="840db-103">API del componente del protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="840db-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="840db-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="840db-104">Purpose</span></span>

<span data-ttu-id="840db-105">L'API del componente del protocollo WebSocket consente canali di comunicazione bidirezionali asincroni su HTTP che funzionano tra gli intermediari di rete esistenti.</span><span class="sxs-lookup"><span data-stu-id="840db-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="840db-106">Con l'API del componente del protocollo WebSocket, un client usa HTTP per comunicare con un server e quindi entrambi i lati passano all'uso del protocollo sottostante su cui HTTP è stato sovrapposto (ad esempio TCP o SSL).</span><span class="sxs-lookup"><span data-stu-id="840db-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="840db-107">L'obiettivo è quello di usare il protocollo HTTP per attraversare gli intermediari di rete e quindi usare il canale TCP/SSL sottostante end-to-end per la comunicazione di applicazioni bidirezionali.</span><span class="sxs-lookup"><span data-stu-id="840db-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="840db-108">Il protocollo WebSocket \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) \] viene definito in IETF, mentre un W3CAPI dell'API JavaScript associato \[ [](https://dev.w3.org/html5/websockets/) \] viene definito in W3C.</span><span class="sxs-lookup"><span data-stu-id="840db-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="840db-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="840db-109">In this section</span></span>



| <span data-ttu-id="840db-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="840db-110">Topic</span></span>                                                                                                          | <span data-ttu-id="840db-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="840db-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="840db-112">**Tipi di dati dell'API del componente del protocollo WebSocket**</span><span class="sxs-lookup"><span data-stu-id="840db-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="840db-113">L'API del componente del protocollo WebSocket definisce questi tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="840db-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="840db-114">Enumerazioni API del componente del protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="840db-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="840db-115">L'API del componente del protocollo WebSocket definisce queste enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="840db-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="840db-116">Funzioni API del componente del protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="840db-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="840db-117">L'API del componente del protocollo WebSocket definisce queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="840db-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="840db-118">Strutture API del componente del protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="840db-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="840db-119">L'API del componente del protocollo WebSocket definisce queste strutture.</span><span class="sxs-lookup"><span data-stu-id="840db-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="840db-120">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="840db-120">Developer audience</span></span>

<span data-ttu-id="840db-121">L'API del componente del protocollo WebSocket è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="840db-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="840db-122">È necessaria una certa familiarità con le funzionalità di rete HTTP e Windows.</span><span class="sxs-lookup"><span data-stu-id="840db-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="840db-123">Il modo migliore per usare il protocollo WebSocket in Windows è tramite l' [API servizi HTTP Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) o lo [spazio dei nomi Windows. Networking. Sockets](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="840db-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="840db-124">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="840db-124">Run-time requirements</span></span>

<span data-ttu-id="840db-125">L'API del componente del protocollo WebSocket richiede Windows 8 e versioni successive del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="840db-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="840db-126">Le API possono essere collegate in modo dinamico tramite websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="840db-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="840db-127">websocket.dll fornisce il supporto per intestazioni HTTP correlate all'handshake client e server, verifica i dati di handshake ricevuti e analizza il flusso di dati WebSocket.</span><span class="sxs-lookup"><span data-stu-id="840db-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="840db-128">Non gestisce operazioni specifiche di HTTP (Reindirizzamento, autenticazione, supporto del proxy) né eseguire operazioni di I/O (invio o ricezione di byte di flusso WebSocket).</span><span class="sxs-lookup"><span data-stu-id="840db-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="840db-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="840db-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="840db-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="840db-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="840db-131">Servizi HTTP di Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="840db-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

