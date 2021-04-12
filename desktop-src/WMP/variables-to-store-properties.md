---
title: Variabili per archiviare le proprietà
description: Variabili per archiviare le proprietà
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
- Esempio di plug-in Echo DSP, variabili per l'archiviazione delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221595"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="b1a3e-109">Variabili per archiviare le proprietà</span><span class="sxs-lookup"><span data-stu-id="b1a3e-109">Variables to Store Properties</span></span>

<span data-ttu-id="b1a3e-110">Per prima cosa, è necessaria una variabile per archiviare l'ora di ritardo.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="b1a3e-111">L'esempio predefinito creato dalla procedura guidata per il plug-in di Windows Media Player fornisce una variabile denominata m \_ fScaleFactor per archiviare il moltiplicatore di scalabilità usato per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="b1a3e-112">Questo esempio non richiede più questa variabile, quindi è possibile modificarne il nome e il tipo per archiviare il valore di tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="b1a3e-113">Sostituire ogni istanza di m \_ fScaleFactor in Echo. h e Echo. cpp con m \_ dwDelayTime.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="b1a3e-114">Modificare il tipo di dati per m \_ fScaleFactor (ora m \_ dwDelayTime) da Double a DWORD in Echo. h.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="b1a3e-115">Nel costruttore per CEcho modificare il valore di tempo di ritardo predefinito in 1000.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="b1a3e-116">Dichiarare quindi due nuove variabili membro per archiviare la percentuale del segnale di effetto e la percentuale del segnale di origine da combinare nel buffer di output finale.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="b1a3e-117">Il termine "Wet" si riferisce all'effetto e il termine "Dry" si riferisce al segnale di origine.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="b1a3e-118">Aggiungere le seguenti dichiarazioni a Echo. h:</span><span class="sxs-lookup"><span data-stu-id="b1a3e-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="b1a3e-119">Questi valori vengono archiviati come rappresentazioni decimali delle percentuali in modo che possano essere facilmente usati come fattori di scala.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="b1a3e-120">Ad esempio, una combinazione di effetto 50% e segnale di origine 50% verrebbe rappresentata come valore 0,50 per ogni variabile.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="b1a3e-121">La somma dei valori per m \_ fWetMix e m \_ fDryMix non deve essere maggiore di 1,0 (100%).</span><span class="sxs-lookup"><span data-stu-id="b1a3e-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="b1a3e-122">Questi valori saranno infine accessibili come proprietà.</span><span class="sxs-lookup"><span data-stu-id="b1a3e-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="b1a3e-123">Aggiungere il codice seguente al costruttore CEcho per impostare i valori predefiniti su 50 percent each:</span><span class="sxs-lookup"><span data-stu-id="b1a3e-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="b1a3e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1a3e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a3e-125">**Proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="b1a3e-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




