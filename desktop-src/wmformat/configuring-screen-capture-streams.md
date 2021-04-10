---
title: Configurazione di flussi di acquisizione schermo
description: Configurazione di flussi di acquisizione schermo
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- flussi, configurazione di flussi di acquisizione schermo
- codec, configurazione di flussi di acquisizione schermo
- flussi di acquisizione schermo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956166"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="b97e7-106">Configurazione di flussi di acquisizione schermo</span><span class="sxs-lookup"><span data-stu-id="b97e7-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="b97e7-107">I flussi che usano il codec Windows Media® video 9 screen sono configurati dalle applicazioni nello stesso modo dei normali flussi video.</span><span class="sxs-lookup"><span data-stu-id="b97e7-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="b97e7-108">Tuttavia, se si imposta il livello di complessità video su 0, il writer ignorerà qualsiasi valore di qualità video impostato con [**IWMVideoMediaProps:: sequality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span><span class="sxs-lookup"><span data-stu-id="b97e7-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="b97e7-109">Per altre informazioni, vedere [ottenere risultati soddisfacenti con il codec della schermata Windows Media video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="b97e7-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b97e7-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b97e7-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97e7-111">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="b97e7-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="b97e7-112">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="b97e7-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="b97e7-113">**Configurazione dei flussi video**</span><span class="sxs-lookup"><span data-stu-id="b97e7-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




