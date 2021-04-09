---
title: Incorporamento del controllo Media Player Windows in un programma personalizzato
description: Incorporamento del controllo Media Player Windows in un programma personalizzato
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- incorporamento, programmi personalizzati
- incorporamento di programmi personalizzati
- incorporamento, programmi basati su Visual Basic
- Incorporamento di programmi basati su Visual Basic
- incorporamento, utilizzo manuale di metodi COM
- incorporamento manuale mediante i metodi COM
- incorporamento, programmi C++
- Incorporamento del programma C++
- incorporamento, programmi di Visual Studio
- Visual Studio, incorporamento del programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044490"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="89d89-120">Incorporamento del controllo Media Player Windows in un programma personalizzato</span><span class="sxs-lookup"><span data-stu-id="89d89-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="89d89-121">Poiché il controllo ActiveX di Windows Media Player è basato sulla tecnologia Microsoft Component Object Model (COM), è possibile incorporarlo nei programmi scritti con molti linguaggi di programmazione diversi.</span><span class="sxs-lookup"><span data-stu-id="89d89-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="89d89-122">Il controllo Windows Media Player rappresenta un modo semplice per aggiungere sofisticate funzionalità multimediali digitali a qualsiasi programma.</span><span class="sxs-lookup"><span data-stu-id="89d89-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="89d89-123">In Microsoft Visual Basic è possibile aggiungere il controllo alla casella degli strumenti del controllo, inserirlo in un form e modificare le proprietà del controllo nella finestra Proprietà.</span><span class="sxs-lookup"><span data-stu-id="89d89-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="89d89-124">Se si vuole un'interfaccia utente personalizzata, è possibile inserire i pulsanti di comando nel form e aggiungere il codice che gestisce il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="89d89-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="89d89-125">Incorporare il controllo in un programma basato su Visual Basic è molto simile all'incorporamento in un documento di Office e alla programmazione con VBA.</span><span class="sxs-lookup"><span data-stu-id="89d89-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="89d89-126">In alternativa, è possibile incorporare il controllo manualmente usando i metodi COM per creare un'istanza del controllo e accedere alle interfacce COM documentate in [riferimento al modello a oggetti per C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="89d89-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="89d89-127">Quando si incorpora il controllo Windows Media Player in un programma C++, è possibile implementare interfacce COM che consentono di eseguire il controllo in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="89d89-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="89d89-128">Ciò significa che il controllo incorporato condivide lo stesso motore di riproduzione della modalità completa del lettore e gli utenti possono spostarsi tra la modalità completa e lo stato ancorato senza interrompere la riproduzione di file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="89d89-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="89d89-129">È anche possibile controllare ciò che viene visualizzato nei vari riquadri del lettore in modalità completa quando gli utenti passano allo stato non ancorato.</span><span class="sxs-lookup"><span data-stu-id="89d89-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="89d89-130">Con l'incorporamento C++, è anche possibile applicare un file di definizione dell'interfaccia per il controllo Player incorporato.</span><span class="sxs-lookup"><span data-stu-id="89d89-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="89d89-131">Si tratta di un modo semplice per creare codice di interfaccia utente leggero che è possibile gestire separatamente dal codice del programma principale.</span><span class="sxs-lookup"><span data-stu-id="89d89-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="89d89-132">Microsoft Visual Studio supporta l'incorporamento di controlli ActiveX, incluso il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="89d89-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="89d89-133">Quando si sceglie di eseguire questa operazione, Visual Studio crea un nuovo assembly di interoperabilità alternativo per gestire l'interoperabilità tra il .NET Framework e il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="89d89-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="89d89-134">Visual Studio usa lo strumento tlbimp.exe .NET Framework per creare l'assembly di interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="89d89-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="89d89-135">Ciò significa che le firme visualizzate quando si usa la funzionalità IntelliSense in Visual Studio usano la semantica determinata dalla versione corrente di Tlbimp.</span><span class="sxs-lookup"><span data-stu-id="89d89-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d89-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89d89-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d89-137">**Incorporamento del controllo Media Player Windows**</span><span class="sxs-lookup"><span data-stu-id="89d89-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="89d89-138">**Uso del controllo Media Player di Windows in un programma C++**</span><span class="sxs-lookup"><span data-stu-id="89d89-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="89d89-139">**Uso del controllo Media Player di Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="89d89-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="89d89-140">**Uso del controllo Media Player di Windows con Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="89d89-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




