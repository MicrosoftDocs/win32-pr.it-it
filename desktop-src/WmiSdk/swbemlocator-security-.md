---
description: La \_ proprietà di sicurezza dell'oggetto SWbemLocator viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto SWbemLocator. Questa proprietà è un oggetto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Proprietà SWbemLocator.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755026"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="870d5-104">Proprietà SWbemLocator. Security \_</span><span class="sxs-lookup"><span data-stu-id="870d5-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="870d5-105">La proprietà di **\_ sicurezza** dell'oggetto [**SWbemLocator**](swbemlocator.md) viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="870d5-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="870d5-106">Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="870d5-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="870d5-107">Impostando la proprietà di **\_ sicurezza** di un oggetto [**SWbemLocator**](swbemlocator.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="870d5-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="870d5-108">Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="870d5-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="870d5-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="870d5-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="870d5-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="870d5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="870d5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="870d5-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="870d5-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="870d5-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="870d5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="870d5-113">Remarks</span></span>

<span data-ttu-id="870d5-114">Le proprietà di un oggetto **SWbemLocator. \_ Security** non hanno valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="870d5-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="870d5-115">Se si tenta di ottenere il valore di [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) su un oggetto [**SWbemLocator**](swbemlocator.md) prima di impostarlo, viene restituito un errore [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .</span><span class="sxs-lookup"><span data-stu-id="870d5-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="870d5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="870d5-116">Requirements</span></span>



| <span data-ttu-id="870d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="870d5-117">Requirement</span></span> | <span data-ttu-id="870d5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="870d5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="870d5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="870d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="870d5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="870d5-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="870d5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="870d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="870d5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="870d5-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="870d5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="870d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="870d5-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="870d5-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="870d5-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="870d5-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="870d5-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="870d5-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="870d5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="870d5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="870d5-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="870d5-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="870d5-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="870d5-129">CLSID</span></span><br/>                    | <span data-ttu-id="870d5-130">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="870d5-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="870d5-131">IID</span><span class="sxs-lookup"><span data-stu-id="870d5-131">IID</span></span><br/>                      | <span data-ttu-id="870d5-132">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="870d5-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="870d5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="870d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870d5-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="870d5-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="870d5-135">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="870d5-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="870d5-136">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="870d5-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="870d5-137">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="870d5-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="870d5-138">**Oggetto SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="870d5-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="870d5-139">Protezione di una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="870d5-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




