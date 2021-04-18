---
description: Calcolo dei valori dei parametri
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calcolo dei valori dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304140"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="7ee3b-103">Calcolo dei valori dei parametri</span><span class="sxs-lookup"><span data-stu-id="7ee3b-103">Calculating Parameter Values</span></span>

<span data-ttu-id="7ee3b-104">Potenzialmente, un buffer di input potrebbe essere molto grande.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="7ee3b-105">Idealmente, quando DMO elabora il buffer, i parametri seguiranno esattamente le curve nell'intero batch di dati.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="7ee3b-106">Tuttavia, un DMO presenta un certo margine di manovra per il calcolo di tali valori.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="7ee3b-107">L'approccio più accurato consiste nel calcolare il valore esatto per ogni unità di dati atomica. ad esempio, ogni esempio di audio.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="7ee3b-108">Questo approccio è il più costoso dal punto di vista del calcolo.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="7ee3b-109">Un altro approccio consiste nel sezionare i dati in unità più piccole di alcune dimensioni fisse, ad esempio 100 esempi.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="7ee3b-110">Questo approccio crea un effetto "scale-stepping".</span><span class="sxs-lookup"><span data-stu-id="7ee3b-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="7ee3b-111">Per alcuni parametri, questo potrebbe essere accettabile.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="7ee3b-112">Negli effetti audio, potrebbe creare artefatti udibili.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="7ee3b-113">Un compromesso consiste nell'utilizzare la tecnica precedente, ma all'interno di ogni batch eseguire un'interpolazione lineare del valore del parametro per ogni campione.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="7ee3b-114">Questi problemi sono particolarmente importanti per l'elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="7ee3b-115">Un secondo di audio potrebbe contenere 48.000 campioni audio per canale, che è un numero elevato di calcoli da eseguire, ma l'orecchio è sensibile agli artefatti, ad esempio l'aliasing.</span><span class="sxs-lookup"><span data-stu-id="7ee3b-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ee3b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ee3b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ee3b-117">Parametri dei supporti</span><span class="sxs-lookup"><span data-stu-id="7ee3b-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



