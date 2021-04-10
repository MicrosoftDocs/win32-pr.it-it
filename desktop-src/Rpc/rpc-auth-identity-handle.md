---
title: RPC_AUTH_IDENTITY_HANDLE (rpcdce. h)
description: Il \_ \_ \_ tipo di dati dell'handle di identità auth RPC dichiara un handle che punta a una struttura contenente le credenziali di autenticazione e autorizzazione del client specificate per le chiamate di procedura remota.
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121575"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="a010d-104">\_handle di \_ identità di autenticazione RPC \_</span><span class="sxs-lookup"><span data-stu-id="a010d-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="a010d-105">Il tipo di dati dell' **\_ \_ \_ handle di identità auth RPC** dichiara un handle che punta a una struttura contenente le credenziali di autenticazione e autorizzazione del client specificate per le chiamate di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a010d-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="a010d-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a010d-106">Requirements</span></span>



| <span data-ttu-id="a010d-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="a010d-107">Requirement</span></span> | <span data-ttu-id="a010d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a010d-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a010d-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a010d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a010d-110">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a010d-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a010d-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a010d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a010d-112">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a010d-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a010d-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a010d-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a010d-114"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a010d-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a010d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a010d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a010d-116">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="a010d-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="a010d-117">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="a010d-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





