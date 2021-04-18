---
title: Oggetto di assegnazione di priorità del flusso
description: Oggetto di assegnazione di priorità del flusso
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK, oggetti di assegnazione di priorità di flusso
- ASF (Advanced Systems Format), oggetti di assegnazione di priorità dei flussi
- ASF (formato avanzato dei sistemi), oggetti di assegnazione di priorità dei flussi
- oggetti, oggetti di assegnazione di priorità di flusso
- oggetti di assegnazione di priorità di flusso
- flussi, oggetti di assegnazione di priorità di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299436"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="d575e-109">Oggetto di assegnazione di priorità del flusso</span><span class="sxs-lookup"><span data-stu-id="d575e-109">Stream Prioritization Object</span></span>

<span data-ttu-id="d575e-110">Un oggetto di assegnazione di priorità del flusso viene usato per specificare un ordine di importanza per i flussi in un profilo.</span><span class="sxs-lookup"><span data-stu-id="d575e-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="d575e-111">Quando la riproduzione completa non è possibile a causa di limitazioni della velocità in bit, i flussi con priorità più bassa saranno il primo a essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="d575e-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="d575e-112">È possibile creare oggetti di assegnazione di priorità del flusso per i dati di assegnazione di priorità del flusso esistenti in un profilo o crearli vuoti, pronti per la ricezione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="d575e-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="d575e-113">Gli oggetti di assegnazione di priorità dei flussi non possono esistere indipendentemente da un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="d575e-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="d575e-114">Per salvare il contenuto di un oggetto di assegnazione di priorità del flusso, è necessario chiamare [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span><span class="sxs-lookup"><span data-stu-id="d575e-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="d575e-115">Per creare un oggetto di assegnazione di priorità del flusso, usare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d575e-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="d575e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="d575e-116">Method</span></span>                                                                                          | <span data-ttu-id="d575e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d575e-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="d575e-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="d575e-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="d575e-119">Crea un oggetto di assegnazione di priorità del flusso senza dati.</span><span class="sxs-lookup"><span data-stu-id="d575e-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="d575e-120">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="d575e-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="d575e-121">Crea un oggetto di assegnazione di priorità del flusso popolato con i dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="d575e-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="d575e-122">In entrambi i metodi della tabella precedente è stato impostato un puntatore a un'interfaccia **IWMStreamPrioritization** .</span><span class="sxs-lookup"><span data-stu-id="d575e-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="d575e-123">Si tratta dell'unica interfaccia supportata dall'oggetto di assegnazione di priorità del flusso.</span><span class="sxs-lookup"><span data-stu-id="d575e-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="d575e-124">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="d575e-124">Interface</span></span>                                                  | <span data-ttu-id="d575e-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d575e-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d575e-126">**IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="d575e-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="d575e-127">Gestisce l'elenco di flussi all'interno dell'oggetto di assegnazione di priorità del flusso.</span><span class="sxs-lookup"><span data-stu-id="d575e-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d575e-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d575e-128">Remarks</span></span>

<span data-ttu-id="d575e-129">Per un determinato profilo possono esistere solo una priorità di flusso.</span><span class="sxs-lookup"><span data-stu-id="d575e-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="d575e-130">Se si crea una nuova priorità di flusso per un profilo che contiene già una priorità di flusso, quella precedente verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="d575e-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d575e-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d575e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d575e-132">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="d575e-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="d575e-133">**Oggetto profilo**</span><span class="sxs-lookup"><span data-stu-id="d575e-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="d575e-134">**Uso della priorità di flusso**</span><span class="sxs-lookup"><span data-stu-id="d575e-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




