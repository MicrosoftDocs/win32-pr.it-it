---
title: Interfaccia utente grafica di AccChecker
description: Questo argomento descrive gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550314"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="4c87a-103">Interfaccia utente grafica di AccChecker</span><span class="sxs-lookup"><span data-stu-id="4c87a-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="4c87a-104">Questo argomento descrive gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.</span><span class="sxs-lookup"><span data-stu-id="4c87a-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="4c87a-105">Scheda verifiche</span><span class="sxs-lookup"><span data-stu-id="4c87a-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="4c87a-106">Scheda risultati</span><span class="sxs-lookup"><span data-stu-id="4c87a-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="4c87a-107">Schede MSAA ed UIA screen reader</span><span class="sxs-lookup"><span data-stu-id="4c87a-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="4c87a-108">Schede di albero MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="4c87a-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="4c87a-109">Menu file</span><span class="sxs-lookup"><span data-stu-id="4c87a-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="4c87a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c87a-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="4c87a-111">Scheda verifiche</span><span class="sxs-lookup"><span data-stu-id="4c87a-111">Verifications Tab</span></span>

<span data-ttu-id="4c87a-112">AccChecker inizia con la visualizzazione predefinita della scheda **verifiche** :</span><span class="sxs-lookup"><span data-stu-id="4c87a-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Screenshot che mostra la scheda "verifiche" nel controllo di accessibilità U I.](images/accchecker-verifications-tab.png)

<span data-ttu-id="4c87a-114">La scheda **verifiche** contiene i componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="4c87a-115">**Selettore destinazione verifica** Offre le opzioni seguenti per selezionare un'applicazione o un controllo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c87a-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="4c87a-116">Scegliere una destinazione dall'elenco a discesa pre-popolato.</span><span class="sxs-lookup"><span data-stu-id="4c87a-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="4c87a-117">Questo elenco contiene tutti gli HWND di primo livello identificati all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4c87a-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="4c87a-118">Scegliere un HWND in base alla posizione del cursore del mouse (i controlli selezionabili sono evidenziati con un rettangolo rosso).</span><span class="sxs-lookup"><span data-stu-id="4c87a-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="4c87a-119">Questa opzione consente di selezionare qualsiasi oggetto visibile con HWND.</span><span class="sxs-lookup"><span data-stu-id="4c87a-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="4c87a-120">Immettere un HWND specifico.</span><span class="sxs-lookup"><span data-stu-id="4c87a-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="4c87a-121">**Elenco di controllo routine di verifica** Consente di selezionare la routine di verifica desiderata da eseguire su un'applicazione o un controllo.</span><span class="sxs-lookup"><span data-stu-id="4c87a-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="4c87a-122">Per ulteriori informazioni, vedere routine di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="4c87a-123">**Selettore file di eliminazione di errori e avvisi** I file di eliminazione vengono generati dalla scheda **risultati** verifica. Facendo clic con il pulsante destro del mouse su un messaggio di errore o di avviso e selezionando **Elimina** dal menu di scelta rapida, viene impostato un flag per il messaggio.</span><span class="sxs-lookup"><span data-stu-id="4c87a-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="4c87a-124">Se la casella di controllo di **eliminazione** è selezionata, le voci non vengono visualizzate nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4c87a-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="4c87a-125">Una voce eliminata può essere annullata usando lo stesso menu di scelta rapida usato per eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="4c87a-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="4c87a-126">Un file di eliminazione viene salvato in formato XML selezionando **Salva eliminazione** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="4c87a-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="4c87a-127">Questo file viene utilizzato nelle esecuzioni successive della verifica in cui i messaggi verranno nascosti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="4c87a-128">Per rimuovere il file di eliminazione, fare clic su **Cancella**.</span><span class="sxs-lookup"><span data-stu-id="4c87a-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="4c87a-129">Per informazioni su messaggi specifici, vedere messaggi di log di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="4c87a-130">Usare **Save log** dal menu **file** per salvare l'intero elenco come file di log in formato XML o come file di testo formattato.</span><span class="sxs-lookup"><span data-stu-id="4c87a-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![scheda risultati AccChecker con l'elemento di contesto non selezionato evidenziato](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="4c87a-132">Nell'esempio seguente viene illustrato il contenuto di un file di eliminazione generato eseguendo le verifiche delle **Proprietà** nell'applicazione del pannello di controllo Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="4c87a-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="4c87a-133">In questo esempio è stato scelto l'errore con ID "ElementHasNoName" per la soppressione.</span><span class="sxs-lookup"><span data-stu-id="4c87a-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="4c87a-134">**Mostra risultati classificati** in ordine di priorità In sono disponibili le opzioni seguenti per filtrare i risultati della verifica in base alla priorità.</span><span class="sxs-lookup"><span data-stu-id="4c87a-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="4c87a-135">**Tutto** Includi tutti i risultati indipendentemente dalla priorità.</span><span class="sxs-lookup"><span data-stu-id="4c87a-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="4c87a-136">**Solo P1** Includere solo i risultati con priorità 0 e priorità 1.</span><span class="sxs-lookup"><span data-stu-id="4c87a-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="4c87a-137">**Solo P1 P2** Includere la priorità 0 tramite i risultati con priorità 2.</span><span class="sxs-lookup"><span data-stu-id="4c87a-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="4c87a-138">**Esegui verifiche selezionate** Fornisce il pulsante **Esegui verifiche** per avviare il processo di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="4c87a-139">Mentre le verifiche sono in esecuzione, il pulsante cambia per **annullare le verifiche** e può essere usato per arrestare le verifiche dopo il completamento di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="4c87a-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="4c87a-140">Scheda Risultati</span><span class="sxs-lookup"><span data-stu-id="4c87a-140">Results Tab</span></span>

