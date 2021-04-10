---
description: Accelerazione video DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Accelerazione video DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225807"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="ed948-103">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="ed948-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="ed948-104">DirectX Video Acceleration (DXVA) è un'API e un DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione dei codec video.</span><span class="sxs-lookup"><span data-stu-id="ed948-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="ed948-105">I codec software e i processori video software possono usare DXVA per eseguire l'offload di alcune operazioni con utilizzo intensivo della CPU nella GPU.</span><span class="sxs-lookup"><span data-stu-id="ed948-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="ed948-106">Un decodificatore software, ad esempio, può eseguire l'offload della trasformazione iDCT (discrete coseno) inversa nella GPU.</span><span class="sxs-lookup"><span data-stu-id="ed948-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="ed948-107">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="ed948-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed948-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ed948-108">In this section</span></span>



| <span data-ttu-id="ed948-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="ed948-109">Topic</span></span>                                                                                             | <span data-ttu-id="ed948-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed948-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed948-111">Informazioni su DXVA 2,0</span><span class="sxs-lookup"><span data-stu-id="ed948-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="ed948-112">Panoramica di DXVA 2 e relativa relazione con DXVA 1.</span><span class="sxs-lookup"><span data-stu-id="ed948-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="ed948-113">Gestione dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="ed948-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="ed948-114">Gestione dispositivi Microsoft Direct3D consente a due o più oggetti di condividere lo stesso dispositivo Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ed948-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="ed948-115">Supporto di DXVA 2,0 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ed948-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="ed948-116">Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ed948-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="ed948-117">Supporto di DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed948-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="ed948-118">Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in una trasformazione Media Foundation (MFT) con Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="ed948-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="ed948-119">Elaborazione video DXVA</span><span class="sxs-lookup"><span data-stu-id="ed948-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="ed948-120">L'elaborazione video di DXVA incapsula le funzioni dell'hardware grafico dedicato all'elaborazione di immagini video non compresse.</span><span class="sxs-lookup"><span data-stu-id="ed948-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="ed948-121">I servizi di elaborazione video includono la deinterlacciamento e la combinazione di video.</span><span class="sxs-lookup"><span data-stu-id="ed948-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="ed948-122">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ed948-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="ed948-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) è un'API per l'elaborazione video con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="ed948-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="ed948-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed948-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed948-125">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed948-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ed948-126">Specifica DXVA 1</span><span class="sxs-lookup"><span data-stu-id="ed948-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
