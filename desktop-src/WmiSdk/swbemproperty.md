---
description: L'oggetto SWbemProperty rappresenta una singola proprietà WMI di un oggetto gestito. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Oggetto SWbemProperty (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233986"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="2b710-104">Oggetto SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="2b710-104">SWbemProperty object</span></span>

<span data-ttu-id="2b710-105">L'oggetto **SWbemProperty** rappresenta una singola proprietà WMI di un oggetto gestito.</span><span class="sxs-lookup"><span data-stu-id="2b710-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="2b710-106">Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="2b710-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="2b710-107">Membri</span><span class="sxs-lookup"><span data-stu-id="2b710-107">Members</span></span>

<span data-ttu-id="2b710-108">L'oggetto **SWbemProperty** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2b710-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="2b710-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b710-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b710-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b710-110">Properties</span></span>

<span data-ttu-id="2b710-111">L'oggetto **SWbemProperty** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b710-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="2b710-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b710-112">Property</span></span>                                                     | <span data-ttu-id="2b710-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2b710-113">Access type</span></span>           | <span data-ttu-id="2b710-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b710-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b710-115">**CIMType**</span><span class="sxs-lookup"><span data-stu-id="2b710-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="2b710-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-116">Read-only</span></span><br/>  | <span data-ttu-id="2b710-117">Tipo di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b710-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="2b710-118">**IsArray**</span><span class="sxs-lookup"><span data-stu-id="2b710-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="2b710-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-119">Read-only</span></span><br/>  | <span data-ttu-id="2b710-120">Valore booleano che indica se questa proprietà ha un tipo di matrice.</span><span class="sxs-lookup"><span data-stu-id="2b710-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="2b710-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="2b710-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="2b710-122">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-122">Read-only</span></span><br/>  | <span data-ttu-id="2b710-123">Valore booleano che indica se questa proprietà è locale.</span><span class="sxs-lookup"><span data-stu-id="2b710-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="2b710-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2b710-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="2b710-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-125">Read-only</span></span><br/>  | <span data-ttu-id="2b710-126">Nome della proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="2b710-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2b710-127">**Origine**</span><span class="sxs-lookup"><span data-stu-id="2b710-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="2b710-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-128">Read-only</span></span><br/>  | <span data-ttu-id="2b710-129">Contiene la classe di origine di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b710-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="2b710-130">**Qualificatori\_**</span><span class="sxs-lookup"><span data-stu-id="2b710-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="2b710-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b710-131">Read-only</span></span><br/>  | <span data-ttu-id="2b710-132">Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) , ovvero la raccolta di qualificatori per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b710-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="2b710-133">**Valore**</span><span class="sxs-lookup"><span data-stu-id="2b710-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="2b710-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2b710-134">Read/write</span></span><br/> | <span data-ttu-id="2b710-135">Valore effettivo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b710-135">Actual value of this property.</span></span> <span data-ttu-id="2b710-136">Si tratta della proprietà di automazione predefinita di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b710-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="2b710-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b710-137">Requirements</span></span>



| <span data-ttu-id="2b710-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b710-138">Requirement</span></span> | <span data-ttu-id="2b710-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2b710-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b710-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b710-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2b710-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b710-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b710-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b710-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2b710-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b710-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b710-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b710-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b710-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b710-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b710-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2b710-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b710-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b710-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b710-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2b710-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b710-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b710-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b710-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="2b710-150">CLSID</span></span><br/>                    | <span data-ttu-id="2b710-151">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="2b710-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="2b710-152">IID</span><span class="sxs-lookup"><span data-stu-id="2b710-152">IID</span></span><br/>                      | <span data-ttu-id="2b710-153">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="2b710-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="2b710-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b710-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b710-155">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="2b710-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




