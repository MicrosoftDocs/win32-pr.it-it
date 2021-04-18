---
title: Funzionamento del campione Echo
description: Funzionamento del campione Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Plug-in di Windows Media Player, panoramica dell'esempio Echo
- plug-in, Panoramica di esempio Echo
- plug-in di elaborazione dei segnali digitali, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298351"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="a6fc7-108">Funzionamento del campione Echo</span><span class="sxs-lookup"><span data-stu-id="a6fc7-108">How the Echo Sample Works</span></span>

<span data-ttu-id="a6fc7-109">Il codice crea l'effetto Echo allocando un buffer sufficientemente grande da contenere esattamente la quantità di dati audio di cui è possibile eseguire il rendering nell'intervallo di tempo specificato dal valore di tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="a6fc7-110">La dimensione del buffer viene calcolata in byte dalla formula seguente:</span><span class="sxs-lookup"><span data-stu-id="a6fc7-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="a6fc7-111">dimensioni del buffer = frequenza di campionamento del tempo di attesa \* / \* allineamento del blocco 1000</span><span class="sxs-lookup"><span data-stu-id="a6fc7-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="a6fc7-112">Il tempo di ritardo è in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="a6fc7-113">I valori di frequenza di campionamento e allineamento blocchi sono forniti in una struttura WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="a6fc7-114">La frequenza di campionamento è in campioni al secondo; la divisione per 1000 restituisce campioni per millisecondo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="a6fc7-115">L'allineamento a blocchi è uguale al prodotto del numero di canali (1 per mono, 2 per stereo) e al numero di bit per campione (8 o 16) diviso per 8 (bit per byte).</span><span class="sxs-lookup"><span data-stu-id="a6fc7-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="a6fc7-116">Oltre alla variabile puntatore che punta all'inizio del buffer di ritardo, il codice crea un puntatore mobile che scorre i dati nel buffer in sincronizzazione con il ciclo di elaborazione nella funzione **DoProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="a6fc7-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="a6fc7-117">Quando il puntatore mobile raggiunge la fine del buffer di ritardo, viene spostato di nuovo all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="a6fc7-118">Un buffer utilizzato in questo modo è denominato buffer circolare.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="a6fc7-119">Una volta che il buffer di ritardo esiste e Windows Media Player ha allocato un buffer di input per fornire dati audio e un buffer di output per la ricezione di dati audio elaborati, l'elaborazione ECHO procede come segue:</span><span class="sxs-lookup"><span data-stu-id="a6fc7-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="a6fc7-120">Immettere un ciclo che consente l'elaborazione di ogni esempio audio nel buffer di input.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="a6fc7-121">Recuperare un campione dal buffer di input.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="a6fc7-122">Spostare quindi il puntatore del buffer di input in avanti nell'esempio successivo per prepararsi alla successiva iterazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="a6fc7-123">Recuperare un campione dal buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="a6fc7-124">Copiare l'esempio dal buffer di input nella stessa posizione del buffer di ritardo dal quale è stato recuperato l'ultimo campione di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="a6fc7-125">Spostare il puntatore del buffer di ritardo in avanti nell'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="a6fc7-126">Se il puntatore viene spostato oltre la fine del buffer, spostarlo all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="a6fc7-127">Combinare l'esempio dal buffer di input con l'esempio dal buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="a6fc7-128">Copiare il risultato nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="a6fc7-129">Spostare quindi il puntatore del buffer di output all'unità successiva per prepararsi alla successiva iterazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="a6fc7-130">Ripetere l'elaborazione fino a quando non vengono elaborati tutti gli esempi.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="a6fc7-131">Quando un esempio di input recuperato nel passaggio 2 viene copiato nel buffer di ritardo nel passaggio 4, rimane disponibile fino a quando il puntatore mobile passa attraverso ogni campione nel buffer di ritardo e infine torna alla stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="a6fc7-132">Poiché la dimensione del buffer di ritardo è progettata per corrispondere al ritardo, il tempo trascorso tra l'esempio copiato nel buffer di ritardo e l'esempio recuperato ancora una volta equivale al ritardo specificato (più qualsiasi latenza introdotta dall'elaborazione effettiva).</span><span class="sxs-lookup"><span data-stu-id="a6fc7-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="a6fc7-133">Quando viene avviato un flusso, non vengono generati dati di ritardo fino a quando non è trascorso il tempo di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="a6fc7-134">Pertanto, è importante che il buffer di ritardo includa inizialmente il silenzio.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="a6fc7-135">Se il buffer di ritardo contiene dati casuali, l'utente riceverà un rumore bianco fino a quando il plug-in genera un numero sufficiente di dati di ritardo per sovrascrivere l'intero buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="a6fc7-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6fc7-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6fc7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6fc7-137">**Panoramica dell'esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="a6fc7-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




