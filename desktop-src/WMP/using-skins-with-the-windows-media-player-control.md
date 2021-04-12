---
title: Uso di interfacce con il controllo Media Player di Windows
description: Uso di interfacce con il controllo Media Player di Windows
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
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
- Controllo ActiveX di Windows Media Player, interfacce
- Controllo ActiveX Windows Media Player Mobile, interfacce
- Controllo ActiveX, interfacce
- interfacce, incorporamento del controllo ActiveX
- Windows Media Player Skin, incorporamento del controllo ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221467"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="7ebfb-124">Uso di interfacce con il controllo Media Player di Windows</span><span class="sxs-lookup"><span data-stu-id="7ebfb-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="7ebfb-125">Quando si incorpora il controllo Media Player di Windows in un programma C++, è possibile personalizzare l'interfaccia utente del lettore applicando un file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="7ebfb-126">Un file di definizione dell'interfaccia è un documento basato su XML che specifica il layout dei componenti dell'interfaccia utente standard e personalizzabili e di qualsiasi grafica associata.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="7ebfb-127">Utilizzando Microsoft JScript, è possibile specificare il comportamento di questi componenti e modificare il controllo Media Player Windows senza l'overhead della sintassi C++ e COM.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="7ebfb-128">Le interfacce forniscono un modo semplice per mantenere il codice dell'interfaccia utente e il codice del programma principale separatamente, in modo che possano essere mantenuti e sviluppati in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="7ebfb-129">È anche possibile riutilizzare le interfacce originariamente progettate per l'uso da parte del lettore autonomo in modalità Skin.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="7ebfb-130">Il codice di interfaccia progettato in modo specifico per i programmi C++ può interagire con i programmi tramite un oggetto che può essere fornito dal programma tramite script.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="7ebfb-131">Per abilitare la modalità Skin per il controllo Media Player di Windows, è necessario che il programma implementi l'interfaccia **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="7ebfb-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="7ebfb-132">Sebbene sia possibile usare le interfacce con il controllo e il controllo in remoto contemporaneamente, è possibile usare questa interfaccia per abilitare le funzionalità senza abilitare l'altra.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="7ebfb-133">Per disabilitare la comunicazione remota, è sufficiente passare un valore di "local" come parametro out del metodo **GetServiceType** e restituire un valore HRESULT di e \_ NOTIMPL dal metodo **getApplicationName** .</span><span class="sxs-lookup"><span data-stu-id="7ebfb-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="7ebfb-134">Per passare il controllo Media Player di Windows alla modalità interfaccia personalizzata, chiamare il metodo **IWMPPlayer::p UT \_ uiMode** , passando il valore "Custom".</span><span class="sxs-lookup"><span data-stu-id="7ebfb-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="7ebfb-135">Specificare il percorso e il nome file del file di definizione Skin da usare restituendo il percorso dal metodo **IWMPRemoteMediaServices:: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="7ebfb-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="7ebfb-136">Se si vuole fornire un oggetto tramite script per la comunicazione tra l'interfaccia utente e il programma, passare un nome e un puntatore a un puntatore **IDispatch** come due parametri out del metodo **IWMPRemoteMediaServices:: GetScriptableObject** .</span><span class="sxs-lookup"><span data-stu-id="7ebfb-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="7ebfb-137">L'interfaccia può quindi effettuare chiamate all'oggetto gestibile tramite script usando il nome specificato come se fosse un attributo globale simile all'attributo globale **Player** .</span><span class="sxs-lookup"><span data-stu-id="7ebfb-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="7ebfb-138">Un'interfaccia applicata a un controllo Media Player Windows remoto può accedere all'oggetto **PlayerApplication** usando un altro attributo globale denominato **PlayerApplication**.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="7ebfb-139">Poiché non è possibile accedere alla proprietà **Player. playerApplication** tramite interfacce, è necessario usare questo attributo globale quando si vuole che il codice dell'interfaccia utente gestisca l'ancoraggio e la disancoraggio.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="7ebfb-140">Esempi</span><span class="sxs-lookup"><span data-stu-id="7ebfb-140">Samples</span></span>

<span data-ttu-id="7ebfb-141">Il pacchetto di installazione di Windows Media Player SDK installa un esempio che illustra l'applicazione di un'interfaccia al controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="7ebfb-142">Per ulteriori informazioni, vedere l'esempio RemoteSkin.</span><span class="sxs-lookup"><span data-stu-id="7ebfb-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ebfb-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ebfb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ebfb-144">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="7ebfb-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="7ebfb-145">**Uso del controllo Media Player di Windows in un programma C++**</span><span class="sxs-lookup"><span data-stu-id="7ebfb-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




