---
description: Esempio di filtro palla
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Esempio di filtro palla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876958"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="a4a3c-103">Esempio di filtro palla</span><span class="sxs-lookup"><span data-stu-id="a4a3c-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="a4a3c-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a3c-104">Description</span></span>

<span data-ttu-id="a4a3c-105">Il filtro palla è un filtro di origine video che produce un'immagine di una palla da rimbalzo.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="a4a3c-106">Questo esempio illustra la negoziazione del formato e l'uso delle classi di base del filtro di origine [**CSource**](csource.md) e [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="a4a3c-107">Il codice in Fball. h e Fball. cpp gestisce le interfacce del filtro.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="a4a3c-108">Questi due file contengono approssimativamente il codice minimo necessario per un filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="a4a3c-109">I file Ball. h e Ball. cpp contengono il codice che rimbalza sulla palla.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="a4a3c-110">Questo filtro ha un singolo pin di output, che fornisce un flusso video che mostra una palla che rimbalza nel frame.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="a4a3c-111">Il filtro palla accetta anche richieste di gestione di qualità dal filtro downstream, che illustra una semplice strategia di gestione della qualità.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="a4a3c-112">Questo filtro implementa l'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a4a3c-113">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="a4a3c-113">Downloading the Sample</span></span>

<span data-ttu-id="a4a3c-114">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4a3c-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="a4a3c-115">Questo esempio viene installato nel percorso seguente: \[ *SDK radice* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Ball.</span><span class="sxs-lookup"><span data-stu-id="a4a3c-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4a3c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4a3c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a3c-117">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4a3c-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



