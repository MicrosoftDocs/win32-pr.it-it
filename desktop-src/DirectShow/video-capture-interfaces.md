---
description: Interfacce di acquisizione video
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfacce di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308961"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="4ead7-103">Interfacce di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="4ead7-103">Video Capture Interfaces</span></span>

<span data-ttu-id="4ead7-104">Queste interfacce supportano l'acquisizione video, usando i dispositivi Microsoft® Windows® Driver Model (WDM) o il video Microsoft® per i dispositivi Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="4ead7-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="4ead7-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="4ead7-105">Interface</span></span>                                                        | <span data-ttu-id="4ead7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ead7-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ead7-107">**IAMAnalogVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="4ead7-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="4ead7-108">Controllare la digitalizzazione dei video in una scheda di acquisizione video WDM.</span><span class="sxs-lookup"><span data-stu-id="4ead7-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="4ead7-109">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="4ead7-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="4ead7-110">Controllare il modo in cui un pin alloca i buffer.</span><span class="sxs-lookup"><span data-stu-id="4ead7-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="4ead7-111">**IAMCopyCaptureFileProgress**</span><span class="sxs-lookup"><span data-stu-id="4ead7-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="4ead7-112">Interfaccia di callback per ricevere lo stato di avanzamento di un'operazione di copia file.</span><span class="sxs-lookup"><span data-stu-id="4ead7-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="4ead7-113">**IAMCrossbar**</span><span class="sxs-lookup"><span data-stu-id="4ead7-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="4ead7-114">Creare una connessione hardware tra un'origine audio o video WDM e un dispositivo di acquisizione WDM.</span><span class="sxs-lookup"><span data-stu-id="4ead7-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="4ead7-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="4ead7-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="4ead7-116">Eseguire una query su un filtro di acquisizione sulle prestazioni di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4ead7-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="4ead7-117">**IAMStreamControl**</span><span class="sxs-lookup"><span data-stu-id="4ead7-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="4ead7-118">Controllare l'ora di inizio e di fine dei singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="4ead7-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="4ead7-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="4ead7-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="4ead7-120">Eseguire una query e impostare il formato di output del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4ead7-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="4ead7-121">**IAMVfwCaptureDialogs**</span><span class="sxs-lookup"><span data-stu-id="4ead7-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="4ead7-122">Consente di visualizzare le finestre di dialogo fornite dai driver di acquisizione di VFW.</span><span class="sxs-lookup"><span data-stu-id="4ead7-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="4ead7-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="4ead7-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="4ead7-124">Controllare l'immagine da un dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4ead7-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="4ead7-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="4ead7-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="4ead7-126">Regolare le qualità di un segnale video, ad esempio luminosità, contrasto, tonalità, saturazione, gamma e nitidezza.</span><span class="sxs-lookup"><span data-stu-id="4ead7-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="4ead7-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="4ead7-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="4ead7-128">Grafici filtro compilazione per acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="4ead7-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="4ead7-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="4ead7-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="4ead7-130">Specificare il nome e gli attributi di un file di output.</span><span class="sxs-lookup"><span data-stu-id="4ead7-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="4ead7-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ead7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ead7-132">Interfacce di controllo del dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="4ead7-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4ead7-133">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="4ead7-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



