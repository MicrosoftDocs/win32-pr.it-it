---
description: La proprietà OutParameters dell'oggetto SWbemMethod è un oggetto SWbemObject le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo. Questa proprietà è di sola lettura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Proprietà SWbemMethod. OutParameters (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313680"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="3d548-104">SWbemMethod. OutParameters (proprietà)</span><span class="sxs-lookup"><span data-stu-id="3d548-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="3d548-105">La proprietà **OutParameters** dell'oggetto [**SWbemMethod**](swbemmethod.md) è un oggetto [**SWbemObject**](swbemobject.md) le cui proprietà definiscono i parametri out e il tipo restituito di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3d548-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="3d548-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3d548-106">This property is read-only.</span></span>

<span data-ttu-id="3d548-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3d548-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3d548-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3d548-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d548-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d548-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="3d548-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3d548-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3d548-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d548-111">Remarks</span></span>

<span data-ttu-id="3d548-112">Per ulteriori informazioni su come utilizzare questa proprietà per ottenere i parametri di output dai metodi del provider, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3d548-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="3d548-113">Si noti che tutte le modifiche apportate a questo oggetto non vengono riflesse nella definizione del metodo sottostante.</span><span class="sxs-lookup"><span data-stu-id="3d548-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d548-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d548-114">Requirements</span></span>



| <span data-ttu-id="3d548-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d548-115">Requirement</span></span> | <span data-ttu-id="3d548-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3d548-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d548-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d548-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d548-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d548-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d548-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d548-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3d548-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d548-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d548-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d548-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d548-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d548-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d548-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3d548-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d548-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d548-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d548-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3d548-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d548-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d548-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3d548-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d548-127">CLSID</span></span><br/>                    | <span data-ttu-id="3d548-128">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="3d548-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="3d548-129">IID</span><span class="sxs-lookup"><span data-stu-id="3d548-129">IID</span></span><br/>                      | <span data-ttu-id="3d548-130">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="3d548-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="3d548-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d548-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d548-132">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="3d548-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="3d548-133">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="3d548-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="3d548-134">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="3d548-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="3d548-135">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="3d548-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="3d548-136">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="3d548-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




