---
description: La \_ proprietà di sicurezza dell'oggetto SWbemObjectSet viene utilizzata per ottenere o impostare le impostazioni di sicurezza per un oggetto SWbemObjectSet. Questa proprietà è un oggetto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Proprietà SWbemObjectSet.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309798"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="02a7a-104">Proprietà SWbemObjectSet. Security \_</span><span class="sxs-lookup"><span data-stu-id="02a7a-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="02a7a-105">La proprietà di **\_ sicurezza** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) viene utilizzata per ottenere o impostare le impostazioni di sicurezza per un oggetto **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="02a7a-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="02a7a-106">Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="02a7a-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="02a7a-107">Impostando la proprietà di [**\_ sicurezza**](swbemobject-security-.md) di un oggetto [**SWbemObjectSet**](swbemobjectset.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="02a7a-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="02a7a-108">Per ulteriori informazioni sulle implicazioni dell'accesso illimitato, vedere [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="02a7a-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="02a7a-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="02a7a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="02a7a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="02a7a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a7a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02a7a-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="02a7a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="02a7a-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="02a7a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02a7a-113">Requirements</span></span>



| <span data-ttu-id="02a7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a7a-114">Requirement</span></span> | <span data-ttu-id="02a7a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02a7a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02a7a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02a7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02a7a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02a7a-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02a7a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02a7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02a7a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02a7a-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02a7a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02a7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02a7a-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a7a-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02a7a-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="02a7a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="02a7a-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02a7a-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02a7a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="02a7a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02a7a-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02a7a-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02a7a-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="02a7a-126">CLSID</span></span><br/>                    | <span data-ttu-id="02a7a-127">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="02a7a-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="02a7a-128">IID</span><span class="sxs-lookup"><span data-stu-id="02a7a-128">IID</span></span><br/>                      | <span data-ttu-id="02a7a-129">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="02a7a-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="02a7a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02a7a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a7a-131">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="02a7a-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="02a7a-132">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="02a7a-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="02a7a-133">Protezione dei client di scripting</span><span class="sxs-lookup"><span data-stu-id="02a7a-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




