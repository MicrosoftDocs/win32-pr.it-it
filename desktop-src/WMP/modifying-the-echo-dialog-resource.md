---
title: Modifica della risorsa della finestra di dialogo Echo
description: Modifica della risorsa della finestra di dialogo Echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
- Esempio di plug-in Echo DSP, risorsa finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331207"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="bdc6e-109">Modifica della risorsa della finestra di dialogo Echo</span><span class="sxs-lookup"><span data-stu-id="bdc6e-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="bdc6e-110">È necessario modificare la risorsa della finestra di dialogo che rappresenta l'interfaccia utente per l'oggetto pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="bdc6e-111">È possibile modificare prima di tutto la casella di modifica e l'etichetta esistenti in modo da essere utile per la proprietà delay time, quindi aggiungere una seconda casella di modifica ed etichetta per la proprietà Wet Mix.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="bdc6e-112">Per modificare la risorsa finestra di dialogo in Visual C++:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="bdc6e-113">Fare clic sulla scheda **ResourceView** nell'area di lavoro progetto.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="bdc6e-114">Espandere l'albero delle risorse aprendo la cartella di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="bdc6e-115">Aprire la cartella della **finestra di dialogo** .</span><span class="sxs-lookup"><span data-stu-id="bdc6e-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="bdc6e-116">Fare doppio clic sul nome della risorsa della finestra di dialogo, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="bdc6e-117">L'editor risorse verrà visualizzato nel riquadro di destra.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="bdc6e-118">Modifica delle risorse esistenti</span><span class="sxs-lookup"><span data-stu-id="bdc6e-118">Changing the Existing Resources</span></span>

<span data-ttu-id="bdc6e-119">Per modificare le risorse della pagina delle proprietà esistenti per la proprietà tempo di ritardo:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="bdc6e-120">Per prima cosa, modificare il testo nel controllo testo statico esistente.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="bdc6e-121">Fare clic con il pulsante destro del mouse sul controllo e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="bdc6e-122">Nel campo **didascalia** Digitare la nuova didascalia:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="bdc6e-123">Chiudere la finestra di dialogo Proprietà testo.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="bdc6e-124">A questo punto, modificare il nome del controllo casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="bdc6e-125">A tale scopo, fare clic con il pulsante destro del mouse sul controllo e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="bdc6e-126">Nel campo **ID** Digitare un nuovo nome per il controllo:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="bdc6e-127">Chiudere la finestra di dialogo Modifica proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="bdc6e-128">Salvare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-128">Save the resource.</span></span>
6.  <span data-ttu-id="bdc6e-129">Risposta **Sì** se viene richiesto di ricaricare il file Resource. h.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="bdc6e-130">Fare clic sulla scheda **FileView** nell'area di lavoro progetto.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="bdc6e-131">Apri Resource. h</span><span class="sxs-lookup"><span data-stu-id="bdc6e-131">Open resource.h</span></span>
8.  <span data-ttu-id="bdc6e-132">Individuare l'oggetto \# define per la risorsa della casella di modifica del fattore di scala (IDC \_ SCALEFACTOR) ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="bdc6e-133">Deve avere lo stesso numero ID di IDC \_ DELAYTIME.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="bdc6e-134">Aggiunta di nuove risorse</span><span class="sxs-lookup"><span data-stu-id="bdc6e-134">Adding the New Resources</span></span>

