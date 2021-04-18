---
title: Costanti Authorization-Service (rpcdce. h)
description: Le costanti del servizio di autorizzazione rappresentano i servizi di autorizzazione passati a varie funzioni di run-time.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519262"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="78d9d-103">Costanti Authorization-Service</span><span class="sxs-lookup"><span data-stu-id="78d9d-103">Authorization-Service Constants</span></span>

<span data-ttu-id="78d9d-104">Le costanti del servizio di autorizzazione rappresentano i servizi di autorizzazione passati a varie funzioni di run-time.</span><span class="sxs-lookup"><span data-stu-id="78d9d-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="78d9d-105">Le costanti seguenti sono valori validi per il parametro *AuthzSvc* .</span><span class="sxs-lookup"><span data-stu-id="78d9d-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="78d9d-106">La maggior parte delle applicazioni trova \_ AUTHZ RPC C \_ \_ non sufficienti.</span><span class="sxs-lookup"><span data-stu-id="78d9d-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="78d9d-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="78d9d-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="78d9d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d9d-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="78d9d-109"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78d9d-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="78d9d-110">Il server non esegue alcuna autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="78d9d-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="78d9d-111"><dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="78d9d-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="78d9d-112">Il server esegue l'autorizzazione in base al nome principale del client.</span><span class="sxs-lookup"><span data-stu-id="78d9d-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="78d9d-113"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="78d9d-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="78d9d-114">Il server esegue il controllo delle autorizzazioni utilizzando le informazioni del certificato dell'attributo Privilege (PAC) del client, che viene inviato al server con ogni chiamata di procedura remota eseguita utilizzando l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="78d9d-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="78d9d-115">In genere, l'accesso viene controllato rispetto agli elenchi di controllo di accesso ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)) DCE.</span><span class="sxs-lookup"><span data-stu-id="78d9d-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="78d9d-116"><dt>**RPC \_ C \_ AUTHZ \_ predefinito**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="78d9d-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="78d9d-117">Il server utilizza il servizio di autorizzazione predefinito per il provider di servizi condivisi corrente.</span><span class="sxs-lookup"><span data-stu-id="78d9d-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="78d9d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78d9d-118">Requirements</span></span>



| <span data-ttu-id="78d9d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78d9d-119">Requirement</span></span> | <span data-ttu-id="78d9d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="78d9d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78d9d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78d9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78d9d-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78d9d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="78d9d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78d9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78d9d-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="78d9d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78d9d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78d9d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d9d-126"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d9d-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d9d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78d9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d9d-128">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="78d9d-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="78d9d-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="78d9d-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="78d9d-130">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="78d9d-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="78d9d-131">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="78d9d-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="78d9d-132">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="78d9d-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="78d9d-133">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="78d9d-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="78d9d-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="78d9d-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