<span data-ttu-id="4c87a-141">La scheda **risultati** viene popolata dopo il completamento delle attività di verifica selezionate.</span><span class="sxs-lookup"><span data-stu-id="4c87a-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="4c87a-142">È costituito dai componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-142">It consists of the following components.</span></span>

-   <span data-ttu-id="4c87a-143">Elenco dei messaggi, che consente di visualizzare i messaggi di errore, di avviso e informativi generati dalle attività di verifica selezionate.</span><span class="sxs-lookup"><span data-stu-id="4c87a-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="4c87a-144">I messaggi visualizzati possono essere filtrati in base al tipo usando le caselle di controllo sopra l'elenco dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="4c87a-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="4c87a-145">I dettagli del messaggio e un'acquisizione schermo della destinazione di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="4c87a-146">La selezione di un messaggio dall'elenco dei messaggi Mostra ulteriori dettagli ed evidenzia l'elemento corrispondente nel riquadro acquisizione schermo.</span><span class="sxs-lookup"><span data-stu-id="4c87a-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="4c87a-147">Il pulsante **Visualizza** , passa AccChecker alla scheda **albero MSAA** . Se viene evidenziato un errore nella scheda **risultati** , l'elemento corrispondente viene evidenziato nella scheda **albero MSAA** .</span><span class="sxs-lookup"><span data-stu-id="4c87a-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="4c87a-148">Facendo clic con il pulsante destro del mouse su un messaggio viene esposto un menu di scelta rapida con gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="4c87a-149">Non **visualizzare** Aggiunge il messaggio all'elenco di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="4c87a-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="4c87a-150">**Copia negli Appunti** Copia i dettagli del messaggio negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="4c87a-151">**Visualizza** Passa AccChecker alla scheda **albero MSAA** . L'elemento che corrisponde all'errore selezionato è evidenziato.</span><span class="sxs-lookup"><span data-stu-id="4c87a-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="4c87a-152">**Guida** di Visualizza informazioni aggiuntive sul messaggio.</span><span class="sxs-lookup"><span data-stu-id="4c87a-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="4c87a-153">Schede MSAA ed UIA screen reader</span><span class="sxs-lookup"><span data-stu-id="4c87a-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="4c87a-154">Le schede lettore schermo MSAA e lettore schermata UIA sono simili.</span><span class="sxs-lookup"><span data-stu-id="4c87a-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="4c87a-155">In entrambi i casi viene visualizzata una trascrizione di elementi rilevati in un attraversamento simulato della destinazione di verifica da parte di un'applicazione per la lettura dello schermo, ad eccezione del fatto che viene mostrata l'implementazione di MSAA e l'altra l'implementazione di</span><span class="sxs-lookup"><span data-stu-id="4c87a-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="4c87a-156">Gli elementi vengono spostati e registrati nello stesso modo in cui vengono letti dal lettore dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4c87a-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="4c87a-157">Le informazioni presentate in questa scheda sono essenziali per confermare che sono state annunciate solo informazioni utili e rilevanti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="4c87a-158">Ad esempio, un nome di controllo di normalizzazione, ad esempio "MenuItem Edit" o "close pulsante", è accettabile. Tuttavia, un nome di controllo che non ha senso, ad esempio "CPNavPanel22" o "DefaultValue1", non è accettabile.</span><span class="sxs-lookup"><span data-stu-id="4c87a-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="4c87a-159">Il pulsante **Visualizza** , fa in modo che AccChecker passi all' **albero MSAA** o alla scheda **albero UIA** . Se un elemento viene evidenziato nella scheda **Visualizzatore schermo** , l'elemento corrispondente viene evidenziato nella scheda **albero MSAA** o **albero** di.</span><span class="sxs-lookup"><span data-stu-id="4c87a-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="4c87a-160">La  routine di verifica ScreenReader **in conformità deve** essere selezionata nella scheda **verifiche** per la visualizzazione della **scheda lettore schermata MSAA** .</span><span class="sxs-lookup"><span data-stu-id="4c87a-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="4c87a-161">Analogamente, è necessario selezionare la routine di verifica **UiaScreenReader** per visualizzare la scheda di **lettura dello schermo di UIA** .</span><span class="sxs-lookup"><span data-stu-id="4c87a-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="4c87a-162">La schermata seguente mostra la scheda lettore schermata UIA con una verifica di esempio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="4c87a-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![scheda lettore schermo AccChecker che Visualizza i risultati della verifica di esempio](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="4c87a-164">Schede di albero MSAA e UIA</span><span class="sxs-lookup"><span data-stu-id="4c87a-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="4c87a-165">L'esecuzione di una routine di verifica causa la compilazione di tutti gli elementi visibili nella destinazione di verifica da parte di AccChecker e la relativa visualizzazione gerarchica nella scheda **albero MSAA** e nella scheda dell' **albero** di gestione dei problemi. Lo screenshot seguente mostra la scheda albero MSAA con la gerarchia di elementi per blocco note.</span><span class="sxs-lookup"><span data-stu-id="4c87a-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![scheda albero MSAA AccChecker](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="4c87a-167">Menu File</span><span class="sxs-lookup"><span data-stu-id="4c87a-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c87a-168">Menu</span><span class="sxs-lookup"><span data-stu-id="4c87a-168">Menu</span></span></th>
<th><span data-ttu-id="4c87a-169">Comando</span><span class="sxs-lookup"><span data-stu-id="4c87a-169">Command</span></span></th>
<th><span data-ttu-id="4c87a-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c87a-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="4c87a-171"><strong>File</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4c87a-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4c87a-172"><strong>Apri</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="4c87a-173">In sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c87a-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="4c87a-174"><strong>Dll di verifica</strong> Apre una DLL di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="4c87a-175">Le verifiche AccChecker native sono incapsulate in una DLL autonoma (VerificationRoutines.dll).</span><span class="sxs-lookup"><span data-stu-id="4c87a-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="4c87a-176">Questa progettazione consente ai team di test di creare un proprio set di verifiche basate sulla piattaforma dell'interfaccia utente sottoposta a test.</span><span class="sxs-lookup"><span data-stu-id="4c87a-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="4c87a-177"><strong>File di log</strong> Consente di scegliere un file di log di verifica da aprire.</span><span class="sxs-lookup"><span data-stu-id="4c87a-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c87a-178"><strong>Carica automaticamente le verifiche disponibili</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="4c87a-179">Carica automaticamente tutte le verifiche AccChecker disponibili.</span><span class="sxs-lookup"><span data-stu-id="4c87a-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4c87a-180"><strong>Salva log</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="4c87a-181">Salvare il log di verifica come XML o come testo normale.</span><span class="sxs-lookup"><span data-stu-id="4c87a-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="4c87a-182">Il testo normale è più leggibile.</span><span class="sxs-lookup"><span data-stu-id="4c87a-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4c87a-183"><strong>Salva eliminazione</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="4c87a-184">Salvare il log di eliminazione come XML.</span><span class="sxs-lookup"><span data-stu-id="4c87a-184">Save the suppression log as XML.</span></span> <span data-ttu-id="4c87a-185">Questo file specifica i messaggi di verifica da ignorare nei test di regressione.</span><span class="sxs-lookup"><span data-stu-id="4c87a-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4c87a-186"><strong>Esci</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="4c87a-187">Chiude lo strumento AccChecker.</span><span class="sxs-lookup"><span data-stu-id="4c87a-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="4c87a-188"><strong>Verifiche</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4c87a-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4c87a-189"><strong>Esegui adesso</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="4c87a-190">Eseguire le routine di verifica come specificato per la destinazione di verifica scelta.</span><span class="sxs-lookup"><span data-stu-id="4c87a-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c87a-191"><strong>Abilita tutto</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="4c87a-192">Selezionare le caselle di controllo di tutte le routine di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4c87a-193"><strong>Disabilita tutto</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="4c87a-194">Deselezionare tutte le caselle di controllo della routine di verifica.</span><span class="sxs-lookup"><span data-stu-id="4c87a-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4c87a-195"><strong>Opzioni</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="4c87a-196"><strong>Always On Top</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="4c87a-197">Rendere AccChecker la finestra in primo piano nell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="4c87a-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="4c87a-198"><strong>Guida</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4c87a-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4c87a-199"><strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="4c87a-200">Visualizzare le informazioni della guida.</span><span class="sxs-lookup"><span data-stu-id="4c87a-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c87a-201"><strong>Informazioni</strong></span><span class="sxs-lookup"><span data-stu-id="4c87a-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="4c87a-202">Visualizzare la versione di AccChecker e un indirizzo di posta elettronica per contattare Microsoft su AccChecker.</span><span class="sxs-lookup"><span data-stu-id="4c87a-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4c87a-203">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c87a-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c87a-204">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4c87a-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





