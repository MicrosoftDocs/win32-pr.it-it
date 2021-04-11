---
description: Recupera le informazioni relative alle classi di evento.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Raccolta EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126588"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="f1a17-103">Raccolta EventClassesForIID</span><span class="sxs-lookup"><span data-stu-id="f1a17-103">EventClassesForIID collection</span></span>

<span data-ttu-id="f1a17-104">Recupera le informazioni relative alle classi di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="f1a17-105">La connessione tra il server di pubblicazione e i sottoscrittori viene gestita da un oggetto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , ovvero un componente COM+ che contiene le interfacce e i metodi utilizzati da un server di pubblicazione per generare eventi.</span><span class="sxs-lookup"><span data-stu-id="f1a17-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="f1a17-106">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f1a17-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f1a17-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f1a17-107">Members</span></span>

<span data-ttu-id="f1a17-108">La raccolta **EventClassesForIID** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f1a17-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f1a17-109">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="f1a17-109">Related Collections</span></span>

<span data-ttu-id="f1a17-110">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1a17-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f1a17-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f1a17-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f1a17-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f1a17-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f1a17-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f1a17-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f1a17-114">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1a17-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f1a17-115">**Radice**</span><span class="sxs-lookup"><span data-stu-id="f1a17-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="f1a17-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1a17-116">Properties</span></span>

