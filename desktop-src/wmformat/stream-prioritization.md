---
title: Assegnazione di priorità al flusso
description: Assegnazione di priorità al flusso
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, assegnazione di priorità al flusso
- ASF (Advanced Systems Format), assegnazione di priorità ai flussi
- ASF (formato avanzato dei sistemi), assegnazione di priorità ai flussi
- Windows Media Format SDK, ordine di priorità per i flussi
- ASF (Advanced Systems Format), ordine di priorità per i flussi
- ASF (Advanced Systems Format), ordine di priorità per i flussi
- flussi, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046324"
---
# <a name="stream-prioritization"></a><span data-ttu-id="e1477-110">Assegnazione di priorità al flusso</span><span class="sxs-lookup"><span data-stu-id="e1477-110">Stream Prioritization</span></span>

<span data-ttu-id="e1477-111">Quando si crea un file ASF, è possibile specificare un ordine di priorità per i flussi costitutivi.</span><span class="sxs-lookup"><span data-stu-id="e1477-111">When you create an ASF file, you can specify a priority order for its constituent streams.</span></span> <span data-ttu-id="e1477-112">Se si esegue il flusso di un file con priorità e la larghezza di banda disponibile non è sufficiente per la distribuzione di tutti i flussi, il lettore eliminerà i flussi in ordine di priorità inverso.</span><span class="sxs-lookup"><span data-stu-id="e1477-112">If you stream a prioritized file and the available bandwidth is not enough to deliver all of the streams, the reader will drop streams in reverse priority order.</span></span> <span data-ttu-id="e1477-113">In questo modo è possibile garantire che i flussi più importanti nel file non verranno eliminati a causa di problemi di rete.</span><span class="sxs-lookup"><span data-stu-id="e1477-113">In this way you can guarantee that the most important streams in your file will not be dropped due to network difficulties.</span></span>

<span data-ttu-id="e1477-114">La definizione delle priorità del flusso viene configurata con un oggetto di assegnazione di priorità del flusso e aggiunta al profilo.</span><span class="sxs-lookup"><span data-stu-id="e1477-114">Stream prioritization is configured with a stream prioritization object and added to the profile.</span></span> <span data-ttu-id="e1477-115">Un profilo può contenere un solo oggetto di assegnazione di priorità del flusso.</span><span class="sxs-lookup"><span data-stu-id="e1477-115">A profile can contain only one stream prioritization object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1477-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1477-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1477-117">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="e1477-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="e1477-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="e1477-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[<span data-ttu-id="e1477-119">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="e1477-119">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[<span data-ttu-id="e1477-120">**IWMProfile3::RemoveStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="e1477-120">**IWMProfile3::RemoveStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[<span data-ttu-id="e1477-121">**IWMProfile3::SetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="e1477-121">**IWMProfile3::SetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[<span data-ttu-id="e1477-122">**Interfaccia IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="e1477-122">**IWMStreamPrioritization Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[<span data-ttu-id="e1477-123">**Uso della priorità di flusso**</span><span class="sxs-lookup"><span data-stu-id="e1477-123">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




