---
description: Contiene un oggetto per ogni sottoscrizione temporanea. Le sottoscrizioni temporanee possono essere create in tempo reale per l'esecuzione di istanze di oggetti e svaniscono quando l'oggetto viene eliminato definitivamente.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Raccolta TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877929"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="ee1bf-104">Raccolta TransientSubscriptions</span><span class="sxs-lookup"><span data-stu-id="ee1bf-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="ee1bf-105">Contiene un oggetto per ogni sottoscrizione temporanea.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="ee1bf-106">Le sottoscrizioni temporanee possono essere create in tempo reale per l'esecuzione di istanze di oggetti e svaniscono quando l'oggetto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="ee1bf-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ee1bf-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ee1bf-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ee1bf-108">Members</span></span>

<span data-ttu-id="ee1bf-109">La raccolta **TransientSubscriptions** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ee1bf-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="ee1bf-110">Related Collections</span></span>

<span data-ttu-id="ee1bf-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee1bf-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ee1bf-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ee1bf-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ee1bf-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="ee1bf-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="ee1bf-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="ee1bf-117">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee1bf-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ee1bf-118">**Radice**</span><span class="sxs-lookup"><span data-stu-id="ee1bf-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ee1bf-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee1bf-119">Properties</span></span>

<span data-ttu-id="ee1bf-120">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="ee1bf-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ee1bf-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-121">Description</span></span>](#description)
-   [<span data-ttu-id="ee1bf-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="ee1bf-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="ee1bf-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="ee1bf-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="ee1bf-125">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="ee1bf-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="ee1bf-126">ID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="ee1bf-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="ee1bf-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="ee1bf-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="ee1bf-129">Nome</span><span class="sxs-lookup"><span data-stu-id="ee1bf-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="ee1bf-130">PerUser</span><span class="sxs-lookup"><span data-stu-id="ee1bf-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="ee1bf-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="ee1bf-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="ee1bf-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="ee1bf-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="ee1bf-134">UserName</span><span class="sxs-lookup"><span data-stu-id="ee1bf-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="ee1bf-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-135">Description</span></span>



| <span data-ttu-id="ee1bf-136">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-136">Entry</span></span> | <span data-ttu-id="ee1bf-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="ee1bf-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-138">Description</span></span>    | <span data-ttu-id="ee1bf-139">Descrizione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-139">A description for the subscription.</span></span> |
| <span data-ttu-id="ee1bf-140">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-140">Access</span></span>         | <span data-ttu-id="ee1bf-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-141">ReadWrite</span></span>                           |
| <span data-ttu-id="ee1bf-142">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-142">Type</span></span>           | <span data-ttu-id="ee1bf-143">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-143">String</span></span>                              |
| <span data-ttu-id="ee1bf-144">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-144">Default</span></span>        | <span data-ttu-id="ee1bf-145">""</span><span class="sxs-lookup"><span data-stu-id="ee1bf-145">""</span></span>                                  |
| <span data-ttu-id="ee1bf-146">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-146">Minimum system</span></span> | <span data-ttu-id="ee1bf-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="ee1bf-148">Abilitato</span><span class="sxs-lookup"><span data-stu-id="ee1bf-148">Enabled</span></span>



| <span data-ttu-id="ee1bf-149">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-149">Entry</span></span> | <span data-ttu-id="ee1bf-150">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="ee1bf-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-151">Description</span></span>    | <span data-ttu-id="ee1bf-152">Indica se la sottoscrizione è attualmente abilitata.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="ee1bf-153">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-153">Access</span></span>         | <span data-ttu-id="ee1bf-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="ee1bf-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-155">Type</span></span>           | <span data-ttu-id="ee1bf-156">Bool</span><span class="sxs-lookup"><span data-stu-id="ee1bf-156">Bool</span></span>                                                     |
| <span data-ttu-id="ee1bf-157">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-157">Default</span></span>        | <span data-ttu-id="ee1bf-158">Vero</span><span class="sxs-lookup"><span data-stu-id="ee1bf-158">True</span></span>                                                     |
| <span data-ttu-id="ee1bf-159">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-159">Minimum system</span></span> | <span data-ttu-id="ee1bf-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="ee1bf-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-161">EventClassPartitionID</span></span>



| <span data-ttu-id="ee1bf-162">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-162">Entry</span></span> | <span data-ttu-id="ee1bf-163">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-164">Description</span></span>    | <span data-ttu-id="ee1bf-165">Quando si sottoscrive una classe di evento, viene utilizzato per rappresentare il GUID dell'ID di partizione che contiene la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="ee1bf-166">Quando si sottoscrive le classi di evento, il Sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="ee1bf-167">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-167">Access</span></span>         | <span data-ttu-id="ee1bf-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="ee1bf-169">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-169">Type</span></span>           | <span data-ttu-id="ee1bf-170">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="ee1bf-171">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-171">Default</span></span>        | <span data-ttu-id="ee1bf-172">NULL</span><span class="sxs-lookup"><span data-stu-id="ee1bf-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="ee1bf-173">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-173">Minimum system</span></span> | <span data-ttu-id="ee1bf-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee1bf-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="ee1bf-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-175">EventCLSID</span></span>



| <span data-ttu-id="ee1bf-176">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-176">Entry</span></span> | <span data-ttu-id="ee1bf-177">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-178">Description</span></span>    | <span data-ttu-id="ee1bf-179">CLSID per la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-179">The CLSID for the event class.</span></span> <span data-ttu-id="ee1bf-180">È possibile indicare un EventCLSID o PublisherID, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="ee1bf-181">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-181">Access</span></span>         | <span data-ttu-id="ee1bf-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="ee1bf-183">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-183">Type</span></span>           | <span data-ttu-id="ee1bf-184">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-184">String</span></span>                                                                                       |
| <span data-ttu-id="ee1bf-185">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-185">Default</span></span>        | <span data-ttu-id="ee1bf-186">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="ee1bf-187">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-187">Minimum system</span></span> | <span data-ttu-id="ee1bf-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="ee1bf-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="ee1bf-189">FilterCriteria</span></span>



| <span data-ttu-id="ee1bf-190">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-190">Entry</span></span> | <span data-ttu-id="ee1bf-191">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-192">Description</span></span>    | <span data-ttu-id="ee1bf-193">Stringa che indica i criteri di filtro.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="ee1bf-194">Può essere un CLSID per una classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="ee1bf-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="ee1bf-195">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-195">Access</span></span>         | <span data-ttu-id="ee1bf-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="ee1bf-197">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-197">Type</span></span>           | <span data-ttu-id="ee1bf-198">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-198">String</span></span>                                                                                                               |
| <span data-ttu-id="ee1bf-199">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-199">Default</span></span>        | <span data-ttu-id="ee1bf-200">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="ee1bf-201">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-201">Minimum system</span></span> | <span data-ttu-id="ee1bf-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="ee1bf-203">ID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-203">ID</span></span>



| <span data-ttu-id="ee1bf-204">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-204">Entry</span></span> | <span data-ttu-id="ee1bf-205">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-206">Description</span></span>    | <span data-ttu-id="ee1bf-207">Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-207">Identifier for the subscription.</span></span> <span data-ttu-id="ee1bf-208">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ee1bf-209">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-209">Access</span></span>         | <span data-ttu-id="ee1bf-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="ee1bf-211">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-211">Type</span></span>           | <span data-ttu-id="ee1bf-212">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="ee1bf-213">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="ee1bf-214">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-214">Minimum system</span></span> | <span data-ttu-id="ee1bf-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="ee1bf-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-216">InterfaceID</span></span>



| <span data-ttu-id="ee1bf-217">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-217">Entry</span></span> | <span data-ttu-id="ee1bf-218">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="ee1bf-219">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-219">Description</span></span>    | <span data-ttu-id="ee1bf-220">IID per l'interfaccia sottoscritta.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="ee1bf-221">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-221">Access</span></span>         | <span data-ttu-id="ee1bf-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-222">WriteOnce</span></span>                        |
| <span data-ttu-id="ee1bf-223">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-223">Type</span></span>           | <span data-ttu-id="ee1bf-224">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-224">String</span></span>                           |
| <span data-ttu-id="ee1bf-225">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-225">Default</span></span>        | <span data-ttu-id="ee1bf-226">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-226">N/A</span></span>                              |
| <span data-ttu-id="ee1bf-227">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-227">Minimum system</span></span> | <span data-ttu-id="ee1bf-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="ee1bf-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="ee1bf-229">MethodName</span></span>



| <span data-ttu-id="ee1bf-230">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-230">Entry</span></span> | <span data-ttu-id="ee1bf-231">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="ee1bf-232">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-232">Description</span></span>    | <span data-ttu-id="ee1bf-233">Metodo sull'interfaccia sottoscritta.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="ee1bf-234">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-234">Access</span></span>         | <span data-ttu-id="ee1bf-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="ee1bf-236">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-236">Type</span></span>           | <span data-ttu-id="ee1bf-237">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-237">String</span></span>                                       |
| <span data-ttu-id="ee1bf-238">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-238">Default</span></span>        | <span data-ttu-id="ee1bf-239">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-239">N/A</span></span>                                          |
| <span data-ttu-id="ee1bf-240">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-240">Minimum system</span></span> | <span data-ttu-id="ee1bf-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="ee1bf-242">Nome</span><span class="sxs-lookup"><span data-stu-id="ee1bf-242">Name</span></span>



| <span data-ttu-id="ee1bf-243">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-243">Entry</span></span> | <span data-ttu-id="ee1bf-244">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-245">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-245">Description</span></span>    | <span data-ttu-id="ee1bf-246">Nome della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-246">The name for the subscription.</span></span> <span data-ttu-id="ee1bf-247">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ee1bf-248">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-248">Access</span></span>         | <span data-ttu-id="ee1bf-249">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="ee1bf-250">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-250">Type</span></span>           | <span data-ttu-id="ee1bf-251">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="ee1bf-252">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-252">Default</span></span>        | <span data-ttu-id="ee1bf-253">"Nuova sottoscrizione"</span><span class="sxs-lookup"><span data-stu-id="ee1bf-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="ee1bf-254">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-254">Minimum system</span></span> | <span data-ttu-id="ee1bf-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="ee1bf-256">PerUser</span><span class="sxs-lookup"><span data-stu-id="ee1bf-256">PerUser</span></span>



| <span data-ttu-id="ee1bf-257">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-257">Entry</span></span> | <span data-ttu-id="ee1bf-258">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-259">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-259">Description</span></span>    | <span data-ttu-id="ee1bf-260">Indica se la sottoscrizione è valida solo per un determinato utente, rappresentato dalla proprietà UserName.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="ee1bf-261">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-261">Access</span></span>         | <span data-ttu-id="ee1bf-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="ee1bf-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-263">Type</span></span>           | <span data-ttu-id="ee1bf-264">Bool</span><span class="sxs-lookup"><span data-stu-id="ee1bf-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="ee1bf-265">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-265">Default</span></span>        | <span data-ttu-id="ee1bf-266">Falso</span><span class="sxs-lookup"><span data-stu-id="ee1bf-266">False</span></span>                                                                                                   |
| <span data-ttu-id="ee1bf-267">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-267">Minimum system</span></span> | <span data-ttu-id="ee1bf-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="ee1bf-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-269">PublisherID</span></span>



| <span data-ttu-id="ee1bf-270">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-270">Entry</span></span> | <span data-ttu-id="ee1bf-271">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-272">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-272">Description</span></span>    | <span data-ttu-id="ee1bf-273">ID del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-273">ID for the publisher.</span></span> <span data-ttu-id="ee1bf-274">È possibile indicare un EventCLSID o PublisherID, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="ee1bf-275">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-275">Access</span></span>         | <span data-ttu-id="ee1bf-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="ee1bf-277">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-277">Type</span></span>           | <span data-ttu-id="ee1bf-278">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-278">String</span></span>                                                                              |
| <span data-ttu-id="ee1bf-279">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-279">Default</span></span>        | <span data-ttu-id="ee1bf-280">""</span><span class="sxs-lookup"><span data-stu-id="ee1bf-280">""</span></span>                                                                                  |
| <span data-ttu-id="ee1bf-281">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-281">Minimum system</span></span> | <span data-ttu-id="ee1bf-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="ee1bf-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="ee1bf-283">SubscriberInterface</span></span>



| <span data-ttu-id="ee1bf-284">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-284">Entry</span></span> | <span data-ttu-id="ee1bf-285">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="ee1bf-286">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-286">Description</span></span>    | <span data-ttu-id="ee1bf-287">Puntatore all'interfaccia del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="ee1bf-288">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-288">Access</span></span>         | <span data-ttu-id="ee1bf-289">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-289">ReadWrite</span></span>                                |
| <span data-ttu-id="ee1bf-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-290">Type</span></span>           | <span data-ttu-id="ee1bf-291">Variant</span><span class="sxs-lookup"><span data-stu-id="ee1bf-291">Variant</span></span>                                  |
| <span data-ttu-id="ee1bf-292">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-292">Default</span></span>        | <span data-ttu-id="ee1bf-293">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-293">N/A</span></span>                                      |
| <span data-ttu-id="ee1bf-294">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-294">Minimum system</span></span> | <span data-ttu-id="ee1bf-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="ee1bf-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="ee1bf-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="ee1bf-297">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-297">Entry</span></span> | <span data-ttu-id="ee1bf-298">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-299">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-299">Description</span></span>    | <span data-ttu-id="ee1bf-300">Quando si sottoscrive una classe di evento nella stessa partizione, utilizzata per rappresentare il GUID dell'ID di partizione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="ee1bf-301">Quando si sottoscrive le classi di evento, il Sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="ee1bf-302">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-302">Access</span></span>         | <span data-ttu-id="ee1bf-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ee1bf-304">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-304">Type</span></span>           | <span data-ttu-id="ee1bf-305">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ee1bf-306">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="ee1bf-307">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-307">Minimum system</span></span> | <span data-ttu-id="ee1bf-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee1bf-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="ee1bf-309">UserName</span><span class="sxs-lookup"><span data-stu-id="ee1bf-309">UserName</span></span>



| <span data-ttu-id="ee1bf-310">Voce</span><span class="sxs-lookup"><span data-stu-id="ee1bf-310">Entry</span></span> | <span data-ttu-id="ee1bf-311">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bf-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ee1bf-312">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1bf-312">Description</span></span>    | <span data-ttu-id="ee1bf-313">Nome dell'utente a cui si applica la sottoscrizione quando l'oggetto di lettura è true.</span><span class="sxs-lookup"><span data-stu-id="ee1bf-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="ee1bf-314">Access</span><span class="sxs-lookup"><span data-stu-id="ee1bf-314">Access</span></span>         | <span data-ttu-id="ee1bf-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee1bf-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="ee1bf-316">Type</span><span class="sxs-lookup"><span data-stu-id="ee1bf-316">Type</span></span>           | <span data-ttu-id="ee1bf-317">string</span><span class="sxs-lookup"><span data-stu-id="ee1bf-317">String</span></span>                                                                  |
| <span data-ttu-id="ee1bf-318">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ee1bf-318">Default</span></span>        | <span data-ttu-id="ee1bf-319">N/D</span><span class="sxs-lookup"><span data-stu-id="ee1bf-319">N/A</span></span>                                                                     |
| <span data-ttu-id="ee1bf-320">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ee1bf-320">Minimum system</span></span> | <span data-ttu-id="ee1bf-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ee1bf-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="ee1bf-322">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee1bf-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1bf-323">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="ee1bf-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
