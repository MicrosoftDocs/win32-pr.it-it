---
title: Oggetto di condivisione della larghezza di banda
description: Oggetto di condivisione della larghezza di banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK, oggetti di condivisione della larghezza di banda
- ASF (Advanced Systems Format), oggetti di condivisione della larghezza di banda
- ASF (Advanced Systems Format), oggetti di condivisione della larghezza di banda
- oggetti, oggetti di condivisione della larghezza di banda
- condivisione della larghezza di banda, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398600"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="f8b7a-108">Oggetto di condivisione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="f8b7a-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="f8b7a-109">Un oggetto di condivisione della larghezza di banda viene usato per indicare che due o più flussi, indipendentemente dalle singole frequenze di bit, non utilizzeranno mai più di una quantità di larghezza di banda specificata tra di essi.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="f8b7a-110">Si tratta di un oggetto puramente informativo. le velocità in bit impostate al suo interno non vengono applicate a livello di codice da qualsiasi oggetto di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="f8b7a-111">Le informazioni sulla condivisione della larghezza di banda sono una parte facoltativa di un profilo.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="f8b7a-112">Gli oggetti di condivisione della larghezza di banda possono essere creati per le informazioni di condivisione della larghezza di banda esistenti in un profilo oppure possono essere creati vuoti, pronti per ricevere nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="f8b7a-113">Gli oggetti di condivisione della larghezza di banda non possono esistere indipendentemente da un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="f8b7a-114">Per salvare il contenuto di un oggetto di condivisione della larghezza di banda, è necessario chiamare [**IWMProfile3:: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span><span class="sxs-lookup"><span data-stu-id="f8b7a-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="f8b7a-115">Per creare un oggetto di condivisione della larghezza di banda, chiamare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="f8b7a-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f8b7a-116">Method</span></span>                                                                                  | <span data-ttu-id="f8b7a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8b7a-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8b7a-118">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="f8b7a-119">Crea un oggetto di condivisione della larghezza di banda senza dati.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="f8b7a-120">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="f8b7a-121">Crea un oggetto di condivisione della larghezza di banda popolato con i dati di un profilo.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="f8b7a-122">Usa l'indice di condivisione della larghezza di banda per identificare le informazioni di condivisione della larghezza di banda desiderata.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="f8b7a-123">In entrambi i metodi della tabella precedente è stato impostato un puntatore a un'interfaccia **IWMBandwidthSharing** .</span><span class="sxs-lookup"><span data-stu-id="f8b7a-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="f8b7a-124">L'interfaccia **IWMStreamList** viene ereditata da **IWMBandwidthSharing**, pertanto non è necessario chiamare **QueryInterface** con questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="f8b7a-125">Le interfacce seguenti sono supportate da ogni oggetto di condivisione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="f8b7a-126">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f8b7a-126">Interface</span></span>                                          | <span data-ttu-id="f8b7a-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8b7a-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="f8b7a-128">**IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="f8b7a-129">Gestisce le proprietà di un gruppo di flussi che condividono la larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="f8b7a-130">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="f8b7a-131">Gestisce l'elenco di flussi che condividono la larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="f8b7a-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="f8b7a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8b7a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8b7a-133">**Condivisione della larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="f8b7a-134">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="f8b7a-135">**Oggetto profilo**</span><span class="sxs-lookup"><span data-stu-id="f8b7a-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




