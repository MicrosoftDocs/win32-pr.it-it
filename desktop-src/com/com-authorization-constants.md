---
title: Costanti di autorizzazione (RpcDce. h)
description: Definisce gli elementi autorizzati dal server.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743711"
---
# <a name="authorization-constants"></a><span data-ttu-id="baff7-103">Costanti di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="baff7-103">Authorization Constants</span></span>

<span data-ttu-id="baff7-104">Definisce gli elementi autorizzati dal server.</span><span class="sxs-lookup"><span data-stu-id="baff7-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="baff7-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="baff7-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="baff7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baff7-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="baff7-107"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="baff7-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="baff7-108">Il server non esegue alcuna autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="baff7-108">The server performs no authorization.</span></span> <span data-ttu-id="baff7-109">Attualmente, le autorizzazioni RPC c AuthN \_ \_ \_ WinNT, RPC \_ c \_ AuthN \_ GSS \_ Schannel e RPC \_ c \_ AuthN \_ GSS \_ Kerberos utilizzano solo RPC \_ c \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="baff7-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="baff7-110"><dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="baff7-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="baff7-111">Il server esegue l'autorizzazione in base al nome principale del client.</span><span class="sxs-lookup"><span data-stu-id="baff7-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="baff7-112"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="baff7-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="baff7-113">Il server esegue il controllo delle autorizzazioni utilizzando le informazioni del certificato dell'attributo Privilege (PAC) del client, che viene inviato al server con ogni chiamata di procedura remota eseguita utilizzando l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="baff7-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="baff7-114">In genere, l'accesso viene controllato rispetto agli elenchi di controllo di accesso (ACL) DCE.</span><span class="sxs-lookup"><span data-stu-id="baff7-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="baff7-115"><dt>**RPC \_ C \_ AUTHZ \_ predefinito**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="baff7-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="baff7-116">DCOM può scegliere il livello di autorizzazione utilizzando il normale algoritmo di negoziazione della copertura di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="baff7-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="baff7-117">Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="baff7-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="baff7-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="baff7-118">Remarks</span></span>

<span data-ttu-id="baff7-119">Queste costanti vengono usate dai metodi dell'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="baff7-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="baff7-120">Vengono usati nell'unica struttura [**del \_ \_ servizio di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , che viene recuperata dalla funzione [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .</span><span class="sxs-lookup"><span data-stu-id="baff7-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="baff7-121">Vengono inoltre usati nell'unica struttura [**di \_ \_ informazioni di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , che a sua volta è un membro della struttura dell' [**unico \_ \_ elenco di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) .</span><span class="sxs-lookup"><span data-stu-id="baff7-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="baff7-122">Questa struttura, ovvero un elenco di servizi di autenticazione, i servizi di autorizzazione che eseguono e le informazioni di autenticazione per ogni servizio, vengono passati alla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e al metodo [**IClientSecurity:: seblank**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .</span><span class="sxs-lookup"><span data-stu-id="baff7-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="baff7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baff7-123">Requirements</span></span>



| <span data-ttu-id="baff7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="baff7-124">Requirement</span></span> | <span data-ttu-id="baff7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="baff7-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="baff7-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baff7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="baff7-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="baff7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="baff7-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baff7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="baff7-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="baff7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="baff7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baff7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="baff7-131"><dt>RpcDce. h</dt></span><span class="sxs-lookup"><span data-stu-id="baff7-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baff7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baff7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baff7-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="baff7-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="baff7-134">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="baff7-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="baff7-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="baff7-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="baff7-136">**\_informazioni di autenticazione esclusiva \_**</span><span class="sxs-lookup"><span data-stu-id="baff7-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="baff7-137">**\_servizio di autenticazione esclusivo \_**</span><span class="sxs-lookup"><span data-stu-id="baff7-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

