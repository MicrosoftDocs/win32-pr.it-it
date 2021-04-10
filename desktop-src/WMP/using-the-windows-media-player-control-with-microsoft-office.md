---
title: Uso del controllo Media Player di Windows con Microsoft Office
description: Uso del controllo Media Player di Windows con Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, Office
- Modello a oggetti di Windows Media Player, Office
- modello a oggetti, Office
- Windows Media Player Mobile, Office
- Windows Media Player ActiveX Control, Office
- Controllo ActiveX Windows Media Player Mobile, Office
- Controllo ActiveX, Office
- Incorporamento di documenti di Office
- incorporamento, documenti di Office
- Controllo ActiveX di Windows Media Player, Excel
- Controllo ActiveX Windows Media Player Mobile, Excel
- Controllo ActiveX, Excel
- incorporamento, fogli di calcolo di Excel
- Incorporamento del foglio di calcolo di Excel
- Controllo ActiveX di Windows Media Player, PowerPoint
- Controllo ActiveX Windows Media Player Mobile, PowerPoint
- Controllo ActiveX, PowerPoint
- incorporamento, presentazioni di PowerPoint
- Presentazione dell'incorporamento in PowerPoint
- Controllo ActiveX di Windows Media Player, Word
- Controllo ActiveX Windows Media Player Mobile, Word
- Controllo ActiveX, Word
- Incorporamento di documenti di Word
- incorporamento, documenti di Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955530"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="86ee3-134">Uso del controllo Media Player di Windows con Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="86ee3-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="86ee3-135">In questa sezione viene descritto come incorporare il controllo ActiveX Windows Media Player 9 o versioni successive in diversi documenti creati con Microsoft Office XP.</span><span class="sxs-lookup"><span data-stu-id="86ee3-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="86ee3-136">In Microsoft Word, Excel e PowerPoint® è possibile incorporare il controllo selezionando **oggetto** dal menu **Inserisci** , quindi scegliendo **Windows Media Player** dall'elenco dei tipi di oggetto disponibili.</span><span class="sxs-lookup"><span data-stu-id="86ee3-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="86ee3-137">Il controllo Media Player Windows viene visualizzato nel documento nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="86ee3-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="86ee3-138">È quindi possibile selezionare **formato controllo** ( **Formatta oggetto** in Excel) dal menu di scelta rapida per il controllo per modificare il layout, lo stile di ritorno a capo del testo e altre opzioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="86ee3-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="86ee3-139">Per eseguire questa operazione in Word ed Excel, è necessario essere in modalità progettazione.</span><span class="sxs-lookup"><span data-stu-id="86ee3-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="86ee3-140">Dopo aver posizionato e formattato il controllo, è possibile configurarlo utilizzando la finestra di dialogo **Proprietà** , accessibile dalla **casella degli strumenti controllo** o dal menu di scelta rapida in modalità progettazione per Word ed Excel.</span><span class="sxs-lookup"><span data-stu-id="86ee3-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="86ee3-141">Qui è possibile specificare le proprietà di base del controllo Player, ad esempio il nome del controllo, l'URL di un file multimediale digitale e la modalità dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="86ee3-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="86ee3-142">Se si imposta la proprietà **uiMode** su "None", tutti gli elementi del controllo vengono nascosti, ad eccezione della finestra video o visualizzazione, consentendo di aggiungere pulsanti personalizzati e scrivere codice script usando Visual Basic, Applications Edition (VBA) per gestire i clic del pulsante e gli eventi di controllo del lettore.</span><span class="sxs-lookup"><span data-stu-id="86ee3-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="86ee3-143">Nella finestra di dialogo **Proprietà** di base è inoltre possibile accedere alla finestra di dialogo **proprietà del controllo di Windows Media Player** più sofisticate facendo doppio clic sulla riga "(personalizzata)" oppure facendo clic sul pulsante con i puntini di sospensione ("...") dopo aver selezionato la riga.</span><span class="sxs-lookup"><span data-stu-id="86ee3-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="86ee3-144">Da questa finestra di dialogo è possibile modificare tutte le proprietà del controllo lettore disponibili.</span><span class="sxs-lookup"><span data-stu-id="86ee3-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="86ee3-145">È necessario prestare attenzione a non eseguire azioni nei gestori di eventi di controllo del lettore che comporteranno la distruzione del controllo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="86ee3-146">Se ad esempio si incorpora il controllo Windows Media Player in una diapositiva in una presentazione di PowerPoint, non chiamare il metodo **Next** di PowerPoint dall'evento Player **openStateChange** o da qualsiasi altro evento.</span><span class="sxs-lookup"><span data-stu-id="86ee3-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="86ee3-147">Inoltre, è consigliabile non impostare la proprietà **Player. URL** da un gestore eventi di controllo del lettore.</span><span class="sxs-lookup"><span data-stu-id="86ee3-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="86ee3-148">In FrontPage aggiungere il controllo Media Player Windows a una pagina Web selezionando **componente Web** dal menu **Inserisci** .</span><span class="sxs-lookup"><span data-stu-id="86ee3-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="86ee3-149">Nella finestra di dialogo **Inserisci componente Web** selezionare **controlli avanzati** nell'elenco **tipo componente** , quindi selezionare **controllo ActiveX** nell'elenco delle opzioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="86ee3-150">Nella finestra successiva della finestra di dialogo selezionare **Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="86ee3-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="86ee3-151">Se non è elencato, fare clic su **Personalizza** e selezionare la casella di controllo **Windows Media Player** nell'elenco di **controllo** .</span><span class="sxs-lookup"><span data-stu-id="86ee3-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="86ee3-152">Dopo aver incorporato il controllo Media Player di Windows, è possibile posizionarlo e ridimensionarlo e modificarne le proprietà selezionando **proprietà del controllo ActiveX** dal menu di scelta rapida per il controllo.</span><span class="sxs-lookup"><span data-stu-id="86ee3-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="86ee3-153">Nella visualizzazione HTML, i valori delle proprietà specificati vengono visualizzati nell'elemento oggetto che rappresenta il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="86ee3-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="86ee3-154">Il nome dell'oggetto viene visualizzato come attributo ID e le proprietà del controllo vengono visualizzate come tag PARAM.</span><span class="sxs-lookup"><span data-stu-id="86ee3-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="86ee3-155">Il nome dell'oggetto consente di accedere al modello a oggetti di controllo Media Player di Windows, che è possibile programmare utilizzando Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="86ee3-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="86ee3-156">Per ulteriori informazioni, vedere [utilizzo del controllo Windows Media Player in una pagina Web](using-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="86ee3-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86ee3-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86ee3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ee3-158">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="86ee3-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




