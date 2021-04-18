---
description: Le proprietà esposte per la raccolta WOWLegacyServers devono essere identiche alla raccolta LegacyServers, ad eccezione del fatto che la raccolta WOWLegacyServers viene disegnata dal registro di sistema a 32 bit nei computer a 64 bit.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Raccolta WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304722"
---
# <a name="wowlegacyservers-collection"></a><span data-ttu-id="b1d22-103">Raccolta WOWLegacyServers</span><span class="sxs-lookup"><span data-stu-id="b1d22-103">WOWLegacyServers collection</span></span>

<span data-ttu-id="b1d22-104">Le proprietà esposte per la raccolta **WOWLegacyServers** devono essere identiche alla raccolta [**LegacyServers**](legacyservers.md) , ad eccezione del fatto che la raccolta **WOWLegacyServers** viene disegnata dal registro di sistema a 32 bit nei computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b1d22-104">Exposed properties for the **WOWLegacyServers** collection are intended to be identical to the [**LegacyServers**](legacyservers.md) collection except that the **WOWLegacyServers** collection is drawn from the 32-bit registry on 64-bit computers.</span></span>

<span data-ttu-id="b1d22-105">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b1d22-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b1d22-106">Membri</span><span class="sxs-lookup"><span data-stu-id="b1d22-106">Members</span></span>

<span data-ttu-id="b1d22-107">La raccolta **WOWLegacyServers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b1d22-107">The **WOWLegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b1d22-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="b1d22-108">Related Collections</span></span>

<span data-ttu-id="b1d22-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1d22-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b1d22-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b1d22-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b1d22-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b1d22-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b1d22-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b1d22-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b1d22-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1d22-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b1d22-114">**Radice**</span><span class="sxs-lookup"><span data-stu-id="b1d22-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b1d22-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1d22-115">Properties</span></span>

<span data-ttu-id="b1d22-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="b1d22-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b1d22-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="b1d22-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="b1d22-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1d22-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="b1d22-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b1d22-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="b1d22-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b1d22-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="b1d22-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="b1d22-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="b1d22-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="b1d22-122">ClassName</span></span>



| <span data-ttu-id="b1d22-123">Voce</span><span class="sxs-lookup"><span data-stu-id="b1d22-123">Entry</span></span> | <span data-ttu-id="b1d22-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d22-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="b1d22-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d22-125">Description</span></span>    | <span data-ttu-id="b1d22-126">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="b1d22-126">The name of the class.</span></span> |
| <span data-ttu-id="b1d22-127">Access</span><span class="sxs-lookup"><span data-stu-id="b1d22-127">Access</span></span>         | <span data-ttu-id="b1d22-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1d22-128">ReadOnly</span></span>               |
| <span data-ttu-id="b1d22-129">Type</span><span class="sxs-lookup"><span data-stu-id="b1d22-129">Type</span></span>           | <span data-ttu-id="b1d22-130">string</span><span class="sxs-lookup"><span data-stu-id="b1d22-130">String</span></span>                 |
| <span data-ttu-id="b1d22-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1d22-131">Default</span></span>        | <span data-ttu-id="b1d22-132">N/D</span><span class="sxs-lookup"><span data-stu-id="b1d22-132">N/A</span></span>                    |
| <span data-ttu-id="b1d22-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b1d22-133">Minimum system</span></span> | <span data-ttu-id="b1d22-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1d22-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="b1d22-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1d22-135">CLSID</span></span>



| <span data-ttu-id="b1d22-136">Voce</span><span class="sxs-lookup"><span data-stu-id="b1d22-136">Entry</span></span> | <span data-ttu-id="b1d22-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d22-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d22-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d22-138">Description</span></span>    | <span data-ttu-id="b1d22-139">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="b1d22-139">A GUID for the component.</span></span> <span data-ttu-id="b1d22-140">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="b1d22-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1d22-141">Access</span><span class="sxs-lookup"><span data-stu-id="b1d22-141">Access</span></span>         | <span data-ttu-id="b1d22-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1d22-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="b1d22-143">Type</span><span class="sxs-lookup"><span data-stu-id="b1d22-143">Type</span></span>           | <span data-ttu-id="b1d22-144">string</span><span class="sxs-lookup"><span data-stu-id="b1d22-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="b1d22-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1d22-145">Default</span></span>        | <span data-ttu-id="b1d22-146">N/D</span><span class="sxs-lookup"><span data-stu-id="b1d22-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="b1d22-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b1d22-147">Minimum system</span></span> | <span data-ttu-id="b1d22-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1d22-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="b1d22-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b1d22-149">InprocServer32</span></span>



