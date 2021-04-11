---
description: Contiene un elenco dei computer server nel cluster di applicazioni. Contiene un oggetto per ogni server.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Raccolta ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126597"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="405ca-104">Raccolta ApplicationCluster</span><span class="sxs-lookup"><span data-stu-id="405ca-104">ApplicationCluster collection</span></span>

<span data-ttu-id="405ca-105">Contiene un elenco dei computer server nel cluster di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="405ca-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="405ca-106">Contiene un oggetto per ogni server.</span><span class="sxs-lookup"><span data-stu-id="405ca-106">It contains an object for each server.</span></span> <span data-ttu-id="405ca-107">Si tratta di una raccolta di primo livello.</span><span class="sxs-lookup"><span data-stu-id="405ca-107">This is a top-level collection.</span></span>

<span data-ttu-id="405ca-108">Il cluster di applicazioni viene definito a scopo del servizio di bilanciamento del carico del componente (CLB).</span><span class="sxs-lookup"><span data-stu-id="405ca-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="405ca-109">Per usare la raccolta di cluster di applicazioni, è necessario che il servizio CLB sia installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="405ca-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="405ca-110">È possibile designare un router nel cluster di applicazioni con la proprietà IsSynchronized nell'oggetto raccolta [**LocalComputer**](localcomputer.md) e si designa che un determinato componente deve essere sottoposto a bilanciamento del carico con la proprietà LoadBalancingSupported su un oggetto raccolta di [**componenti**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="405ca-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="405ca-111">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="405ca-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="405ca-112">Membri</span><span class="sxs-lookup"><span data-stu-id="405ca-112">Members</span></span>

<span data-ttu-id="405ca-113">La raccolta **ApplicationCluster** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="405ca-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="405ca-114">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="405ca-114">Related Collections</span></span>

<span data-ttu-id="405ca-115">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="405ca-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="405ca-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="405ca-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="405ca-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="405ca-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="405ca-118">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="405ca-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="405ca-119">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="405ca-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="405ca-120">**Radice**</span><span class="sxs-lookup"><span data-stu-id="405ca-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="405ca-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="405ca-121">Properties</span></span>

<span data-ttu-id="405ca-122">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="405ca-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="405ca-123">Nome</span><span class="sxs-lookup"><span data-stu-id="405ca-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="405ca-124">Nome</span><span class="sxs-lookup"><span data-stu-id="405ca-124">Name</span></span>



| <span data-ttu-id="405ca-125">Voce</span><span class="sxs-lookup"><span data-stu-id="405ca-125">Entry</span></span> | <span data-ttu-id="405ca-126">Valore</span><span class="sxs-lookup"><span data-stu-id="405ca-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="405ca-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="405ca-127">Description</span></span>    | <span data-ttu-id="405ca-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="405ca-128">The name of the server.</span></span> <span data-ttu-id="405ca-129">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="405ca-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="405ca-130">Access</span><span class="sxs-lookup"><span data-stu-id="405ca-130">Access</span></span>         | <span data-ttu-id="405ca-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="405ca-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="405ca-132">Type</span><span class="sxs-lookup"><span data-stu-id="405ca-132">Type</span></span>           | <span data-ttu-id="405ca-133">string</span><span class="sxs-lookup"><span data-stu-id="405ca-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="405ca-134">Predefinito</span><span class="sxs-lookup"><span data-stu-id="405ca-134">Default</span></span>        | <span data-ttu-id="405ca-135">"Nuovo computer"</span><span class="sxs-lookup"><span data-stu-id="405ca-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="405ca-136">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="405ca-136">Minimum system</span></span> | <span data-ttu-id="405ca-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="405ca-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="405ca-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="405ca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405ca-139">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="405ca-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
