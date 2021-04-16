---
title: Supporto del codice ora SMPTE
description: Supporto del codice ora SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK, codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- ASF (Advanced Systems Format), codici temporali SMPTE
- Windows Media Format SDK, interfaccia IWMReaderTimecode
- Advanced Systems Format (ASF), interfaccia IWMReaderTimecode
- ASF (formato avanzato dei sistemi), interfaccia IWMReaderTimecode
- Codici temporali SMPTE, informazioni
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516609"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="a9e00-111">Supporto del codice ora SMPTE</span><span class="sxs-lookup"><span data-stu-id="a9e00-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="a9e00-112">Windows Media Format SDK fornisce supporto limitato per il codice ora SMPTE, che è un formato di codice ora solare per i film e la televisione.</span><span class="sxs-lookup"><span data-stu-id="a9e00-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="a9e00-113">È possibile includere i dati del codice ora SMPTE con esempi come estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="a9e00-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="a9e00-114">La parte relativa ai dati dell'estensione è una struttura di [**\_ dati dell' \_ estensione \_ del codice temporale WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) contenente le informazioni del timestamp originale del SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a9e00-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="a9e00-115">Il mantenimento del codice ora SMPTE nei file ASF comporta limiti di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a9e00-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="a9e00-116">Ogni campione con un timestamp SMPTE associato richiede il trasporto dei 14 byte nella struttura del timestamp.</span><span class="sxs-lookup"><span data-stu-id="a9e00-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="a9e00-117">In uno scenario di streaming, questo requisito di larghezza di banda maggiore potrebbe essere catastrofico.</span><span class="sxs-lookup"><span data-stu-id="a9e00-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="a9e00-118">Di conseguenza, è consigliabile che i codici temporali SMPTE siano salvati in modo permanente solo nei file ASF durante il processo di modifica video, che in genere viene eseguito con i file locali.</span><span class="sxs-lookup"><span data-stu-id="a9e00-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="a9e00-119">Quando viene creato il file finale, è necessario rimuovere le estensioni dell'unità dati.</span><span class="sxs-lookup"><span data-stu-id="a9e00-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="a9e00-120">È possibile leggere i timestamp SMPTE esattamente come si legge qualsiasi altra estensione di unità dati, ma gli oggetti di lettura forniscono il supporto integrato per la ricerca in base al codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a9e00-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="a9e00-121">Per poter cercare i timestamp SMPTE, è necessario innanzitutto indicizzare il file in base al codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a9e00-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="a9e00-122">È possibile configurare l'indicizzatore per indicizzare i codici temporali usando il metodo [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .</span><span class="sxs-lookup"><span data-stu-id="a9e00-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="a9e00-123">Utilizzando il Reader asincrono, è possibile spostarsi in un file in base ai timestamp SMPTE utilizzando i metodi dell'interfaccia [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) e il metodo [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) .</span><span class="sxs-lookup"><span data-stu-id="a9e00-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="a9e00-124">Con il lettore sincrono, utilizzare [**IWMSyncReader2:: SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span><span class="sxs-lookup"><span data-stu-id="a9e00-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9e00-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9e00-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9e00-126">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="a9e00-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="a9e00-127">**Configurazione di estensioni delle unità dati**</span><span class="sxs-lookup"><span data-stu-id="a9e00-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




