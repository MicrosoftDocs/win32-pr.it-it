---
title: Implementazione di un plug-in DSP audio
description: Implementazione di un plug-in DSP audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, implementazione del codice
- Plug-in DSP, implementazione del codice
- plug-in di elaborazione dei segnali digitali, modifica del codice di esempio
- Plug-in DSP, modifica del codice di esempio
- plug-in di elaborazione dei segnali digitali, implementazione audio
- Plug-in DSP, implementazione audio
- plug-in DSP audio, implementazione del codice
- plug-in audio DSP, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045031"
---
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="c25ce-113">Implementazione di un plug-in DSP audio</span><span class="sxs-lookup"><span data-stu-id="c25ce-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="c25ce-114">Per creare un plug-in Windows Media Player DSP che elabora l'audio, è necessario modificare il codice di esempio nella funzione denominata **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="c25ce-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="c25ce-115">**DoProcessOutput** viene chiamato ogni volta che Windows Media Player chiama correttamente **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="c25ce-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="c25ce-116">Si tratta della funzione che esegue le attività di elaborazione dei segnali digitali che producono il risultato udibile che il plug-in DSP deve produrre.</span><span class="sxs-lookup"><span data-stu-id="c25ce-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="c25ce-117">L'elaborazione di un flusso audio è simile alla gestione di un evento temporizzato.</span><span class="sxs-lookup"><span data-stu-id="c25ce-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="c25ce-118">**DoProcessOutput** verrà chiamato ripetutamente e a intervalli specifici.</span><span class="sxs-lookup"><span data-stu-id="c25ce-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="c25ce-119">Ogni volta che il codice viene eseguito, sarà necessario elaborare un numero specifico di byte di dati.</span><span class="sxs-lookup"><span data-stu-id="c25ce-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="c25ce-120">**DoProcessOutput** contiene i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c25ce-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="c25ce-121">Parametro</span><span class="sxs-lookup"><span data-stu-id="c25ce-121">Parameter</span></span>          | <span data-ttu-id="c25ce-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25ce-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25ce-123">*pbOutputData*</span><span class="sxs-lookup"><span data-stu-id="c25ce-123">*pbOutputData*</span></span>     | <span data-ttu-id="c25ce-124">Si tratta di un puntatore di **byte** al buffer in cui l'implementazione di **DoProcessOutput** deve copiare i dati elaborati.</span><span class="sxs-lookup"><span data-stu-id="c25ce-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="c25ce-125">*pbInputData*</span><span class="sxs-lookup"><span data-stu-id="c25ce-125">*pbInputData*</span></span>      | <span data-ttu-id="c25ce-126">Puntatore di **byte** costante al buffer che contiene i dati da elaborare.</span><span class="sxs-lookup"><span data-stu-id="c25ce-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="c25ce-127">*cbBytesToProcess*</span><span class="sxs-lookup"><span data-stu-id="c25ce-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="c25ce-128">Si tratta di un valore **DWORD** che contiene un conteggio del numero di byte nel buffer di input da elaborare.</span><span class="sxs-lookup"><span data-stu-id="c25ce-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="c25ce-129">Nelle sezioni seguenti vengono fornite informazioni dettagliate su come modificare il codice generato dalla procedura guidata plug-in di Windows Media Player per creare un plug-in di DSP audio personalizzato:</span><span class="sxs-lookup"><span data-stu-id="c25ce-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="c25ce-130">Implementazione di DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="c25ce-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="c25ce-131">Aggiunta di proprietà al plug-in audio DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="c25ce-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="c25ce-132">Implementazione della pagina delle proprietà per un plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="c25ce-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="c25ce-133">Modifica della proprietà del plug-in audio DSP di esempio</span><span class="sxs-lookup"><span data-stu-id="c25ce-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="c25ce-134">Informazioni sulla discontinuità</span><span class="sxs-lookup"><span data-stu-id="c25ce-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="c25ce-135">Informazioni sull'allocazione delle risorse di streaming</span><span class="sxs-lookup"><span data-stu-id="c25ce-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="c25ce-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c25ce-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c25ce-137">**Informazioni sui plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="c25ce-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




