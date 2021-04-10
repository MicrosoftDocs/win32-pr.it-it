---
description: Viene illustrato come scrivere un decodificatore per Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Esempio di decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966401"
---
# <a name="decoder-sample"></a><span data-ttu-id="44c07-103">Esempio di decodificatore</span><span class="sxs-lookup"><span data-stu-id="44c07-103">Decoder Sample</span></span>

<span data-ttu-id="44c07-104">Viene illustrato come scrivere un decodificatore per Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="44c07-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="44c07-105">Questo esempio implementa un decodificatore video MPEG-1 fittizio che Visualizza il codice temporale per ogni fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="44c07-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="44c07-106">Non decodifica effettivamente il Bitstream MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="44c07-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="44c07-107">La figura seguente mostra l'output video del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="44c07-107">The following image shows the video output from the decoder.</span></span>

![Screenshot di un frame video dal decodificatore](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="44c07-109">Prima del Windows SDK per Windows 7, questo esempio era incluso nell' [esempio MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="44c07-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="44c07-110">API illustrate</span><span class="sxs-lookup"><span data-stu-id="44c07-110">APIs Demonstrated</span></span>

<span data-ttu-id="44c07-111">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="44c07-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="44c07-112">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="44c07-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="44c07-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44c07-113">Requirements</span></span>



| <span data-ttu-id="44c07-114">Prodotto</span><span class="sxs-lookup"><span data-stu-id="44c07-114">Product</span></span>                                                        | <span data-ttu-id="44c07-115">Versione</span><span class="sxs-lookup"><span data-stu-id="44c07-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="44c07-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="44c07-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="44c07-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="44c07-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="44c07-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="44c07-118">Downloading the Sample</span></span>

<span data-ttu-id="44c07-119">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span><span class="sxs-lookup"><span data-stu-id="44c07-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44c07-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44c07-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c07-121">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="44c07-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="44c07-122">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44c07-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="44c07-123">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="44c07-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



