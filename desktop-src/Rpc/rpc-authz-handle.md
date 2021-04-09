---
title: RPC_AUTHZ_HANDLE (rpcdce. h)
description: Il \_ tipo di dati della gestione AUTHZ RPC \_ dichiara un handle di autorizzazione. Questo handle indica le informazioni sui privilegi per l'applicazione client che ha eseguito la chiamata RPC.
ms.assetid: 35b6a3f4-1703-4244-98fd-fad7de48b262
keywords:
- RPC_AUTHZ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b095100e1e224590ef6a285785da632e198e1b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121574"
---
# <a name="rpc_authz_handle"></a><span data-ttu-id="548be-105">\_handle AUTHZ \_ RPC</span><span class="sxs-lookup"><span data-stu-id="548be-105">RPC\_AUTHZ\_HANDLE</span></span>

<span data-ttu-id="548be-106">Il tipo di dati della **\_ \_ gestione AUTHZ RPC** dichiara un handle di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="548be-106">The **RPC\_AUTHZ\_HANDLE** data type declares an authorization handle.</span></span> <span data-ttu-id="548be-107">Questo handle indica le informazioni sui privilegi per l'applicazione client che ha eseguito la chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="548be-107">This handle points to the privileges information for the client application that made the remote procedure call.</span></span>


```C++
typedef void* RPC_AUTHZ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="548be-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="548be-108">Requirements</span></span>



| <span data-ttu-id="548be-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="548be-109">Requirement</span></span> | <span data-ttu-id="548be-110">Valore</span><span class="sxs-lookup"><span data-stu-id="548be-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="548be-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="548be-111">Minimum supported client</span></span><br/> | <span data-ttu-id="548be-112">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="548be-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="548be-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="548be-113">Minimum supported server</span></span><br/> | <span data-ttu-id="548be-114">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="548be-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="548be-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="548be-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="548be-116"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="548be-116"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548be-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="548be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548be-118">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="548be-118">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> </dl>

 

 





