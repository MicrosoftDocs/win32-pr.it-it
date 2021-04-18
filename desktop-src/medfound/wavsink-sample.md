---
description: Esempio WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Esempio WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310159"
---
# <a name="wavsink-sample"></a><span data-ttu-id="7fba6-103">Esempio WavSink</span><span class="sxs-lookup"><span data-stu-id="7fba6-103">WavSink Sample</span></span>

<span data-ttu-id="7fba6-104">Viene illustrato come implementare un sink multimediale personalizzato in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7fba6-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="7fba6-105">L'esempio implementa un sink di archiviazione che scrive audio PCM non compresso in un file WAV.</span><span class="sxs-lookup"><span data-stu-id="7fba6-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="7fba6-106">API illustrate</span><span class="sxs-lookup"><span data-stu-id="7fba6-106">APIs Demonstrated</span></span>

<span data-ttu-id="7fba6-107">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="7fba6-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="7fba6-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="7fba6-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="7fba6-109">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="7fba6-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="7fba6-110">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="7fba6-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="7fba6-111">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="7fba6-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="7fba6-112">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="7fba6-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="7fba6-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7fba6-113">Usage</span></span>

<span data-ttu-id="7fba6-114">L'esempio WavSink contiene due progetti di Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="7fba6-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="7fba6-115">WavSink. vcproj compila una libreria statica che contiene l'implementazione del sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="7fba6-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="7fba6-116">WriteWavFile. vcproj compila un'applicazione console che usa il sink multimediale per produrre un file WAV.</span><span class="sxs-lookup"><span data-stu-id="7fba6-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="7fba6-117">Questa applicazione consente di collegarsi alla libreria creata dal progetto WavSink.</span><span class="sxs-lookup"><span data-stu-id="7fba6-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fba6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fba6-118">Requirements</span></span>



| <span data-ttu-id="7fba6-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7fba6-119">Product</span></span>                                                        | <span data-ttu-id="7fba6-120">Versione</span><span class="sxs-lookup"><span data-stu-id="7fba6-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7fba6-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7fba6-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7fba6-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7fba6-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7fba6-123">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="7fba6-123">Downloading the Sample</span></span>

<span data-ttu-id="7fba6-124">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span><span class="sxs-lookup"><span data-stu-id="7fba6-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fba6-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fba6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fba6-126">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="7fba6-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="7fba6-127">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="7fba6-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



