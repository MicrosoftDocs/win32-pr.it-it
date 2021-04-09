---
title: Creazione dell'effetto Echo
description: Creazione dell'effetto Echo
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, creazione dell'effetto Echo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044152"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="0df8a-109">Creazione dell'effetto Echo</span><span class="sxs-lookup"><span data-stu-id="0df8a-109">Creating the Echo Effect</span></span>

<span data-ttu-id="0df8a-110">È necessario innanzitutto rimuovere il codice dall'esempio della procedura guidata che consente di ridimensionare l'audio.</span><span class="sxs-lookup"><span data-stu-id="0df8a-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="0df8a-111">Dalla sezione a 8 bit rimuovere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="0df8a-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="0df8a-112">Tenere presente che m \_ fScaleFactor è stato sostituito da m \_ dwDelayTime.</span><span class="sxs-lookup"><span data-stu-id="0df8a-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="0df8a-113">Dalla sezione a 16 bit rimuovere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="0df8a-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="0df8a-114">L'implementazione di **DoProcessOutput** fornita dal codice di esempio della procedura guidata plug-in crea un ciclo while che esegue l'iterazione una volta per ogni campione nel buffer di input fornito da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0df8a-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="0df8a-115">Questo ciclo funziona allo stesso modo per l'audio a 8 bit e a 16 bit, anche se per ciascuna è necessario un ciclo separato.</span><span class="sxs-lookup"><span data-stu-id="0df8a-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="0df8a-116">In ogni caso, il ciclo inizia con il test seguente:</span><span class="sxs-lookup"><span data-stu-id="0df8a-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="0df8a-117">Una volta all'interno del ciclo, le routine di elaborazione sono molto simili per l'audio a 8 bit e a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0df8a-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="0df8a-118">La differenza principale consiste nel fatto che il codice nella sezione a 8 bit modifica l'intervallo di valori dei dati da-128 a 127, quindi converte di nuovo l'intervallo prima di scrivere i dati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="0df8a-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="0df8a-119">Questo è importante per mantenere la simmetria della forma d'onda audio durante l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="0df8a-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="0df8a-120">A questo punto è possibile iniziare ad aggiungere e sostituire il codice nel ciclo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="0df8a-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="0df8a-121">Recuperare un campione dal buffer di input</span><span class="sxs-lookup"><span data-stu-id="0df8a-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="0df8a-122">Durante ogni iterazione del ciclo, viene recuperato un singolo campione dal buffer di input.</span><span class="sxs-lookup"><span data-stu-id="0df8a-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="0df8a-123">Per l'audio a 8 bit, l'esempio viene spostato nel nuovo intervallo, quindi il puntatore al buffer di input è avanzato per l'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="0df8a-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="0df8a-124">Il codice seguente viene dalla procedura guidata plug-in:</span><span class="sxs-lookup"><span data-stu-id="0df8a-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="0df8a-125">Per l'audio a 16 bit, il processo è lo stesso ad eccezione della normalizzazione:</span><span class="sxs-lookup"><span data-stu-id="0df8a-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="0df8a-126">Tenere presente che i puntatori nel codice a 16 bit sono stati convertiti nel tipo **short**.</span><span class="sxs-lookup"><span data-stu-id="0df8a-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="0df8a-127">Recuperare un campione dal buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="0df8a-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="0df8a-128">Recuperare quindi un singolo campione dal buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="0df8a-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="0df8a-129">Per il codice a 8 bit, gli esempi di ritardo vengono archiviati nell'intervallo nativo compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="0df8a-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="0df8a-130">Il codice seguente, che è necessario aggiungere, recupera un esempio di ritardo a 8 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="0df8a-131">Per l'audio a 16 bit, il processo è simile:</span><span class="sxs-lookup"><span data-stu-id="0df8a-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="0df8a-132">Scrivere l'esempio di input nel buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="0df8a-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="0df8a-133">A questo punto, è necessario archiviare l'esempio di input nel buffer di ritardo nello stesso percorso da cui è stato recuperato l'esempio di ritardo.</span><span class="sxs-lookup"><span data-stu-id="0df8a-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="0df8a-134">Di seguito è riportato il codice che è necessario aggiungere per audio a 8 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="0df8a-135">Si tratta del codice da aggiungere per la sezione a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="0df8a-136">Spostare il puntatore del buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="0df8a-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="0df8a-137">Ora che il lavoro nel buffer di ritardo è terminato per questa iterazione, è possibile far avanzare il puntatore mobile al buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="0df8a-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="0df8a-138">Se il puntatore raggiunge la fine del buffer circolare, è necessario modificarne il valore in modo che punti all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="0df8a-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="0df8a-139">Per eseguire questa operazione per audio a 8 bit, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="0df8a-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="0df8a-140">Ecco il codice per la sezione a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="0df8a-141">Poiché il puntatore nella sezione a 16 bit è effettivamente una copia della variabile membro, è necessario ricordarsi di aggiornare il valore nella variabile membro con il nuovo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="0df8a-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="0df8a-142">Se non si riesce a eseguire questa operazione, il puntatore del buffer di ritardo punterà ripetutamente all'inizio del buffer e l'effetto Echo non funzionerà come previsto.</span><span class="sxs-lookup"><span data-stu-id="0df8a-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="0df8a-143">Aggiungere il codice seguente alla sezione a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="0df8a-144">Combinare l'esempio di input con l'esempio delay</span><span class="sxs-lookup"><span data-stu-id="0df8a-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="0df8a-145">Questa è la posizione in cui si usano i valori Wet Mix e dry mix per creare l'esempio di output finale.</span><span class="sxs-lookup"><span data-stu-id="0df8a-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="0df8a-146">È sufficiente moltiplicare ogni campione in base al valore a virgola mobile che rappresenta la percentuale del segnale finale per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0df8a-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="0df8a-147">Moltiplicare l'esempio di input in base al valore archiviato in m \_ fDryMix; moltiplicare l'esempio di ritardo in base al valore archiviato in m \_ fWetMix.</span><span class="sxs-lookup"><span data-stu-id="0df8a-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="0df8a-148">Quindi, aggiungere i due valori.</span><span class="sxs-lookup"><span data-stu-id="0df8a-148">Then, add the two values.</span></span> <span data-ttu-id="0df8a-149">Il codice che è necessario aggiungere è identico per le sezioni a 8 bit e a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="0df8a-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="0df8a-150">Scrivere i dati nel buffer di output</span><span class="sxs-lookup"><span data-stu-id="0df8a-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="0df8a-151">Infine, copiare l'esempio misto nel buffer di output, quindi spostare il puntatore del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="0df8a-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="0df8a-152">Per l'audio a 8 bit, la procedura guidata plug-in USA il codice seguente per restituire l'esempio nell'intervallo originale:</span><span class="sxs-lookup"><span data-stu-id="0df8a-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="0df8a-153">Per audio a 16 bit, la procedura guidata usa il codice seguente come passaggio finale del ciclo di elaborazione:</span><span class="sxs-lookup"><span data-stu-id="0df8a-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="0df8a-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0df8a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df8a-155">**Implementazione di CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="0df8a-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




