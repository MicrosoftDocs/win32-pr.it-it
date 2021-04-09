---
description: Viene illustrato come implementare un effetto video come una trasformazione Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Esempio MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130510"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="c45e7-103">\_Esempio di scala di grigi MFT</span><span class="sxs-lookup"><span data-stu-id="c45e7-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="c45e7-104">Viene illustrato come implementare un effetto video come una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="c45e7-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="c45e7-105">La MFT in scala di grigi converte il video YUV in scala di grigi impostando i valori croma nel video su neutro.</span><span class="sxs-lookup"><span data-stu-id="c45e7-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="c45e7-106">Il MFT accetta video non compressi nei formati UYVY, YUY2 o NV12.</span><span class="sxs-lookup"><span data-stu-id="c45e7-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="c45e7-107">API illustrate</span><span class="sxs-lookup"><span data-stu-id="c45e7-107">APIs Demonstrated</span></span>

<span data-ttu-id="c45e7-108">In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="c45e7-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="c45e7-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="c45e7-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="c45e7-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c45e7-110">Usage</span></span>

<span data-ttu-id="c45e7-111">L' \_ esempio relativo alle gradazioni di grigio per MFT compila una dll che è un server com per MFT.</span><span class="sxs-lookup"><span data-stu-id="c45e7-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="c45e7-112">Prima di usare il file MFT, è necessario registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="c45e7-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="c45e7-113">Per visualizzare la MFT in scala di grigi in uso, eseguire l' [esempio PlaybackFX](/previous-versions//bb970336(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c45e7-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="c45e7-114">È anche possibile usare lo strumento TopoEdit per compilare una topologia che include la MFT in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="c45e7-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="c45e7-115">Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="c45e7-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c45e7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c45e7-116">Requirements</span></span>



| <span data-ttu-id="c45e7-117">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c45e7-117">Product</span></span>                                                        | <span data-ttu-id="c45e7-118">Versione</span><span class="sxs-lookup"><span data-stu-id="c45e7-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c45e7-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c45e7-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c45e7-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c45e7-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c45e7-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c45e7-121">Downloading the Sample</span></span>

<span data-ttu-id="c45e7-122">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span><span class="sxs-lookup"><span data-stu-id="c45e7-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c45e7-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c45e7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c45e7-124">Video su YUV</span><span class="sxs-lookup"><span data-stu-id="c45e7-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="c45e7-125">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="c45e7-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="c45e7-126">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c45e7-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="c45e7-127">\_Esempio di AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="c45e7-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="c45e7-128">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="c45e7-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
