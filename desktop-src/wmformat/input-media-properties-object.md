---
title: Oggetto proprietà supporti di input
description: Oggetto proprietà supporti di input
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, oggetti proprietà supporti di input
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di input
- ASF (formato avanzato dei sistemi), oggetti proprietà supporti di input
- oggetti, oggetti proprietà supporti di input
- oggetti proprietà supporti di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103857994"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="59026-108">Oggetto proprietà supporti di input</span><span class="sxs-lookup"><span data-stu-id="59026-108">Input Media Properties Object</span></span>

<span data-ttu-id="59026-109">Un oggetto proprietà del supporto di input creato dall'oggetto Writer supporta le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="59026-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="59026-110">È possibile accedere a queste interfacce mediante una chiamata a **QueryInterface** su una delle interfacce dell'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="59026-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="59026-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="59026-111">Interface</span></span>                                        | <span data-ttu-id="59026-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59026-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59026-113">**IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="59026-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="59026-114">Recupera le proprietà di un flusso di input.</span><span class="sxs-lookup"><span data-stu-id="59026-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="59026-115">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="59026-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="59026-116">Usato come interfaccia di base per le altre interfacce di proprietà del supporto (input, output e video).</span><span class="sxs-lookup"><span data-stu-id="59026-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="59026-117">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="59026-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="59026-118">Gestisce le proprietà di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="59026-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="59026-119">Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video.</span><span class="sxs-lookup"><span data-stu-id="59026-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="59026-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59026-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59026-121">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="59026-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="59026-122">**Oggetto writer**</span><span class="sxs-lookup"><span data-stu-id="59026-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




