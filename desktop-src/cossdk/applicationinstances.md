---
description: Recupera le informazioni relative alle applicazioni in esecuzione.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Raccolta ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483164"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="135c1-103">Raccolta ApplicationInstances</span><span class="sxs-lookup"><span data-stu-id="135c1-103">ApplicationInstances collection</span></span>

<span data-ttu-id="135c1-104">Recupera le informazioni relative alle applicazioni in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="135c1-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="135c1-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="135c1-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="135c1-106">Membri</span><span class="sxs-lookup"><span data-stu-id="135c1-106">Members</span></span>

<span data-ttu-id="135c1-107">La raccolta **ApplicationInstances** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="135c1-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="135c1-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="135c1-108">Related Collections</span></span>

<span data-ttu-id="135c1-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="135c1-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="135c1-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="135c1-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="135c1-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="135c1-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="135c1-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="135c1-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="135c1-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="135c1-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="135c1-114">**Applicazioni**</span><span class="sxs-lookup"><span data-stu-id="135c1-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="135c1-115">**Radice**</span><span class="sxs-lookup"><span data-stu-id="135c1-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="135c1-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="135c1-116">Properties</span></span>

<span data-ttu-id="135c1-117">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="135c1-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="135c1-118">Applicazione</span><span class="sxs-lookup"><span data-stu-id="135c1-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="135c1-119">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="135c1-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="135c1-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="135c1-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="135c1-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="135c1-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="135c1-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="135c1-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="135c1-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="135c1-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="135c1-124">Applicazione</span><span class="sxs-lookup"><span data-stu-id="135c1-124">Application</span></span>



| <span data-ttu-id="135c1-125">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-125">Entry</span></span> | <span data-ttu-id="135c1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="135c1-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-127">Description</span></span>    | <span data-ttu-id="135c1-128">ID per l'applicazione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="135c1-128">The ID for the running application.</span></span> |
| <span data-ttu-id="135c1-129">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-129">Access</span></span>         | <span data-ttu-id="135c1-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-130">ReadOnly</span></span>                            |
| <span data-ttu-id="135c1-131">Type</span><span class="sxs-lookup"><span data-stu-id="135c1-131">Type</span></span>           | <span data-ttu-id="135c1-132">string</span><span class="sxs-lookup"><span data-stu-id="135c1-132">String</span></span>                              |
| <span data-ttu-id="135c1-133">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-133">Default</span></span>        | <span data-ttu-id="135c1-134">N/D</span><span class="sxs-lookup"><span data-stu-id="135c1-134">N/A</span></span>                                 |
| <span data-ttu-id="135c1-135">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-135">Minimum system</span></span> | <span data-ttu-id="135c1-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="135c1-137">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="135c1-137">HasRecycled</span></span>



| <span data-ttu-id="135c1-138">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-138">Entry</span></span> | <span data-ttu-id="135c1-139">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="135c1-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-140">Description</span></span>    | <span data-ttu-id="135c1-141">Indica se l'istanza dell'applicazione è stata riciclata.</span><span class="sxs-lookup"><span data-stu-id="135c1-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="135c1-142">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-142">Access</span></span>         | <span data-ttu-id="135c1-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="135c1-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="135c1-144">Type</span></span>           | <span data-ttu-id="135c1-145">Bool</span><span class="sxs-lookup"><span data-stu-id="135c1-145">Bool</span></span>                                                          |
| <span data-ttu-id="135c1-146">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-146">Default</span></span>        | <span data-ttu-id="135c1-147">Falso</span><span class="sxs-lookup"><span data-stu-id="135c1-147">False</span></span>                                                         |
| <span data-ttu-id="135c1-148">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-148">Minimum system</span></span> | <span data-ttu-id="135c1-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="135c1-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="135c1-150">InstanceID</span></span>



