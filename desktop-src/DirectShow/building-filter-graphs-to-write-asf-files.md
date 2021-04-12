---
description: Creazione di grafici filtro per la scrittura di file ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Creazione di grafici filtro per la scrittura di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482269"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="1ff2c-103">Creazione di grafici filtro per la scrittura di file ASF</span><span class="sxs-lookup"><span data-stu-id="1ff2c-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="1ff2c-104">Quando si crea contenuto basato su Windows Media, le applicazioni usano in genere uno degli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ff2c-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="1ff2c-105">Conversione o transcodifica del contenuto da un altro formato in formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="1ff2c-106">Inserimento di contenuto non basato su Windows Media (formati di flusso nativo) in file ASF.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="1ff2c-107">Acquisizione dei dati in tempo reale e codifica immediata nel formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="1ff2c-108">Transcodifica di file ASF</span><span class="sxs-lookup"><span data-stu-id="1ff2c-108">Transcoding ASF Files</span></span>

<span data-ttu-id="1ff2c-109">È possibile creare un grafico di filtro per la transcodifica di file usando il [writer ASF WM](wm-asf-writer-filter.md) in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="1ff2c-110">Il modo più semplice consiste nell'aggiungere il writer ASF WM al grafico di filtro e quindi usare il metodo IGraphBuilder:: RenderFile per creare automaticamente il grafo.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="1ff2c-111">In alternativa, è possibile aggiungere manualmente ogni filtro al grafico e connettere i pin.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="1ff2c-112">Dopo aver aggiunto il writer WM ASF, configurarlo usando i metodi IConfigAsfWriter se il profilo predefinito non è adatto e connettere i pin di input del writer ASF WM ai pin di output corrispondenti nei filtri upstream.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="1ff2c-113">Nella figura seguente viene illustrata la tipica configurazione del grafico di filtro per la transcodifica del writer WM ASF.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![transcodifica del grafico filtro](images/asf-transcode.png)

<span data-ttu-id="1ff2c-115">Inserimento di formati di flusso nativi in file ASF</span><span class="sxs-lookup"><span data-stu-id="1ff2c-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="1ff2c-116">Per impostazione predefinita, il filtro di scrittura WM ASF prevede flussi audio e video non compressi nei pin di input e usa i codec Windows Media Audio e Windows Media Video per comprimere i flussi.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="1ff2c-117">Tuttavia, il contenitore di file ASF può essere usato per qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="1ff2c-118">Inserendo i dati multimediali digitali in un contenitore di file ASF, è possibile aggiungere funzionalità fornite da ASF, ad esempio metadati e Digital Rights Management (DRM), senza la necessità di transcodificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="1ff2c-119">Per creare un file ASF che contiene contenuto non basato su Windows Media, l'applicazione deve comprimere il flusso nel grafico del filtro a Monte del writer ASF WM e ignorare il meccanismo di compressione del writer ASF WM chiamando [**IConfigAsfWriter2:: separat**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="1ff2c-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="1ff2c-120">Configurare quindi il filtro con il profilo desiderato.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="1ff2c-121">È essenziale che il tipo di supporto del flusso di input corrisponda esattamente al formato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="1ff2c-122">In alcuni casi, potrebbe essere necessario esaminare il formato del flusso di input e creare un profilo personalizzato per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="1ff2c-123">Quando si connette il writer ASF WM al filtro upstream, usare il metodo IGraphBuilder:: ConnectDirect.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="1ff2c-124">Non usare alcun metodo di "connessione intelligente", ad esempio IGraphBuilder:: Connect o IGraphBuilder:: RenderFile per connettere il filtro in quanto questa operazione Disabilita la modalità "bypass Compression" del filtro.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="1ff2c-125">Acquisizione diretta da un dispositivo a un file ASF</span><span class="sxs-lookup"><span data-stu-id="1ff2c-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="1ff2c-126">Quando si acquisisce audio o video direttamente in un file ASF, il grafico del filtro sarà simile al seguente, a seconda del tipo di dispositivo di acquisizione usato.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![grafico di acquisizione video di Windows Media](images/asf-webcam.png)

<span data-ttu-id="1ff2c-128">Per ulteriori informazioni sulla creazione di grafici di acquisizione video e audio, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ff2c-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="1ff2c-129">Acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="1ff2c-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="1ff2c-130">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="1ff2c-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="1ff2c-131">Il writer ASF WM non verrà eseguito a meno che tutti i relativi pin non siano connessi.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="1ff2c-132">Se si configura il writer ASF WM con il profilo di sistema predefinito (scelta non consigliata) o qualsiasi profilo con flussi audio e video, verrà creato un pin di input per ogni flusso e ognuno di questi pin deve essere connesso.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="1ff2c-133">Se non si intende acquisire audio, ad esempio, assicurarsi di configurare il filtro con un profilo di solo video in modo che non venga creato alcun pin audio.</span><span class="sxs-lookup"><span data-stu-id="1ff2c-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ff2c-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ff2c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ff2c-135">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1ff2c-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



