---
description: Un oggetto SWbemMethodSet è una raccolta di oggetti SWbemMethod. Gli elementi vengono recuperati utilizzando il metodo dell'elemento. Per ulteriori informazioni, vedere Accesso a una raccolta. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Oggetto SWbemMethodSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882306"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="4392d-106">Oggetto SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="4392d-106">SWbemMethodSet object</span></span>

<span data-ttu-id="4392d-107">Un oggetto **SWbemMethodSet** è una raccolta di oggetti [**SWbemMethod**](swbemmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="4392d-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="4392d-108">Gli elementi vengono recuperati utilizzando il metodo dell' [**elemento**](swbemmethodset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4392d-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="4392d-109">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="4392d-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="4392d-110">Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="4392d-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="4392d-111">In questa versione dell'API, l'accesso in scrittura alle informazioni sul metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4392d-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="4392d-112">Se si desidera definire metodi o modificare definizioni di metodo esistenti, è possibile definire le modifiche al metodo in un file MOF e inviare le modifiche utilizzando il compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="4392d-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="4392d-113">In alternativa, usare l'API COM WMI.</span><span class="sxs-lookup"><span data-stu-id="4392d-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="4392d-114">Membri</span><span class="sxs-lookup"><span data-stu-id="4392d-114">Members</span></span>

<span data-ttu-id="4392d-115">L'oggetto **SWbemMethodSet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4392d-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="4392d-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="4392d-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="4392d-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4392d-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4392d-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="4392d-118">Methods</span></span>

<span data-ttu-id="4392d-119">L'oggetto **SWbemMethodSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4392d-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="4392d-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="4392d-120">Method</span></span>                              | <span data-ttu-id="4392d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4392d-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4392d-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4392d-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="4392d-123">Recupera un oggetto [**SWbemMethod**](swbemmethod.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4392d-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="4392d-124">Si tratta del metodo di automazione predefinito di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4392d-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4392d-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4392d-125">Properties</span></span>

<span data-ttu-id="4392d-126">L'oggetto **SWbemMethodSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4392d-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="4392d-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4392d-127">Property</span></span>                                         | <span data-ttu-id="4392d-128">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4392d-128">Access type</span></span>          | <span data-ttu-id="4392d-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4392d-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="4392d-130">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="4392d-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="4392d-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4392d-131">Read-only</span></span><br/> | <span data-ttu-id="4392d-132">Numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="4392d-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4392d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4392d-133">Requirements</span></span>



| <span data-ttu-id="4392d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4392d-134">Requirement</span></span> | <span data-ttu-id="4392d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4392d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4392d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4392d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4392d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4392d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4392d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4392d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4392d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4392d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4392d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4392d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4392d-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4392d-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4392d-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4392d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="4392d-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4392d-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4392d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4392d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4392d-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4392d-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4392d-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="4392d-146">CLSID</span></span><br/>                    | <span data-ttu-id="4392d-147">\_SWBEMMETHODSET CLSID</span><span class="sxs-lookup"><span data-stu-id="4392d-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="4392d-148">IID</span><span class="sxs-lookup"><span data-stu-id="4392d-148">IID</span></span><br/>                      | <span data-ttu-id="4392d-149">\_ISWBEMMETHODSET IID</span><span class="sxs-lookup"><span data-stu-id="4392d-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="4392d-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4392d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4392d-151">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="4392d-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




