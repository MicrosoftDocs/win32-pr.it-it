---
title: Ricezione della risposta asincrona
description: Dopo la notifica che il server ha inviato una risposta, il client chiama RpcAsyncCompleteCall con l'handle asincrono in modo che possa ricevere la risposta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399601"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="d3dab-103">Ricezione della risposta asincrona</span><span class="sxs-lookup"><span data-stu-id="d3dab-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="d3dab-104">Dopo la notifica che il server ha inviato una risposta, il client chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con l'handle asincrono in modo che possa ricevere la risposta.</span><span class="sxs-lookup"><span data-stu-id="d3dab-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="d3dab-105">Quando **RpcAsyncCompleteCall** è stato completato correttamente, il parametro *Reply* punta a un buffer che contiene il valore restituito della funzione remota.</span><span class="sxs-lookup"><span data-stu-id="d3dab-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="d3dab-106">Tutti i buffer forniti dal programma client come \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ [**in**](/windows/desktop/Midl/in), i parametri **out** \] per la funzione remota asincrona contengono dati validi.</span><span class="sxs-lookup"><span data-stu-id="d3dab-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="d3dab-107">Se il client chiama **RpcAsyncCompleteCall** prima dell'invio della risposta da parte del server, la chiamata avrà esito negativo e restituirà un valore della \_ \_ chiamata asincrona RPC \_ \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="d3dab-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="d3dab-108">Se il programma client usa porte o eventi di completamento di I/O per la notifica, deve chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per rilasciare la porta o il punto di gestione quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="d3dab-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 