<span data-ttu-id="bdc6e-135">Per aggiungere le nuove risorse della pagina delle proprietà per la proprietà Wet Mix:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="bdc6e-136">Fare clic sulla scheda **ResourceView** nell'area di lavoro del progetto per selezionarla.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="bdc6e-137">Fare doppio clic sul nome della finestra di dialogo pagina delle proprietà, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="bdc6e-138">L'editor risorse verrà visualizzato nel riquadro di destra.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="bdc6e-139">Utilizzare la casella degli strumenti per aggiungere un controllo testo statico e una casella di modifica alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="bdc6e-140">Fare clic con il pulsante destro del mouse sul controllo testo statico e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="bdc6e-141">Digitare un nuovo nome per il controllo testo statico nel campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="bdc6e-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="bdc6e-142">Digitare una didascalia per l'etichetta:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="bdc6e-143">Chiudere la finestra di dialogo Proprietà testo.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="bdc6e-144">Fare clic con il pulsante destro del mouse sulla casella di modifica e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="bdc6e-145">Digitare un nuovo nome per la casella di modifica nel campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="bdc6e-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="bdc6e-146">Chiudere la finestra di dialogo Modifica proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="bdc6e-147">Quando si salva il progetto, potrebbe essere richiesto di ricaricare Resource. h.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="bdc6e-148">Se ciò accade, fare clic su **Sì** .</span><span class="sxs-lookup"><span data-stu-id="bdc6e-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="bdc6e-149">L'editor risorse della finestra di dialogo deve aggiungere i nomi delle risorse e i numeri ID a Resource. h per gli elementi aggiunti.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="bdc6e-150">Se per qualche motivo questa operazione non viene eseguita, è necessario aprire Resource. h e digitare le nuove voci per il controllo etichetta e casella di modifica e assegnare ogni numero ID univoco.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="bdc6e-151">Modifica e aggiunta di risorse di stringa</span><span class="sxs-lookup"><span data-stu-id="bdc6e-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="bdc6e-152">Il codice di esempio della procedura guidata plug-in specifica una risorsa stringa denominata ID \_ SCALERANGEERROR che contiene un messaggio da visualizzare quando l'input dell'utente non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="bdc6e-153">È possibile modificare questa risorsa per adattarla alle proprie esigenze per il valore di tempo di ritardo attenendosi alla procedura descritta in Visual C++:</span><span class="sxs-lookup"><span data-stu-id="bdc6e-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="bdc6e-154">Fare clic sulla scheda **ResourceView** .</span><span class="sxs-lookup"><span data-stu-id="bdc6e-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="bdc6e-155">Aprire la cartella della **tabella di stringhe** .</span><span class="sxs-lookup"><span data-stu-id="bdc6e-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="bdc6e-156">Fare doppio clic sull'icona della **tabella di stringhe** per aprire l'editor risorse.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="bdc6e-157">Fare doppio clic sul nome della risorsa che si desidera modificare, in questo caso ID \_ SCALERANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="bdc6e-158">Verrà visualizzata la finestra di dialogo Proprietà stringa.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="bdc6e-159">Modificare il nome nel campo **ID** in ID \_ DELAYRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="bdc6e-160">Modificare il testo nel campo **didascalia** :</span><span class="sxs-lookup"><span data-stu-id="bdc6e-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="bdc6e-161">Chiudere la finestra di dialogo Proprietà stringa.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="bdc6e-162">Successivamente, aggiungere una nuova risorsa di stringa per il messaggio di errore della proprietà Wet Mix.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="bdc6e-163">Fare doppio clic sulla riga vuota nella parte inferiore dell'editor risorse.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="bdc6e-164">Modificare il nome nel campo **ID** in ID \_ MIXRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="bdc6e-165">Aggiungere il testo seguente al campo **didascalia** :</span><span class="sxs-lookup"><span data-stu-id="bdc6e-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="bdc6e-166">Chiudere la finestra di dialogo Proprietà stringa.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="bdc6e-167">Esistono altri due valori che si desidera modificare nella tabella delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="bdc6e-168">IDS \_ FriendlyName è il nome visualizzato nell'interfaccia utente di Windows Media Player per identificare il plug-in.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="bdc6e-169">\_Descrizione ID consente di comunicare all'utente il plug-in.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="bdc6e-170">Entrambe queste stringhe vengono passate come parametri alla funzione **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , che viene chiamata nel metodo DllRegisterServer in Echodll. cpp.</span><span class="sxs-lookup"><span data-stu-id="bdc6e-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc6e-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdc6e-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc6e-172">**Modifica della pagina delle proprietà di esempio Echo**</span><span class="sxs-lookup"><span data-stu-id="bdc6e-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