| <span data-ttu-id="135c1-151">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-151">Entry</span></span> | <span data-ttu-id="135c1-152">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="135c1-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-153">Description</span></span>    | <span data-ttu-id="135c1-154">Identificatore univoco globale per l'istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="135c1-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="135c1-155">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="135c1-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="135c1-156">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-156">Access</span></span>         | <span data-ttu-id="135c1-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="135c1-158">Type</span><span class="sxs-lookup"><span data-stu-id="135c1-158">Type</span></span>           | <span data-ttu-id="135c1-159">string</span><span class="sxs-lookup"><span data-stu-id="135c1-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="135c1-160">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-160">Default</span></span>        | <span data-ttu-id="135c1-161">N/D</span><span class="sxs-lookup"><span data-stu-id="135c1-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="135c1-162">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-162">Minimum system</span></span> | <span data-ttu-id="135c1-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="135c1-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="135c1-164">IsPaused</span></span>



| <span data-ttu-id="135c1-165">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-165">Entry</span></span> | <span data-ttu-id="135c1-166">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="135c1-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-167">Description</span></span>    | <span data-ttu-id="135c1-168">Indica se l'istanza dell'applicazione è attualmente sospesa.</span><span class="sxs-lookup"><span data-stu-id="135c1-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="135c1-169">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-169">Access</span></span>         | <span data-ttu-id="135c1-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="135c1-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="135c1-171">Type</span></span>           | <span data-ttu-id="135c1-172">Bool</span><span class="sxs-lookup"><span data-stu-id="135c1-172">Bool</span></span>                                                            |
| <span data-ttu-id="135c1-173">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-173">Default</span></span>        | <span data-ttu-id="135c1-174">Falso</span><span class="sxs-lookup"><span data-stu-id="135c1-174">False</span></span>                                                           |
| <span data-ttu-id="135c1-175">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-175">Minimum system</span></span> | <span data-ttu-id="135c1-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="135c1-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="135c1-177">PartitionID</span></span>



| <span data-ttu-id="135c1-178">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-178">Entry</span></span> | <span data-ttu-id="135c1-179">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="135c1-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-180">Description</span></span>    | <span data-ttu-id="135c1-181">ID di partizione usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="135c1-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="135c1-182">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-182">Access</span></span>         | <span data-ttu-id="135c1-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="135c1-184">Type</span><span class="sxs-lookup"><span data-stu-id="135c1-184">Type</span></span>           | <span data-ttu-id="135c1-185">string</span><span class="sxs-lookup"><span data-stu-id="135c1-185">String</span></span>                                          |
| <span data-ttu-id="135c1-186">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-186">Default</span></span>        | <span data-ttu-id="135c1-187">N/D</span><span class="sxs-lookup"><span data-stu-id="135c1-187">N/A</span></span>                                             |
| <span data-ttu-id="135c1-188">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-188">Minimum system</span></span> | <span data-ttu-id="135c1-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="135c1-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="135c1-190">ProcessID</span></span>



| <span data-ttu-id="135c1-191">Voce</span><span class="sxs-lookup"><span data-stu-id="135c1-191">Entry</span></span> | <span data-ttu-id="135c1-192">Valore</span><span class="sxs-lookup"><span data-stu-id="135c1-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="135c1-193">Descrizione</span><span class="sxs-lookup"><span data-stu-id="135c1-193">Description</span></span>    | <span data-ttu-id="135c1-194">ID del processo dell'istanza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="135c1-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="135c1-195">Access</span><span class="sxs-lookup"><span data-stu-id="135c1-195">Access</span></span>         | <span data-ttu-id="135c1-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="135c1-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="135c1-197">Type</span><span class="sxs-lookup"><span data-stu-id="135c1-197">Type</span></span>           | <span data-ttu-id="135c1-198">string</span><span class="sxs-lookup"><span data-stu-id="135c1-198">String</span></span>                                      |
| <span data-ttu-id="135c1-199">Predefinito</span><span class="sxs-lookup"><span data-stu-id="135c1-199">Default</span></span>        | <span data-ttu-id="135c1-200">N/D</span><span class="sxs-lookup"><span data-stu-id="135c1-200">N/A</span></span>                                         |
| <span data-ttu-id="135c1-201">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="135c1-201">Minimum system</span></span> | <span data-ttu-id="135c1-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="135c1-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="135c1-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="135c1-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135c1-204">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="135c1-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
