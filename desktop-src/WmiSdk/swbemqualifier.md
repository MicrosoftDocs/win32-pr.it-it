---
description: È possibile utilizzare le proprietà dell'oggetto oggetto SWbemQualifier per rappresentare un singolo qualificatore di una classe, un'istanza, una proprietà o un parametro di metodo WMI. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Oggetto oggetto SWbemQualifier (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226806"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="72f1b-104">Oggetto oggetto SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="72f1b-104">SWbemQualifier object</span></span>

<span data-ttu-id="72f1b-105">È possibile utilizzare le proprietà dell'oggetto **oggetto SWbemQualifier** per rappresentare un singolo qualificatore di una classe, un'istanza, una proprietà o un parametro di metodo WMI.</span><span class="sxs-lookup"><span data-stu-id="72f1b-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="72f1b-106">Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="72f1b-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="72f1b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="72f1b-107">Members</span></span>

<span data-ttu-id="72f1b-108">L'oggetto **oggetto SWbemQualifier** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72f1b-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="72f1b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72f1b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72f1b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72f1b-110">Properties</span></span>

<span data-ttu-id="72f1b-111">L'oggetto **oggetto SWbemQualifier** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="72f1b-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="72f1b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72f1b-112">Property</span></span>                                                                       | <span data-ttu-id="72f1b-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="72f1b-113">Access type</span></span>           | <span data-ttu-id="72f1b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72f1b-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72f1b-115">**IsAmended**</span><span class="sxs-lookup"><span data-stu-id="72f1b-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="72f1b-116">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="72f1b-116">Read-only</span></span><br/>  | <span data-ttu-id="72f1b-117">Valore booleano che indica se il qualificatore è stato localizzato utilizzando un'operazione di Unione.</span><span class="sxs-lookup"><span data-stu-id="72f1b-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="72f1b-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="72f1b-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="72f1b-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="72f1b-119">Read-only</span></span><br/>  | <span data-ttu-id="72f1b-120">Valore booleano che indica se il qualificatore è locale.</span><span class="sxs-lookup"><span data-stu-id="72f1b-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="72f1b-121">**IsOverridable**</span><span class="sxs-lookup"><span data-stu-id="72f1b-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="72f1b-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="72f1b-122">Read/write</span></span><br/> | <span data-ttu-id="72f1b-123">Valore booleano che indica se il qualificatore può essere sottoposto a override quando viene propagato.</span><span class="sxs-lookup"><span data-stu-id="72f1b-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="72f1b-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="72f1b-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="72f1b-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="72f1b-125">Read-only</span></span><br/>  | <span data-ttu-id="72f1b-126">Nome del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="72f1b-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="72f1b-127">**PropagatesToInstance**</span><span class="sxs-lookup"><span data-stu-id="72f1b-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="72f1b-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="72f1b-128">Read/write</span></span><br/> | <span data-ttu-id="72f1b-129">Valore booleano che indica se il qualificatore può essere propagato a un'istanza.</span><span class="sxs-lookup"><span data-stu-id="72f1b-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="72f1b-130">**PropagatesToSubClass**</span><span class="sxs-lookup"><span data-stu-id="72f1b-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="72f1b-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="72f1b-131">Read-only</span></span><br/>  | <span data-ttu-id="72f1b-132">Valore booleano che indica se il qualificatore può essere propagato a una sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="72f1b-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="72f1b-133">**Valore**</span><span class="sxs-lookup"><span data-stu-id="72f1b-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="72f1b-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="72f1b-134">Read/write</span></span><br/> | <span data-ttu-id="72f1b-135">Valore Variant di questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="72f1b-135">Variant value of this qualifier.</span></span> <span data-ttu-id="72f1b-136">Si tratta della proprietà predefinita di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="72f1b-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="72f1b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72f1b-137">Requirements</span></span>



| <span data-ttu-id="72f1b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f1b-138">Requirement</span></span> | <span data-ttu-id="72f1b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="72f1b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72f1b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72f1b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="72f1b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72f1b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72f1b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72f1b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="72f1b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72f1b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72f1b-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72f1b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f1b-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f1b-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72f1b-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="72f1b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="72f1b-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72f1b-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72f1b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="72f1b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f1b-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f1b-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72f1b-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="72f1b-150">CLSID</span></span><br/>                    | <span data-ttu-id="72f1b-151">\_Oggetto SWBEMQUALIFIER CLSID</span><span class="sxs-lookup"><span data-stu-id="72f1b-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="72f1b-152">IID</span><span class="sxs-lookup"><span data-stu-id="72f1b-152">IID</span></span><br/>                      | <span data-ttu-id="72f1b-153">\_ISWBEMQUALIFIER IID</span><span class="sxs-lookup"><span data-stu-id="72f1b-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="72f1b-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72f1b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f1b-155">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="72f1b-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




