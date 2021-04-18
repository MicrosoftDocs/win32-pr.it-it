---
description: Uso di Media Detector
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Uso di Media Detector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320469"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="ff8da-103">Uso di Media Detector</span><span class="sxs-lookup"><span data-stu-id="ff8da-103">Using the Media Detector</span></span>

<span data-ttu-id="ff8da-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="ff8da-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="ff8da-105">Il rilevatore multimediale è un oggetto helper in grado di recuperare informazioni su un file, ad esempio il numero di flussi, il tipo e la durata.</span><span class="sxs-lookup"><span data-stu-id="ff8da-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="ff8da-106">Contiene inoltre metodi per il recupero di frame di poster da un flusso video.</span><span class="sxs-lookup"><span data-stu-id="ff8da-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="ff8da-107">Espone l'interfaccia [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="ff8da-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="ff8da-108">Il rilevatore multimediale funziona in una delle due modalità.</span><span class="sxs-lookup"><span data-stu-id="ff8da-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="ff8da-109">Quando si crea un'istanza del rilevamento multimediale, questa non è associata a un file di origine specifico.</span><span class="sxs-lookup"><span data-stu-id="ff8da-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="ff8da-110">In questa modalità è possibile recuperare informazioni sul flusso da più file di origine.</span><span class="sxs-lookup"><span data-stu-id="ff8da-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="ff8da-111">Tuttavia, una volta usato il rilevatore multimediale per ottenere un frame di poster, passa alla modalità di acquisizione *bitmap*.</span><span class="sxs-lookup"><span data-stu-id="ff8da-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="ff8da-112">In modalità di cattura bitmap, il rilevatore multimediale è collegato a un flusso video specifico e i metodi di informazioni sul flusso non funzionano più.</span><span class="sxs-lookup"><span data-stu-id="ff8da-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="ff8da-113">Inoltre, non è possibile riattivare il rilevatore multimediale fino alla modalità di avvio.</span><span class="sxs-lookup"><span data-stu-id="ff8da-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="ff8da-114">Pertanto, ottenere tutte le informazioni sul flusso necessarie prima di recuperare i frame dei poster oppure creare nuove istanze del rilevamento multimediale per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="ff8da-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="ff8da-115">Per ottenere informazioni sul flusso, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="ff8da-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="ff8da-116">Chiamare [**IMediaDet::p \_ nome file UT**](imediadet-put-filename.md) con il nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="ff8da-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="ff8da-117">Chiamare [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) per ottenere il numero di flussi nell'origine.</span><span class="sxs-lookup"><span data-stu-id="ff8da-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="ff8da-118">Specificare un numero di flusso con [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="ff8da-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="ff8da-119">Chiamare quindi uno o più dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff8da-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="ff8da-120">[**IMediaDet:: Get \_ StreamType**](imediadet-get-streamtype.md): Recupera il tipo di supporto del flusso.</span><span class="sxs-lookup"><span data-stu-id="ff8da-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="ff8da-121">[**IMediaDet:: Get \_ StreamLength**](imediadet-get-streamlength.md): Recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="ff8da-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="ff8da-122">[**IMediaDet:: Get \_ FrameRate**](imediadet-get-framerate.md): Recupera la frequenza dei fotogrammi di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="ff8da-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="ff8da-123">Per ottenere un frame di poster, specificare il numero di flusso, come nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="ff8da-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="ff8da-124">Chiamare quindi [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), che copia un frame di poster in un buffer o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), che salva un frame di poster in un file.</span><span class="sxs-lookup"><span data-stu-id="ff8da-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff8da-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff8da-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff8da-126">Utilizzo di origini</span><span class="sxs-lookup"><span data-stu-id="ff8da-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



