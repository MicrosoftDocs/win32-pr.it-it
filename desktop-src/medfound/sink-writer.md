---
description: Il writer di sink è un componente per la codifica di file audio o video.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Writer sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344386"
---
# <a name="sink-writer"></a><span data-ttu-id="42424-103">Writer sink</span><span class="sxs-lookup"><span data-stu-id="42424-103">Sink Writer</span></span>

<span data-ttu-id="42424-104">Il writer di sink è un componente per la codifica di file audio o video.</span><span class="sxs-lookup"><span data-stu-id="42424-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="42424-105">Il diagramma seguente illustra, a livello generale, il modo in cui un'applicazione usa il writer di sink per codificare e file audio/video.</span><span class="sxs-lookup"><span data-stu-id="42424-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![diagramma che mostra il writer del sink.](images/encoding09.png)

<span data-ttu-id="42424-107">Il writer di sink ospita un sink multimediale e, facoltativamente, uno o più codificatori.</span><span class="sxs-lookup"><span data-stu-id="42424-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="42424-108">I codificatori convertono i dati audio o video non compressi nei Bitstream codificati.</span><span class="sxs-lookup"><span data-stu-id="42424-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="42424-109">Il sink multimediale restituisce i Bitstream a un file.</span><span class="sxs-lookup"><span data-stu-id="42424-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="42424-110">Il writer di sink esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="42424-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="42424-111">Carica il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="42424-111">Loads the media sink.</span></span>
-   <span data-ttu-id="42424-112">Trova e carica i codificatori.</span><span class="sxs-lookup"><span data-stu-id="42424-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="42424-113">Gestisce il flusso di dati ai codificatori e al sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="42424-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="42424-114">L'applicazione passa i dati audio/video al writer di sink come input.</span><span class="sxs-lookup"><span data-stu-id="42424-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="42424-115">Non è importante il modo in cui l'applicazione Ottiene o genera i dati di input.</span><span class="sxs-lookup"><span data-stu-id="42424-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="42424-116">Un'opzione consiste nell'usare il [lettore di origine](source-reader.md), come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="42424-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="42424-117">Tuttavia, il writer di sink non richiede l'utilizzo del lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="42424-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="42424-118">Questi due componenti sono indipendenti.</span><span class="sxs-lookup"><span data-stu-id="42424-118">These two components are independent.</span></span>

![diagramma che mostra l'Reader di origine e il writer del sink.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="42424-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="42424-120">In this section</span></span>

-   [<span data-ttu-id="42424-121">Uso del writer di sink</span><span class="sxs-lookup"><span data-stu-id="42424-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="42424-122">Esercitazione: uso del writer di sink per codificare video</span><span class="sxs-lookup"><span data-stu-id="42424-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="42424-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42424-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42424-124">Codifica e creazione di file</span><span class="sxs-lookup"><span data-stu-id="42424-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="42424-125">Cenni preliminari sulla codifica in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42424-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



