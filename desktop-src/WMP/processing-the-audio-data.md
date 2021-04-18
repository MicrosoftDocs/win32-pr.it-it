---
title: Elaborazione dei dati audio
description: Elaborazione dei dati audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, dati audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298555"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="c4b77-109">Elaborazione dei dati audio</span><span class="sxs-lookup"><span data-stu-id="c4b77-109">Processing the Audio Data</span></span>

<span data-ttu-id="c4b77-110">L'implementazione predefinita di **DoProcessOutput** inizia con il recupero di un puntatore a una struttura **WAVEFORMATEX** valida, esattamente come è stato fatto in **AllocateStreamingResources**.</span><span class="sxs-lookup"><span data-stu-id="c4b77-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="c4b77-111">USA quindi le informazioni contenute in tale struttura per calcolare il numero di campioni nel buffer di input in attesa di essere elaborati.</span><span class="sxs-lookup"><span data-stu-id="c4b77-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="c4b77-112">Il codice seguente viene dall'implementazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="c4b77-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="c4b77-113">Il codice esamina quindi il membro **wBitsPerSample** per determinare la profondità del bit dell'audio.</span><span class="sxs-lookup"><span data-stu-id="c4b77-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="c4b77-114">Questo valore viene utilizzato in un'istruzione switch per fornire un'elaborazione separata per audio a 8 bit e a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c4b77-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="c4b77-115">Differenze tra audio a 8 e 16 bit</span><span class="sxs-lookup"><span data-stu-id="c4b77-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="c4b77-116">Esistono differenze importanti tra audio a 8 e 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c4b77-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="c4b77-117">Pertanto, le routine di elaborazione per creare l'effetto Echo sono diverse.</span><span class="sxs-lookup"><span data-stu-id="c4b77-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="c4b77-118">I due formati sono diversi nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4b77-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="c4b77-119">Ogni formato ha dimensioni di campionamento diverse: gli esempi a 8 bit occupano un byte di memoria, mentre gli esempi a 16 bit occupano due byte.</span><span class="sxs-lookup"><span data-stu-id="c4b77-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="c4b77-120">Ogni formato rappresenta l'ampiezza audio in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="c4b77-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="c4b77-121">l'audio a 8 bit è rappresentato da un Unsigned Integer con un intervallo compreso tra 0 e 255; il valore 128 rappresenta il silenzio.</span><span class="sxs-lookup"><span data-stu-id="c4b77-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="c4b77-122">l'audio a 16 bit è rappresentato da un Signed Integer con un intervallo compreso tra-32768 e 32767; il valore zero rappresenta il silenzio.</span><span class="sxs-lookup"><span data-stu-id="c4b77-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="c4b77-123">Mentre il processo di creazione dell'effetto Echo è sostanzialmente identico per ogni formato, i dettagli devono essere leggermente diversi.</span><span class="sxs-lookup"><span data-stu-id="c4b77-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4b77-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4b77-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b77-125">**Implementazione di CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="c4b77-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




