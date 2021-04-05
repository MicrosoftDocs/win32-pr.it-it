---
title: Flusso di controllo
description: Flusso di controllo
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- Visualizzazioni, flusso di programma
- Visualizzazioni personalizzate, flusso di programma
- Visualizzazioni, flusso di controllo
- Visualizzazioni personalizzate, flusso di controllo
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Visualizzazioni, funzione RenderWindow
- Visualizzazioni personalizzate, funzione RenderWindow
- Funzione render, flusso del programma di visualizzazione
- RenderWindow (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955230"
---
# <a name="flow-of-control"></a><span data-ttu-id="6cf18-115">Flusso di controllo</span><span class="sxs-lookup"><span data-stu-id="6cf18-115">Flow of Control</span></span>

<span data-ttu-id="6cf18-116">I dati audio entrano in Windows Media Player continuamente tramite un file o un flusso.</span><span class="sxs-lookup"><span data-stu-id="6cf18-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="6cf18-117">I dati vengono passati alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6cf18-117">That data is passed to your visualization.</span></span> <span data-ttu-id="6cf18-118">Viene disegnato su una superficie definita e viene ripassata la superficie a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6cf18-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="6cf18-119">Questo interscambio si verifica più volte al secondo e, per l'utente, il risultato è un'animazione piacevole che si sposta nel tempo per la musica.</span><span class="sxs-lookup"><span data-stu-id="6cf18-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="6cf18-120">Di seguito è illustrata la sequenza specifica del flusso del programma di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="6cf18-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="6cf18-121">A un intervallo di tempo, Windows Media Player acquisisce uno snapshot dell'audio che sta eseguendo.</span><span class="sxs-lookup"><span data-stu-id="6cf18-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="6cf18-122">Windows Media Player fornisce i dati dallo snapshot alla visualizzazione tramite la funzione **Render** e la funzione **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="6cf18-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="6cf18-123">È necessario scrivere codice che verrà eseguito quando viene chiamato **il metodo Render** e **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="6cf18-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="6cf18-124">Il codice viene disegnato usando un contesto di dispositivo definito da Windows Media Player quando viene eseguito il rendering senza finestra o usando una finestra creata durante il rendering con finestra.</span><span class="sxs-lookup"><span data-stu-id="6cf18-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="6cf18-125">In un'area specificata dall'interfaccia corrente, Windows Media Player Visualizza il codice disegnato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6cf18-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="6cf18-126">Questo processo si ripete più volte al secondo, creando animazioni grafiche temporizzate per la musica.</span><span class="sxs-lookup"><span data-stu-id="6cf18-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="6cf18-127">Quando la musica smette di suonare, la visualizzazione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="6cf18-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cf18-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cf18-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf18-129">**Panoramica degli sviluppatori**</span><span class="sxs-lookup"><span data-stu-id="6cf18-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




