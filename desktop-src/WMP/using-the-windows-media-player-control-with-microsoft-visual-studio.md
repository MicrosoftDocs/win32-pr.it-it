---
title: Uso del controllo Media Player di Windows con Microsoft Visual Studio
description: Uso del controllo Media Player di Windows con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, .NET Framework
- Modello a oggetti Media Player Windows, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Windows Media Player ActiveX Control, .NET Framework
- Controllo ActiveX Windows Media Player Mobile, .NET Framework
- Controllo ActiveX, .NET Framework
- Controllo ActiveX di Windows Media Player, Visual Studio
- Controllo ActiveX Windows Media Player Mobile, Visual Studio
- Controllo ActiveX, Visual Studio
- .NET Framework, incorporamento del programma Visual Studio
- incorporamento, programmi di Visual Studio
- Visual Studio, incorporamento del programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104045417"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="23e03-123">Uso del controllo Media Player di Windows con Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="23e03-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="23e03-124">È possibile aggiungere il controllo ActiveX Windows Media Player 9 o versioni successive a un'applicazione .NET Framework tramite la casella degli strumenti in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="23e03-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="23e03-125">Aggiunta del controllo Media Player di Windows</span><span class="sxs-lookup"><span data-stu-id="23e03-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="23e03-126">Prima di creare un nuovo progetto, assicurarsi che nel computer sia installata la versione più recente di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="23e03-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="23e03-127">Avviare Visual Studio e quindi creare un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="23e03-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="23e03-128">In Visual Studio aprire la casella degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="23e03-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="23e03-129">Se Windows Media Player non viene visualizzato nella parte relativa ai **componenti** della casella degli strumenti, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="23e03-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="23e03-130">Fare clic con il pulsante destro del mouse all'interno della casella degli strumenti e **scegliere Scegli elementi**.</span><span class="sxs-lookup"><span data-stu-id="23e03-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="23e03-131">Verrà visualizzata la finestra di dialogo **Personalizza casella degli strumenti** .</span><span class="sxs-lookup"><span data-stu-id="23e03-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="23e03-132">Nella scheda **componenti com** selezionare Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="23e03-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="23e03-133">Se Windows Media Player non viene visualizzato nell'elenco, fare clic su **Sfoglia**, quindi aprire Wmp.dll, che dovrebbe trovarsi nella \\ cartella system32 di Windows.</span><span class="sxs-lookup"><span data-stu-id="23e03-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="23e03-134">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="23e03-134">Click **OK**.</span></span> <span data-ttu-id="23e03-135">Il controllo Media Player Windows verrà inserito nella scheda della casella degli strumenti corrente.</span><span class="sxs-lookup"><span data-stu-id="23e03-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="23e03-136">È ora possibile selezionare Windows Media Player nella casella degli strumenti e aggiungerlo a un modulo.</span><span class="sxs-lookup"><span data-stu-id="23e03-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="23e03-137">Visual Studio fornisce al controllo Windows Media Player un nome predefinito, ad esempio "axWindowsMediaPlayer1".</span><span class="sxs-lookup"><span data-stu-id="23e03-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="23e03-138">È possibile modificare il nome in un elemento più facilmente memorizzabile, ad esempio "Player".</span><span class="sxs-lookup"><span data-stu-id="23e03-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="23e03-139">L'aggiunta del controllo Windows Media Player dalla casella degli strumenti aggiunge anche riferimenti a due librerie create da Visual Studio, AxWMPLib e WMPLib.</span><span class="sxs-lookup"><span data-stu-id="23e03-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="23e03-140">È possibile trovarli nel Esplora soluzioni in **riferimenti**.</span><span class="sxs-lookup"><span data-stu-id="23e03-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="23e03-141">Per semplificare l'uso degli oggetti nello spazio dei nomi del lettore, è necessario includere lo spazio dei nomi nelle direttive using o Imports dei file, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="23e03-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="23e03-142">La direttiva garantisce che sia possibile fare riferimento a oggetti **Player** senza qualificare il nome completo.</span><span class="sxs-lookup"><span data-stu-id="23e03-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="23e03-143">Il controllo Media Player Windows è un oggetto **AxWindowsMediaPlayer** dello spazio dei nomi **AxWMPLib** .</span><span class="sxs-lookup"><span data-stu-id="23e03-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="23e03-144">Tuttavia, la classe **AxWindowsMediaPlayer** usa tipi di dati, interfacce e altri elementi dallo spazio dei nomi **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="23e03-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="23e03-145">Configurazione della visibilità del controllo</span><span class="sxs-lookup"><span data-stu-id="23e03-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="23e03-146">Quando si aggiunge per la prima volta il controllo Windows Media Player a un modulo, questo sarà visibile.</span><span class="sxs-lookup"><span data-stu-id="23e03-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="23e03-147">Se non si vuole usare l'immagine visibile del lettore nell'applicazione, nascondere il lettore predefinito impostando una delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="23e03-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="23e03-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="23e03-148">Property</span></span>        | <span data-ttu-id="23e03-149">Valore</span><span class="sxs-lookup"><span data-stu-id="23e03-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="23e03-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="23e03-150">**uiMode**</span></span>      | <span data-ttu-id="23e03-151">"invisibile" (vedere [Player. uiMode](player-uimode.md).)</span><span class="sxs-lookup"><span data-stu-id="23e03-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="23e03-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="23e03-152">**Visible**</span></span>     | <span data-ttu-id="23e03-153">"false"</span><span class="sxs-lookup"><span data-stu-id="23e03-153">"false"</span></span>                                               |
| <span data-ttu-id="23e03-154">**Size. Width**</span><span class="sxs-lookup"><span data-stu-id="23e03-154">**Size.Width**</span></span>  | <span data-ttu-id="23e03-155">0</span><span class="sxs-lookup"><span data-stu-id="23e03-155">0</span></span>                                                     |
| <span data-ttu-id="23e03-156">**Size. Height**</span><span class="sxs-lookup"><span data-stu-id="23e03-156">**Size.Height**</span></span> | <span data-ttu-id="23e03-157">0</span><span class="sxs-lookup"><span data-stu-id="23e03-157">0</span></span>                                                     |



 

