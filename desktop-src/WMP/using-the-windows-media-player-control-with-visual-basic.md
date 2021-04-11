---
title: Uso del controllo Media Player di Windows con Visual Basic
description: Uso del controllo Media Player di Windows con Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, Visual Basic
- Modello a oggetti di Windows Media Player, Visual Basic
- modello a oggetti, Visual Basic
- Windows Media Player Mobile Visual Basic
- Controllo ActiveX di Windows Media Player, Visual Basic
- Controllo ActiveX Windows Media Player Mobile Visual Basic
- Controllo ActiveX, Visual Basic
- Incorporamento di programmi basati su Visual Basic
- incorporamento, programmi basati su Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330836"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="5a28c-119">Uso del controllo Media Player di Windows con Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5a28c-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="5a28c-120">In questa sezione viene descritto come utilizzare il controllo ActiveX Windows Media Player 9 o versioni successive nelle applicazioni create con Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="5a28c-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="5a28c-121">Introduzione</span><span class="sxs-lookup"><span data-stu-id="5a28c-121">Getting Started</span></span>

<span data-ttu-id="5a28c-122">Per aggiungere il controllo Media Player Windows alla casella degli strumenti, selezionare innanzitutto **componenti** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="5a28c-123">Nella finestra di dialogo componenti selezionare la casella di controllo accanto a "Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="5a28c-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="5a28c-124">Nella parte inferiore della finestra di dialogo verificare che il file selezionato sia wmp.dll.</span><span class="sxs-lookup"><span data-stu-id="5a28c-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="5a28c-125">Dopo aver chiuso la finestra di dialogo, è possibile inserire un'istanza del controllo Media Player Windows sul form nel modo consueto.</span><span class="sxs-lookup"><span data-stu-id="5a28c-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="5a28c-126">È possibile impostare molte proprietà del controllo usando il Finestra Proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a28c-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="5a28c-127">Per impostare alcune proprietà, è necessario utilizzare la finestra di dialogo Proprietà Media Player di Windows, che è possibile aprire utilizzando l'elemento "(personalizzato)" nel Finestra Proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a28c-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="5a28c-128">Riferimenti a oggetti</span><span class="sxs-lookup"><span data-stu-id="5a28c-128">Object References</span></span>

<span data-ttu-id="5a28c-129">È possibile utilizzare determinate proprietà del controllo lettore per ottenere riferimenti a oggetti specifici.</span><span class="sxs-lookup"><span data-stu-id="5a28c-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="5a28c-130">Ad esempio, la proprietà **cdromcollection** restituisce un riferimento a un oggetto **cdromcollection** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="5a28c-131">È necessario assegnare tale riferimento a una variabile dichiarata come interfaccia corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5a28c-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="5a28c-132">Nel caso della proprietà **cdromcollection** , ad esempio, si assegna il relativo valore restituito a una variabile di tipo **IWMPCdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="5a28c-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="5a28c-133">Leggere l'argomento [interfacce](interfaces.md) nel [riferimento del modello a oggetti per C++](object-model-reference-for-c.md) per identificare gli oggetti che implementano più interfacce.</span><span class="sxs-lookup"><span data-stu-id="5a28c-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="5a28c-134">In questi casi, è necessario dichiarare una variabile oggetto come l'interfaccia con il numero più elevato documentato in questo SDK per avere accesso a tutte le proprietà e i metodi di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a28c-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="5a28c-135">Ad esempio, è necessario assegnare il valore della proprietà **currentMedia** del controllo Windows Media Player a una variabile dichiarata come **IWMPMedia3** per assicurarsi di avere accesso ai metodi **getAttributeCountByType** e **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="5a28c-136">L'oggetto **windowsmediaplayer** implementa tutte le proprietà e i metodi delle interfacce **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** e **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="5a28c-137">Non è necessario dichiarare variabili separate per nessuna di queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="5a28c-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="5a28c-138">È possibile accedere a tutti i relativi membri usando il nome assegnato all'istanza di **windowsmediaplayer** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="5a28c-139">Nella Visual Basic Visualizzatore oggetti verranno visualizzate numerose interfacce destinate all'uso privato da parte del controllo Windows Media Player, incluse alcune che supportano gli sviluppatori di skin.</span><span class="sxs-lookup"><span data-stu-id="5a28c-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="5a28c-140">È consigliabile utilizzare solo gli oggetti, le proprietà, i metodi e gli eventi documentati in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="5a28c-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="5a28c-141">Suggerimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="5a28c-141">Additional Tips</span></span>

-   <span data-ttu-id="5a28c-142">Nella documentazione di riferimento viene illustrata la sintassi di JScript.</span><span class="sxs-lookup"><span data-stu-id="5a28c-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="5a28c-143">In JScript gli argomenti passati ai metodi sono sempre racchiusi tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="5a28c-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="5a28c-144">In Visual Basic 6,0 gli argomenti passati ai metodi che non restituiscono un valore non devono essere racchiusi tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="5a28c-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="5a28c-145">Alcune proprietà o metodi potrebbero non essere visualizzati nella funzionalità di completamento automatico del codice nell'editor di codice Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5a28c-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="5a28c-146">È comunque possibile usare tali membri digitando i relativi nomi esattamente come appaiono in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="5a28c-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="5a28c-147">Gestire l'aspetto visivo del controllo utilizzando la proprietà **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="5a28c-148">Questa operazione può essere eseguita in due modi.</span><span class="sxs-lookup"><span data-stu-id="5a28c-148">You can do so in two ways.</span></span> <span data-ttu-id="5a28c-149">È possibile utilizzare l'elenco a discesa **Seleziona modalità** nella finestra di dialogo Proprietà Media Player di Windows oppure è possibile digitare il valore corretto nel finestra Proprietà.</span><span class="sxs-lookup"><span data-stu-id="5a28c-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="5a28c-150">In particolare, non utilizzare la proprietà **Visible** per nascondere il controllo; Assegnare invece il valore "invisibile" alla proprietà **uiMode** .</span><span class="sxs-lookup"><span data-stu-id="5a28c-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a28c-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a28c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a28c-152">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="5a28c-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




