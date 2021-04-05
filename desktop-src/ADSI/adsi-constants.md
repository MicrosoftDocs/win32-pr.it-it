---
title: Costanti ADSI
description: Nella tabella seguente sono elencate le costanti definite e utilizzate in ADSI (Active Directory Service Interfaces).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707486"
---
# <a name="adsi-constants"></a><span data-ttu-id="bb784-109">Costanti ADSI</span><span class="sxs-lookup"><span data-stu-id="bb784-109">ADSI Constants</span></span>

<span data-ttu-id="bb784-110">Nella tabella seguente sono elencate le costanti definite e utilizzate in ADSI (Active Directory Service Interfaces).</span><span class="sxs-lookup"><span data-stu-id="bb784-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="bb784-111">ADSI (costante)</span><span class="sxs-lookup"><span data-stu-id="bb784-111">ADSI constant</span></span>                      | <span data-ttu-id="bb784-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bb784-112">Value</span></span>                                   | <span data-ttu-id="bb784-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb784-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb784-114">**ANNUNCI \_ ext \_ INITCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="bb784-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="bb784-115">1</span><span class="sxs-lookup"><span data-stu-id="bb784-115">1</span></span>                                       | <span data-ttu-id="bb784-116">Codice di controllo che indica che i dati personalizzati forniti al metodo [**IADsExtension:: Oper**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contengono le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="bb784-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="bb784-117">**\_inizializzazione EXT di ADS \_ \_ completata**</span><span class="sxs-lookup"><span data-stu-id="bb784-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="bb784-118">2</span><span class="sxs-lookup"><span data-stu-id="bb784-118">2</span></span>                                       | <span data-ttu-id="bb784-119">Codice di controllo utilizzato con [**IADsExtension:: opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) per indicare che le estensioni possono eseguire tutte le inizializzazioni necessarie, a seconda delle funzionalità supportate dall'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="bb784-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="bb784-120">**ANNUNCI \_ ext \_ MAXEXTDISPID**</span><span class="sxs-lookup"><span data-stu-id="bb784-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="bb784-121">16777215</span><span class="sxs-lookup"><span data-stu-id="bb784-121">16777215</span></span>                                | <span data-ttu-id="bb784-122">Il DISPID più alto che può essere utilizzato da un oggetto di estensione per i relativi metodi e proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb784-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="bb784-123">**ANNUNCI \_ ext \_ MINEXTDISPID**</span><span class="sxs-lookup"><span data-stu-id="bb784-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="bb784-124">1</span><span class="sxs-lookup"><span data-stu-id="bb784-124">1</span></span>                                       | <span data-ttu-id="bb784-125">DISPID più basso che può essere utilizzato da un oggetto di estensione per i relativi metodi e proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb784-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="bb784-126">**\_risposta VLV \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="bb784-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="bb784-127">L "fc8cb04d-311d-406c-8CB9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="bb784-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="bb784-128">Usato con il metodo [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) per recuperare i metadati di ricerca VLV.</span><span class="sxs-lookup"><span data-stu-id="bb784-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="bb784-129">Per altre informazioni, vedere [come eseguire la ricerca con VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="bb784-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="bb784-130">**\_ADSISEARCH DBPROPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="bb784-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="bb784-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="bb784-131">0x0000C000</span></span>                              | <span data-ttu-id="bb784-132">Utilizzato per utilizzare il provider di OLE DB.</span><span class="sxs-lookup"><span data-stu-id="bb784-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




