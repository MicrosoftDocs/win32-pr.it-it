---
title: RpcTryFinally (RPC. h)
description: L'istruzione RpcTryFinally fornisce la gestione strutturata della terminazione.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477506"
---
# <a name="rpctryfinally"></a><span data-ttu-id="3c561-104">RpcTryFinally</span><span class="sxs-lookup"><span data-stu-id="3c561-104">RpcTryFinally</span></span>

<span data-ttu-id="3c561-105">L'istruzione **RpcTryFinally** fornisce la gestione strutturata della terminazione.</span><span class="sxs-lookup"><span data-stu-id="3c561-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="3c561-106">Si verifica un'eccezione durante le istruzioni di esecuzione del blocco di codice associato all'istruzione **RpcTryFinally** , le istruzioni nel blocco di codice associate all'istruzione [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) vengono eseguite.</span><span class="sxs-lookup"><span data-stu-id="3c561-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="3c561-107">Tutte le istruzioni **RpcTryFinally** devono terminare con un'istruzione [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="3c561-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="3c561-108">Per ulteriori informazioni, vedere [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="3c561-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c561-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c561-109">Requirements</span></span>



| <span data-ttu-id="3c561-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c561-110">Requirement</span></span> | <span data-ttu-id="3c561-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3c561-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c561-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c561-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3c561-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c561-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c561-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c561-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3c561-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c561-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c561-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c561-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c561-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c561-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c561-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c561-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c561-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="3c561-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="3c561-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="3c561-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

