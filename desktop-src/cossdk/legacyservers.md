---
description: Identico alla raccolta InprocServers con la differenza che questa raccolta include anche server locali.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Raccolta LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2ea542fa539ea1eb1cceae0f4cb8ba8dc2012085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304613"
---
# <a name="legacyservers-collection"></a><span data-ttu-id="1d8a8-103">Raccolta LegacyServers</span><span class="sxs-lookup"><span data-stu-id="1d8a8-103">LegacyServers collection</span></span>

<span data-ttu-id="1d8a8-104">Identico alla raccolta [**InprocServers**](inprocservers.md) con la differenza che questa raccolta include anche server locali.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-104">Identical to the [**InprocServers**](inprocservers.md) collection except that this collection also includes local servers.</span></span>

<span data-ttu-id="1d8a8-105">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1d8a8-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1d8a8-106">Membri</span><span class="sxs-lookup"><span data-stu-id="1d8a8-106">Members</span></span>

<span data-ttu-id="1d8a8-107">La raccolta **LegacyServers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-107">The **LegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1d8a8-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="1d8a8-108">Related Collections</span></span>

<span data-ttu-id="1d8a8-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d8a8-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1d8a8-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1d8a8-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1d8a8-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1d8a8-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1d8a8-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="1d8a8-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="1d8a8-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d8a8-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1d8a8-114">**Radice**</span><span class="sxs-lookup"><span data-stu-id="1d8a8-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="1d8a8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d8a8-115">Properties</span></span>

<span data-ttu-id="1d8a8-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="1d8a8-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1d8a8-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="1d8a8-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="1d8a8-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="1d8a8-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="1d8a8-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="1d8a8-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="1d8a8-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="1d8a8-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="1d8a8-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="1d8a8-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="1d8a8-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="1d8a8-122">ClassName</span></span>



| <span data-ttu-id="1d8a8-123">Voce</span><span class="sxs-lookup"><span data-stu-id="1d8a8-123">Entry</span></span> | <span data-ttu-id="1d8a8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8a8-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="1d8a8-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8a8-125">Description</span></span>    | <span data-ttu-id="1d8a8-126">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-126">The name of the class.</span></span> |
| <span data-ttu-id="1d8a8-127">Access</span><span class="sxs-lookup"><span data-stu-id="1d8a8-127">Access</span></span>         | <span data-ttu-id="1d8a8-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d8a8-128">ReadOnly</span></span>               |
| <span data-ttu-id="1d8a8-129">Type</span><span class="sxs-lookup"><span data-stu-id="1d8a8-129">Type</span></span>           | <span data-ttu-id="1d8a8-130">string</span><span class="sxs-lookup"><span data-stu-id="1d8a8-130">String</span></span>                 |
| <span data-ttu-id="1d8a8-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8a8-131">Default</span></span>        | <span data-ttu-id="1d8a8-132">N/D</span><span class="sxs-lookup"><span data-stu-id="1d8a8-132">N/A</span></span>                    |
| <span data-ttu-id="1d8a8-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1d8a8-133">Minimum system</span></span> | <span data-ttu-id="1d8a8-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d8a8-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="1d8a8-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="1d8a8-135">CLSID</span></span>



| <span data-ttu-id="1d8a8-136">Voce</span><span class="sxs-lookup"><span data-stu-id="1d8a8-136">Entry</span></span> | <span data-ttu-id="1d8a8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8a8-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8a8-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8a8-138">Description</span></span>    | <span data-ttu-id="1d8a8-139">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-139">A GUID for the component.</span></span> <span data-ttu-id="1d8a8-140">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1d8a8-141">Access</span><span class="sxs-lookup"><span data-stu-id="1d8a8-141">Access</span></span>         | <span data-ttu-id="1d8a8-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d8a8-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="1d8a8-143">Type</span><span class="sxs-lookup"><span data-stu-id="1d8a8-143">Type</span></span>           | <span data-ttu-id="1d8a8-144">string</span><span class="sxs-lookup"><span data-stu-id="1d8a8-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="1d8a8-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8a8-145">Default</span></span>        | <span data-ttu-id="1d8a8-146">N/D</span><span class="sxs-lookup"><span data-stu-id="1d8a8-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="1d8a8-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1d8a8-147">Minimum system</span></span> | <span data-ttu-id="1d8a8-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d8a8-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="1d8a8-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="1d8a8-149">InprocServer32</span></span>