<span data-ttu-id="f1a17-117">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="f1a17-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f1a17-118">Applicazione</span><span class="sxs-lookup"><span data-stu-id="f1a17-118">Application</span></span>](#application)
-   [<span data-ttu-id="f1a17-119">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="f1a17-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="f1a17-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1a17-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="f1a17-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-121">Description</span></span>](#description)
-   [<span data-ttu-id="f1a17-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f1a17-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="f1a17-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="f1a17-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="f1a17-124">Applicazione</span><span class="sxs-lookup"><span data-stu-id="f1a17-124">Application</span></span>



| <span data-ttu-id="f1a17-125">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-125">Entry</span></span> | <span data-ttu-id="f1a17-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="f1a17-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-127">Description</span></span>    | <span data-ttu-id="f1a17-128">GUID per l'applicazione che contiene la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="f1a17-129">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-129">Access</span></span>         | <span data-ttu-id="f1a17-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="f1a17-131">Type</span><span class="sxs-lookup"><span data-stu-id="f1a17-131">Type</span></span>           | <span data-ttu-id="f1a17-132">string</span><span class="sxs-lookup"><span data-stu-id="f1a17-132">String</span></span>                                                   |
| <span data-ttu-id="f1a17-133">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-133">Default</span></span>        | <span data-ttu-id="f1a17-134">N/D</span><span class="sxs-lookup"><span data-stu-id="f1a17-134">N/A</span></span>                                                      |
| <span data-ttu-id="f1a17-135">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-135">Minimum system</span></span> | <span data-ttu-id="f1a17-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="f1a17-137">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="f1a17-137">Bitness</span></span>



| <span data-ttu-id="f1a17-138">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-138">Entry</span></span> | <span data-ttu-id="f1a17-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a17-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-140">Description</span></span>    | <span data-ttu-id="f1a17-141">Rappresenta il tipo bit binario della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="f1a17-142">Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f1a17-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="f1a17-143">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-143">Access</span></span>         | <span data-ttu-id="f1a17-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="f1a17-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1a17-145">Type</span></span>           | <span data-ttu-id="f1a17-146">Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="f1a17-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="f1a17-147">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-147">Default</span></span>        | <span data-ttu-id="f1a17-148">N/D</span><span class="sxs-lookup"><span data-stu-id="f1a17-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f1a17-149">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-149">Minimum system</span></span> | <span data-ttu-id="f1a17-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="f1a17-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1a17-151">CLSID</span></span>



| <span data-ttu-id="f1a17-152">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-152">Entry</span></span> | <span data-ttu-id="f1a17-153">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a17-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-154">Description</span></span>    | <span data-ttu-id="f1a17-155">GUID per la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-155">The GUID for the event class.</span></span> <span data-ttu-id="f1a17-156">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f1a17-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f1a17-157">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-157">Access</span></span>         | <span data-ttu-id="f1a17-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="f1a17-159">Type</span><span class="sxs-lookup"><span data-stu-id="f1a17-159">Type</span></span>           | <span data-ttu-id="f1a17-160">string</span><span class="sxs-lookup"><span data-stu-id="f1a17-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="f1a17-161">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-161">Default</span></span>        | <span data-ttu-id="f1a17-162">N/D</span><span class="sxs-lookup"><span data-stu-id="f1a17-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="f1a17-163">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-163">Minimum system</span></span> | <span data-ttu-id="f1a17-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="f1a17-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-165">Description</span></span>



| <span data-ttu-id="f1a17-166">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-166">Entry</span></span> | <span data-ttu-id="f1a17-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="f1a17-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-168">Description</span></span>    | <span data-ttu-id="f1a17-169">Descrive la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-169">Describes the event class.</span></span> |
| <span data-ttu-id="f1a17-170">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-170">Access</span></span>         | <span data-ttu-id="f1a17-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-171">ReadOnly</span></span>                   |
| <span data-ttu-id="f1a17-172">Type</span><span class="sxs-lookup"><span data-stu-id="f1a17-172">Type</span></span>           | <span data-ttu-id="f1a17-173">string</span><span class="sxs-lookup"><span data-stu-id="f1a17-173">String</span></span>                     |
| <span data-ttu-id="f1a17-174">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-174">Default</span></span>        | <span data-ttu-id="f1a17-175">""</span><span class="sxs-lookup"><span data-stu-id="f1a17-175">""</span></span>                         |
| <span data-ttu-id="f1a17-176">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-176">Minimum system</span></span> | <span data-ttu-id="f1a17-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="f1a17-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f1a17-178">IsPrivateComponent</span></span>



| <span data-ttu-id="f1a17-179">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-179">Entry</span></span> | <span data-ttu-id="f1a17-180">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="f1a17-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-181">Description</span></span>    | <span data-ttu-id="f1a17-182">Indica se il componente della classe di evento è privato.</span><span class="sxs-lookup"><span data-stu-id="f1a17-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="f1a17-183">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-183">Access</span></span>         | <span data-ttu-id="f1a17-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="f1a17-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1a17-185">Type</span></span>           | <span data-ttu-id="f1a17-186">Bool</span><span class="sxs-lookup"><span data-stu-id="f1a17-186">Bool</span></span>                                                    |
| <span data-ttu-id="f1a17-187">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-187">Default</span></span>        | <span data-ttu-id="f1a17-188">Falso</span><span class="sxs-lookup"><span data-stu-id="f1a17-188">False</span></span>                                                   |
| <span data-ttu-id="f1a17-189">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-189">Minimum system</span></span> | <span data-ttu-id="f1a17-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="f1a17-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="f1a17-191">ProgID</span></span>



| <span data-ttu-id="f1a17-192">Voce</span><span class="sxs-lookup"><span data-stu-id="f1a17-192">Entry</span></span> | <span data-ttu-id="f1a17-193">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a17-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a17-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a17-194">Description</span></span>    | <span data-ttu-id="f1a17-195">Nome descrittivo usato per identificare la classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1a17-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="f1a17-196">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f1a17-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f1a17-197">Access</span><span class="sxs-lookup"><span data-stu-id="f1a17-197">Access</span></span>         | <span data-ttu-id="f1a17-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1a17-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="f1a17-199">Type</span><span class="sxs-lookup"><span data-stu-id="f1a17-199">Type</span></span>           | <span data-ttu-id="f1a17-200">string</span><span class="sxs-lookup"><span data-stu-id="f1a17-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f1a17-201">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f1a17-201">Default</span></span>        | <span data-ttu-id="f1a17-202">""</span><span class="sxs-lookup"><span data-stu-id="f1a17-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="f1a17-203">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="f1a17-203">Minimum system</span></span> | <span data-ttu-id="f1a17-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1a17-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="f1a17-205">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1a17-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a17-206">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="f1a17-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
