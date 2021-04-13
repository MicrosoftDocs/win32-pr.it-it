---
description: Contiene un elenco dei protocolli che devono essere utilizzati da DCOM. Contiene un oggetto per ogni protocollo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Raccolta DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483213"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="3ab67-104">Raccolta DCOMProtocols</span><span class="sxs-lookup"><span data-stu-id="3ab67-104">DCOMProtocols collection</span></span>

<span data-ttu-id="3ab67-105">Contiene un elenco dei protocolli che devono essere utilizzati da DCOM.</span><span class="sxs-lookup"><span data-stu-id="3ab67-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="3ab67-106">Contiene un oggetto per ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="3ab67-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="3ab67-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="3ab67-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3ab67-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3ab67-108">Members</span></span>

<span data-ttu-id="3ab67-109">La raccolta **DCOMProtocols** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3ab67-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3ab67-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="3ab67-110">Related Collections</span></span>

<span data-ttu-id="3ab67-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ab67-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3ab67-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3ab67-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3ab67-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3ab67-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3ab67-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="3ab67-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3ab67-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ab67-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3ab67-116">**Radice**</span><span class="sxs-lookup"><span data-stu-id="3ab67-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="3ab67-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ab67-117">Properties</span></span>

<span data-ttu-id="3ab67-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="3ab67-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3ab67-119">Nome</span><span class="sxs-lookup"><span data-stu-id="3ab67-119">Name</span></span>](#name)
-   [<span data-ttu-id="3ab67-120">Ordine</span><span class="sxs-lookup"><span data-stu-id="3ab67-120">Order</span></span>](#order)
-   [<span data-ttu-id="3ab67-121">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="3ab67-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="3ab67-122">Nome</span><span class="sxs-lookup"><span data-stu-id="3ab67-122">Name</span></span>



| <span data-ttu-id="3ab67-123">Voce</span><span class="sxs-lookup"><span data-stu-id="3ab67-123">Entry</span></span> | <span data-ttu-id="3ab67-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab67-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab67-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ab67-125">Description</span></span>    | <span data-ttu-id="3ab67-126">Nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3ab67-126">The name of the protocol.</span></span> <span data-ttu-id="3ab67-127">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="3ab67-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3ab67-128">Access</span><span class="sxs-lookup"><span data-stu-id="3ab67-128">Access</span></span>         | <span data-ttu-id="3ab67-129">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ab67-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="3ab67-130">Type</span><span class="sxs-lookup"><span data-stu-id="3ab67-130">Type</span></span>           | <span data-ttu-id="3ab67-131">string</span><span class="sxs-lookup"><span data-stu-id="3ab67-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="3ab67-132">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ab67-132">Default</span></span>        | <span data-ttu-id="3ab67-133">"Nuovo protocollo"</span><span class="sxs-lookup"><span data-stu-id="3ab67-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="3ab67-134">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ab67-134">Minimum system</span></span> | <span data-ttu-id="3ab67-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ab67-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="3ab67-136">JSON</span><span class="sxs-lookup"><span data-stu-id="3ab67-136">Order</span></span>



| <span data-ttu-id="3ab67-137">Voce</span><span class="sxs-lookup"><span data-stu-id="3ab67-137">Entry</span></span> | <span data-ttu-id="3ab67-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab67-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="3ab67-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ab67-139">Description</span></span>    | <span data-ttu-id="3ab67-140">Ordine in cui provare il protocollo.</span><span class="sxs-lookup"><span data-stu-id="3ab67-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="3ab67-141">Access</span><span class="sxs-lookup"><span data-stu-id="3ab67-141">Access</span></span>         | <span data-ttu-id="3ab67-142">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ab67-142">ReadWrite</span></span>                               |
| <span data-ttu-id="3ab67-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ab67-143">Type</span></span>           | <span data-ttu-id="3ab67-144">Long (0-65000)</span><span class="sxs-lookup"><span data-stu-id="3ab67-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="3ab67-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ab67-145">Default</span></span>        | <span data-ttu-id="3ab67-146">0</span><span class="sxs-lookup"><span data-stu-id="3ab67-146">0</span></span>                                       |
| <span data-ttu-id="3ab67-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ab67-147">Minimum system</span></span> | <span data-ttu-id="3ab67-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ab67-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="3ab67-149">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="3ab67-149">ProtocolCode</span></span>



| <span data-ttu-id="3ab67-150">Voce</span><span class="sxs-lookup"><span data-stu-id="3ab67-150">Entry</span></span> | <span data-ttu-id="3ab67-151">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab67-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab67-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ab67-152">Description</span></span>    | <span data-ttu-id="3ab67-153">Codice che specifica la sequenza del protocollo RPC.</span><span class="sxs-lookup"><span data-stu-id="3ab67-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="3ab67-154">I codici di protocollo supportati sono i seguenti: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="3ab67-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="3ab67-155">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="3ab67-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3ab67-156">Access</span><span class="sxs-lookup"><span data-stu-id="3ab67-156">Access</span></span>         | <span data-ttu-id="3ab67-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="3ab67-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3ab67-158">Type</span><span class="sxs-lookup"><span data-stu-id="3ab67-158">Type</span></span>           | <span data-ttu-id="3ab67-159">string</span><span class="sxs-lookup"><span data-stu-id="3ab67-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3ab67-160">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ab67-160">Default</span></span>        | <span data-ttu-id="3ab67-161">""</span><span class="sxs-lookup"><span data-stu-id="3ab67-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ab67-162">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ab67-162">Minimum system</span></span> | <span data-ttu-id="3ab67-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ab67-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="3ab67-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ab67-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab67-165">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="3ab67-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
