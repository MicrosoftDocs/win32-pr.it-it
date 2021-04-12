---
title: Implementazione di DoProcessOutput
description: Implementazione di DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in per l'elaborazione di segnali digitali, DoProcessOutput
- Plug-in DSP, DoProcessOutput
- plug-in DSP audio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396202"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="42fb7-108">Implementazione di DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="42fb7-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="42fb7-109">Per elaborare i dati audio, è necessario eseguire diversi passaggi in **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="42fb7-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="42fb7-110">Nei passaggi seguenti viene utilizzato il codice di esempio della procedura guidata plug-in come esempi.</span><span class="sxs-lookup"><span data-stu-id="42fb7-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="42fb7-111">Se si desidera creare un plug-in DSP audio che elabora il contenuto multimediale dello stesso tipo utilizzato dal codice di esempio della procedura guidata per il plug-in, sarà necessario solo modificare il codice di elaborazione effettivo a cui fa riferimento il passaggio 6.</span><span class="sxs-lookup"><span data-stu-id="42fb7-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="42fb7-112">Di seguito sono riportati tutti i passaggi implementati in **DoProcessOutput**:</span><span class="sxs-lookup"><span data-stu-id="42fb7-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="42fb7-113">Se il plug-in non è attualmente abilitato, copiare semplicemente i dati invariati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="42fb7-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="42fb7-114">Se il plug-in converte i dati in un formato diverso, è necessario eseguire anche l'elaborazione della conversione.</span><span class="sxs-lookup"><span data-stu-id="42fb7-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="42fb7-115">Recuperare un puntatore alla struttura del formato di input.</span><span class="sxs-lookup"><span data-stu-id="42fb7-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="42fb7-116">È necessario recuperare i dati dei membri da questa struttura, quindi copiare il puntatore da *m \_ mtInput*.**pbFormat** a una variabile puntatore locale di un tipo che corrisponde al tipo di struttura del formato.</span><span class="sxs-lookup"><span data-stu-id="42fb7-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="42fb7-117">Nell'esempio seguente viene archiviato un puntatore a una struttura del formato di input **WAVEFORMATEX** :</span><span class="sxs-lookup"><span data-stu-id="42fb7-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="42fb7-118">Calcolare il numero di campioni da elaborare.</span><span class="sxs-lookup"><span data-stu-id="42fb7-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="42fb7-119">Il codice di esempio generato dalla procedura guidata plug-in esegue questo passaggio dividendo il numero di byte da elaborare per il membro **nBlockAlign** della struttura del formato di input WAVEFORMATEX e quindi moltiplicando il risultato per il numero di canali, che è stato archiviato nel membro **nChannels** .</span><span class="sxs-lookup"><span data-stu-id="42fb7-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="42fb7-120">Nell'esempio seguente viene riportato il codice di esempio della procedura guidata plug-in:</span><span class="sxs-lookup"><span data-stu-id="42fb7-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="42fb7-121">Determinare la profondità del bit dell'audio.</span><span class="sxs-lookup"><span data-stu-id="42fb7-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="42fb7-122">Il codice di esempio della procedura guidata plug-in determina l'audio a 8 bit o a 16 bit esaminando il membro **wBitsPerSample** della struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="42fb7-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="42fb7-123">USA quindi tale valore in un'istruzione switch per fornire routine di elaborazione separate per ogni profondità di bit.</span><span class="sxs-lookup"><span data-stu-id="42fb7-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="42fb7-124">Potrebbe essere necessario usare una tecnica diversa quando si gestiscono altri tipi di formato e profondità dei bit.</span><span class="sxs-lookup"><span data-stu-id="42fb7-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="42fb7-125">Creare un ciclo per esaminare gli esempi audio nel buffer di input.</span><span class="sxs-lookup"><span data-stu-id="42fb7-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="42fb7-126">Recuperare un campione dal buffer di input.</span><span class="sxs-lookup"><span data-stu-id="42fb7-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="42fb7-127">A tale scopo, dereferenziare il puntatore ai dati di input e archiviare il risultato in una variabile di tipo int. Per l'audio a 16 bit, è necessario eseguire il cast del puntatore di BYTE a un puntatore breve per gestire la precisione del campione audio maggiore.</span><span class="sxs-lookup"><span data-stu-id="42fb7-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="42fb7-128">Una volta ottenuto il valore, è possibile incrementare immediatamente il puntatore *pbInputData* in modo che punti all'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="42fb7-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="42fb7-129">Negli esempi seguenti viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="42fb7-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="42fb7-130">-oppure-</span><span class="sxs-lookup"><span data-stu-id="42fb7-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="42fb7-131">Eseguire l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="42fb7-131">Perform the processing.</span></span> <span data-ttu-id="42fb7-132">Questo è il punto in cui si applicano in qualche modo gli algoritmi che modificano l'esempio.</span><span class="sxs-lookup"><span data-stu-id="42fb7-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="42fb7-133">Questa operazione è stata eseguita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="42fb7-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="42fb7-134">Scrivere i dati elaborati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="42fb7-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="42fb7-135">Incrementare immediatamente il puntatore al buffer di output, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="42fb7-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="42fb7-136">Ripetere il ciclo finché non vengono elaborati tutti gli esempi.</span><span class="sxs-lookup"><span data-stu-id="42fb7-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="42fb7-137">Restituisce un valore **HRESULT** appropriato.</span><span class="sxs-lookup"><span data-stu-id="42fb7-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42fb7-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42fb7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42fb7-139">**Implementazione di un plug-in DSP audio**</span><span class="sxs-lookup"><span data-stu-id="42fb7-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




