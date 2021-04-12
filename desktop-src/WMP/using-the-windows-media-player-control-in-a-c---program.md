---
title: Uso del controllo Media Player di Windows in un programma C++
description: Uso del controllo Media Player di Windows in un programma C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, C++
- Modello a oggetti di Windows Media Player, C++
- modello a oggetti, C++
- Windows Media Player Mobile, C++
- Controllo ActiveX di Windows Media Player, C++
- Controllo ActiveX Windows Media Player Mobile, C++
- Controllo ActiveX, C++
- Incorporamento del programma C++
- incorporamento, programmi C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221729"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="8159d-119">Uso del controllo Media Player di Windows in un programma C++</span><span class="sxs-lookup"><span data-stu-id="8159d-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="8159d-120">L'uso di C++ per incorporare il controllo Media Player Windows è supportato per la serie Windows Media Player 9 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8159d-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="8159d-121">Esistono diversi modi per usare il controllo Windows Media Player in un programma C++.</span><span class="sxs-lookup"><span data-stu-id="8159d-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="8159d-122">È possibile creare un'istanza del controllo in un'applicazione console oppure incorporare il controllo in un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="8159d-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="8159d-123">Inoltre, è possibile implementare interfacce che consentono di eseguire un controllo Player incorporato in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="8159d-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="8159d-124">È possibile personalizzare l'interfaccia utente di un controllo incorporato applicando un file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8159d-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="8159d-125">Queste informazioni sono descritte negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="8159d-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="8159d-126">Argomento</span><span class="sxs-lookup"><span data-stu-id="8159d-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="8159d-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8159d-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8159d-128">Uso del controllo Media Player Windows in un'applicazione console</span><span class="sxs-lookup"><span data-stu-id="8159d-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="8159d-129">Descrive una semplice applicazione console C++ che crea un'istanza del controllo Media Player Windows per visualizzare la versione.</span><span class="sxs-lookup"><span data-stu-id="8159d-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="8159d-130">Hosting del controllo Media Player Windows in un'applicazione Windows</span><span class="sxs-lookup"><span data-stu-id="8159d-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="8159d-131">Viene descritto come utilizzare la finestra host ActiveX ATL per incorporare il controllo Media Player di Windows in un programma Windows.</span><span class="sxs-lookup"><span data-stu-id="8159d-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="8159d-132">Gestione remota del controllo di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="8159d-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="8159d-133">Viene descritto come incorporare il controllo Windows Media Player in un programma C++ in modalità remota, che consente agli utenti di disancorare il controllo per passare alla modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="8159d-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="8159d-134">Gestione degli eventi in C++</span><span class="sxs-lookup"><span data-stu-id="8159d-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="8159d-135">Viene descritto come ricevere notifiche di eventi da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8159d-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="8159d-136">Uso di interfacce con il controllo Media Player di Windows</span><span class="sxs-lookup"><span data-stu-id="8159d-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="8159d-137">Viene descritto come applicare un file di interfaccia a un controllo di Windows Media Player incorporato in un programma C++.</span><span class="sxs-lookup"><span data-stu-id="8159d-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="8159d-138">È possibile incorporare il controllo Windows Media Player 10 mobile in un'applicazione Windows CE.</span><span class="sxs-lookup"><span data-stu-id="8159d-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="8159d-139">Le tecniche usate per eseguire questa operazione sono simili a quelle usate con il controllo desktop di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8159d-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="8159d-140">Esistono tuttavia differenze tra ATL per Windows e ATL per Windows CE.</span><span class="sxs-lookup"><span data-stu-id="8159d-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="8159d-141">Questa documentazione descrive le differenze tra queste implementazioni, laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="8159d-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8159d-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8159d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8159d-143">**Riferimento del modello a oggetti per C++**</span><span class="sxs-lookup"><span data-stu-id="8159d-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="8159d-144">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="8159d-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




