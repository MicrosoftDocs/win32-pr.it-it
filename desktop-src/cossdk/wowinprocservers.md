---
description: Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit. Contiene un oggetto per ogni componente.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Raccolta WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523234"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="742e8-104">Raccolta WOWInprocServers</span><span class="sxs-lookup"><span data-stu-id="742e8-104">WOWInprocServers collection</span></span>

<span data-ttu-id="742e8-105">Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="742e8-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="742e8-106">Contiene un oggetto per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="742e8-106">It contains an object for each component.</span></span>

<span data-ttu-id="742e8-107">Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="742e8-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="742e8-108">Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="742e8-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="742e8-109">Membri</span><span class="sxs-lookup"><span data-stu-id="742e8-109">Members</span></span>

<span data-ttu-id="742e8-110">La raccolta **WOWInprocServers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="742e8-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="742e8-111">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="742e8-111">Related Collections</span></span>

<span data-ttu-id="742e8-112">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="742e8-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="742e8-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="742e8-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="742e8-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="742e8-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="742e8-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="742e8-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="742e8-116">**Radice**</span><span class="sxs-lookup"><span data-stu-id="742e8-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="742e8-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="742e8-117">Properties</span></span>

<span data-ttu-id="742e8-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="742e8-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="742e8-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="742e8-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="742e8-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="742e8-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="742e8-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="742e8-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="742e8-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="742e8-122">CLSID</span></span>



| <span data-ttu-id="742e8-123">Voce</span><span class="sxs-lookup"><span data-stu-id="742e8-123">Entry</span></span> | <span data-ttu-id="742e8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="742e8-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742e8-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="742e8-125">Description</span></span>    | <span data-ttu-id="742e8-126">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="742e8-126">A GUID for the component.</span></span> <span data-ttu-id="742e8-127">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="742e8-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="742e8-128">Access</span><span class="sxs-lookup"><span data-stu-id="742e8-128">Access</span></span>         | <span data-ttu-id="742e8-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="742e8-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="742e8-130">Type</span><span class="sxs-lookup"><span data-stu-id="742e8-130">Type</span></span>           | <span data-ttu-id="742e8-131">string</span><span class="sxs-lookup"><span data-stu-id="742e8-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="742e8-132">Predefinito</span><span class="sxs-lookup"><span data-stu-id="742e8-132">Default</span></span>        | <span data-ttu-id="742e8-133">N/D</span><span class="sxs-lookup"><span data-stu-id="742e8-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="742e8-134">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="742e8-134">Minimum system</span></span> | <span data-ttu-id="742e8-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="742e8-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="742e8-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="742e8-136">InprocServer32</span></span>



| <span data-ttu-id="742e8-137">Voce</span><span class="sxs-lookup"><span data-stu-id="742e8-137">Entry</span></span> | <span data-ttu-id="742e8-138">Valore</span><span class="sxs-lookup"><span data-stu-id="742e8-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="742e8-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="742e8-139">Description</span></span>    | <span data-ttu-id="742e8-140">Percorso del file per il componente.</span><span class="sxs-lookup"><span data-stu-id="742e8-140">The file path for the component.</span></span> |
| <span data-ttu-id="742e8-141">Access</span><span class="sxs-lookup"><span data-stu-id="742e8-141">Access</span></span>         | <span data-ttu-id="742e8-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="742e8-142">ReadOnly</span></span>                         |
| <span data-ttu-id="742e8-143">Type</span><span class="sxs-lookup"><span data-stu-id="742e8-143">Type</span></span>           | <span data-ttu-id="742e8-144">string</span><span class="sxs-lookup"><span data-stu-id="742e8-144">String</span></span>                           |
| <span data-ttu-id="742e8-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="742e8-145">Default</span></span>        | <span data-ttu-id="742e8-146">N/D</span><span class="sxs-lookup"><span data-stu-id="742e8-146">N/A</span></span>                              |
| <span data-ttu-id="742e8-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="742e8-147">Minimum system</span></span> | <span data-ttu-id="742e8-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="742e8-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="742e8-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="742e8-149">ProgID</span></span>



| <span data-ttu-id="742e8-150">Voce</span><span class="sxs-lookup"><span data-stu-id="742e8-150">Entry</span></span> | <span data-ttu-id="742e8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="742e8-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742e8-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="742e8-152">Description</span></span>    | <span data-ttu-id="742e8-153">Nome che identifica il componente.</span><span class="sxs-lookup"><span data-stu-id="742e8-153">A name identifying the component.</span></span> <span data-ttu-id="742e8-154">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="742e8-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="742e8-155">Access</span><span class="sxs-lookup"><span data-stu-id="742e8-155">Access</span></span>         | <span data-ttu-id="742e8-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="742e8-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="742e8-157">Type</span><span class="sxs-lookup"><span data-stu-id="742e8-157">Type</span></span>           | <span data-ttu-id="742e8-158">string</span><span class="sxs-lookup"><span data-stu-id="742e8-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="742e8-159">Predefinito</span><span class="sxs-lookup"><span data-stu-id="742e8-159">Default</span></span>        | <span data-ttu-id="742e8-160">N/D</span><span class="sxs-lookup"><span data-stu-id="742e8-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="742e8-161">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="742e8-161">Minimum system</span></span> | <span data-ttu-id="742e8-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="742e8-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="742e8-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="742e8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742e8-164">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="742e8-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
