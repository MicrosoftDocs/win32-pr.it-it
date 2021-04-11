---
description: Recupera le informazioni sulle proprietà supportate da una raccolta specificata.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Raccolta PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127019"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="b701c-103">Raccolta PropertyInfo</span><span class="sxs-lookup"><span data-stu-id="b701c-103">PropertyInfo collection</span></span>

<span data-ttu-id="b701c-104">Recupera le informazioni sulle proprietà supportate da una raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="b701c-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="b701c-105">La raccolta **PropertyInfo** è accessibile da qualsiasi oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="b701c-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="b701c-106">La raccolta **PropertyInfo** contiene un oggetto per ogni proprietà supportata dalla raccolta originale.</span><span class="sxs-lookup"><span data-stu-id="b701c-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="b701c-107">Membri</span><span class="sxs-lookup"><span data-stu-id="b701c-107">Members</span></span>

<span data-ttu-id="b701c-108">La raccolta **PropertyInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b701c-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b701c-109">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="b701c-109">Related Collections</span></span>

<span data-ttu-id="b701c-110">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="b701c-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="b701c-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b701c-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="b701c-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b701c-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b701c-113">È possibile passare a questa raccolta da ogni raccolta.</span><span class="sxs-lookup"><span data-stu-id="b701c-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="b701c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b701c-114">Properties</span></span>

<span data-ttu-id="b701c-115">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="b701c-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b701c-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b701c-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="b701c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="b701c-117">Name</span></span>



| <span data-ttu-id="b701c-118">Voce</span><span class="sxs-lookup"><span data-stu-id="b701c-118">Entry</span></span> | <span data-ttu-id="b701c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b701c-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b701c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b701c-120">Description</span></span>    | <span data-ttu-id="b701c-121">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b701c-121">The name of the property.</span></span> <span data-ttu-id="b701c-122">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="b701c-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b701c-123">Access</span><span class="sxs-lookup"><span data-stu-id="b701c-123">Access</span></span>         | <span data-ttu-id="b701c-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b701c-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="b701c-125">Type</span><span class="sxs-lookup"><span data-stu-id="b701c-125">Type</span></span>           | <span data-ttu-id="b701c-126">string</span><span class="sxs-lookup"><span data-stu-id="b701c-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="b701c-127">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b701c-127">Default</span></span>        | <span data-ttu-id="b701c-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="b701c-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b701c-129">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="b701c-129">Minimum system</span></span> | <span data-ttu-id="b701c-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b701c-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="b701c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b701c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b701c-132">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="b701c-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
