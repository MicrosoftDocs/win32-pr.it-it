---
description: Elaborazione In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Elaborazione In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304138"
---
# <a name="in-place-processing"></a><span data-ttu-id="f0d37-103">Elaborazione In-Place</span><span class="sxs-lookup"><span data-stu-id="f0d37-103">In-Place Processing</span></span>

<span data-ttu-id="f0d37-104">Alcune trasformazioni dei dati possono essere eseguite modificando direttamente i dati.</span><span class="sxs-lookup"><span data-stu-id="f0d37-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="f0d37-105">Questa operazione è denominata elaborazione *sul posto* .</span><span class="sxs-lookup"><span data-stu-id="f0d37-105">This is called *in-place* processing.</span></span> <span data-ttu-id="f0d37-106">Molti effetti audio e video possono essere eseguiti in questo modo.</span><span class="sxs-lookup"><span data-stu-id="f0d37-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="f0d37-107">Se un DMO supporta l'elaborazione sul posto, espone l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="f0d37-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="f0d37-108">L'elaborazione sul posto è in genere più efficiente rispetto all'uso di buffer distinti per l'output.</span><span class="sxs-lookup"><span data-stu-id="f0d37-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="f0d37-109">(Un'eccezione principale è quando il buffer risiede nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="f0d37-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="f0d37-110">In tal caso, le operazioni di lettura sono molto più lente delle operazioni di scrittura, pertanto l'elaborazione sul posto non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="f0d37-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="f0d37-111">Per elaborare i dati sul posto, il client effettua una singola chiamata al metodo [**IMediaObjectInPlace::P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , anziché a chiamate separate a **ProcessInput** e **ProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="f0d37-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="f0d37-112">Il metodo **Process** è sincrono; tutte le operazioni di elaborazione avvengono all'interno della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0d37-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="f0d37-113">Inoltre, l'elaborazione sul posto non usa gli oggetti **IMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="f0d37-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="f0d37-114">Il metodo **Process** accetta un puntatore direttamente al buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="f0d37-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="f0d37-115">Un DMO che supporta l'elaborazione sul posto deve comunque implementare l'interfaccia **IMediaObject** , inclusi i metodi **ProcessInput** e **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="f0d37-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="f0d37-116">Il client può scegliere se usare l'elaborazione sul posto o usare buffer distinti.</span><span class="sxs-lookup"><span data-stu-id="f0d37-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="f0d37-117">Tuttavia, non combinare i due tipi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f0d37-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="f0d37-118">Se si chiama il **Metodo Process**, non chiamare **ProcessInput** o **ProcessOutput** e viceversa.</span><span class="sxs-lookup"><span data-stu-id="f0d37-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="f0d37-119">**Effetti della coda**</span><span class="sxs-lookup"><span data-stu-id="f0d37-119">**Effect Tails**</span></span>

<span data-ttu-id="f0d37-120">Una DMO sul posto potrebbe creare un output aggiuntivo dopo l'arresto dell'input.</span><span class="sxs-lookup"><span data-stu-id="f0d37-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="f0d37-121">Questa operazione è detta *coda effetto*.</span><span class="sxs-lookup"><span data-stu-id="f0d37-121">This is called an *effect tail*.</span></span> <span data-ttu-id="f0d37-122">Un effetto di riverbero continua, ad esempio, dopo che l'input raggiunge il silenzio.</span><span class="sxs-lookup"><span data-stu-id="f0d37-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="f0d37-123">Se è presente un effetto Tail, il metodo **Process** restituisce S \_ false.</span><span class="sxs-lookup"><span data-stu-id="f0d37-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="f0d37-124">Una volta che l'applicazione ha elaborato tutti i dati, può generare la coda degli effetti inviando buffer vuoti al metodo **Process** .</span><span class="sxs-lookup"><span data-stu-id="f0d37-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0d37-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0d37-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0d37-126">Hosting diretto di un DMO</span><span class="sxs-lookup"><span data-stu-id="f0d37-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



