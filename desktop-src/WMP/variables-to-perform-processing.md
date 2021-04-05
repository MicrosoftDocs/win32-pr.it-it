---
title: Variabili per l'esecuzione dell'elaborazione
description: Variabili per l'esecuzione dell'elaborazione
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, elaborazione di variabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711107"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="f95c1-109">Variabili per l'esecuzione dell'elaborazione</span><span class="sxs-lookup"><span data-stu-id="f95c1-109">Variables to Perform Processing</span></span>

<span data-ttu-id="f95c1-110">Le variabili membro per la gestione del buffer di ritardo occupano le quantità di **byte** ; si tratta di puntatori a **byte** e di un numero intero che archivia un conteggio di byte.</span><span class="sxs-lookup"><span data-stu-id="f95c1-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="f95c1-111">Questa soluzione è ideale per l'elaborazione di audio a 8 bit, perché un campione a 8 bit si adatta perfettamente a un byte di memoria.</span><span class="sxs-lookup"><span data-stu-id="f95c1-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="f95c1-112">Quando si elaborano audio a 16 bit, tuttavia, è più comodo convertirli in puntatori **brevi** , in modo che l'elaborazione possa essere eseguita due byte alla volta.</span><span class="sxs-lookup"><span data-stu-id="f95c1-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="f95c1-113">Il codice di esempio seguente alloca i nuovi puntatori a 16 bit e aggiunge una variabile puntatore che archivia l'indirizzo della fine del buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="f95c1-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="f95c1-114">Inserirlo nella sezione "Case 16" immediatamente prima del punto di ingresso del ciclo:</span><span class="sxs-lookup"><span data-stu-id="f95c1-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="f95c1-115">Il codice per l'elaborazione a 8 bit consente inoltre di allocare una variabile che archivia l'indirizzo della fine del buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="f95c1-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="f95c1-116">L'archiviazione di questo valore rende più semplice verificare se il puntatore del buffer dei ritardi mobili ha raggiunto la fine del buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="f95c1-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="f95c1-117">Il codice di esempio seguente calcola il valore:</span><span class="sxs-lookup"><span data-stu-id="f95c1-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="f95c1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f95c1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f95c1-119">**Implementazione di CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="f95c1-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




