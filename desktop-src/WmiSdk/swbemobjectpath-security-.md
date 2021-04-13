---
description: La proprietà di sicurezza dell'oggetto SWbemObjectPath viene utilizzata per ottenere o impostare i componenti di sicurezza di un percorso dell'oggetto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226811"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="3e291-103">Proprietà SWbemObjectPath. Security \_</span><span class="sxs-lookup"><span data-stu-id="3e291-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="3e291-104">La proprietà di **sicurezza** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) viene utilizzata per ottenere o impostare i componenti di sicurezza di un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e291-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="3e291-105">Si noti che non viene usato per impostare gli attributi di sicurezza dell'oggetto **SWbemObjectPath** .</span><span class="sxs-lookup"><span data-stu-id="3e291-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="3e291-106">Viene utilizzato solo per rappresentare i componenti di sicurezza del percorso di un oggetto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="3e291-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="3e291-107">Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="3e291-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="3e291-108">Impostando la proprietà di [**\_ sicurezza**](swbemobject-security-.md) di un oggetto [**SWbemObjectPath**](swbemobjectset.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="3e291-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="3e291-109">Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="3e291-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="3e291-110">Per altre informazioni, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3e291-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3e291-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3e291-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e291-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e291-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="3e291-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3e291-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3e291-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e291-114">Requirements</span></span>



| <span data-ttu-id="3e291-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e291-115">Requirement</span></span> | <span data-ttu-id="3e291-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3e291-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e291-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e291-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e291-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e291-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e291-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e291-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e291-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e291-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e291-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e291-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e291-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e291-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e291-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3e291-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e291-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e291-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e291-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e291-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e291-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e291-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e291-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="3e291-127">CLSID</span></span><br/>                    | <span data-ttu-id="3e291-128">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="3e291-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="3e291-129">IID</span><span class="sxs-lookup"><span data-stu-id="3e291-129">IID</span></span><br/>                      | <span data-ttu-id="3e291-130">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="3e291-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="3e291-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e291-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e291-132">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="3e291-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="3e291-133">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="3e291-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="3e291-134">Impostazione della \_ sicurezza del processo dell'applicazione client \_</span><span class="sxs-lookup"><span data-stu-id="3e291-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




