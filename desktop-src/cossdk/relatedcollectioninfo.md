---
description: Recupera informazioni su altre raccolte correlate alla raccolta dalla quale viene chiamato.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Raccolta RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225635"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="b8e9a-103">Raccolta RelatedCollectionInfo</span><span class="sxs-lookup"><span data-stu-id="b8e9a-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="b8e9a-104">Recupera informazioni su altre raccolte correlate alla raccolta dalla quale viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="b8e9a-105">La raccolta **RelatedCollectionInfo** è accessibile da qualsiasi oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) tramite il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="b8e9a-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="b8e9a-106">La raccolta **RelatedCollectionInfo** contiene un oggetto per ogni raccolta accessibile dalla raccolta originale.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="b8e9a-107">Le raccolte correlate seguono la gerarchia della raccolta di strumenti di amministrazione di Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="b8e9a-108">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b8e9a-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b8e9a-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b8e9a-109">Members</span></span>

<span data-ttu-id="b8e9a-110">La raccolta **RelatedCollectionInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b8e9a-111">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="b8e9a-111">Related Collections</span></span>

<span data-ttu-id="b8e9a-112">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8e9a-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b8e9a-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b8e9a-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="b8e9a-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b8e9a-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="b8e9a-115">È possibile passare a questa raccolta da ogni raccolta.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="b8e9a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8e9a-116">Properties</span></span>

<span data-ttu-id="b8e9a-117">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="b8e9a-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b8e9a-118">Nome</span><span class="sxs-lookup"><span data-stu-id="b8e9a-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="b8e9a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="b8e9a-119">Name</span></span>



| <span data-ttu-id="b8e9a-120">Voce</span><span class="sxs-lookup"><span data-stu-id="b8e9a-120">Entry</span></span> | <span data-ttu-id="b8e9a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e9a-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e9a-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8e9a-122">Description</span></span>    | <span data-ttu-id="b8e9a-123">Nome della raccolta correlata.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-123">The name of the related collection.</span></span> <span data-ttu-id="b8e9a-124">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="b8e9a-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b8e9a-125">Access</span><span class="sxs-lookup"><span data-stu-id="b8e9a-125">Access</span></span>         | <span data-ttu-id="b8e9a-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b8e9a-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="b8e9a-127">Type</span><span class="sxs-lookup"><span data-stu-id="b8e9a-127">Type</span></span>           | <span data-ttu-id="b8e9a-128">string</span><span class="sxs-lookup"><span data-stu-id="b8e9a-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="b8e9a-129">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8e9a-129">Default</span></span>        | <span data-ttu-id="b8e9a-130">nessuno</span><span class="sxs-lookup"><span data-stu-id="b8e9a-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="b8e9a-131">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b8e9a-131">Minimum system</span></span> | <span data-ttu-id="b8e9a-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b8e9a-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="b8e9a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e9a-134">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="b8e9a-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
