---
description: Contiene un elenco dei server in-process registrati con il sistema. Contiene un oggetto per ogni componente registrato come server in-process.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Raccolta InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304616"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="8e6be-104">Raccolta InprocServers</span><span class="sxs-lookup"><span data-stu-id="8e6be-104">InprocServers collection</span></span>

<span data-ttu-id="8e6be-105">Contiene un elenco dei server in-process registrati con il sistema.</span><span class="sxs-lookup"><span data-stu-id="8e6be-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="8e6be-106">Contiene un oggetto per ogni componente registrato come server in-process.</span><span class="sxs-lookup"><span data-stu-id="8e6be-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="8e6be-107">Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="8e6be-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="8e6be-108">Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="8e6be-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8e6be-109">Membri</span><span class="sxs-lookup"><span data-stu-id="8e6be-109">Members</span></span>

<span data-ttu-id="8e6be-110">La raccolta **InprocServers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8e6be-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8e6be-111">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="8e6be-111">Related Collections</span></span>

<span data-ttu-id="8e6be-112">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e6be-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8e6be-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8e6be-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8e6be-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8e6be-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="8e6be-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e6be-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8e6be-116">**Radice**</span><span class="sxs-lookup"><span data-stu-id="8e6be-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="8e6be-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e6be-117">Properties</span></span>

<span data-ttu-id="8e6be-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="8e6be-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8e6be-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="8e6be-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="8e6be-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="8e6be-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="8e6be-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="8e6be-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="8e6be-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="8e6be-122">CLSID</span></span>



| <span data-ttu-id="8e6be-123">Voce</span><span class="sxs-lookup"><span data-stu-id="8e6be-123">Entry</span></span> | <span data-ttu-id="8e6be-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8e6be-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6be-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e6be-125">Description</span></span>    | <span data-ttu-id="8e6be-126">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="8e6be-126">A GUID for the component.</span></span> <span data-ttu-id="8e6be-127">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8e6be-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8e6be-128">Access</span><span class="sxs-lookup"><span data-stu-id="8e6be-128">Access</span></span>         | <span data-ttu-id="8e6be-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e6be-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="8e6be-130">Type</span><span class="sxs-lookup"><span data-stu-id="8e6be-130">Type</span></span>           | <span data-ttu-id="8e6be-131">string</span><span class="sxs-lookup"><span data-stu-id="8e6be-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="8e6be-132">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8e6be-132">Default</span></span>        | <span data-ttu-id="8e6be-133">N/D</span><span class="sxs-lookup"><span data-stu-id="8e6be-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="8e6be-134">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8e6be-134">Minimum system</span></span> | <span data-ttu-id="8e6be-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8e6be-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="8e6be-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="8e6be-136">InprocServer32</span></span>



| <span data-ttu-id="8e6be-137">Voce</span><span class="sxs-lookup"><span data-stu-id="8e6be-137">Entry</span></span> | <span data-ttu-id="8e6be-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8e6be-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="8e6be-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e6be-139">Description</span></span>    | <span data-ttu-id="8e6be-140">Percorso del file per il componente.</span><span class="sxs-lookup"><span data-stu-id="8e6be-140">The file path for the component.</span></span> |
| <span data-ttu-id="8e6be-141">Access</span><span class="sxs-lookup"><span data-stu-id="8e6be-141">Access</span></span>         | <span data-ttu-id="8e6be-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e6be-142">ReadOnly</span></span>                         |
| <span data-ttu-id="8e6be-143">Type</span><span class="sxs-lookup"><span data-stu-id="8e6be-143">Type</span></span>           | <span data-ttu-id="8e6be-144">string</span><span class="sxs-lookup"><span data-stu-id="8e6be-144">String</span></span>                           |
| <span data-ttu-id="8e6be-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8e6be-145">Default</span></span>        | <span data-ttu-id="8e6be-146">N/D</span><span class="sxs-lookup"><span data-stu-id="8e6be-146">N/A</span></span>                              |
| <span data-ttu-id="8e6be-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8e6be-147">Minimum system</span></span> | <span data-ttu-id="8e6be-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8e6be-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="8e6be-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="8e6be-149">ProgID</span></span>



| <span data-ttu-id="8e6be-150">Voce</span><span class="sxs-lookup"><span data-stu-id="8e6be-150">Entry</span></span> | <span data-ttu-id="8e6be-151">Valore</span><span class="sxs-lookup"><span data-stu-id="8e6be-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6be-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e6be-152">Description</span></span>    | <span data-ttu-id="8e6be-153">Nome che identifica il componente.</span><span class="sxs-lookup"><span data-stu-id="8e6be-153">A name identifying the component.</span></span> <span data-ttu-id="8e6be-154">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8e6be-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8e6be-155">Access</span><span class="sxs-lookup"><span data-stu-id="8e6be-155">Access</span></span>         | <span data-ttu-id="8e6be-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8e6be-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="8e6be-157">Type</span><span class="sxs-lookup"><span data-stu-id="8e6be-157">Type</span></span>           | <span data-ttu-id="8e6be-158">string</span><span class="sxs-lookup"><span data-stu-id="8e6be-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="8e6be-159">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8e6be-159">Default</span></span>        | <span data-ttu-id="8e6be-160">N/D</span><span class="sxs-lookup"><span data-stu-id="8e6be-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="8e6be-161">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8e6be-161">Minimum system</span></span> | <span data-ttu-id="8e6be-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8e6be-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="8e6be-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e6be-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e6be-164">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="8e6be-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
