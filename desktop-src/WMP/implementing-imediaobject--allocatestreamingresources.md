---
title: Implementazione di IMediaObject AllocateStreamingResources
description: Implementazione di IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Plug-in di Windows Media Player, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, buffer di ritardo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396242"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="bbda0-109">Implementazione di IMediaObject:: AllocateStreamingResources</span><span class="sxs-lookup"><span data-stu-id="bbda0-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="bbda0-110">Nell'esempio Echo il metodo **AllocateStreamingResources** crea il buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="bbda0-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="bbda0-111">A tale scopo, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbda0-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="bbda0-112">Calcolo di una dimensione per il buffer che corrisponde al tempo di ritardo specificato per il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="bbda0-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="bbda0-113">Allocando una nuova memoria o riallocando la dimensione del buffer, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="bbda0-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="bbda0-114">Chiamata a un metodo che riempie il buffer con i valori che rappresentano il silenzio.</span><span class="sxs-lookup"><span data-stu-id="bbda0-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="bbda0-115">Il valore di Silence è diverso a seconda della profondità del bit.</span><span class="sxs-lookup"><span data-stu-id="bbda0-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="bbda0-116">Per audio a 8 bit, il silenzio è rappresentato dal valore esadecimale 80; per audio a 16 bit, il silenzio è rappresentato da zero.</span><span class="sxs-lookup"><span data-stu-id="bbda0-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="bbda0-117">Calcolo della dimensione del buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="bbda0-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="bbda0-118">Per calcolare le dimensioni necessarie per il buffer di ritardo, è necessario innanzitutto recuperare una struttura **WAVEFORMATEX** contenente informazioni sui dati audio.</span><span class="sxs-lookup"><span data-stu-id="bbda0-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="bbda0-119">Nell'esempio seguente viene recuperato un puntatore a questa struttura dalla struttura **del \_ \_ tipo di supporto DMO** di input:</span><span class="sxs-lookup"><span data-stu-id="bbda0-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="bbda0-120">Una volta archiviato un puntatore alla struttura **WAVEFORMATEX** corretta, è possibile esaminarne i membri e usarli per calcolare le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="bbda0-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="bbda0-121">Nell'esempio di codice seguente viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bbda0-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="bbda0-122">Questo algoritmo calcola la dimensione del buffer moltiplicando il tempo di ritardo, in millisecondi, per il numero di campioni per millisecondo, moltiplicando quindi il risultato per il numero di canali, quindi moltiplicando il risultato per il numero di byte per campione.</span><span class="sxs-lookup"><span data-stu-id="bbda0-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="bbda0-123">Il numero di canali e il numero di byte per campione non sono evidenti. sono codificati nel membro nBlockAlign.</span><span class="sxs-lookup"><span data-stu-id="bbda0-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="bbda0-124">Dividendo per 1000, il valore nSamplesPerSec viene ridotto a campioni per millisecondo; il millisecondo è l'unità desiderata perché il tempo di ritardo è espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="bbda0-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="bbda0-125">Allocazione della memoria del buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="bbda0-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="bbda0-126">Una volta calcolati i requisiti di memoria, è possibile allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="bbda0-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="bbda0-127">Potrebbe essere necessario eliminare il buffer, se esistente, ad esempio quando l'utente richiama la pagina delle proprietà per modificare il valore di tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="bbda0-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="bbda0-128">Il codice seguente illustra l'allocazione del buffer di ritardo:</span><span class="sxs-lookup"><span data-stu-id="bbda0-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="bbda0-129">Se il buffer viene allocato correttamente, è necessario spostare il puntatore mobile nell'intestazione del buffer, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="bbda0-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="bbda0-130">Riempimento del buffer di ritardo con silenziosità</span><span class="sxs-lookup"><span data-stu-id="bbda0-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="bbda0-131">È opportuno scrivere un metodo per riempire il buffer di ritardo con i valori che rappresentano il silenzio.</span><span class="sxs-lookup"><span data-stu-id="bbda0-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="bbda0-132">Il metodo deve ricevere il puntatore alla struttura WAVEFORMATEX valida e quindi ispezionare il membro wBitsPerSample per determinare se l'audio è a 8 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="bbda0-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="bbda0-133">Nell'esempio seguente viene compilato il buffer di ritardo con il valore corretto per il silenzio:</span><span class="sxs-lookup"><span data-stu-id="bbda0-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="bbda0-134">Ricordarsi di aggiungere la dichiarazione in diretta per la funzione al file di intestazione Echo. h nella sezione privata:</span><span class="sxs-lookup"><span data-stu-id="bbda0-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="bbda0-135">È necessario aggiungere il codice alla fine di AllocateStreamingResources per chiamare questo metodo ogni volta che il buffer di ritardo viene creato o ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="bbda0-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="bbda0-136">Il codice di esempio seguente passa il puntatore WAVEFORMATEX denominato pWave al nuovo metodo:</span><span class="sxs-lookup"><span data-stu-id="bbda0-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="bbda0-137">Riallocazione della memoria del buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="bbda0-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="bbda0-138">Quando l'utente modifica il tempo di ritardo utilizzando la pagina delle proprietà, è necessario modificare anche la dimensione del buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="bbda0-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="bbda0-139">Il codice è già stato aggiunto a AllocateStreamingResources per ridimensionare il buffer, ma è necessario aggiungere una riga di codice a CEcho::p \_ intervallo di tempo ut per chiamare il metodo di allocazione delle risorse ogni volta che il valore della proprietà cambia.</span><span class="sxs-lookup"><span data-stu-id="bbda0-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="bbda0-140">Il codice è il seguente:</span><span class="sxs-lookup"><span data-stu-id="bbda0-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="bbda0-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbda0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbda0-142">**Uso delle risorse di streaming**</span><span class="sxs-lookup"><span data-stu-id="bbda0-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




