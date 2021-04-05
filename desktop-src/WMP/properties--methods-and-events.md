---
title: Proprietà, metodi ed eventi
description: Proprietà, metodi ed eventi
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Media Player di Windows, proprietà del modello a oggetti
- Windows Media Player, metodi per il modello a oggetti
- Windows Media Player, eventi per il modello a oggetti
- Windows Media Player modello a oggetti, proprietà
- Modello a oggetti di Windows Media Player, metodi
- Modello a oggetti di Windows Media Player, eventi
- modello a oggetti, proprietà
- modello a oggetti, metodi
- modello a oggetti, eventi
- Controllo ActiveX di Windows Media Player, proprietà per il modello a oggetti
- Controllo ActiveX, proprietà per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, proprietà per il modello a oggetti
- Windows Media Player Mobile, proprietà del modello a oggetti
- Controllo ActiveX di Windows Media Player, metodi per il modello a oggetti
- Controllo ActiveX, metodi per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, metodi per il modello a oggetti
- Windows Media Player Mobile, metodi per il modello a oggetti
- Controllo ActiveX di Windows Media Player, eventi per il modello a oggetti
- Controllo ActiveX, eventi per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, eventi per il modello a oggetti
- Windows Media Player Mobile, eventi per il modello a oggetti
- Proprietà, modello a oggetti di Windows Media Player
- metodi, modello a oggetti di Windows Media Player
- eventi, modello a oggetti di Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116845"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="ce143-127">Proprietà, metodi ed eventi</span><span class="sxs-lookup"><span data-stu-id="ce143-127">Properties, Methods and Events</span></span>

<span data-ttu-id="ce143-128">Ogni oggetto dispone di metodi e proprietà tramite i quali è possibile programmare il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce143-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="ce143-129">Un metodo è un'azione che può essere eseguita dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ce143-129">A method is an action that the object can take.</span></span> <span data-ttu-id="ce143-130">Una proprietà è un valore di dati che è possibile leggere o modificare.</span><span class="sxs-lookup"><span data-stu-id="ce143-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="ce143-131">Ad esempio, il metodo **Play** avvia la riproduzione del contenuto e la proprietà **framerate** indica la frequenza dei fotogrammi corrente del contenuto che viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="ce143-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="ce143-132">Inoltre, l'oggetto **Player** genera eventi che offrono la possibilità di eseguire azioni in momenti specifici.</span><span class="sxs-lookup"><span data-stu-id="ce143-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="ce143-133">È possibile scrivere codice in un gestore eventi che verrà eseguito quando Windows Media Player genera l'evento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ce143-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="ce143-134">Ad esempio, è possibile scrivere il codice in un gestore eventi **PlayStateChange** che determina se la modifica dello stato è che i supporti sono terminati e in tal caso viene visualizzata una finestra di dialogo in cui viene chiesto agli utenti se desiderano riprodurre nuovamente i supporti.</span><span class="sxs-lookup"><span data-stu-id="ce143-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="ce143-135">Tutti i metodi del modello a oggetti di Windows Media Player sono asincroni.</span><span class="sxs-lookup"><span data-stu-id="ce143-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="ce143-136">Se si chiamano due metodi nella stessa procedura, il secondo metodo non può basarsi sul primo metodo che ha completato l'azione.</span><span class="sxs-lookup"><span data-stu-id="ce143-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ce143-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce143-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce143-138">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="ce143-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




