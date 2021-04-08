---
description: Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Esempio di DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878446"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="c2d7b-103">Esempio di DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="c2d7b-103">DXVA-HD Sample</span></span>

<span data-ttu-id="c2d7b-104">Mostra come usare Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="c2d7b-105">Questo esempio è essenzialmente una porta dell' [esempio DXVA2 \_ VideoProc](dxva2-videoproc-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="c2d7b-106">Ha le stesse funzioni di base e la maggior parte dei comandi della tastiera sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="c2d7b-107">L'esempio genera un video a livello di codice con un flusso primario e un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="c2d7b-108">Il flusso primario Visualizza le barre dei colori SMPTE.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="c2d7b-109">Il sottoflusso è in alfa Blend nel flusso primario usando la chiave Luma.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="c2d7b-110">L'utente può modificare i parametri di elaborazione video, inclusi i valori alfa planari, i rettangoli di origine e di destinazione, le regolazioni dei colori e lo spazio colore.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="c2d7b-111">Nell'immagine seguente viene illustrato il video generato.</span><span class="sxs-lookup"><span data-stu-id="c2d7b-111">The following image shows that video that is generated.</span></span>

![screenshot dell'esempio DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="c2d7b-113">API illustrate</span><span class="sxs-lookup"><span data-stu-id="c2d7b-113">APIs Demonstrated</span></span>

<span data-ttu-id="c2d7b-114">Questo esempio illustra le interfacce DXVA-HD seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2d7b-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="c2d7b-115">**\_Dispositivo IDXVAHD**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="c2d7b-116">**\_VIDEOPROCESSOR IDXVAHD**</span><span class="sxs-lookup"><span data-stu-id="c2d7b-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="c2d7b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2d7b-117">Requirements</span></span>



| <span data-ttu-id="c2d7b-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c2d7b-118">Product</span></span>                                                        | <span data-ttu-id="c2d7b-119">Versione</span><span class="sxs-lookup"><span data-stu-id="c2d7b-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c2d7b-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c2d7b-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c2d7b-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2d7b-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c2d7b-122">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c2d7b-122">Downloading the Sample</span></span>

<span data-ttu-id="c2d7b-123">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span><span class="sxs-lookup"><span data-stu-id="c2d7b-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2d7b-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2d7b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d7b-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="c2d7b-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="c2d7b-126">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="c2d7b-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



