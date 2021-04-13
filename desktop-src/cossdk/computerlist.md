---
description: Contiene un elenco dei computer nella cartella computer dello strumento di amministrazione Servizi componenti. Contiene un oggetto per ogni computer.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Raccolta di computer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483221"
---
# <a name="computerlist-collection"></a><span data-ttu-id="e69fb-104">Raccolta di computer</span><span class="sxs-lookup"><span data-stu-id="e69fb-104">ComputerList collection</span></span>

<span data-ttu-id="e69fb-105">Contiene un elenco dei computer nella cartella **computer** dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="e69fb-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="e69fb-106">Contiene un oggetto per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="e69fb-106">It contains an object for each computer.</span></span>

<span data-ttu-id="e69fb-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="e69fb-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="e69fb-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e69fb-108">Members</span></span>

<span data-ttu-id="e69fb-109">La raccolta **nomecomputer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e69fb-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="e69fb-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="e69fb-110">Related Collections</span></span>

<span data-ttu-id="e69fb-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="e69fb-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="e69fb-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e69fb-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="e69fb-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="e69fb-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="e69fb-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e69fb-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="e69fb-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="e69fb-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="e69fb-116">**Radice**</span><span class="sxs-lookup"><span data-stu-id="e69fb-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="e69fb-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e69fb-117">Properties</span></span>

<span data-ttu-id="e69fb-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="e69fb-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="e69fb-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e69fb-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="e69fb-120">Nome</span><span class="sxs-lookup"><span data-stu-id="e69fb-120">Name</span></span>



| <span data-ttu-id="e69fb-121">Voce</span><span class="sxs-lookup"><span data-stu-id="e69fb-121">Entry</span></span> | <span data-ttu-id="e69fb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e69fb-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69fb-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e69fb-123">Description</span></span>    | <span data-ttu-id="e69fb-124">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="e69fb-124">The name of the computer.</span></span> <span data-ttu-id="e69fb-125">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="e69fb-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="e69fb-126">Access</span><span class="sxs-lookup"><span data-stu-id="e69fb-126">Access</span></span>         | <span data-ttu-id="e69fb-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="e69fb-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e69fb-128">Type</span><span class="sxs-lookup"><span data-stu-id="e69fb-128">Type</span></span>           | <span data-ttu-id="e69fb-129">string</span><span class="sxs-lookup"><span data-stu-id="e69fb-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e69fb-130">Predefinito</span><span class="sxs-lookup"><span data-stu-id="e69fb-130">Default</span></span>        | <span data-ttu-id="e69fb-131">"Nuovo computer"</span><span class="sxs-lookup"><span data-stu-id="e69fb-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e69fb-132">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="e69fb-132">Minimum system</span></span> | <span data-ttu-id="e69fb-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e69fb-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="e69fb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e69fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69fb-135">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e69fb-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
