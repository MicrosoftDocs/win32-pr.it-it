---
title: Gestione delle chiamate asincrone
description: La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro. Il server deve tenere traccia di questo handle e utilizzarlo per inviare la risposta al termine della chiamata asincrona di procedura remota.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396206"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="d5ab3-104">Gestione delle chiamate asincrone</span><span class="sxs-lookup"><span data-stu-id="d5ab3-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="d5ab3-105">La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="d5ab3-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="d5ab3-106">Il server deve tenere traccia di questo handle e utilizzarlo per inviare la risposta al termine della chiamata asincrona di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="d5ab3-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="d5ab3-107">Se il server deve interrompere un RPC asincrono, viene chiamato [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="d5ab3-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="d5ab3-108">Questa funzione esegue la stessa pulizia sul lato server di [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e propaga al client un codice di eccezione (fornito dall'applicazione server), ad eccezione del fatto che non esegue il marshalling degli argomenti out.</span><span class="sxs-lookup"><span data-stu-id="d5ab3-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="d5ab3-109">Per un esempio di una procedura asincrona, vedere [invio della risposta asincrona](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="d5ab3-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




