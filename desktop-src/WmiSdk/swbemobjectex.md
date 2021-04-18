---
description: Fornisce funzionalità estese per SWbemObject. Analogamente a SWbemObject, i metodi di questo oggetto esteso possono essere utilizzati da tutti gli oggetti WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Oggetto SWbemObjectEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309811"
---
# <a name="swbemobjectex-object"></a><span data-ttu-id="ee4c1-104">Oggetto SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="ee4c1-104">SWbemObjectEx object</span></span>

<span data-ttu-id="ee4c1-105">L'oggetto **SWbemObjectEx** fornisce funzionalità estese per [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="ee4c1-105">The **SWbemObjectEx** object provides extended functionality for [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="ee4c1-106">Analogamente a **SWbemObject**, i metodi di questo oggetto esteso possono essere utilizzati da tutti gli oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-106">Like **SWbemObject**, the methods of this extended object can be used by all WMI objects.</span></span> <span data-ttu-id="ee4c1-107">Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="ee4c1-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ee4c1-108">Members</span></span>

<span data-ttu-id="ee4c1-109">L'oggetto **SWbemObjectEx** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ee4c1-109">The **SWbemObjectEx** object has these types of members:</span></span>

-   [<span data-ttu-id="ee4c1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee4c1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee4c1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee4c1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee4c1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ee4c1-112">Methods</span></span>

<span data-ttu-id="ee4c1-113">L'oggetto **SWbemObjectEx** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-113">The **SWbemObjectEx** object has these methods.</span></span>



| <span data-ttu-id="ee4c1-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee4c1-114">Method</span></span>                                      | <span data-ttu-id="ee4c1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee4c1-115">Description</span></span>                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="ee4c1-116">**GetText\_**</span><span class="sxs-lookup"><span data-stu-id="ee4c1-116">**GetText\_**</span></span>](swbemobjectex-gettext-.md) | <span data-ttu-id="ee4c1-117">Restituisce un file di testo che mostra il contenuto di un oggetto in XML.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-117">Returns a text file showing the contents of an object in XML.</span></span><br/> |
| [<span data-ttu-id="ee4c1-118">**Aggiorna\_**</span><span class="sxs-lookup"><span data-stu-id="ee4c1-118">**Refresh\_**</span></span>](swbemobjectex-refresh-.md) | <span data-ttu-id="ee4c1-119">Aggiorna i dati in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-119">Refreshes data in an object.</span></span><br/>                                  |
| <span data-ttu-id="ee4c1-120">**SetFromText\_**</span><span class="sxs-lookup"><span data-stu-id="ee4c1-120">**SetFromText\_**</span></span>                           | <span data-ttu-id="ee4c1-121">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-121">Reserved for future use.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="ee4c1-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee4c1-122">Properties</span></span>

<span data-ttu-id="ee4c1-123">L'oggetto **SWbemObjectEx** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-123">The **SWbemObjectEx** object has these properties.</span></span>



| <span data-ttu-id="ee4c1-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee4c1-124">Property</span></span>                                                                 | <span data-ttu-id="ee4c1-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ee4c1-125">Access type</span></span>           | <span data-ttu-id="ee4c1-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee4c1-126">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee4c1-127">**SystemProperties\_**</span><span class="sxs-lookup"><span data-stu-id="ee4c1-127">**SystemProperties\_**</span></span>](swbemobjectex-systemproperties-.md)<br/> | <span data-ttu-id="ee4c1-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ee4c1-128">Read/write</span></span><br/> | <span data-ttu-id="ee4c1-129">Oggetto [**SWbemPropertySet**](swbempropertyset.md) che contiene la raccolta di proprietà di sistema che si applicano a **SWbemObjectEx**.</span><span class="sxs-lookup"><span data-stu-id="ee4c1-129">An [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of system properties that apply to the **SWbemObjectEx**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ee4c1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee4c1-130">Requirements</span></span>



| <span data-ttu-id="ee4c1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4c1-131">Requirement</span></span> | <span data-ttu-id="ee4c1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ee4c1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4c1-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee4c1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4c1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee4c1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee4c1-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee4c1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4c1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee4c1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee4c1-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee4c1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4c1-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4c1-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee4c1-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ee4c1-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee4c1-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee4c1-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee4c1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ee4c1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee4c1-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee4c1-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee4c1-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="ee4c1-143">CLSID</span></span><br/>                    | <span data-ttu-id="ee4c1-144">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="ee4c1-144">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="ee4c1-145">IID</span><span class="sxs-lookup"><span data-stu-id="ee4c1-145">IID</span></span><br/>                      | <span data-ttu-id="ee4c1-146">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="ee4c1-146">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ee4c1-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee4c1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4c1-148">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="ee4c1-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="ee4c1-149">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ee4c1-149">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="ee4c1-150">WbemObjectTextFormatEnum</span><span class="sxs-lookup"><span data-stu-id="ee4c1-150">WbemObjectTextFormatEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