| <span data-ttu-id="1d8a8-150">Voce</span><span class="sxs-lookup"><span data-stu-id="1d8a8-150">Entry</span></span> | <span data-ttu-id="1d8a8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8a8-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="1d8a8-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8a8-152">Description</span></span>    | <span data-ttu-id="1d8a8-153">Percorso del file per il componente.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-153">The file path for the component.</span></span> |
| <span data-ttu-id="1d8a8-154">Access</span><span class="sxs-lookup"><span data-stu-id="1d8a8-154">Access</span></span>         | <span data-ttu-id="1d8a8-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d8a8-155">ReadOnly</span></span>                         |
| <span data-ttu-id="1d8a8-156">Type</span><span class="sxs-lookup"><span data-stu-id="1d8a8-156">Type</span></span>           | <span data-ttu-id="1d8a8-157">string</span><span class="sxs-lookup"><span data-stu-id="1d8a8-157">String</span></span>                           |
| <span data-ttu-id="1d8a8-158">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8a8-158">Default</span></span>        | <span data-ttu-id="1d8a8-159">N/D</span><span class="sxs-lookup"><span data-stu-id="1d8a8-159">N/A</span></span>                              |
| <span data-ttu-id="1d8a8-160">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1d8a8-160">Minimum system</span></span> | <span data-ttu-id="1d8a8-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d8a8-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="1d8a8-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="1d8a8-162">LocalServer32</span></span>



| <span data-ttu-id="1d8a8-163">Voce</span><span class="sxs-lookup"><span data-stu-id="1d8a8-163">Entry</span></span> | <span data-ttu-id="1d8a8-164">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8a8-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="1d8a8-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8a8-165">Description</span></span>    | <span data-ttu-id="1d8a8-166">Specifica il percorso completo di un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="1d8a8-167">Access</span><span class="sxs-lookup"><span data-stu-id="1d8a8-167">Access</span></span>         | <span data-ttu-id="1d8a8-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d8a8-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="1d8a8-169">Type</span><span class="sxs-lookup"><span data-stu-id="1d8a8-169">Type</span></span>           | <span data-ttu-id="1d8a8-170">string</span><span class="sxs-lookup"><span data-stu-id="1d8a8-170">String</span></span>                                                        |
| <span data-ttu-id="1d8a8-171">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8a8-171">Default</span></span>        | <span data-ttu-id="1d8a8-172">N/D</span><span class="sxs-lookup"><span data-stu-id="1d8a8-172">N/A</span></span>                                                           |
| <span data-ttu-id="1d8a8-173">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1d8a8-173">Minimum system</span></span> | <span data-ttu-id="1d8a8-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d8a8-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="1d8a8-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="1d8a8-175">ProgID</span></span>



| <span data-ttu-id="1d8a8-176">Voce</span><span class="sxs-lookup"><span data-stu-id="1d8a8-176">Entry</span></span> | <span data-ttu-id="1d8a8-177">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8a8-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8a8-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8a8-178">Description</span></span>    | <span data-ttu-id="1d8a8-179">Nome che identifica il componente.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-179">A name identifying the component.</span></span> <span data-ttu-id="1d8a8-180">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="1d8a8-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1d8a8-181">Access</span><span class="sxs-lookup"><span data-stu-id="1d8a8-181">Access</span></span>         | <span data-ttu-id="1d8a8-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1d8a8-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="1d8a8-183">Type</span><span class="sxs-lookup"><span data-stu-id="1d8a8-183">Type</span></span>           | <span data-ttu-id="1d8a8-184">string</span><span class="sxs-lookup"><span data-stu-id="1d8a8-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="1d8a8-185">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8a8-185">Default</span></span>        | <span data-ttu-id="1d8a8-186">N/D</span><span class="sxs-lookup"><span data-stu-id="1d8a8-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="1d8a8-187">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1d8a8-187">Minimum system</span></span> | <span data-ttu-id="1d8a8-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d8a8-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="1d8a8-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d8a8-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8a8-190">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="1d8a8-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
