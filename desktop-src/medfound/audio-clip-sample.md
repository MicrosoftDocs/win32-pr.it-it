---
description: Viene illustrato come utilizzare Microsoft Media Foundation per decodificare l'audio da un file multimediale.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Esempio di clip audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305515"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="268e5-103">Esempio di clip audio</span><span class="sxs-lookup"><span data-stu-id="268e5-103">Audio Clip Sample</span></span>

<span data-ttu-id="268e5-104">Viene illustrato come utilizzare Microsoft Media Foundation per decodificare l'audio da un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="268e5-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="268e5-105">L'applicazione di esempio clip audio legge i dati audio da un file multimediale e scrive l'audio non compresso in un file WAVE.</span><span class="sxs-lookup"><span data-stu-id="268e5-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="268e5-106">API illustrate</span><span class="sxs-lookup"><span data-stu-id="268e5-106">APIs Demonstrated</span></span>

<span data-ttu-id="268e5-107">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="268e5-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="268e5-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="268e5-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="268e5-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="268e5-109">Usage</span></span>

<span data-ttu-id="268e5-110">Questo esempio è un'applicazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="268e5-110">This sample is a command-line application.</span></span> <span data-ttu-id="268e5-111">USA gli argomenti della riga di comando seguenti:</span><span class="sxs-lookup"><span data-stu-id="268e5-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="268e5-112">InputFile: nome di un file che contiene un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="268e5-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="268e5-113">outputfile. wav: nome del file WAVE da scrivere.</span><span class="sxs-lookup"><span data-stu-id="268e5-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="268e5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="268e5-114">Requirements</span></span>



| <span data-ttu-id="268e5-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="268e5-115">Product</span></span>                                                        | <span data-ttu-id="268e5-116">Versione</span><span class="sxs-lookup"><span data-stu-id="268e5-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="268e5-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="268e5-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="268e5-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="268e5-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="268e5-119">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="268e5-119">Downloading the Sample</span></span>

<span data-ttu-id="268e5-120">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="268e5-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="268e5-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="268e5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="268e5-122">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="268e5-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="268e5-123">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="268e5-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="268e5-124">Esercitazione: decodifica audio</span><span class="sxs-lookup"><span data-stu-id="268e5-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



