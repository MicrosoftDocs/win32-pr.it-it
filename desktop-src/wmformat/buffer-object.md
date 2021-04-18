---
title: Oggetto buffer
description: Oggetto buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, oggetti buffer
- ASF (Advanced Systems Format), oggetti buffer
- ASF (formato avanzato dei sistemi), oggetti buffer
- oggetti, oggetti buffer
- oggetti buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299505"
---
# <a name="buffer-object"></a><span data-ttu-id="71b7a-108">Oggetto buffer</span><span class="sxs-lookup"><span data-stu-id="71b7a-108">Buffer Object</span></span>

<span data-ttu-id="71b7a-109">Un oggetto buffer viene usato per conservare gli esempi e distribuirli tra gli oggetti di Windows Media Format SDK e l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71b7a-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="71b7a-110">Quando si scrive un file, si passano gli esempi di input al writer usando oggetti buffer.</span><span class="sxs-lookup"><span data-stu-id="71b7a-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="71b7a-111">Quando si legge un file, l'oggetto Reader o l'oggetto Reader sincrono fornisce esempi all'applicazione negli oggetti buffer.</span><span class="sxs-lookup"><span data-stu-id="71b7a-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="71b7a-112">Per la scrittura di esempi in un file, è possibile creare un oggetto buffer usando il metodo [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) .</span><span class="sxs-lookup"><span data-stu-id="71b7a-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="71b7a-113">Per la lettura di esempi, l'oggetto Reader e l'oggetto Reader sincrono creano entrambi oggetti buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="71b7a-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="71b7a-114">Se si sceglie di, è possibile allocare oggetti buffer personalizzati per la lettura dei file tramite [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) o [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="71b7a-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="71b7a-115">Le interfacce seguenti sono supportate da ogni oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="71b7a-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="71b7a-116">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="71b7a-116">Interface</span></span>                          | <span data-ttu-id="71b7a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71b7a-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="71b7a-118">**INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="71b7a-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="71b7a-119">Controlla e fornisce l'accesso al buffer.</span><span class="sxs-lookup"><span data-stu-id="71b7a-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="71b7a-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="71b7a-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="71b7a-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="71b7a-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="71b7a-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="71b7a-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="71b7a-123">Supporta le proprietà del buffer, utilizzate per le estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="71b7a-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="71b7a-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="71b7a-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="71b7a-125">Enumera le proprietà del buffer.</span><span class="sxs-lookup"><span data-stu-id="71b7a-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="71b7a-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71b7a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b7a-127">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="71b7a-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




