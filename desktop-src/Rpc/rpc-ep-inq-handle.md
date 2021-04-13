---
title: RPC_EP_INQ_HANDLE (Rpcasync. h)
description: Il \_ \_ \_ tipo di dati della gestione INQ RPC EP dichiara un handle per un contesto di richiesta. Le applicazioni RPC lo usano per visualizzare le informazioni sull'indirizzo del server archiviate nella mappa dell'endpoint.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400862"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="596cf-105">\_ \_ handle INQ EP \_ RPC</span><span class="sxs-lookup"><span data-stu-id="596cf-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="596cf-106">Il tipo di dati della **\_ \_ \_ gestione INQ RPC EP** dichiara un handle per un contesto di richiesta.</span><span class="sxs-lookup"><span data-stu-id="596cf-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="596cf-107">Le applicazioni RPC lo usano per visualizzare le informazioni sull'indirizzo del server archiviate nella mappa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="596cf-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="596cf-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="596cf-108">Requirements</span></span>



| <span data-ttu-id="596cf-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="596cf-109">Requirement</span></span> | <span data-ttu-id="596cf-110">Valore</span><span class="sxs-lookup"><span data-stu-id="596cf-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="596cf-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="596cf-111">Minimum supported client</span></span><br/> | <span data-ttu-id="596cf-112">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="596cf-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="596cf-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="596cf-113">Minimum supported server</span></span><br/> | <span data-ttu-id="596cf-114">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="596cf-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="596cf-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="596cf-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="596cf-116"><dt>Rpcasync. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="596cf-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="596cf-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="596cf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="596cf-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="596cf-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="596cf-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="596cf-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="596cf-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="596cf-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





