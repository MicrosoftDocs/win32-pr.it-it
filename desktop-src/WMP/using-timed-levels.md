---
title: Utilizzo di livelli temporizzati
description: Utilizzo di livelli temporizzati
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, matrice di frequenza
- Visualizzazioni personalizzate, matrice di frequenza
- Visualizzazioni, matrice di forme d'onda
- Visualizzazioni personalizzate, matrice di forme d'onda
- Visualizzazioni, variabile di stato
- Visualizzazioni personalizzate, variabile di stato
- Visualizzazioni, variabile timeStamp
- Visualizzazioni personalizzate, variabile timeStamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044739"
---
# <a name="using-timed-levels"></a><span data-ttu-id="8233f-113">Utilizzo di livelli temporizzati</span><span class="sxs-lookup"><span data-stu-id="8233f-113">Using Timed Levels</span></span>

<span data-ttu-id="8233f-114">La struttura **TimedLevel** è costituita da matrici 2 2-dimensionali, da un valore di stato e da un valore di timestamp.</span><span class="sxs-lookup"><span data-stu-id="8233f-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="8233f-115">Matrice di frequenza</span><span class="sxs-lookup"><span data-stu-id="8233f-115">Frequency Array</span></span>

<span data-ttu-id="8233f-116">La matrice di frequenze è una matrice bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="8233f-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="8233f-117">La prima dimensione di ogni matrice corrisponde al canale audio stereo (a sinistra o a destra) e il secondo corrisponde ai livelli di frequenza (in byte) dello snapshot, in cui lo spettro audio è diviso in 1024 aree.</span><span class="sxs-lookup"><span data-stu-id="8233f-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="8233f-118">È possibile ottenere i dati della matrice di frequenza forniti dal Media Player Windows nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8233f-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="8233f-119">Il valore dello snapshot è per il canale sinistro e contiene il valore della parte più bassa dello spettro di frequenza.</span><span class="sxs-lookup"><span data-stu-id="8233f-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="8233f-120">Se, ad esempio, lo snapshot ha un valore elevato, significa che la parte 1024th più bassa dello spettro di frequenza è ricca di frequenza.</span><span class="sxs-lookup"><span data-stu-id="8233f-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="8233f-121">Un valore pari a zero indica che non sono presenti valori a bassa frequenza in tale parte dello spettro per il canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="8233f-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="8233f-122">Se si dispone di un segnale monofonico, solo la prima dimensione ha valori validi.</span><span class="sxs-lookup"><span data-stu-id="8233f-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="8233f-123">Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono.</span><span class="sxs-lookup"><span data-stu-id="8233f-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="8233f-124">Ovvero la frequenza \[ 0 \] \[ *n* \] e la frequenza \[ 1 n conterranno \] \[  \] gli stessi dati, dove *n* è l'indice in una cella particolare.</span><span class="sxs-lookup"><span data-stu-id="8233f-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="8233f-125">Matrice di forme d'onda</span><span class="sxs-lookup"><span data-stu-id="8233f-125">Waveform Array</span></span>

<span data-ttu-id="8233f-126">Anche la matrice di forme d'onda è una matrice bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="8233f-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="8233f-127">La prima dimensione della matrice corrisponde al canale (a sinistra o a destra) e il secondo corrisponde ai livelli di risparmio energia (in byte) dello snapshot, in cui la potenza audio viene suddivisa in 1024 segmenti di tempo contigui.</span><span class="sxs-lookup"><span data-stu-id="8233f-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="8233f-128">È possibile ottenere i dati della matrice di forme d'onda da Windows Media Player nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="8233f-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="8233f-129">Il valore dello snapshot è per il canale sinistro e contiene il primo valore dello snapshot quantizzato dei valori di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="8233f-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="8233f-130">Quando viene eseguito uno snapshot, è costituito da 1024 misure incrementali minime della potenza audio.</span><span class="sxs-lookup"><span data-stu-id="8233f-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="8233f-131">Il valore più basso della matrice viene generato dalla prima misurazione incrementale della potenza audio.</span><span class="sxs-lookup"><span data-stu-id="8233f-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="8233f-132">Si noti che i valori della potenza sono misurati da-128 a + 127, ma i valori nella matrice variano da 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="8233f-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="8233f-133">Se si dispone di un'onda monofonica, solo la prima dimensione avrà valori validi.</span><span class="sxs-lookup"><span data-stu-id="8233f-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="8233f-134">Se il segnale non è stereo, la seconda matrice conterrà una copia del segnale mono.</span><span class="sxs-lookup"><span data-stu-id="8233f-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="8233f-135">Ovvero, la forma \[ d'onda 0 \] \[ *n* \] e la forma \[ d'onda 1 n conterranno \] \[  \] gli stessi dati, dove *n* è l'indice in una cella particolare.</span><span class="sxs-lookup"><span data-stu-id="8233f-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="8233f-136">State</span><span class="sxs-lookup"><span data-stu-id="8233f-136">State</span></span>

<span data-ttu-id="8233f-137">La variabile di stato riflette lo stato di riproduzione audio di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8233f-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="8233f-138">I valori di enumerazione PlayerState sono</span><span class="sxs-lookup"><span data-stu-id="8233f-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="8233f-139">È possibile usare questa variabile per eseguire azioni diverse a seconda dello stato di riproduzione audio.</span><span class="sxs-lookup"><span data-stu-id="8233f-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="8233f-140">Ad esempio, è possibile riprodurre un tipo di visualizzazione quando l'audio viene riprodotto e un altro quando viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="8233f-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="8233f-141">Timestamp</span><span class="sxs-lookup"><span data-stu-id="8233f-141">Time Stamp</span></span>

<span data-ttu-id="8233f-142">La variabile timeStamp riflette l'ora corrente in cui viene eseguita la snapshot.</span><span class="sxs-lookup"><span data-stu-id="8233f-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="8233f-143">Questa operazione può essere usata per misurare la frequenza con cui vengono effettuati gli snapshot.</span><span class="sxs-lookup"><span data-stu-id="8233f-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="8233f-144">È possibile usare questa variabile per ora le animazioni.</span><span class="sxs-lookup"><span data-stu-id="8233f-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="8233f-145">Se gli snapshot sono troppo frequenti, è possibile ridurre normalmente l'immagine per visualizzarla nel modo scelto.</span><span class="sxs-lookup"><span data-stu-id="8233f-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8233f-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8233f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8233f-147">**Implementazione di rendering**</span><span class="sxs-lookup"><span data-stu-id="8233f-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




