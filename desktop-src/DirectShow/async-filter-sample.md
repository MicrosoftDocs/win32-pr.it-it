---
description: Esempio di filtro asincrono
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Esempio di filtro asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049048"
---
# <a name="async-filter-sample"></a><span data-ttu-id="650d7-103">Esempio di filtro asincrono</span><span class="sxs-lookup"><span data-stu-id="650d7-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="650d7-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="650d7-104">Description</span></span>

<span data-ttu-id="650d7-105">L'esempio di filtro asincrono è un filtro di lettura file che supporta il download progressivo.</span><span class="sxs-lookup"><span data-stu-id="650d7-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="650d7-106">Questo filtro di esempio implementa le interfacce [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="650d7-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="650d7-107">Supporta i file MPEG, ma non i file AVI.</span><span class="sxs-lookup"><span data-stu-id="650d7-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="650d7-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="650d7-108">Usage</span></span>

<span data-ttu-id="650d7-109">Questo esempio include una piccola applicazione della riga di comando, Memfile.exe, che illustra il filtro.</span><span class="sxs-lookup"><span data-stu-id="650d7-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="650d7-110">Gli argomenti della riga di comando specificano un file multimediale e una velocità in bit, espressa in kilobyte al secondo.</span><span class="sxs-lookup"><span data-stu-id="650d7-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="650d7-111">L'applicazione legge il file in memoria alla velocità specificata e riproduce il file.</span><span class="sxs-lookup"><span data-stu-id="650d7-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="650d7-112">A tale scopo, viene creata un'istanza del filtro, viene aggiunto il filtro al grafo del filtro ed eseguito il rendering del PIN di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="650d7-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="650d7-113">Dalla riga di comando digitare:</span><span class="sxs-lookup"><span data-stu-id="650d7-113">At the command line, type:</span></span>

<span data-ttu-id="650d7-114">**Velocità in bit del file Memfile**</span><span class="sxs-lookup"><span data-stu-id="650d7-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="650d7-115">Il filtro di esempio asincrono non supporta i file AVI, perché non è in grado di connettersi al filtro del [separatore AVI](avi-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="650d7-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="650d7-116">Il pin di output del filtro asincrono propone MEDIATYPE \_ Stream e MEDIASUBTYPE \_ null per il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="650d7-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="650d7-117">Il pin di input nel filtro di separatore AVI non accetta MEDIASUBTYPE \_ null e non propone alcun tipo.</span><span class="sxs-lookup"><span data-stu-id="650d7-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="650d7-118">Pertanto, la connessione al pin ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="650d7-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="650d7-119">Il filtro asincrono potrebbe essere migliorato per offrire MEDIASUBTYPE \_ AVI quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="650d7-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="650d7-120">Ad esempio, potrebbe esaminare il formato di file o usare l'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="650d7-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="650d7-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="650d7-121">Downloading the Sample</span></span>

<span data-ttu-id="650d7-122">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="650d7-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="650d7-123">Questo esempio viene installato nel percorso seguente: \[ *SDK radice* \] \\ esempi di \\ \\ filtri DirectShow \\ multimediali \\ Async.</span><span class="sxs-lookup"><span data-stu-id="650d7-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="650d7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="650d7-124">Related topics</span></span>



[<span data-ttu-id="650d7-125">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="650d7-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



