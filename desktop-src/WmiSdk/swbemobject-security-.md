---
description: La \_ proprietà di sicurezza dell'oggetto SWbemObject viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349221"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="bbe59-103">Proprietà SWbemObject. Security \_</span><span class="sxs-lookup"><span data-stu-id="bbe59-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="bbe59-104">La proprietà di **\_ sicurezza** dell'oggetto [**SWbemObject**](swbemobject.md) viene utilizzata per leggere o impostare le impostazioni di sicurezza per un oggetto **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="bbe59-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="bbe59-105">Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe59-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="bbe59-106">Le impostazioni di sicurezza in questo oggetto non indicano le impostazioni di autenticazione, rappresentazione o privilegio effettuate in una connessione a Strumentazione gestione Windows (WMI) o la sicurezza attiva per il proxy quando un oggetto viene recapitato a un sink in una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="bbe59-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="bbe59-107">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="bbe59-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="bbe59-108">Impostando la proprietà di **\_ sicurezza** di un oggetto [**SWbemObject**](swbemobject.md) su **null** , viene concesso l'accesso illimitato a tutti i tempi.</span><span class="sxs-lookup"><span data-stu-id="bbe59-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="bbe59-109">Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="bbe59-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="bbe59-110">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bbe59-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bbe59-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bbe59-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe59-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbe59-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="bbe59-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bbe59-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe59-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe59-114">Requirements</span></span>



| <span data-ttu-id="bbe59-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe59-115">Requirement</span></span> | <span data-ttu-id="bbe59-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe59-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe59-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe59-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe59-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbe59-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbe59-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbe59-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe59-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbe59-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbe59-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe59-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe59-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe59-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbe59-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bbe59-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbe59-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bbe59-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bbe59-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe59-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe59-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe59-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbe59-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbe59-127">CLSID</span></span><br/>                    | <span data-ttu-id="bbe59-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="bbe59-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="bbe59-129">IID</span><span class="sxs-lookup"><span data-stu-id="bbe59-129">IID</span></span><br/>                      | <span data-ttu-id="bbe59-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="bbe59-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="bbe59-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe59-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe59-132">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="bbe59-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="bbe59-133">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="bbe59-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="bbe59-134">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="bbe59-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="bbe59-135">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="bbe59-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="bbe59-136">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="bbe59-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="bbe59-137">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="bbe59-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="bbe59-138">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="bbe59-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="bbe59-139">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="bbe59-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




