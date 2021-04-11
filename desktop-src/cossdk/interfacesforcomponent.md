---
description: Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Raccolta InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127026"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="6f22f-103">Raccolta InterfacesForComponent</span><span class="sxs-lookup"><span data-stu-id="6f22f-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="6f22f-104">Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f22f-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="6f22f-105">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6f22f-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6f22f-106">Membri</span><span class="sxs-lookup"><span data-stu-id="6f22f-106">Members</span></span>

<span data-ttu-id="6f22f-107">La raccolta **InterfacesForComponent** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="6f22f-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6f22f-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="6f22f-108">Related Collections</span></span>

<span data-ttu-id="6f22f-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f22f-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6f22f-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6f22f-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6f22f-111">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="6f22f-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="6f22f-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6f22f-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6f22f-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="6f22f-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="6f22f-114">**RolesForInterface**</span><span class="sxs-lookup"><span data-stu-id="6f22f-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="6f22f-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f22f-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6f22f-116">**Componenti**</span><span class="sxs-lookup"><span data-stu-id="6f22f-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="6f22f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f22f-117">Properties</span></span>

<span data-ttu-id="6f22f-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="6f22f-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6f22f-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f22f-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="6f22f-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-120">Description</span></span>](#description)
-   [<span data-ttu-id="6f22f-121">IID</span><span class="sxs-lookup"><span data-stu-id="6f22f-121">IID</span></span>](#iid)
-   [<span data-ttu-id="6f22f-122">Nome</span><span class="sxs-lookup"><span data-stu-id="6f22f-122">Name</span></span>](#name)
-   [<span data-ttu-id="6f22f-123">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="6f22f-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="6f22f-124">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="6f22f-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="6f22f-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f22f-125">CLSID</span></span>



| <span data-ttu-id="6f22f-126">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-126">Entry</span></span> | <span data-ttu-id="6f22f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="6f22f-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-128">Description</span></span>    | <span data-ttu-id="6f22f-129">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="6f22f-129">A GUID for the component.</span></span> |
| <span data-ttu-id="6f22f-130">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-130">Access</span></span>         | <span data-ttu-id="6f22f-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f22f-131">ReadOnly</span></span>                  |
| <span data-ttu-id="6f22f-132">Type</span><span class="sxs-lookup"><span data-stu-id="6f22f-132">Type</span></span>           | <span data-ttu-id="6f22f-133">string</span><span class="sxs-lookup"><span data-stu-id="6f22f-133">String</span></span>                    |
| <span data-ttu-id="6f22f-134">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-134">Default</span></span>        | <span data-ttu-id="6f22f-135">N/D</span><span class="sxs-lookup"><span data-stu-id="6f22f-135">N/A</span></span>                       |
| <span data-ttu-id="6f22f-136">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-136">Minimum system</span></span> | <span data-ttu-id="6f22f-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="6f22f-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-138">Description</span></span>



| <span data-ttu-id="6f22f-139">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-139">Entry</span></span> | <span data-ttu-id="6f22f-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="6f22f-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-141">Description</span></span>    | <span data-ttu-id="6f22f-142">Descrizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f22f-142">A description for the interface.</span></span> |
| <span data-ttu-id="6f22f-143">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-143">Access</span></span>         | <span data-ttu-id="6f22f-144">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f22f-144">ReadWrite</span></span>                        |
| <span data-ttu-id="6f22f-145">Type</span><span class="sxs-lookup"><span data-stu-id="6f22f-145">Type</span></span>           | <span data-ttu-id="6f22f-146">string</span><span class="sxs-lookup"><span data-stu-id="6f22f-146">String</span></span>                           |
| <span data-ttu-id="6f22f-147">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-147">Default</span></span>        | <span data-ttu-id="6f22f-148">""</span><span class="sxs-lookup"><span data-stu-id="6f22f-148">""</span></span>                               |
| <span data-ttu-id="6f22f-149">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-149">Minimum system</span></span> | <span data-ttu-id="6f22f-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="6f22f-151">IID</span><span class="sxs-lookup"><span data-stu-id="6f22f-151">IID</span></span>



| <span data-ttu-id="6f22f-152">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-152">Entry</span></span> | <span data-ttu-id="6f22f-153">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f22f-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-154">Description</span></span>    | <span data-ttu-id="6f22f-155">GUID per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f22f-155">A GUID for the interface.</span></span> <span data-ttu-id="6f22f-156">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f22f-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6f22f-157">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-157">Access</span></span>         | <span data-ttu-id="6f22f-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f22f-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="6f22f-159">Type</span><span class="sxs-lookup"><span data-stu-id="6f22f-159">Type</span></span>           | <span data-ttu-id="6f22f-160">string</span><span class="sxs-lookup"><span data-stu-id="6f22f-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="6f22f-161">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-161">Default</span></span>        | <span data-ttu-id="6f22f-162">N/D</span><span class="sxs-lookup"><span data-stu-id="6f22f-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="6f22f-163">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-163">Minimum system</span></span> | <span data-ttu-id="6f22f-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="6f22f-165">Nome</span><span class="sxs-lookup"><span data-stu-id="6f22f-165">Name</span></span>



| <span data-ttu-id="6f22f-166">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-166">Entry</span></span> | <span data-ttu-id="6f22f-167">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f22f-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-168">Description</span></span>    | <span data-ttu-id="6f22f-169">Nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6f22f-169">A name for the interface.</span></span> <span data-ttu-id="6f22f-170">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f22f-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6f22f-171">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-171">Access</span></span>         | <span data-ttu-id="6f22f-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f22f-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="6f22f-173">Type</span><span class="sxs-lookup"><span data-stu-id="6f22f-173">Type</span></span>           | <span data-ttu-id="6f22f-174">string</span><span class="sxs-lookup"><span data-stu-id="6f22f-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="6f22f-175">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-175">Default</span></span>        | <span data-ttu-id="6f22f-176">N/D</span><span class="sxs-lookup"><span data-stu-id="6f22f-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="6f22f-177">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-177">Minimum system</span></span> | <span data-ttu-id="6f22f-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="6f22f-179">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="6f22f-179">QueuingEnabled</span></span>



| <span data-ttu-id="6f22f-180">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-180">Entry</span></span> | <span data-ttu-id="6f22f-181">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f22f-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-182">Description</span></span>    | <span data-ttu-id="6f22f-183">Contrassegna l'interfaccia come accodabile e può essere impostata tramite l'SDK di amministrazione o lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="6f22f-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="6f22f-184">Tuttavia, è possibile impostare il flag di **Accodamento abilitato** solo per un'interfaccia con il flag di **Accodamento supportato** impostato.</span><span class="sxs-lookup"><span data-stu-id="6f22f-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="6f22f-185">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-185">Access</span></span>         | <span data-ttu-id="6f22f-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6f22f-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="6f22f-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f22f-187">Type</span></span>           | <span data-ttu-id="6f22f-188">Bool</span><span class="sxs-lookup"><span data-stu-id="6f22f-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="6f22f-189">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-189">Default</span></span>        | <span data-ttu-id="6f22f-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6f22f-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="6f22f-191">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-191">Minimum system</span></span> | <span data-ttu-id="6f22f-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="6f22f-193">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="6f22f-193">QueueingSupported</span></span>



| <span data-ttu-id="6f22f-194">Voce</span><span class="sxs-lookup"><span data-stu-id="6f22f-194">Entry</span></span> | <span data-ttu-id="6f22f-195">Valore</span><span class="sxs-lookup"><span data-stu-id="6f22f-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f22f-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f22f-196">Description</span></span>    | <span data-ttu-id="6f22f-197">L'interfaccia supporta l'accodamento.</span><span class="sxs-lookup"><span data-stu-id="6f22f-197">Interface supports queuing.</span></span> <span data-ttu-id="6f22f-198">Affinché un'interfaccia supporti l'accodamento, tutti i metodi devono avere solo parametri in.</span><span class="sxs-lookup"><span data-stu-id="6f22f-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="6f22f-199">L' **Accodamento supportato** viene esposto come proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f22f-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="6f22f-200">Access</span><span class="sxs-lookup"><span data-stu-id="6f22f-200">Access</span></span>         | <span data-ttu-id="6f22f-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f22f-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="6f22f-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f22f-202">Type</span></span>           | <span data-ttu-id="6f22f-203">Bool</span><span class="sxs-lookup"><span data-stu-id="6f22f-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6f22f-204">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6f22f-204">Default</span></span>        | <span data-ttu-id="6f22f-205">Falso</span><span class="sxs-lookup"><span data-stu-id="6f22f-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6f22f-206">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6f22f-206">Minimum system</span></span> | <span data-ttu-id="6f22f-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f22f-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="6f22f-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f22f-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f22f-209">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="6f22f-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