| <span data-ttu-id="b1d22-150">Voce</span><span class="sxs-lookup"><span data-stu-id="b1d22-150">Entry</span></span> | <span data-ttu-id="b1d22-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d22-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="b1d22-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d22-152">Description</span></span>    | <span data-ttu-id="b1d22-153">Percorso del file per il componente.</span><span class="sxs-lookup"><span data-stu-id="b1d22-153">The file path for the component.</span></span> |
| <span data-ttu-id="b1d22-154">Access</span><span class="sxs-lookup"><span data-stu-id="b1d22-154">Access</span></span>         | <span data-ttu-id="b1d22-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1d22-155">ReadOnly</span></span>                         |
| <span data-ttu-id="b1d22-156">Type</span><span class="sxs-lookup"><span data-stu-id="b1d22-156">Type</span></span>           | <span data-ttu-id="b1d22-157">string</span><span class="sxs-lookup"><span data-stu-id="b1d22-157">String</span></span>                           |
| <span data-ttu-id="b1d22-158">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1d22-158">Default</span></span>        | <span data-ttu-id="b1d22-159">N/D</span><span class="sxs-lookup"><span data-stu-id="b1d22-159">N/A</span></span>                              |
| <span data-ttu-id="b1d22-160">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b1d22-160">Minimum system</span></span> | <span data-ttu-id="b1d22-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1d22-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="b1d22-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b1d22-162">LocalServer32</span></span>



| <span data-ttu-id="b1d22-163">Voce</span><span class="sxs-lookup"><span data-stu-id="b1d22-163">Entry</span></span> | <span data-ttu-id="b1d22-164">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d22-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="b1d22-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d22-165">Description</span></span>    | <span data-ttu-id="b1d22-166">Specifica il percorso completo di un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b1d22-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="b1d22-167">Access</span><span class="sxs-lookup"><span data-stu-id="b1d22-167">Access</span></span>         | <span data-ttu-id="b1d22-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1d22-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="b1d22-169">Type</span><span class="sxs-lookup"><span data-stu-id="b1d22-169">Type</span></span>           | <span data-ttu-id="b1d22-170">string</span><span class="sxs-lookup"><span data-stu-id="b1d22-170">String</span></span>                                                        |
| <span data-ttu-id="b1d22-171">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1d22-171">Default</span></span>        | <span data-ttu-id="b1d22-172">N/D</span><span class="sxs-lookup"><span data-stu-id="b1d22-172">N/A</span></span>                                                           |
| <span data-ttu-id="b1d22-173">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b1d22-173">Minimum system</span></span> | <span data-ttu-id="b1d22-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1d22-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="b1d22-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="b1d22-175">ProgID</span></span>



| <span data-ttu-id="b1d22-176">Voce</span><span class="sxs-lookup"><span data-stu-id="b1d22-176">Entry</span></span> | <span data-ttu-id="b1d22-177">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d22-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d22-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d22-178">Description</span></span>    | <span data-ttu-id="b1d22-179">Nome che identifica il componente.</span><span class="sxs-lookup"><span data-stu-id="b1d22-179">A name identifying the component.</span></span> <span data-ttu-id="b1d22-180">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="b1d22-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1d22-181">Access</span><span class="sxs-lookup"><span data-stu-id="b1d22-181">Access</span></span>         | <span data-ttu-id="b1d22-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b1d22-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="b1d22-183">Type</span><span class="sxs-lookup"><span data-stu-id="b1d22-183">Type</span></span>           | <span data-ttu-id="b1d22-184">string</span><span class="sxs-lookup"><span data-stu-id="b1d22-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="b1d22-185">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1d22-185">Default</span></span>        | <span data-ttu-id="b1d22-186">N/D</span><span class="sxs-lookup"><span data-stu-id="b1d22-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="b1d22-187">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b1d22-187">Minimum system</span></span> | <span data-ttu-id="b1d22-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1d22-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="b1d22-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1d22-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d22-190">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="b1d22-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
