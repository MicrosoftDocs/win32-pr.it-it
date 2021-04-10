---
title: RpcTryExcept (RPC. h)
description: L'istruzione RpcTryExcept fornisce la gestione strutturata delle eccezioni per le applicazioni RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RPC RpcTryExcept
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120235"
---
# <a name="rpctryexcept"></a><span data-ttu-id="a9786-104">RpcTryExcept</span><span class="sxs-lookup"><span data-stu-id="a9786-104">RpcTryExcept</span></span>

<span data-ttu-id="a9786-105">L'istruzione **RpcTryExcept** fornisce la gestione strutturata delle eccezioni per le applicazioni RPC.</span><span class="sxs-lookup"><span data-stu-id="a9786-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="a9786-106">Se una qualsiasi delle istruzioni Program in **RpcTryExcept** genera un'eccezione, vengono eseguite le istruzioni nel blocco di codice [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="a9786-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="a9786-107">Tutte le istruzioni **RpcTryExcept** devono terminare con l'istruzione [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="a9786-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="a9786-108">Per ulteriori informazioni, vedere [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="a9786-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="a9786-109">**Windows Vista e versioni successive di Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) è consigliato per la gestione delle eccezioni strutturata per le eccezioni più comuni come alternativa ai filtri personalizzati con [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="a9786-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9786-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9786-110">Requirements</span></span>



| <span data-ttu-id="a9786-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9786-111">Requirement</span></span> | <span data-ttu-id="a9786-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a9786-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a9786-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9786-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a9786-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9786-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a9786-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9786-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a9786-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9786-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a9786-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9786-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9786-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9786-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9786-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9786-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9786-120">**RpcExcept**</span><span class="sxs-lookup"><span data-stu-id="a9786-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="a9786-121">**RpcExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="a9786-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="a9786-122">**RpcTryFinally**</span><span class="sxs-lookup"><span data-stu-id="a9786-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

