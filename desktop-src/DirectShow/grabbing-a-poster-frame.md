---
description: Acquisizione di un frame di poster
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Acquisizione di un frame di poster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482693"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="a7e01-103">Acquisizione di un frame di poster</span><span class="sxs-lookup"><span data-stu-id="a7e01-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="a7e01-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a7e01-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a7e01-105">Questo articolo descrive come visualizzare un frame di poster da un file multimediale digitale, usando l'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) fornito con i [servizi di modifica DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="a7e01-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="a7e01-106">Il rilevatore multimediale è un oggetto helper che può ottenere informazioni sul formato da un file di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7e01-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="a7e01-107">Può inoltre acquisire un'immagine bitmap da un flusso video nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="a7e01-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="a7e01-108">Supponendo che il file sia ricercabile, è possibile ottenere l'immagine da qualsiasi punto del file.</span><span class="sxs-lookup"><span data-stu-id="a7e01-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="a7e01-109">L'immagine restituita è sempre in formato RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="a7e01-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="a7e01-110">Il rilevatore multimediale non è un filtro e non è necessario che l'applicazione usi Filter Graph Manager o crei un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="a7e01-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="a7e01-111">Internamente, il rilevatore multimediale crea un grafico di filtro che contiene il [**filtro Grabber di esempio**](sample-grabber-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a7e01-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="a7e01-112">Per ottenere una bitmap, il rilevatore multimediale Cerca e sospende il grafico del filtro e quindi recupera la bitmap dal filtro Grabber di esempio.</span><span class="sxs-lookup"><span data-stu-id="a7e01-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="a7e01-113">L'applicazione comunica con il rilevatore multimediale tramite l'interfaccia [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e01-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="a7e01-114">Il rilevatore multimediale è un valido esempio di incapsulamento di un grafico di filtro all'interno di un oggetto helper, allo scopo di proteggere le applicazioni dai dettagli correlati al grafo.</span><span class="sxs-lookup"><span data-stu-id="a7e01-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="a7e01-115">Il rilevatore multimediale funziona in due modalità.</span><span class="sxs-lookup"><span data-stu-id="a7e01-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="a7e01-116">Quando viene creata per la prima volta, il rilevatore multimediale si trova in modalità "raccolta informazioni".</span><span class="sxs-lookup"><span data-stu-id="a7e01-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="a7e01-117">È possibile specificare il nome di un file multimediale e ottenere informazioni su ognuno dei flussi nel file, ad esempio il tipo di formato, la frequenza dei fotogrammi o la durata.</span><span class="sxs-lookup"><span data-stu-id="a7e01-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="a7e01-118">Se il file contiene un flusso video, è possibile passare il rilevatore multimediale alla modalità "bitmap" e recuperare le bitmap dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a7e01-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="a7e01-119">Tuttavia, una volta eseguita questa operazione, non è possibile riportare il rilevatore multimediale alla modalità originale; viene collegato in modo permanente a tale flusso video.</span><span class="sxs-lookup"><span data-stu-id="a7e01-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="a7e01-120">Per usare un altro flusso o un altro file, è necessario creare una nuova istanza del rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7e01-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="a7e01-121">Gli esempi di codice in questa esercitazione usano la classe ATL **CComPtr** , che gestisce automaticamente i conteggi dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="a7e01-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="a7e01-122">Se si preferisce usare i puntatori dell'interfaccia raw, ricordarsi di rilasciare ogni interfaccia al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a7e01-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="a7e01-123">Inoltre, per brevità gli esempi di codice omettono gran parte del controllo degli errori che un'applicazione deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="a7e01-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="a7e01-124">Nel codice funzionante, controllare sempre i valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7e01-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="a7e01-125">Questa esercitazione include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7e01-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="a7e01-126">Passaggio 1: creare il Framework Windows</span><span class="sxs-lookup"><span data-stu-id="a7e01-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="a7e01-127">Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster</span><span class="sxs-lookup"><span data-stu-id="a7e01-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="a7e01-128">Passaggio 3: implementare la funzione Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="a7e01-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="a7e01-129">Passaggio 4: creare la bitmap nell'area client</span><span class="sxs-lookup"><span data-stu-id="a7e01-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="a7e01-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7e01-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e01-131">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="a7e01-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



