---
description: Esempio di filtro di ambito
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Esempio di filtro di ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481517"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="69f54-103">Esempio di filtro di ambito</span><span class="sxs-lookup"><span data-stu-id="69f54-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="69f54-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69f54-104">Description</span></span>

<span data-ttu-id="69f54-105">Il filtro ambito è un filtro renderer che Visualizza i dati audio come moduli Wave.</span><span class="sxs-lookup"><span data-stu-id="69f54-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="69f54-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="69f54-106">Usage</span></span>

<span data-ttu-id="69f54-107">Per usare questo filtro, aprire GraphEdit ed eseguire il rendering di un file audio o di un file video con un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="69f54-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="69f54-108">Disconnettere temporaneamente il renderer audio e inserire il filtro di esempio Infinite-Pin Tee ([esempio di filtro InfTee](inftee-filter-sample.md)).</span><span class="sxs-lookup"><span data-stu-id="69f54-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="69f54-109">Riconnettere il renderer audio.</span><span class="sxs-lookup"><span data-stu-id="69f54-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="69f54-110">Connettere quindi il secondo pin di output del filtro Infinite-Pin tee al filtro ambito.</span><span class="sxs-lookup"><span data-stu-id="69f54-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="69f54-111">A questo punto, eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="69f54-111">Now run the graph.</span></span>

<span data-ttu-id="69f54-112">La finestra ambito viene implementata come finestra di dialogo, non come finestra effettiva.</span><span class="sxs-lookup"><span data-stu-id="69f54-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="69f54-113">Gli sviluppatori che creano pannelli di controllo per modificare i parametri di filtro in tempo reale potrebbero voler usare una tecnica come questa piuttosto che le pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="69f54-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="69f54-114">Il filtro di ambito illustra la configurazione di un thread separato per elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="69f54-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="69f54-115">In questo caso, i dati vengono semplicemente copiati in un buffer separato nel metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) e vengono quindi disegnati sulla finestra ambito nel thread separato.</span><span class="sxs-lookup"><span data-stu-id="69f54-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="69f54-116">Il filtro ambito consente inoltre di monitorare l'output audio per determinare se si sta ritagliando, in modo da poter modificare il guadagno.</span><span class="sxs-lookup"><span data-stu-id="69f54-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="69f54-117">Questo filtro viene visualizzato in GraphEdit come "oscilloscopio".</span><span class="sxs-lookup"><span data-stu-id="69f54-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="69f54-118">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="69f54-118">Downloading the Sample</span></span>

<span data-ttu-id="69f54-119">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69f54-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="69f54-120">Questo esempio viene installato nel percorso seguente: *\[ directory radice \] SDK* \\ esempi di \\ \\ filtri DirectShow multimediali \\ \\ ambito.</span><span class="sxs-lookup"><span data-stu-id="69f54-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69f54-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69f54-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f54-122">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="69f54-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



