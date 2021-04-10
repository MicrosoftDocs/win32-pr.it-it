---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967119"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="0069a-103">Uso del writer di sink</span><span class="sxs-lookup"><span data-stu-id="0069a-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="0069a-104">Panoramica</span><span class="sxs-lookup"><span data-stu-id="0069a-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="0069a-105">Tipi di contenitori di file</span><span class="sxs-lookup"><span data-stu-id="0069a-105">File Container Types</span></span>

<span data-ttu-id="0069a-106">Il writer di sink dispone del supporto incorporato per diversi tipi di contenitori di file.</span><span class="sxs-lookup"><span data-stu-id="0069a-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="0069a-107">Per un elenco completo, vedere [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="0069a-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="0069a-108">Per supportare tipi di contenitori aggiuntivi, è possibile scrivere un [sink multimediale](media-sinks.md)personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0069a-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="0069a-109">Il contenitore di file viene specificato quando si crea una nuova istanza del writer del sink.</span><span class="sxs-lookup"><span data-stu-id="0069a-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="0069a-110">Formati di flusso</span><span class="sxs-lookup"><span data-stu-id="0069a-110">Stream Formats</span></span>

<span data-ttu-id="0069a-111">Per ogni flusso, l'applicazione deve specificare quanto segue.</span><span class="sxs-lookup"><span data-stu-id="0069a-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="0069a-112">Il *formato di input* è il formato inviato dall'applicazione al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="0069a-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="0069a-113">Il *formato di output* è il formato che verrà scritto nel file.</span><span class="sxs-lookup"><span data-stu-id="0069a-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="0069a-114">I formati di input e di output possono essere compressi o decompressi.</span><span class="sxs-lookup"><span data-stu-id="0069a-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="0069a-115">Il writer di sink supporta le combinazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0069a-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="0069a-116">Input non compresso con output compresso.</span><span class="sxs-lookup"><span data-stu-id="0069a-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="0069a-117">Questo è il caso tipico e viene usato per gli scenari di codifica o di transcodifica.</span><span class="sxs-lookup"><span data-stu-id="0069a-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="0069a-118">Deve essere disponibile un codificatore Microsoft Media Foundation che accetta il tipo di input e codifica per il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="0069a-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="0069a-119">Input compresso con output identico.</span><span class="sxs-lookup"><span data-stu-id="0069a-119">Compressed input with identical output.</span></span> <span data-ttu-id="0069a-120">Usare questa combinazione per remux un file senza transcodifica.</span><span class="sxs-lookup"><span data-stu-id="0069a-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="0069a-121">Input non compresso con output identico.</span><span class="sxs-lookup"><span data-stu-id="0069a-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="0069a-122">Usare questa combinazione per scrivere audio o video non compressi in un contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="0069a-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="0069a-123">Il writer di sink non supporta il ridimensionamento video, la conversione della frequenza dei frame o il ricampionamento audio, a meno che queste funzioni non siano fornite dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0069a-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="0069a-124">In caso contrario, l'applicazione può usare i [processori di segnale digitale](windowsmediadigitalsignalprocessors.md) per convertire i dati di input, prima di inviare i dati al</span><span class="sxs-lookup"><span data-stu-id="0069a-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="0069a-125">Creazione del writer di sink</span><span class="sxs-lookup"><span data-stu-id="0069a-125">Creating the Sink Writer</span></span>

<span data-ttu-id="0069a-126">Sono disponibili due funzioni che creano il writer di sink:</span><span class="sxs-lookup"><span data-stu-id="0069a-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="0069a-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) accetta l'URL di un file di output o un puntatore a un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="0069a-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="0069a-128">Questa funzione crea il sink multimediale internamente.</span><span class="sxs-lookup"><span data-stu-id="0069a-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="0069a-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) accetta un puntatore a un sink multimediale che è già stato creato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0069a-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="0069a-130">Se si usa uno dei sink di supporto incorporati, la funzione [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) è preferibile, perché il chiamante non deve configurare il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0069a-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="0069a-131">Il metodo [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fornisce diverse opzioni per specificare il tipo di contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="0069a-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="0069a-132">Nel caso più semplice, la funzione usa l'estensione del nome file nell'URL per selezionare il contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="0069a-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="0069a-133">Per informazioni dettagliate, vedere la pagina di riferimento per le funzioni.</span><span class="sxs-lookup"><span data-stu-id="0069a-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="0069a-134">Il codice seguente, ad esempio, specifica il nome file "output. wmv" per l'URL.</span><span class="sxs-lookup"><span data-stu-id="0069a-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="0069a-135">In base all'estensione del nome di file, il writer di sink caricherà il [sink multimediale ASF](asf-media-sinks.md) per creare un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="0069a-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="0069a-136">Nel caso di [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), il tipo di file è determinato dal sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="0069a-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0069a-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0069a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0069a-138">Writer sink</span><span class="sxs-lookup"><span data-stu-id="0069a-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



