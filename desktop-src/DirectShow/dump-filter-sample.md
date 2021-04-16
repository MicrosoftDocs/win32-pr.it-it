---
description: Esempio di filtro dump
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Esempio di filtro dump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522417"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="6f5bb-103">Esempio di filtro dump</span><span class="sxs-lookup"><span data-stu-id="6f5bb-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="6f5bb-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f5bb-104">Description</span></span>

<span data-ttu-id="6f5bb-105">Il filtro dump è un filtro renderer che scrive gli esempi di supporti ricevuti in un file di testo.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="6f5bb-106">Questo esempio illustra come usare la classe di filtro di base [**CBaseFilter**](cbasefilter.md) e la classe del PIN di input con rendering [**CRenderedInputPin**](crenderedinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="6f5bb-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="6f5bb-107">Viene inoltre illustrato come implementare l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) .</span><span class="sxs-lookup"><span data-stu-id="6f5bb-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="6f5bb-108">Il filtro dump ha un singolo pin di input, che scrive tutti i campioni ricevuti direttamente in un file.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="6f5bb-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6f5bb-109">Usage</span></span>

<span data-ttu-id="6f5bb-110">Questo filtro è un utile strumento di debug.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="6f5bb-111">Ad esempio, è possibile verificare, bit per bit, i risultati di un filtro di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="6f5bb-112">È possibile compilare un grafo manualmente usando GraphEdit e connettere il filtro dump all'output di un filtro di trasformazione o di qualsiasi altro pin di output.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="6f5bb-113">È anche possibile connettere un filtro Tee e inserire il filtro dump su una gamba del filtro Tee e l'output tipico su un'altra parte per monitorare i risultati in uno scenario in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="6f5bb-114">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6f5bb-114">Downloading the Sample</span></span>

<span data-ttu-id="6f5bb-115">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6f5bb-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="6f5bb-116">Questo esempio viene installato nel percorso seguente: *\[ directory radice \] SDK* \\ esempi di \\ \\ filtri DirectShow Multimedia \\ \\ dump.</span><span class="sxs-lookup"><span data-stu-id="6f5bb-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f5bb-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f5bb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f5bb-118">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="6f5bb-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



