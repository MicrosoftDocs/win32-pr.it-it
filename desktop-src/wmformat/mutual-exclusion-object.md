---
title: Oggetto di esclusione reciproca
description: Oggetto di esclusione reciproca
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media Format SDK, oggetti di esclusione reciproca
- ASF (Advanced Systems Format), oggetti di esclusione reciproca
- ASF (Advanced Systems Format), oggetti di esclusione reciproca
- oggetti, oggetti di esclusione reciproca
- esclusione reciproca, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117442"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="81179-108">Oggetto di esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="81179-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="81179-109">Un oggetto di esclusione reciproca viene usato per specificare un numero di flussi, di cui è possibile recapitare solo uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="81179-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="81179-110">Questo può essere usato in diversi modi, ad esempio fornendo un flusso audio in diversi linguaggi come colonna sonora per un flusso video.</span><span class="sxs-lookup"><span data-stu-id="81179-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="81179-111">L'esclusione reciproca è una parte facoltativa di un profilo.</span><span class="sxs-lookup"><span data-stu-id="81179-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="81179-112">È possibile creare oggetti di esclusione reciproca per le informazioni di esclusione reciproca esistenti in un profilo o crearli vuoti, pronti per la ricezione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="81179-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="81179-113">Gli oggetti di esclusione reciproca non possono esistere indipendentemente da un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="81179-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="81179-114">Per salvare il contenuto di un oggetto di esclusione reciproca, è necessario chiamare [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="81179-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="81179-115">Per creare un oggetto di esclusione reciproca, usare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="81179-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="81179-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="81179-116">Method</span></span>                                                                              | <span data-ttu-id="81179-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81179-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81179-118">**IWMProfile::CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="81179-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="81179-119">Crea un oggetto di esclusione reciproca senza dati.</span><span class="sxs-lookup"><span data-stu-id="81179-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="81179-120">**IWMProfile::GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="81179-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="81179-121">Crea un oggetto di esclusione reciproca popolato con i dati di un profilo.</span><span class="sxs-lookup"><span data-stu-id="81179-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="81179-122">Usa l'indice di esclusione reciproca per identificare le informazioni desiderate di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="81179-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="81179-123">In entrambi i metodi della tabella precedente è stato impostato un puntatore a un'interfaccia **IWMMutualExclusion** .</span><span class="sxs-lookup"><span data-stu-id="81179-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="81179-124">L'interfaccia **IWMStreamList** viene ereditata da **IWMMutualExclusion** e non è mai necessario accedervi direttamente.</span><span class="sxs-lookup"><span data-stu-id="81179-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="81179-125">L'altra interfaccia dell'oggetto di esclusione reciproca può essere ottenuta chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="81179-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="81179-126">Le interfacce seguenti sono supportate da ogni oggetto di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="81179-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="81179-127">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="81179-127">Interface</span></span>                                          | <span data-ttu-id="81179-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81179-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81179-129">**IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="81179-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="81179-130">Imposta e recupera il tipo di esclusione reciproca da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="81179-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="81179-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="81179-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="81179-132">Organizza i flussi nei record, che possono essere usati per creare scenari di esclusione reciproca complessi.</span><span class="sxs-lookup"><span data-stu-id="81179-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="81179-133">Eredita tutti i metodi di **IWMMutualExclusion**.</span><span class="sxs-lookup"><span data-stu-id="81179-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="81179-134">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="81179-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="81179-135">Gestisce l'elenco di flussi che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="81179-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="81179-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81179-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81179-137">**Esclusione reciproca**</span><span class="sxs-lookup"><span data-stu-id="81179-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="81179-138">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="81179-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="81179-139">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="81179-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




