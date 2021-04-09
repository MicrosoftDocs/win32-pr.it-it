---
title: Scrittura di flussi di immagini
description: Scrittura di flussi di immagini
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Formato di sistemi avanzati (ASF), scrittura di flussi di immagini
- ASF (Advanced Systems Format), scrittura di flussi di immagini
- Formati di sistemi avanzati (ASF), flussi di immagini
- ASF (formato avanzato dei sistemi), flussi di immagini
- flussi di immagini, scrittura
- flussi, scrittura di flussi di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956192"
---
# <a name="writing-image-streams"></a><span data-ttu-id="3bebd-109">Scrittura di flussi di immagini</span><span class="sxs-lookup"><span data-stu-id="3bebd-109">Writing Image Streams</span></span>

<span data-ttu-id="3bebd-110">Gli input per un flusso di immagini devono essere immagini bitmap in formato RGB.</span><span class="sxs-lookup"><span data-stu-id="3bebd-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="3bebd-111">Il writer coordina la compressione degli esempi di immagini di input usando il formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="3bebd-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="3bebd-112">Prima di iniziare a scrivere un file contenente un flusso di immagini, è necessario impostare la qualità dell'immagine per l'input usando l' \_ impostazione g wszJPEGCompressionQuality.</span><span class="sxs-lookup"><span data-stu-id="3bebd-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="3bebd-113">Usare [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per impostare la qualità su un valore **DWORD** compreso tra 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="3bebd-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="3bebd-114">I valori bassi rappresentano un rapporto di compressione elevato a scapito della qualità, mentre i valori elevati producono immagini di alta qualità che richiedono più spazio.</span><span class="sxs-lookup"><span data-stu-id="3bebd-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="3bebd-115">I flussi di immagini spesso richiedono finestre di buffer più grandi rispetto ai flussi video comuni.</span><span class="sxs-lookup"><span data-stu-id="3bebd-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="3bebd-116">La dimensione esatta richiesta dipende dal tipo di immagine e dalla qualità dell'immagine, tra gli altri fattori.</span><span class="sxs-lookup"><span data-stu-id="3bebd-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="3bebd-117">Utilizzare la versione di valutazione e l'errore per determinare le dimensioni appropriate per le immagini che si desidera elaborare.</span><span class="sxs-lookup"><span data-stu-id="3bebd-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bebd-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bebd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bebd-119">**Flussi di immagini**</span><span class="sxs-lookup"><span data-stu-id="3bebd-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="3bebd-120">**Per impostare le impostazioni di input**</span><span class="sxs-lookup"><span data-stu-id="3bebd-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="3bebd-121">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="3bebd-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




