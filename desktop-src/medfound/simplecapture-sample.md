---
description: Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando l'API MFPlay.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Esempio SimpleCapture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226500"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="ff732-103">Esempio SimpleCapture</span><span class="sxs-lookup"><span data-stu-id="ff732-103">SimpleCapture Sample</span></span>

<span data-ttu-id="ff732-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ff732-104">\[Deprecated.</span></span> <span data-ttu-id="ff732-105">L'API MFPlay può essere rimossa dalle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ff732-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="ff732-106">Le applicazioni devono usare il [lettore di origine](source-reader.md) per l'acquisizione video.\]</span><span class="sxs-lookup"><span data-stu-id="ff732-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="ff732-107">Mostra come visualizzare in anteprima i video da un dispositivo di acquisizione video, usando l'API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="ff732-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="ff732-108">API illustrate</span><span class="sxs-lookup"><span data-stu-id="ff732-108">APIs Demonstrated</span></span>

<span data-ttu-id="ff732-109">In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff732-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="ff732-110">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ff732-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="ff732-111">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="ff732-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="ff732-112">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="ff732-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="ff732-113">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="ff732-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="ff732-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff732-114">Requirements</span></span>



| <span data-ttu-id="ff732-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ff732-115">Product</span></span>                                                        | <span data-ttu-id="ff732-116">Versione</span><span class="sxs-lookup"><span data-stu-id="ff732-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="ff732-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ff732-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="ff732-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff732-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ff732-119">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ff732-119">Downloading the Sample</span></span>

<span data-ttu-id="ff732-120">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span><span class="sxs-lookup"><span data-stu-id="ff732-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff732-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff732-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff732-122">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="ff732-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="ff732-123">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="ff732-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



