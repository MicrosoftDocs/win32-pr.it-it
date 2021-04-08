---
title: Propagazione delle informazioni sugli errori
description: La propagazione delle informazioni dettagliate sugli errori consente ai server che ricevono un \_ \_ errore RPC o a qualsiasi altro codice di errore, per consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai chiamanti.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856669"
---
# <a name="propagating-error-information"></a><span data-ttu-id="5edbf-103">Propagazione delle informazioni sugli errori</span><span class="sxs-lookup"><span data-stu-id="5edbf-103">Propagating Error Information</span></span>

<span data-ttu-id="5edbf-104">La propagazione delle informazioni estese sugli errori consente ai server che ricevono un errore di RPC \_ \_ \* o a qualsiasi altro codice di errore, per consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai chiamanti.</span><span class="sxs-lookup"><span data-stu-id="5edbf-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="5edbf-105">Tutto il server deve eseguire la chiamata a [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) quando si verifica un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="5edbf-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="5edbf-106">Il tempo di esecuzione RPC gestisce il concatenamento delle informazioni di errore estese, se presenti, causando l'errore irreversibile nel segnalare l'errore irreversibile, purché il codice di errore assegnato a **RpcRaiseException** o **RpcAsyncAbortCall** sia uguale al codice di errore che ha causato l'errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="5edbf-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