<span data-ttu-id="23e03-158">È possibile impostare queste proprietà nel codice o nella finestra **Proprietà** quando si seleziona il controllo Media Player Windows nella finestra di progettazione del form.</span><span class="sxs-lookup"><span data-stu-id="23e03-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="23e03-159">Compatibilità del modello a oggetti del controllo</span><span class="sxs-lookup"><span data-stu-id="23e03-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="23e03-160">Il modello a oggetti per il controllo Media Player di Windows è fondamentalmente lo stesso nel .NET Framework come nel codice non gestito e nello script.</span><span class="sxs-lookup"><span data-stu-id="23e03-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="23e03-161">Tuttavia, esistono differenze nel modo in cui vengono esposti gli elementi:</span><span class="sxs-lookup"><span data-stu-id="23e03-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="23e03-162">La maggior parte degli oggetti è esposta sotto il nome dell'interfaccia COM sottostante.</span><span class="sxs-lookup"><span data-stu-id="23e03-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="23e03-163">Ad esempio, l'oggetto **playlist** viene esposto come **IWMPPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="23e03-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="23e03-164">Alcune interfacce hanno versioni successive.</span><span class="sxs-lookup"><span data-stu-id="23e03-164">Some interfaces have later versions.</span></span> <span data-ttu-id="23e03-165">Ad esempio, a **IWMPMedia** sono state assegnate funzionalità aggiuntive in **IWMPMedia2** e **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="23e03-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="23e03-166">Se si dichiara un oggetto come **IWMPMedia**, è in genere possibile accedere alla funzionalità di tutte le versioni dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="23e03-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="23e03-167">Tuttavia,® IntelliSense non riconoscerà i metodi o le proprietà delle interfacce di versione successiva e l'editor .NET Visual Basic non correggerà automaticamente le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="23e03-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="23e03-168">Per sfruttare tutti i vantaggi di IntelliSense e altre funzionalità di Visual Studio, dichiarare l'oggetto usando la versione più recente dell'interfaccia, ad esempio **IWMPMedia3**.</span><span class="sxs-lookup"><span data-stu-id="23e03-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="23e03-169">Non sono presenti proprietà indicizzate (C#) o proprietà predefinite (Visual Basic .NET).</span><span class="sxs-lookup"><span data-stu-id="23e03-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="23e03-170">Ad esempio, per recuperare una **playlist. Item**, è necessario chiamare il metodo della funzione di accesso **IWMPlaylist. Get \_ Item** in C# o recuperare la proprietà **IWMPlayist. Item** in Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="23e03-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="23e03-171">A causa di un conflitto di denominazione tra la proprietà **controlli** Media Player di Windows e la proprietà **controlli** esposti da ogni controllo, la versione del lettore di questa proprietà è denominata **CtlControls** nel contesto del controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="23e03-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="23e03-172">(Tuttavia, questo non avviene quando si crea il lettore a livello di codice anziché come controllo ActiveX).</span><span class="sxs-lookup"><span data-stu-id="23e03-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="23e03-173">Usare il Visualizzatore oggetti in Visual Studio per individuare i nomi API corretti per i metodi e gli oggetti negli spazi dei nomi **AxWMPLib** e **WMPLib** .</span><span class="sxs-lookup"><span data-stu-id="23e03-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="23e03-174">Distribuzione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="23e03-174">Distributing Your Application</span></span>

<span data-ttu-id="23e03-175">Quando si distribuisce l'applicazione, assicurarsi di installare AxInterop.WMPLib.dll e Interop.WMPLib.dll nella cartella dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="23e03-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="23e03-176">Sarà inoltre necessario assicurarsi che la versione di Windows Media Player richiesta sia installata nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="23e03-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23e03-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23e03-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23e03-178">**Creazione del controllo Media Player Windows a livello di codice**</span><span class="sxs-lookup"><span data-stu-id="23e03-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="23e03-179">**Incorporamento del controllo Media Player Windows in una soluzione C#**</span><span class="sxs-lookup"><span data-stu-id="23e03-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="23e03-180">**Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET**</span><span class="sxs-lookup"><span data-stu-id="23e03-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




