---
description: PIN della porta video nell'acquisizione di file
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: PIN della porta video nell'acquisizione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308955"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="dfee0-103">PIN della porta video nell'acquisizione di file</span><span class="sxs-lookup"><span data-stu-id="dfee0-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="dfee0-104">Se il dispositivo di acquisizione ha una porta video, il PIN della porta video deve essere connesso a un renderer video, anche se si vuole solo acquisire in un file.</span><span class="sxs-lookup"><span data-stu-id="dfee0-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="dfee0-105">Se si chiama [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con il valore **di \_ \_ acquisizione categoria pin** e il dispositivo ha un PIN della porta video, il generatore del grafico di acquisizione connette automaticamente il PIN della porta video al filtro [Overlay Mixer](overlay-mixer-filter.md) e connette il mixer sovrapposto al renderer video.</span><span class="sxs-lookup"><span data-stu-id="dfee0-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="dfee0-106">Il generatore di grafici di acquisizione nasconde la finestra video chiamando [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore **OAFALSE**.</span><span class="sxs-lookup"><span data-stu-id="dfee0-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="dfee0-107">Se l'applicazione chiama in seguito **RenderStream** con la **\_ categoria pin \_ Preview**, il generatore del grafico di acquisizione chiama **put \_ AutoShow** con il valore **OATRUE** per visualizzare la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="dfee0-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="dfee0-108">Dopo aver chiamato **RenderStream** con **l' \_ \_ acquisizione della categoria pin**, è possibile verificare se è stato aggiunto il renderer video eseguendo una query su Filter Graph Manager per l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="dfee0-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfee0-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dfee0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfee0-110">Acquisizione di video in un file</span><span class="sxs-lookup"><span data-stu-id="dfee0-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



