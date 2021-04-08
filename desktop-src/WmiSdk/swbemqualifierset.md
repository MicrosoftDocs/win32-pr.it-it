---
description: Un oggetto dell'SWbemQualifierSet è una raccolta di oggetti oggetto SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Oggetto dell'SWbemQualifierSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058262"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="56a50-103">Oggetto dell'SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="56a50-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="56a50-104">Un oggetto **dell'SWbemQualifierSet** è una raccolta di oggetti [**oggetto SWbemQualifier**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="56a50-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="56a50-105">Gli elementi vengono aggiunti alla raccolta usando il metodo [**Add**](swbemqualifierset-add.md) , recuperati dalla raccolta usando il metodo [**Item**](swbemqualifierset-item.md) e rimossi dalla raccolta usando il metodo [**Remove**](swbemqualifierset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="56a50-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="56a50-106">Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="56a50-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="56a50-107">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="56a50-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="56a50-108">Gli oggetti [**oggetto SWbemQualifier**](swbemqualifier.md) che costituiscono una raccolta **dell'SWbemQualifierSet** descrivono i qualificatori associati a una classe WMI, un'istanza, un metodo o un parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="56a50-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="56a50-109">Membri</span><span class="sxs-lookup"><span data-stu-id="56a50-109">Members</span></span>

<span data-ttu-id="56a50-110">L'oggetto **dell'SWbemQualifierSet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="56a50-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="56a50-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="56a50-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="56a50-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56a50-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56a50-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="56a50-113">Methods</span></span>

<span data-ttu-id="56a50-114">L'oggetto **dell'SWbemQualifierSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="56a50-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="56a50-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="56a50-115">Method</span></span>                                     | <span data-ttu-id="56a50-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a50-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56a50-117">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="56a50-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="56a50-118">Aggiunge un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) alla raccolta **dell'SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="56a50-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="56a50-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56a50-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="56a50-120">Restituisce un oggetto denominato [**oggetto SWbemQualifier**](swbemqualifier.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="56a50-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="56a50-121">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="56a50-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="56a50-122">Elimina un qualificatore denominato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="56a50-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="56a50-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56a50-123">Properties</span></span>

<span data-ttu-id="56a50-124">L'oggetto **dell'SWbemQualifierSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="56a50-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="56a50-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="56a50-125">Property</span></span>                                            | <span data-ttu-id="56a50-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="56a50-126">Access type</span></span>          | <span data-ttu-id="56a50-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a50-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="56a50-128">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="56a50-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="56a50-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="56a50-129">Read-only</span></span><br/> | <span data-ttu-id="56a50-130">Contiene il numero di elementi in una raccolta **dell'SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="56a50-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56a50-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56a50-131">Requirements</span></span>



| <span data-ttu-id="56a50-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a50-132">Requirement</span></span> | <span data-ttu-id="56a50-133">Valore</span><span class="sxs-lookup"><span data-stu-id="56a50-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a50-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a50-134">Minimum supported client</span></span><br/> | <span data-ttu-id="56a50-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56a50-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56a50-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a50-136">Minimum supported server</span></span><br/> | <span data-ttu-id="56a50-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56a50-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56a50-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56a50-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a50-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a50-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56a50-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="56a50-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="56a50-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56a50-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56a50-142">DLL</span><span class="sxs-lookup"><span data-stu-id="56a50-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a50-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a50-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="56a50-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="56a50-144">CLSID</span></span><br/>                    | <span data-ttu-id="56a50-145">\_Dell'SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="56a50-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="56a50-146">IID</span><span class="sxs-lookup"><span data-stu-id="56a50-146">IID</span></span><br/>                      | <span data-ttu-id="56a50-147">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="56a50-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="56a50-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56a50-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a50-149">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="56a50-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




