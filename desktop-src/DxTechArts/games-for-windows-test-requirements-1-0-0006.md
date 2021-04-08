---
title: 'Test case dei giochi di Windows: procedure consigliate per giochi su Windows XP, Windows Vista, Windows 7 e Windows 8'
description: Questo articolo fornisce i test case per i giochi per Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047068"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="3eeca-103">Giochi per i test case di Windows: procedure consigliate per i giochi in Windows XP, Windows Vista, Windows 7 e Windows 8</span><span class="sxs-lookup"><span data-stu-id="3eeca-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="3eeca-104">Questo articolo fornisce i test case per i giochi per Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="3eeca-105">Come usare questo articolo</span><span class="sxs-lookup"><span data-stu-id="3eeca-105">How to Use This Article</span></span>

<span data-ttu-id="3eeca-106">Questo articolo include tre sezioni principali:</span><span class="sxs-lookup"><span data-stu-id="3eeca-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="3eeca-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisiti di test**</span><span class="sxs-lookup"><span data-stu-id="3eeca-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-108">Ogni requisito di test in questo documento è costituito da quattro sezioni principali: un titolo e una tabella con tre sezioni rilevanti (colonna sinistra, a destra in alto, a destra in basso).</span><span class="sxs-lookup"><span data-stu-id="3eeca-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="3eeca-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo</span><span class="sxs-lookup"><span data-stu-id="3eeca-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-110">Nome del test case.</span><span class="sxs-lookup"><span data-stu-id="3eeca-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, colonna all'estrema sinistra</span><span class="sxs-lookup"><span data-stu-id="3eeca-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-112">Nomi dei sistemi operativi a cui si applica il test case.</span><span class="sxs-lookup"><span data-stu-id="3eeca-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, a destra in alto</span><span class="sxs-lookup"><span data-stu-id="3eeca-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-114">Breve riepilogo del test case.</span><span class="sxs-lookup"><span data-stu-id="3eeca-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, a destra in basso</span><span class="sxs-lookup"><span data-stu-id="3eeca-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-116">Dettagli del test case effettivo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3eeca-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script di test di esempio**</span><span class="sxs-lookup"><span data-stu-id="3eeca-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-118">Questa sezione è un esempio della sequenza che dovrebbe essere seguita da un passaggio di test tipico se si usano i requisiti di test come guida.</span><span class="sxs-lookup"><span data-stu-id="3eeca-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Note sugli strumenti di test**</span><span class="sxs-lookup"><span data-stu-id="3eeca-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-120">Questa sezione contiene le note dettagliate su ciascuno degli strumenti di test usati per verificare le condizioni di superamento o di errore nei requisiti di test.</span><span class="sxs-lookup"><span data-stu-id="3eeca-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="3eeca-121">Requisiti di test</span><span class="sxs-lookup"><span data-stu-id="3eeca-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="3eeca-122">1. requisiti del gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="3eeca-123">1,1 Esplora giochi di Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-124">Windows 7</span></span><br/> <span data-ttu-id="3eeca-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-126">Il gioco deve essere visibile all'interno di Esplora giochi in Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeca-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="3eeca-127">Quando questa opzione è selezionata, il gioco deve anche visualizzare i metadati corretti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="3eeca-128">L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altra posizione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="3eeca-129">Le attività e i tasti di scelta rapida per la rimozione non devono essere creati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-130">Dopo l'installazione del gioco, aprire giochi Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="3eeca-131">Verificare che l'icona del gioco sia visualizzata in Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="3eeca-132">Fare clic con il pulsante destro del mouse sull'icona e testare tutte le attività di riproduzione & del supporto definite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="3eeca-133">Fare clic sull'icona e verificare che i metadati (Publisher, Developer, genre, data di rilascio, versione) nella parte inferiore visualizzino e siano corretti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="3eeca-134">Verificare che nell'icona del gioco siano visualizzate le informazioni sugli indici di Windows Experience (WEI) in Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="3eeca-135">Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Game Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="3eeca-136">Se non vengono visualizzati collegamenti ipertestuali, questo è un possibile segno che il file exe non è firmato. vedere la <a href="#23-sign-files">sezione 2,3</a>.</span><span class="sxs-lookup"><span data-stu-id="3eeca-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="3eeca-137">Verificare che il gioco visualizzi una classificazione di controllo parentale accurata in Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="3eeca-138">Se viene indicato senza classificazione, verificare che si tratta di un gioco senza classificazione. in caso contrario, si tratta di un indicatore indicante che il file exe non è firmato. vedere la <a href="#23-sign-files">sezione 2,3</a>.</span><span class="sxs-lookup"><span data-stu-id="3eeca-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="3eeca-139">Verificare che il gioco non disponga dei collegamenti di avvio sul desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="3eeca-140">Fare clic su Start-> tutti i programmi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="3eeca-141">Verificare che il gioco non disponga dei collegamenti di avvio nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="3eeca-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="3eeca-142">Verificare che il gioco non disponga dei collegamenti di disinstallazione nel menu Start esterno al pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="3eeca-143">Se il gioco è distribuito in formato digitale, verificare che il provider di servizi sia visualizzato in Esplora giochi di Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="3eeca-144">1,2 sicurezza della famiglia di Windows/controlli padre</span><span class="sxs-lookup"><span data-stu-id="3eeca-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-145">Windows 7</span></span><br/> <span data-ttu-id="3eeca-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-147">Il gioco deve essere eseguito nel contesto di un &quot; utente standard &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="3eeca-148">I controlli padre devono essere in grado di bloccare il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="3eeca-149">Verificare che l'oggetto GDF abbia nomi EXE.</span><span class="sxs-lookup"><span data-stu-id="3eeca-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-150">Creare un account utente standard in Windows Vista o Windows 7 denominato Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="3eeca-151">Start-> pannello di controllo-> aggiungere o rimuovere account utente-> creare un nuovo account</span><span class="sxs-lookup"><span data-stu-id="3eeca-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="3eeca-152">Come Jane, dall'account amministratore impostare i controlli padre per il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="3eeca-153">Start-> pannello di controllo-> configurare i controlli padre per qualsiasi utente-> Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="3eeca-154">Verificare che il gioco venga avviato dall'icona di Esplora giochi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="3eeca-155">Verificare che il gioco visualizzi una valutazione accurata del controllo parentale sotto il titolo del gioco nel pannello di controllo dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="3eeca-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="3eeca-156">Prima di applicare i controlli padre, verificare che il gioco non richieda le credenziali di amministratore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3eeca-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="3eeca-157">Impostare i controlli padre &quot; su on &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="3eeca-158">Nella sezione impostazioni di Windows fare clic su giochi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="3eeca-159">Fare clic su OK (l'impostazione dovrebbe essere ora &quot; Ao/tutti i giochi &quot; ).</span><span class="sxs-lookup"><span data-stu-id="3eeca-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="3eeca-160">Verificare che il gioco venga eseguito con queste impostazioni come utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="3eeca-161">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="3eeca-162">Verificare che il gioco venga eseguito con queste impostazioni come utente Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="3eeca-163">Disconnettersi come Toby e accedere come Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="3eeca-164">Tornare alla schermata precedente e selezionare &quot; imposta classificazioni giochi &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="3eeca-165">Selezionare una classificazione inferiore alla classificazione ESRB del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-166">Se il gioco non viene valutato, ignorare questo passaggio e passare alla parte successiva di questo test.</span><span class="sxs-lookup"><span data-stu-id="3eeca-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="3eeca-167">Potrebbe essere necessario scegliere un sistema di classificazione diverso per trovare una classificazione del gioco, a seconda delle impostazioni locali della lingua dello SKU testato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="3eeca-168">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="3eeca-169">Verificare che il gioco non venga avviato per l'utente Toby quando ESRB è bloccato dall'utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="3eeca-170">Disconnettersi come Toby e accedere come Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="3eeca-171">Se è stato modificato in precedenza, ripristinare le impostazioni di ESRB.</span><span class="sxs-lookup"><span data-stu-id="3eeca-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="3eeca-172">Se non sono presenti impostazioni di ESRB, selezionare &quot; blocca o Consenti giochi specifici &quot; e selezionare il gioco in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3eeca-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="3eeca-173">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="3eeca-174">Verificare che il gioco non venga avviato per l'utente Toby quando il nome di file EXE/nome è bloccato dall'utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="3eeca-175">Disconnettersi da Toby e viceversa come Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="3eeca-176">Come Jane, aprire controlli utente-> restrizioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="3eeca-177">Fare clic su &quot; Toby è possibile utilizzare solo i programmi consentiti &quot; e fare clic su OK, ovvero non consentire alcun exe.</span><span class="sxs-lookup"><span data-stu-id="3eeca-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="3eeca-178">Vai a controlli utente | I giochi controllano e consentono al gioco specifico di usare la classificazione ESRB.</span><span class="sxs-lookup"><span data-stu-id="3eeca-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="3eeca-179">Disconnettersi da Jane e accedere come Toby e provare a riprodurre il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="3eeca-180">Verificare che il gioco non sia bloccato e che Toby possa riprodurlo quando non è &quot; impostato alcun exe &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="3eeca-181">1,3 giochi Rich salvati di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="3eeca-182">Questo requisito è stato ritirato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="3eeca-183">1,4 controller comune di Xbox 360 per \[ requisito condizionale di Windows\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-184">Windows 7</span></span><br/> <span data-ttu-id="3eeca-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-185">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-187">I giochi che supportano i controller di gamepad devono supportare il controller Xbox 360 per Windows con l'API XInput.</span><span class="sxs-lookup"><span data-stu-id="3eeca-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="3eeca-188">Tutti i riferimenti ai trigger e ai pulsanti comuni del controller devono usare i nomi di Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="3eeca-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-189">Avvia il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-189">Launch the game.</span></span></li>
<li><span data-ttu-id="3eeca-190">Passare alle opzioni del controller.</span><span class="sxs-lookup"><span data-stu-id="3eeca-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="3eeca-191">Verificare che il gioco riconosca il controller Xbox 360 per Windows come dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="3eeca-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="3eeca-192">Riprodurre il gioco e verificare che il sistema di gioco e menu siano controllabili con il controller Xbox 360 per Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="3eeca-193">Verificare che il controller Xbox 360 per Windows si comportano in base agli standard accettati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="3eeca-194">(B per indietro, A per accettazione, avvio per nel menu del gioco/pausa o accettazione e così via)</span><span class="sxs-lookup"><span data-stu-id="3eeca-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="3eeca-195">Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando i nomi di Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="3eeca-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-196">Se il gioco non supporta un controller di gioco e/o supporta solo tastiera/mouse, ignorare questo test case.</span><span class="sxs-lookup"><span data-stu-id="3eeca-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="3eeca-197">\* \* Le impostazioni per il controller potrebbero trovarsi all'esterno del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="3eeca-198">1,5 più proporzioni e risoluzioni</span><span class="sxs-lookup"><span data-stu-id="3eeca-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-199">Windows 7</span></span><br/> <span data-ttu-id="3eeca-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-200">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-202">Il gioco deve supportare almeno le proporzioni seguenti e le risoluzioni dello schermo associate:</span><span class="sxs-lookup"><span data-stu-id="3eeca-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="3eeca-203">4:3 &quot; normale &quot; (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="3eeca-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="3eeca-204">16:9 &quot; widescreen &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="3eeca-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="3eeca-205">16:10 &quot; widescreen &quot; (1152 720, 1680 1050 o 800 480)</span><span class="sxs-lookup"><span data-stu-id="3eeca-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-206">Individuare le opzioni video per il gioco. è possibile che si trovino in gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-207">I test seguenti devono essere eseguiti su un monitor widescreen.</span><span class="sxs-lookup"><span data-stu-id="3eeca-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="3eeca-208">Nella sezione risoluzione del video selezionare 800 600 o 1024 768.</span><span class="sxs-lookup"><span data-stu-id="3eeca-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="3eeca-209">Verificare che il gioco venga eseguito a una risoluzione di 4:3 proporzioni.</span><span class="sxs-lookup"><span data-stu-id="3eeca-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="3eeca-210">Nella sezione risoluzione del video selezionare 1280 720.</span><span class="sxs-lookup"><span data-stu-id="3eeca-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="3eeca-211">Verificare che il gioco venga eseguito a una risoluzione di 16:9 proporzioni.</span><span class="sxs-lookup"><span data-stu-id="3eeca-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="3eeca-212">Nella sezione risoluzione del video selezionare 1680 1050, 800 480 o 1152 720.</span><span class="sxs-lookup"><span data-stu-id="3eeca-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="3eeca-213">Verificare che il gioco venga eseguito a una risoluzione di 16:10 proporzioni.</span><span class="sxs-lookup"><span data-stu-id="3eeca-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="3eeca-214">Verificare che il gioco non estenda l'immagine e a sua volta presenta un'area di visualizzazione più ampia.</span><span class="sxs-lookup"><span data-stu-id="3eeca-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="3eeca-215">Verificare che il gioco chieda all'utente quando viene apportata una modifica alla risoluzione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="3eeca-216">Se l'utente non accetta entro 15 secondi, verificare che venga ripristinata l'impostazione precedente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="3eeca-217">Verificare che il gioco non aggiunga barre nere a sinistra e a destra dell'area giochi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="3eeca-218">(In questo caso, l'area del gioco sarà ancora in un rapporto 4:3 al centro dello schermo).</span><span class="sxs-lookup"><span data-stu-id="3eeca-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="3eeca-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="3eeca-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="3eeca-220">Questo requisito è stato ritirato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="3eeca-221">1,7 \[ requisito condizionale Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eeca-222">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-222">Windows 7</span></span><br/> <span data-ttu-id="3eeca-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-223">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-224">Windows XP</span></span><br/> | <span data-ttu-id="3eeca-225">Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere l'impostazione predefinita per qualsiasi opzione di configurazione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-225">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <span data-ttu-id="3eeca-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt></span><span class="sxs-lookup"><span data-stu-id="3eeca-226"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="3eeca-227">Avvia il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-227">Launch the game.</span></span> <span data-ttu-id="3eeca-228">Nelle opzioni video verificare se sono presenti opzioni di rendering, D3D e/o OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3eeca-228">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="3eeca-229">Se sono presenti, verificare che le opzioni di rendering del gioco siano predefinite in Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3eeca-229">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="3eeca-230">Se non si riesce a verificare che D3D9 sia la versione di DirectX in uso, procedere con il test automatizzato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-230">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="3eeca-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt></span><span class="sxs-lookup"><span data-stu-id="3eeca-231"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="3eeca-232">Usare lo strumento: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-232">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="3eeca-233">1,8 Abilita compatibilità DPI elevata</span><span class="sxs-lookup"><span data-stu-id="3eeca-233">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-234">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-234">Windows 7</span></span><br/> <span data-ttu-id="3eeca-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-235">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-236">I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando è abilitata la scalabilità DPI.</span><span class="sxs-lookup"><span data-stu-id="3eeca-236">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="3eeca-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-237"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="3eeca-238">Impostare il sistema su DPI 150%:</span><span class="sxs-lookup"><span data-stu-id="3eeca-238">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="3eeca-239">Windows Vista: Pannello di controllo: personalizzazione, regolazione della dimensione del carattere (DPI), DPI personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-239">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="3eeca-240">Impostare su 150%.</span><span class="sxs-lookup"><span data-stu-id="3eeca-240">Set to 150%.</span></span><br/> <span data-ttu-id="3eeca-241">Windows 7: Pannello di controllo: visualizzazione, impostata su un numero di 150% superiore.</span><span class="sxs-lookup"><span data-stu-id="3eeca-241">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="3eeca-242">Eseguire il processo di installazione e il gioco per verificare che non vi siano problemi con schermate o finestre di dialogo ritagliate.</span><span class="sxs-lookup"><span data-stu-id="3eeca-242">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="3eeca-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-243"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="3eeca-244">Verificare che l'elemento <dpiAware>true</dpiAware> sia contenuto nel manifesto incorporato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-244">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="3eeca-245">Usare lo strumento: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-245">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="3eeca-246">2. sicurezza e compatibilità</span><span class="sxs-lookup"><span data-stu-id="3eeca-246">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="3eeca-247">2,1 seguire le linee guida per il controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="3eeca-247">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-248">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-248">Windows 7</span></span><br/> <span data-ttu-id="3eeca-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-249">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-250">Ogni file eseguibile (. Estensione EXE) inclusa in un'applicazione deve avere un manifesto incorporato che ne definisce il livello di esecuzione:</span><span class="sxs-lookup"><span data-stu-id="3eeca-250">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-251">Per i programmi di installazione dei giochi e dei giochi, uiAccess deve essere sempre impostato su &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-251">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-252">Verificare che i file eseguibili del gioco contengano manifesti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-252">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="3eeca-253">Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="3eeca-253">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="3eeca-254">Usare lo strumento: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-254">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="3eeca-255">2,2 supportano le versioni x64 di Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-255">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-256">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-256">Windows 7</span></span><br/> <span data-ttu-id="3eeca-257">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-257">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-258">Per mantenere la compatibilità con le versioni x64 di Windows:</span><span class="sxs-lookup"><span data-stu-id="3eeca-258">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="3eeca-259">I titoli e i programmi di installazione del titolo non devono contenere codice a 16 bit o basarsi su un componente a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3eeca-259">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="3eeca-260">Se il gioco dipende da driver in modalità kernel per l'operazione, è necessario che siano disponibili versioni x64 di questi driver.</span><span class="sxs-lookup"><span data-stu-id="3eeca-260">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="3eeca-261">L'installazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni di Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="3eeca-261">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-262">Il supporto per l'edizione a 64 bit di Windows XP Professional è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-262">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-263">Test manuale</span><span class="sxs-lookup"><span data-stu-id="3eeca-263">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-264">Esegui il gioco nelle edizioni di Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="3eeca-264">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="3eeca-265">Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeca-265">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="3eeca-266">Verificare che il gioco non riscontri un errore a causa di eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeca-266">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="3eeca-267">Nell'errore verrà citata l'applicazione a 16 bit nella finestra di errore.</span><span class="sxs-lookup"><span data-stu-id="3eeca-267">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="3eeca-268">Se il gioco ha un eseguibile nativo a 64 bit, usare anche tale file.</span><span class="sxs-lookup"><span data-stu-id="3eeca-268">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="3eeca-269">2,3 file di firma</span><span class="sxs-lookup"><span data-stu-id="3eeca-269">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-270">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-270">Windows 7</span></span><br/> <span data-ttu-id="3eeca-271">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-271">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-272">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-272">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-273">Tutti i file di codice eseguibile (ad esempio, con estensione exe e dll) devono essere firmati con un certificato Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3eeca-273">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="3eeca-274">Se si utilizza Windows Installer, i file del pacchetto del programma di installazione (file con estensione msi) devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-274">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-275">Test manuale</span><span class="sxs-lookup"><span data-stu-id="3eeca-275">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-276">Passare alla directory del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-276">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="3eeca-277">Individuare tutti i file con estensione exe e dll.</span><span class="sxs-lookup"><span data-stu-id="3eeca-277">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="3eeca-278">Fare clic con il pulsante destro del mouse su proprietà per ogni file.</span><span class="sxs-lookup"><span data-stu-id="3eeca-278">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="3eeca-279">Verificare che i file eseguibili del gioco contengano una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="3eeca-279">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="3eeca-280">2,4 firmare i driver</span><span class="sxs-lookup"><span data-stu-id="3eeca-280">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-281">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-281">Windows 7</span></span><br/> <span data-ttu-id="3eeca-282">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-282">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-283">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-283">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-284">Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-284">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="3eeca-285">Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve avere una firma Microsoft ottenuta tramite il programma Windows Hardware Quality Labs (WHQL) o driver affidabilità Signature (DRS).</span><span class="sxs-lookup"><span data-stu-id="3eeca-285">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-286">Test manuale</span><span class="sxs-lookup"><span data-stu-id="3eeca-286">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-287">Installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-287">Install the game.</span></span></li>
<li><span data-ttu-id="3eeca-288">Verificare che il processo di installazione del gioco non visualizzi finestre di dialogo di driver non firmate.</span><span class="sxs-lookup"><span data-stu-id="3eeca-288">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="3eeca-289">2,5 eseguire correttamente il controllo della versione</span><span class="sxs-lookup"><span data-stu-id="3eeca-289">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-290">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-290">Windows 7</span></span><br/> <span data-ttu-id="3eeca-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-291">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-292">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-293">I giochi non devono essere eseguiti nei sistemi operativi futuri, come indicato dalle modifiche apportate al numero di versione di Windows, a meno che il contratto di licenza con l'utente finale non vieti l'uso nei sistemi operativi futuri.</span><span class="sxs-lookup"><span data-stu-id="3eeca-293">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="3eeca-294">Se si suppone che il gioco abbia esito negativo, è necessario che venga visualizzato un messaggio all'utente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-294">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="3eeca-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-295"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="3eeca-296">Installare il gioco in Windows XP, nelle edizioni a 32 bit di Windows Vista e Windows 7 e nelle edizioni a 64 bit di Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeca-296">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="3eeca-297">Verificare che il processo di installazione del gioco non riscontri un errore relativo alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-297">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="3eeca-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-298"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="3eeca-299">Usare lo strumento: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="3eeca-299">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-300">Avviare Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="3eeca-300">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="3eeca-301">Abilitare il test Compatibility: HighVersionLie dopo aver selezionato il INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="3eeca-301">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="3eeca-302">Installare il gioco e assicurarsi che non blocchi l'installazione in base alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-302">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="3eeca-303">Abilitare il test Compatibility: HighVersionLie dopo aver selezionato il GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="3eeca-303">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="3eeca-304">Eseguire il gioco e assicurarsi che non blocchi l'esecuzione in base alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-304">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="3eeca-305">2,6 supportare sessioni utente simultanee</span><span class="sxs-lookup"><span data-stu-id="3eeca-305">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-306">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-306">Windows 7</span></span><br/> <span data-ttu-id="3eeca-307">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-307">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-308">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-308">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-309">I giochi devono supportare scenari multitasking standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-309">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-310">Creare un account utente standard in Windows Vista o Windows 7 denominato Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-310">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="3eeca-311">Start-> pannello di controllo-> aggiungere o rimuovere account utente-> creare un nuovo account</span><span class="sxs-lookup"><span data-stu-id="3eeca-311">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="3eeca-312">Avviare il gioco come utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-312">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="3eeca-313">ALT + TAB per tornare al desktop.</span><span class="sxs-lookup"><span data-stu-id="3eeca-313">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="3eeca-314">Verificare che il gioco ALT + TAB sia corretto al desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-314">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="3eeca-315">Fare clic su Start-> [freccia a destra di Lock]-> switch user.</span><span class="sxs-lookup"><span data-stu-id="3eeca-315">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="3eeca-316">Accedere come utente Toby.</span><span class="sxs-lookup"><span data-stu-id="3eeca-316">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="3eeca-317">Verificare che il gioco venga avviato come utente Toby mentre è ancora in esecuzione come utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-317">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="3eeca-318">Verificare che il gioco non riscontri errori per l'utente Toby o l'utente Jane durante il processo switch utente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-318">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="3eeca-319">Se è possibile avviare un'altra sessione del gioco, verificare che non sia possibile ascoltare audio dalla sessione del gioco originale.</span><span class="sxs-lookup"><span data-stu-id="3eeca-319">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="3eeca-320">Chiudere il gioco e tornare all'utente e al gioco originali.</span><span class="sxs-lookup"><span data-stu-id="3eeca-320">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="3eeca-321">2,7 supporto di nomi lunghi</span><span class="sxs-lookup"><span data-stu-id="3eeca-321">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-322">Windows 7</span></span><br/> <span data-ttu-id="3eeca-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-323">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-324">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-324">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-325">Se un gioco supporta il salvataggio di file, deve essere in grado di salvare i file con nomi e percorsi lunghi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-325">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="3eeca-326">Il gioco deve gestire correttamente caratteri di file system speciali, ad esempio \/: \*?</span><span class="sxs-lookup"><span data-stu-id="3eeca-326">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="3eeca-327">&quot; < o > in tutti i campi di input utente utilizzati per creare nomi file o percorsi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-327">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-328">Avvia il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-328">Launch the game.</span></span></li>
<li><span data-ttu-id="3eeca-329">Inizia una nuova partita.</span><span class="sxs-lookup"><span data-stu-id="3eeca-329">Start a new game.</span></span></li>
<li><span data-ttu-id="3eeca-330">Salvare il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-330">Save the game.</span></span> <span data-ttu-id="3eeca-331">Durante il processo di salvataggio, verificare che il gioco venga salvato usando il nome Salva: il primo gioco Salva.</span><span class="sxs-lookup"><span data-stu-id="3eeca-331">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="3eeca-332">Tornare al menu principale.</span><span class="sxs-lookup"><span data-stu-id="3eeca-332">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="3eeca-333">Provare a caricare il gioco appena salvato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-333">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="3eeca-334">Verificare che il gioco non riscontri errori durante la gestione di caratteri file system non supportati, ad esempio \/: \*?</span><span class="sxs-lookup"><span data-stu-id="3eeca-334">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="3eeca-335">&quot; < o > se il gioco ti consente, denominare il gioco salvato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-335">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="3eeca-336">Se l'utente è autorizzato a assegnare un nome al profilo e/o a un carattere o a salvare le partite, verificare che il gioco non riscontri errori quando si usano nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-336">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="3eeca-337">3. installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-337">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="3eeca-338">3,1 installazione semplificata</span><span class="sxs-lookup"><span data-stu-id="3eeca-338">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-339">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-339">Windows 7</span></span><br/> <span data-ttu-id="3eeca-340">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-340">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-341">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-341">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-342">I giochi con un'installazione tradizionale devono fornire un percorso semplificato nell'interfaccia utente di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-342">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-343">Inserire il disco del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-343">Insert the game disc.</span></span></li>
<li><span data-ttu-id="3eeca-344">Verificare che il gioco non visualizzi più di un contratto di licenza End-User (EULA).</span><span class="sxs-lookup"><span data-stu-id="3eeca-344">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="3eeca-345">Se il gioco supporta un'opzione di installazione personalizzata o avanzata, verificare che questa opzione sia accessibile durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-345">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="3eeca-346">Verificare che l'opzione di installazione predefinita ignori tutte le selezioni di input dell'utente per il processo di installazione (selezione cartella di installazione, selezione componenti e così via).</span><span class="sxs-lookup"><span data-stu-id="3eeca-346">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="3eeca-347">Verificare che il processo di installazione del gioco non richieda la configurazione del componente del sistema operativo (installazione di DirectX, Runtime di Visual C e così via).</span><span class="sxs-lookup"><span data-stu-id="3eeca-347">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="3eeca-348">Verificare che il processo di installazione del gioco non richieda l'interazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="3eeca-348">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="3eeca-349">Verificare che il gioco venga eseguito automaticamente o che al termine del processo di installazione sia presente un menu di avvio.</span><span class="sxs-lookup"><span data-stu-id="3eeca-349">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="3eeca-350">Verificare che il processo di disinstallazione del gioco rimuova tutti i file dei componenti del sistema operativo non ridistribuiti e installati e cancelli tutte le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3eeca-350">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="3eeca-351">La pulizia di tutti i dati e le impostazioni per utente (ad esempio giochi salvati) non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="3eeca-351">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="3eeca-352">3,2 supporto del controllo dell'account utente per l'installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-352">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-353">Windows 7</span></span><br/> <span data-ttu-id="3eeca-354">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-354">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="3eeca-355">Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-355">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="3eeca-356">I giochi devono pertanto eseguire attività per singolo utente durante la prima esecuzione separatamente dall'installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-356">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-357">Verificare che sia possibile installare il gioco come utente Jane.</span><span class="sxs-lookup"><span data-stu-id="3eeca-357">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="3eeca-358">Questa operazione richiederà diritti elevati durante il processo di installazione/installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-358">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="3eeca-359">Verificare che il processo di installazione del gioco chieda all'utente Jane di elevare le credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="3eeca-359">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="3eeca-360">La richiesta di elevazione verrà rilevata quando l'utente tenta di installare.</span><span class="sxs-lookup"><span data-stu-id="3eeca-360">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="3eeca-361">Scegliere di eseguire l'autorun del gioco al termine dell'installazione, se non è già stato fatto, o di avviarlo dal menu visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-361">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="3eeca-362">Una volta in gioco, creare un nuovo profilo, riprodurre e salvare un gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-362">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="3eeca-363">Uscire dal gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-363">Exit the game.</span></span></li>
<li><span data-ttu-id="3eeca-364">Riavviare il gioco e verificare che l'account utente Jane possa accedere a profili utente e giochi salvati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-364">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="3eeca-365">3,3 installare in cartelle corrette</span><span class="sxs-lookup"><span data-stu-id="3eeca-365">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-366">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-366">Windows 7</span></span><br/> <span data-ttu-id="3eeca-367">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-367">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-368">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-368">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-369">Per impostazione predefinita, i giochi devono essere installati nella cartella programmi.</span><span class="sxs-lookup"><span data-stu-id="3eeca-369">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="3eeca-370">I dati utente devono essere scritti alla prima esecuzione e non durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-370">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-371">Installare il gioco usando il tipo di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="3eeca-371">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="3eeca-372">Verificare che il gioco sia stato installato nei file di programma.</span><span class="sxs-lookup"><span data-stu-id="3eeca-372">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-373">Se il test non riesce, verificare che il gioco sia destinato all'installazione per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-373">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="3eeca-374">In caso affermativo, si tratta di un errore.</span><span class="sxs-lookup"><span data-stu-id="3eeca-374">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="3eeca-375">3,4 installare correttamente le risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-375">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-376">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-376">Windows 7</span></span><br/> <span data-ttu-id="3eeca-377">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-377">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-378">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-378">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-379">Le applicazioni non devono tentare di installare file o chiavi del registro di sistema protetti da Protezione risorse di Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="3eeca-379">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="3eeca-380">Verificare che durante il processo di installazione non vengano visualizzate finestre di dialogo Protezione risorse di Windows WRP.</span><span class="sxs-lookup"><span data-stu-id="3eeca-380">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="3eeca-381">3,5 evitare il riavvio durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-381">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-382">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-382">Windows 7</span></span><br/> <span data-ttu-id="3eeca-383">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-383">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-384">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-384">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-385">Il programma di installazione del gioco non deve presupporre che l'installazione dei componenti di Windows dai pacchetti di ridistribuzione richieda un riavvio, a meno che il riavvio non sia indicato da un risultato restituito o dalla documentazione Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3eeca-385">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-386">Installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-386">Install the game.</span></span></li>
<li><span data-ttu-id="3eeca-387">Verificare che il gioco non richieda il riavvio del sistema dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-387">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-388">Se un Microsoft System Update REDIST richiede un riavvio, procedere come segue: completare l'installazione del gioco, disinstallare il gioco e reinstallare il gioco una seconda volta.</span><span class="sxs-lookup"><span data-stu-id="3eeca-388">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="3eeca-389">Il processo di installazione del gioco non deve richiedere un riavvio in questa seconda installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-389">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="3eeca-390">3,6 usare correttamente il controllo delle versioni dei file</span><span class="sxs-lookup"><span data-stu-id="3eeca-390">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-391">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-391">Windows 7</span></span><br/> <span data-ttu-id="3eeca-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-392">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-393">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-393">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-394">Il programma di installazione del gioco deve verificare in modo corretto che siano installate le versioni dei file più recenti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-394">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="3eeca-395">L'installazione di un gioco non deve mai far regredire alcun file che non viene prodotto o condiviso da applicazioni che non vengono generate.</span><span class="sxs-lookup"><span data-stu-id="3eeca-395">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-396">Prima di installare il gioco, creare uno snapshot di pre-installazione di system32.</span><span class="sxs-lookup"><span data-stu-id="3eeca-396">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-397">Creare una directory denominata G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="3eeca-397">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="3eeca-398">Visualizzare una finestra di comando (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="3eeca-398">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="3eeca-399">Passare a c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="3eeca-399">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="3eeca-400">Digitare dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="3eeca-400">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="3eeca-401">Creare uno snapshot di post-installazione di system32.</span><span class="sxs-lookup"><span data-stu-id="3eeca-401">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="3eeca-402">Visualizzare una finestra di comando (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="3eeca-402">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="3eeca-403">Passare a c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="3eeca-403">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="3eeca-404">Digitare dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="3eeca-404">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="3eeca-405">Verificare che il gioco non regressioni le versioni di file dei file non prodotte dal gioco (... dei file elencati nei due documenti confrontando pregame.txt postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="3eeca-405">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="3eeca-406">3,7 supporto \[ requisito condizionale Autorun\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-406">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-407">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-407">Windows 7</span></span><br/> <span data-ttu-id="3eeca-408">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-408">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-409">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-409">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-410">Per i giochi distribuiti su CD, DVD o altri supporti rimovibili che supportano l'esecuzione automatica, quando il disco viene inserito per la prima volta, l'applicazione deve essere eseguita automaticamente o richiedere all'utente di installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-410">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-411">I programmi di avvio automatico scritti per l'utilizzo nelle versioni di Windows precedenti a Windows Vista non devono utilizzare il Runtime .NET, perché questa tecnologia non è inclusa in Windows XP o nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-411">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="3eeca-412">Per ulteriori informazioni, fare riferimento a <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">giochi per i requisiti tecnici di Windows</a> 3,7, supporto di autorun.</span><span class="sxs-lookup"><span data-stu-id="3eeca-412">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="3eeca-413">Inserire il disco del gioco o il supporto.</span><span class="sxs-lookup"><span data-stu-id="3eeca-413">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="3eeca-414">Verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-414">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="3eeca-415">Windows Vista o Windows 7: verificare che il programma di avvio automatico del gioco non chieda all'utente Jane di elevare le credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="3eeca-415">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="3eeca-416">Verificare che l'eseguibile di autorun non richieda componenti predefiniti di REDIST, ad esempio .NET 3,5, librerie di Run-Time C e così via.</span><span class="sxs-lookup"><span data-stu-id="3eeca-416">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="3eeca-417">Verificare che la reinserimento del disco nell'unità dopo l'installazione non riavvii automaticamente l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-417">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="3eeca-418">4. affidabilità</span><span class="sxs-lookup"><span data-stu-id="3eeca-418">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="3eeca-419">4,1 eliminare i riavvii non necessari</span><span class="sxs-lookup"><span data-stu-id="3eeca-419">4.1 Eliminate Unnecessary Reboots</span></span>



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eeca-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-420">Windows 7</span></span><br/> <span data-ttu-id="3eeca-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-421">Windows Vista</span></span><br/> | <span data-ttu-id="3eeca-422">Tutti i programmi di installazione di applicazioni devono sfruttare le API di gestione riavvio per evitare il riavvio del sistema (vedere [requisito 3,5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="3eeca-422">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="3eeca-423">4,2 eliminare Application Verifier errori</span><span class="sxs-lookup"><span data-stu-id="3eeca-423">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-424">Windows 7</span></span><br/> <span data-ttu-id="3eeca-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-425">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-426">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-426">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-427">Il gioco non deve generare errori con Microsoft Application Verifier (AppVerifier), versione 4,0 o successiva, nei test seguenti:</span><span class="sxs-lookup"><span data-stu-id="3eeca-427">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="3eeca-428">Nozioni fondamentali: handle, heap, blocchi, memoria, TLS</span><span class="sxs-lookup"><span data-stu-id="3eeca-428">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="3eeca-429">Varie: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="3eeca-429">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-430">Usare lo strumento: AppVerifier 4,0 (o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="3eeca-430">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="3eeca-431">Installare AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="3eeca-431">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="3eeca-432">Avviare AppVerifier e selezionare file-> Aggiungi applicazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-432">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="3eeca-433">Individuare l'eseguibile del gioco, selezionarlo e fare clic sul &quot; &quot; pulsante Apri.</span><span class="sxs-lookup"><span data-stu-id="3eeca-433">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="3eeca-434">Nella &quot; sezione applicazioni &quot; selezionare l'eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-434">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="3eeca-435">Nella &quot; sezione test &quot; selezionare i test sopra elencati sotto le categorie &quot; nozioni di &quot; base &quot; e &quot; varie (deselezionare ThreadPool e TimeRollOver) e assicurarsi che tutti gli altri test non siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-435">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="3eeca-436">Avvia il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-436">Launch the game.</span></span></li>
<li><span data-ttu-id="3eeca-437">Verificare che il gioco non generi errori quando viene eseguito in Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="3eeca-437">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eeca-438">Per alcuni test è necessario eseguire completamente un debugger.</span><span class="sxs-lookup"><span data-stu-id="3eeca-438">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="3eeca-439">Potrebbe essere necessaria una versione di rilascio non protetta del file eseguibile del gioco, perché la tecnologia anti-cheat/anti-pirateria potrebbe interferire con AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-439">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="3eeca-440">4,3 supporto Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-440">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-441">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-441">Windows 7</span></span><br/> <span data-ttu-id="3eeca-442">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-442">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-443">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-443">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-444">I giochi devono gestire solo le eccezioni note e previste e Segnalazione errori Windows non devono essere disabilitate.</span><span class="sxs-lookup"><span data-stu-id="3eeca-444">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="3eeca-445">Se un errore, ad esempio una violazione di accesso, viene inserito in un gioco, deve consentire Segnalazione errori Windows di segnalare l'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-445">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="3eeca-446">Usare lo strumento: thread hijacker</span><span class="sxs-lookup"><span data-stu-id="3eeca-446">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="3eeca-447">Se l'applicazione si arresta in modo anomalo durante il test, verificare che il gioco venga visualizzato Segnalazione errori Windows correttamente e raccolga i dati di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="3eeca-447">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-448">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-448">Windows 7</span></span><br/> <span data-ttu-id="3eeca-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-449">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-450">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-450">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-451">Tutti i file eseguibili (ad esempio, file con estensione exe o dll) devono contenere un nome di prodotto, un nome della società e una versione del file accurati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-451">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="3eeca-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuale:</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-452"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="3eeca-453">Fare clic con il pulsante destro del mouse sui file eseguibili del gioco nel supporto di installazione di e in quelli installati sul disco rigido del computer.</span><span class="sxs-lookup"><span data-stu-id="3eeca-453">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="3eeca-454">Selezionare Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3eeca-454">Select Properties.</span></span></li>
<li><span data-ttu-id="3eeca-455">Windows XP: fare clic sulla scheda <strong>versione</strong> . Verificare che il nome del prodotto, il nome della società e i campi della versione del file siano stati popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-455">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="3eeca-456">Windows Vista o Windows 7: fare clic sulla scheda <strong>Dettagli</strong> . Verificare che i campi nome prodotto e versione file siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-456">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="3eeca-457">Il nome della società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3eeca-457">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="3eeca-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatizzato:</dt> </span><span class="sxs-lookup"><span data-stu-id="3eeca-458"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="3eeca-459">Usare lo strumento di test di Microsoft Games per Windows; vedere la <a href="#64-microsoft-games-for-windows-test-tool">sezione 6,4</a>.</span><span class="sxs-lookup"><span data-stu-id="3eeca-459">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eeca-460">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-460">Windows 7</span></span><br/> <span data-ttu-id="3eeca-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eeca-461">Windows Vista</span></span><br/> <span data-ttu-id="3eeca-462">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-462">Windows XP</span></span><br/></td>
<td><span data-ttu-id="3eeca-463">La normale uscita del gioco non può causare un errore di eccezione sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3eeca-463">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="3eeca-464">Dopo aver giocato il gioco per una normale sessione di gioco, verificare che il gioco non generi errori all'uscita.</span><span class="sxs-lookup"><span data-stu-id="3eeca-464">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="3eeca-465">5. script di test di esempio</span><span class="sxs-lookup"><span data-stu-id="3eeca-465">5. Sample Test Script</span></span>

<span data-ttu-id="3eeca-466">Questo è un esempio di un test tipico che usa i requisiti di test precedenti come guida.</span><span class="sxs-lookup"><span data-stu-id="3eeca-466">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="3eeca-467">strumenti di 5,1</span><span class="sxs-lookup"><span data-stu-id="3eeca-467">5.1 Tools</span></span>

-   <span data-ttu-id="3eeca-468">edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="3eeca-468">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="3eeca-469">edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="3eeca-469">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="3eeca-470">edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="3eeca-470">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="3eeca-471">edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="3eeca-471">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="3eeca-472">edizione a 32 bit di Windows XP SP2 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="3eeca-472">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="3eeca-473">edizione a 32 bit di Windows XP SP2 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="3eeca-473">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="3eeca-474">Monitor a schermo intero che supporta 1680 1050</span><span class="sxs-lookup"><span data-stu-id="3eeca-474">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="3eeca-475">Controller Xbox 360 per Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-475">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="3eeca-476">5,2 pre-installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-476">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="3eeca-477">Windows Vista e Windows 7: creazione di due utenti standard: Jane e Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-477">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="3eeca-478">Windows Vista e Windows 7: verificare che il controllo dell'account utente sia abilitato</span><span class="sxs-lookup"><span data-stu-id="3eeca-478">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="3eeca-479">Creare uno snapshot di pre-installazione di system32</span><span class="sxs-lookup"><span data-stu-id="3eeca-479">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="3eeca-480">Creare una directory denominata G4Wtest</span><span class="sxs-lookup"><span data-stu-id="3eeca-480">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="3eeca-481">Visualizzare una finestra di comando (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="3eeca-481">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="3eeca-482">Passare a c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="3eeca-482">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="3eeca-483">Digitare dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="3eeca-483">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="3eeca-484">Windows Vista e Windows 7: impostare su 150% DPI \[ 1,8\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-484">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="3eeca-485">Procedere con l' [installazione](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="3eeca-485">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="3eeca-486">5,3 installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-486">5.3 Install</span></span>

1.  <span data-ttu-id="3eeca-487">Accedi come utente Jane</span><span class="sxs-lookup"><span data-stu-id="3eeca-487">Log on as User Jane</span></span>
2.  <span data-ttu-id="3eeca-488">Inserire il disco del gioco nell'unità CD/DVD, verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-488">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="3eeca-489">Verificare che il processo di installazione del gioco chieda all'utente Jane di elevare le credenziali di amministratore \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-489">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="3eeca-490">Verificare che il programma di avvio automatico del gioco non chieda all'utente Jane di elevare le credenziali di amministratore \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-490">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="3eeca-491">Verificare che il gioco non visualizzi più di un contratto di licenza di End-User (EULA) \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-491">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="3eeca-492">Verificare che il gioco visualizzi le opzioni di installazione predefinite/semplici e personalizzate/avanzate \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-492">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="3eeca-493">Verificare che l'opzione di installazione predefinita/semplice ignori tutte le selezioni di input dell'utente per il processo di installazione (selezione cartella di installazione, selezione componenti e così via) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-493">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="3eeca-494">Verificare che il processo di installazione del gioco non richieda la configurazione del componente del sistema operativo (installazione di DirectX, librerie di Run-Time C e così via) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-494">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="3eeca-495">Verificare che il processo di installazione del gioco non richieda l'interazione del firewall \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-495">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="3eeca-496">Verificare che il processo di installazione del gioco non riscontri un errore relativo alla versione del sistema operativo \[ 2,5 \] \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-496">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="3eeca-497">Verificare che il processo di installazione del gioco non visualizzi finestre di dialogo di driver non firmate \[ 2,4\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-497">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="3eeca-498">Verificare che non venga visualizzata alcuna finestra di dialogo Protezione risorse di Windows (WRP) durante il processo di installazione \[ 3,4\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-498">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="3eeca-499">Verificare che il nuovo inserimento del disco nell'unità dopo l'installazione non riavvii automaticamente l'installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-499">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="3eeca-500">Verificare che il gioco non richieda il riavvio del sistema dopo l'installazione \[ 3,5\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-500">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="3eeca-501">Verificare che sia possibile installare il gioco come utente Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-501">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="3eeca-502">Verificare che venga eseguito automaticamente il gioco o che sia presente un menu di avvio al termine del processo di installazione \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-502">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="3eeca-503">Se il gioco viene eseguito automaticamente dopo l'installazione, passare al [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="3eeca-503">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="3eeca-504">Se il gioco ha lasciato un menu di avvio o non è stato possibile disinstallarlo, vedere la sezione [post-installazione](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="3eeca-504">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="3eeca-505">5,4 post-installazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-505">5.4 Post-Install</span></span>

1.  <span data-ttu-id="3eeca-506">Verificare che il gioco non disponga dei collegamenti di avvio sul desktop dell'utente \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-506">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="3eeca-507">Verificare che il gioco non disponga dei collegamenti di avvio nel menu Start \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-507">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="3eeca-508">Verificare che l'icona del gioco sia visualizzata in Windows Games Explorer \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-508">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="3eeca-509">Verificare che i metadati (Publisher, Developer, genre, data di rilascio, versione) nella parte inferiore visualizzino e siano corretti \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-509">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="3eeca-510">Verificare che nell'icona del gioco siano visualizzate le informazioni sugli indici Windows Experience (WEI) in Windows Games Explorer \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-510">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="3eeca-511">Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Esplora giochi di Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-511">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="3eeca-512">Verificare che il gioco visualizzi una classificazione di controllo parentale accurata in Windows Games Explorer \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-512">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="3eeca-513">Creare uno snapshot di post-installazione di system32</span><span class="sxs-lookup"><span data-stu-id="3eeca-513">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="3eeca-514">Visualizzare una finestra di comando (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="3eeca-514">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="3eeca-515">Passare a c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="3eeca-515">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="3eeca-516">Digitare dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="3eeca-516">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="3eeca-517">Verificare che il gioco non regressione le versioni dei file elencate nei due documenti confrontando pregame.txt con postgame.txt \[ 3,6\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-517">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="3eeca-518">Vai al [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="3eeca-518">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="3eeca-519">5,5 Runtime</span><span class="sxs-lookup"><span data-stu-id="3eeca-519">5.5 Runtime</span></span>

1.  <span data-ttu-id="3eeca-520">RUNTIME 1: se il menu Launch è presente, avviare il gioco da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-520">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="3eeca-521">Se il gioco è stato eseguito automaticamente o è stato avviato dal menu di avvio del gioco dopo l'installazione, eseguire le operazioni seguenti: in caso contrario, passare a RUNTIME 2:</span><span class="sxs-lookup"><span data-stu-id="3eeca-521">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="3eeca-522">Crea un profilo (se il gioco lo consente)</span><span class="sxs-lookup"><span data-stu-id="3eeca-522">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="3eeca-523">Avvia un nuovo gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-523">Start a new game</span></span>
    3.  <span data-ttu-id="3eeca-524">Salva il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-524">Save the game</span></span>
    4.  <span data-ttu-id="3eeca-525">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-525">Exit the game</span></span>
    5.  <span data-ttu-id="3eeca-526">Avvia il gioco da Esplora giochi</span><span class="sxs-lookup"><span data-stu-id="3eeca-526">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="3eeca-527">Verificare che il gioco venga avviato dall'icona di Esplora giochi \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-527">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="3eeca-528">Verificare che il gioco non richieda le credenziali di amministratore all'avvio \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-528">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="3eeca-529">Verificare che sia possibile accedere ai profili utente e salvare le partite dall'account utente Jane \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-529">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="3eeca-530">Vai al RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="3eeca-530">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="3eeca-531">RUNTIME 2: se il gioco non è stato eseguito automaticamente o Visualizza un avvio dal menu di avvio del gioco, si tratta di un errore \[ 3,1 \] . Tuttavia, il test può continuare normalmente:</span><span class="sxs-lookup"><span data-stu-id="3eeca-531">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="3eeca-532">Avvia il gioco da Esplora giochi</span><span class="sxs-lookup"><span data-stu-id="3eeca-532">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="3eeca-533">Verificare che il gioco venga avviato dall'icona di Esplora giochi \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-533">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="3eeca-534">Verificare che il gioco non richieda le credenziali di amministratore all'avvio \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-534">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="3eeca-535">Vai al RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="3eeca-535">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="3eeca-536">RUNTIME 3: se il gioco supporta un riquadro del gioco, verificare che il gioco riconosca il controller Xbox 360 per Windows come dispositivo di input \[ 1,4\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-536">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="3eeca-537">Se necessario, abilitare il controller tramite il menu opzioni</span><span class="sxs-lookup"><span data-stu-id="3eeca-537">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="3eeca-538">Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando i nomi di Xbox 360</span><span class="sxs-lookup"><span data-stu-id="3eeca-538">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="3eeca-539">Verificare che il sistema di gioco e menu siano controllabili con il controller Xbox 360 per Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-539">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="3eeca-540">Verificare che il controller Xbox 360 per Windows si comportano in base agli standard accettati</span><span class="sxs-lookup"><span data-stu-id="3eeca-540">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="3eeca-541">Impostare il video su \[ 1,5 \] :</span><span class="sxs-lookup"><span data-stu-id="3eeca-541">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="3eeca-542">Verificare che il gioco venga eseguito a una risoluzione di 4:3 proporzioni (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="3eeca-542">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="3eeca-543">Verificare che il gioco venga eseguito a una risoluzione di 16:9 proporzioni (1280 720)</span><span class="sxs-lookup"><span data-stu-id="3eeca-543">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="3eeca-544">Verificare che il gioco venga eseguito a una risoluzione di 16:10 proporzioni (1680 1050, 800 480 o 1152 720)</span><span class="sxs-lookup"><span data-stu-id="3eeca-544">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="3eeca-545">Verificare che il gioco chieda all'utente quando viene apportata una modifica alla risoluzione</span><span class="sxs-lookup"><span data-stu-id="3eeca-545">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="3eeca-546">Se non si accettano entro 15 secondi, verificare che venga ripristinata l'impostazione precedente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-546">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="3eeca-547">Verificare che il gioco non estenda l'immagine e a sua volta presenta un'area di visualizzazione più ampia</span><span class="sxs-lookup"><span data-stu-id="3eeca-547">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="3eeca-548">Verificare che il gioco non aggiunga barre nere a sinistra e a destra dell'area giochi</span><span class="sxs-lookup"><span data-stu-id="3eeca-548">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="3eeca-549">Se disponibile nelle impostazioni video, verificare che le opzioni di rendering del gioco siano predefinite per Direct3D \[ 1,7 \] . in caso contrario, procedere con i [test automatizzati](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="3eeca-549">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="3eeca-550">Se richiesto o se l'opzione è disponibile, creare un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-550">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="3eeca-551">Verificare che il gioco non riscontri errori durante l'uso di nomi di file lunghi \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-551">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="3eeca-552">Avviare un nuovo gioco, creare un gioco e verificare che nel gioco non si verifichino errori durante la gestione di caratteri file system non supportati \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-552">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="3eeca-553">Verificare che il gioco ALT + TAB sia corretto al desktop di Windows \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-553">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="3eeca-554">Cambiare gli utenti con il gioco in esecuzione facendo clic su Start-> utente switch</span><span class="sxs-lookup"><span data-stu-id="3eeca-554">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="3eeca-555">Accedi come Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-555">Log on as Toby</span></span>
    3.  <span data-ttu-id="3eeca-556">Verificare che il gioco venga avviato come utente Toby mentre è ancora in esecuzione come utente Jane \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-556">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="3eeca-557">Verificare che il gioco non riscontri errori per l'utente Toby o l'utente Jane durante il passaggio dell'utente processo \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-557">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="3eeca-558">Verificare che non sia possibile ascoltare audio dalla sessione di gioco originale \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-558">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="3eeca-559">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-559">Exit the game</span></span>
    7.  <span data-ttu-id="3eeca-560">Disconnetti Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-560">Log off Toby</span></span>
    8.  <span data-ttu-id="3eeca-561">Tornare all'utente originale in cui è in esecuzione il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-561">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="3eeca-562">ALT + TAB di nuovo nel gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-562">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="3eeca-563">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-563">Exit the game</span></span>
10. <span data-ttu-id="3eeca-564">Passa a [post-Runtime](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="3eeca-564">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="3eeca-565">5,6 post-Runtime</span><span class="sxs-lookup"><span data-stu-id="3eeca-565">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="3eeca-566">Verificare che il gioco non generi errori all'uscita \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-566">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="3eeca-567">Verificare che il gioco sia installato nei file di programma \[ 3,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-567">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="3eeca-568">Passare a [controlli padre](/windows)</span><span class="sxs-lookup"><span data-stu-id="3eeca-568">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="3eeca-569">5,7 controlli parentali</span><span class="sxs-lookup"><span data-stu-id="3eeca-569">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="3eeca-570">Aprire i controlli padre nel pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="3eeca-570">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="3eeca-571">Verificare che il gioco visualizzi una valutazione del controllo parentale accurata sotto il titolo del gioco nel pannello di controllo dei controlli padre \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-571">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="3eeca-572">Vedere il test case \[ 1,2 \] per i test seguenti:</span><span class="sxs-lookup"><span data-stu-id="3eeca-572">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="3eeca-573">Dopo aver impostato i controlli padre su "on", verificare che il gioco venga eseguito con queste impostazioni come utente Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-573">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="3eeca-574">Disconnettersi e accedere come Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-574">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="3eeca-575">Verificare che il gioco venga eseguito con queste impostazioni come utente Toby \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-575">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="3eeca-576">Disconnettersi e accedere come Jane</span><span class="sxs-lookup"><span data-stu-id="3eeca-576">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="3eeca-577">Nella sezione Parental Control (controllo parentale) impedire all'utente Toby di visualizzare i giochi un livello di ESRB superiore e superiore del gioco appena installato</span><span class="sxs-lookup"><span data-stu-id="3eeca-577">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="3eeca-578">Esempio: se il gioco è classificato E, impostarlo in modo che Toby possa riprodurre solo giochi con classificazione C</span><span class="sxs-lookup"><span data-stu-id="3eeca-578">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="3eeca-579">Verificare che il gioco venga eseguito con queste impostazioni come utente Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-579">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="3eeca-580">Disconnetti e accedi come utente Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-580">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="3eeca-581">Verificare che il gioco non venga avviato all'utente Toby quando ESRB è bloccato dall'utente Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-581">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="3eeca-582">Disconnetti come utente Toby e viceversa come utente Jane</span><span class="sxs-lookup"><span data-stu-id="3eeca-582">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="3eeca-583">Se è stato modificato in precedenza, ripristinare le impostazioni di ESRB</span><span class="sxs-lookup"><span data-stu-id="3eeca-583">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="3eeca-584">Se non sono presenti impostazioni di ESRB, selezionare "blocca o Consenti giochi specifici" e selezionare il gioco per nome</span><span class="sxs-lookup"><span data-stu-id="3eeca-584">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="3eeca-585">Disconnettersi come Jane e come Toby</span><span class="sxs-lookup"><span data-stu-id="3eeca-585">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="3eeca-586">Verificare che il gioco non venga avviato all'utente Toby quando il nome del file/EXE è bloccato dall'utente Jane \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-586">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="3eeca-587">Disconnettersi come Toby e tornare indietro come Jane</span><span class="sxs-lookup"><span data-stu-id="3eeca-587">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="3eeca-588">Come Jane, aprire controlli utente-> restrizioni applicazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-588">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="3eeca-589">Fare clic su "Toby può utilizzare solo i programmi consentiti", quindi fare clic su OK, ovvero non consentire alcun exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-589">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="3eeca-590">Fare clic sulla casella Deseleziona tutto, quindi fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="3eeca-590">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="3eeca-591">Passare a controlli utente \| giochi controlli e consentire il gioco specifico usando la classificazione ESRB</span><span class="sxs-lookup"><span data-stu-id="3eeca-591">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="3eeca-592">Disconnettersi con Jane e accedere come Toby e provare a riprodurre il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-592">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="3eeca-593">Verificare che il gioco non sia bloccato e che Toby possa riprodurlo quando l'impostazione "Consenti nessun exe" è impostata su \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-593">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="3eeca-594">Disconnetti come utente Toby e viceversa come utente Jane</span><span class="sxs-lookup"><span data-stu-id="3eeca-594">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="3eeca-595">Passare a controlli padre nel pannello di controllo e rimuovere le restrizioni</span><span class="sxs-lookup"><span data-stu-id="3eeca-595">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="3eeca-596">Verificare che entrambi gli utenti possano ora riprodurre il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-596">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="3eeca-597">Procedi ai [test automatizzati](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="3eeca-597">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="3eeca-598">5,8 test automatizzati</span><span class="sxs-lookup"><span data-stu-id="3eeca-598">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="3eeca-599">Verificare che il gioco non generi errori quando viene eseguito in Application Verifier. vedere la documentazione dello strumento di test di personalizzazione \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-599">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="3eeca-600">Verificare che i file eseguibili del gioco contengano manifesti. vedere la documentazione dello strumento di test di personalizzazione \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-600">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="3eeca-601">Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia "AsInvoker". vedere la documentazione dello strumento di test di personalizzazione \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-601">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="3eeca-602">Procedi ad [altri test](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="3eeca-602">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="3eeca-603">5,9 altri test</span><span class="sxs-lookup"><span data-stu-id="3eeca-603">5.9 Other Tests</span></span>

1.  <span data-ttu-id="3eeca-604">Verificare che i file eseguibili del gioco contengano una firma digitale \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-604">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="3eeca-605">Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-605">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="3eeca-606">Verificare che il gioco non riscontri un errore a causa di eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-606">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="3eeca-607">Forzare l'arresto anomalo dell'applicazione durante il test e verificare che il gioco venga visualizzato Segnalazione errori Windows correttamente e raccoglie i dati di arresto anomalo \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-607">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="3eeca-608">Verificare che i riepiloghi di file 4,3 siano corretti \[\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-608">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="3eeca-609">Fare clic su Start-> computer</span><span class="sxs-lookup"><span data-stu-id="3eeca-609">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="3eeca-610">Passare alla directory del gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-610">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="3eeca-611">Nella finestra di ricerca digitare \* . dll</span><span class="sxs-lookup"><span data-stu-id="3eeca-611">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="3eeca-612">Per ogni file: fare clic con il pulsante destro del mouse sul file e scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3eeca-612">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="3eeca-613">In Windows XP: fare clic sulla scheda versione. Verificare che il nome del prodotto, il nome della società e i campi della versione del file siano stati popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-613">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="3eeca-614">\[4,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-614">\[4.3\]</span></span>
        -   <span data-ttu-id="3eeca-615">In Windows Vista e Windows 7: fare clic sulla scheda Dettagli. Verificare che i campi nome prodotto e versione file siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-615">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="3eeca-616">Il nome della società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7 \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-616">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="3eeca-617">Ripeti questo controllo per i file exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-617">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="3eeca-618">Avvia il gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-618">Launch the game.</span></span>

    1.  <span data-ttu-id="3eeca-619">Premere CTRL + ALT + CANC</span><span class="sxs-lookup"><span data-stu-id="3eeca-619">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="3eeca-620">Fare clic sulla freccia "opzioni di arresto"</span><span class="sxs-lookup"><span data-stu-id="3eeca-620">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="3eeca-621">Fare clic su Riavvia</span><span class="sxs-lookup"><span data-stu-id="3eeca-621">Click Restart</span></span>
    4.  <span data-ttu-id="3eeca-622">Verify Game non blocca l'arresto \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-622">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="3eeca-623">Procedere alla [disinstallazione](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="3eeca-623">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="3eeca-624">5,10 Disinstalla</span><span class="sxs-lookup"><span data-stu-id="3eeca-624">5.10 Uninstall</span></span>

-   <span data-ttu-id="3eeca-625">Verificare che il processo di disinstallazione del gioco elimini tutti i file dei componenti del sistema operativo installati e non ridistribuiti e elimini tutte le impostazioni \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-625">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="3eeca-626">Verificare in Windows Vista o Windows 7 che il pannello di controllo sia l'unico modo per rimuovere il programma \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="3eeca-626">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="3eeca-627">Note sugli strumenti di test</span><span class="sxs-lookup"><span data-stu-id="3eeca-627">Test Tool Notes</span></span>

<span data-ttu-id="3eeca-628">Si tratta di note per ciascuno degli strumenti di test elencati nei requisiti di test precedenti.</span><span class="sxs-lookup"><span data-stu-id="3eeca-628">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="3eeca-629">6,1 AppVerifier 4,0 (o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="3eeca-629">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="3eeca-630">**Test case: 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="3eeca-630">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="3eeca-631">Alcune applicazioni non vengono eseguite con AppVerifier in esecuzione, a causa della protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="3eeca-631">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="3eeca-632">Questo problema può essere risolto eseguendo con una versione di rilascio non protetta del file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-632">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="3eeca-633">Installare AppVerifier 4,0 (o versione successiva) in un computer che esegue Windows XP</span><span class="sxs-lookup"><span data-stu-id="3eeca-633">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="3eeca-634">Avviare AppVerifier e fare clic su file-> Aggiungi applicazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-634">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="3eeca-635">Individuare il file eseguibile del gioco, selezionarlo e fare clic su Apri</span><span class="sxs-lookup"><span data-stu-id="3eeca-635">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="3eeca-636">Nella sezione "applicazioni" selezionare il file eseguibile del gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-636">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="3eeca-637">Nella sezione "Nozioni di base" selezionare i test seguenti:</span><span class="sxs-lookup"><span data-stu-id="3eeca-637">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="3eeca-638">Selettori</span><span class="sxs-lookup"><span data-stu-id="3eeca-638">Handles</span></span>
    -   <span data-ttu-id="3eeca-639">Heap</span><span class="sxs-lookup"><span data-stu-id="3eeca-639">Heaps</span></span>
    -   <span data-ttu-id="3eeca-640">Locks</span><span class="sxs-lookup"><span data-stu-id="3eeca-640">Locks</span></span>
    -   <span data-ttu-id="3eeca-641">Memoria</span><span class="sxs-lookup"><span data-stu-id="3eeca-641">Memory</span></span>
    -   <span data-ttu-id="3eeca-642">TLS</span><span class="sxs-lookup"><span data-stu-id="3eeca-642">TLS</span></span>

6.  <span data-ttu-id="3eeca-643">Nella sezione "varie" selezionare i test seguenti:</span><span class="sxs-lookup"><span data-stu-id="3eeca-643">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="3eeca-644">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="3eeca-644">DangerousAPIs</span></span>
    -   <span data-ttu-id="3eeca-645">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="3eeca-645">DirtyStacks</span></span>

7.  <span data-ttu-id="3eeca-646">Assicurarsi che tutti gli altri test non siano selezionati</span><span class="sxs-lookup"><span data-stu-id="3eeca-646">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="3eeca-647">Avvia il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-647">Launch the game</span></span>
9.  <span data-ttu-id="3eeca-648">Gioca il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-648">Play the game</span></span>
10. <span data-ttu-id="3eeca-649">Chiudere il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-649">Close the game</span></span>
11. <span data-ttu-id="3eeca-650">In AppVerifier selezionare Visualizza-> log</span><span class="sxs-lookup"><span data-stu-id="3eeca-650">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="3eeca-651">Nella sezione "applicazioni" selezionare il file app. exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-651">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="3eeca-652">Nella sezione "log" selezionare il file di log e osservare il numero di errori.</span><span class="sxs-lookup"><span data-stu-id="3eeca-652">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="3eeca-653">Se non sono presenti errori, terminare i test di AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="3eeca-653">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="3eeca-654">Se sono presenti errori, fare clic sul pulsante Visualizza.</span><span class="sxs-lookup"><span data-stu-id="3eeca-654">If there are errors, click the View button</span></span>
14. <span data-ttu-id="3eeca-655">Eseguire una ricerca nel documento (CTRL + F) per gravità = "errore</span><span class="sxs-lookup"><span data-stu-id="3eeca-655">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="3eeca-656">Crea bug in base alla parte dell'errore LayerName =</span><span class="sxs-lookup"><span data-stu-id="3eeca-656">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="3eeca-657">Test del manifesto 6,2-mt.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-657">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="3eeca-658">**Test case: 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="3eeca-658">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="3eeca-659">Questo strumento viene eseguito da un prompt dei comandi in cui si trova MT.exe.</span><span class="sxs-lookup"><span data-stu-id="3eeca-659">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="3eeca-660">Esempio:</span><span class="sxs-lookup"><span data-stu-id="3eeca-660">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="3eeca-661">Fare clic su Start-> Esegui-> digitare cmd e fare clic sul pulsante OK</span><span class="sxs-lookup"><span data-stu-id="3eeca-661">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="3eeca-662">Eseguire lo strumento mt.exe per generare un file con estensione manifest per ogni file exe che viene installato con il gioco</span><span class="sxs-lookup"><span data-stu-id="3eeca-662">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="3eeca-663">Aprire il file con estensione manifest generato</span><span class="sxs-lookup"><span data-stu-id="3eeca-663">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="3eeca-664">Verificare che ogni file con estensione exe includa le seguenti richieste:</span><span class="sxs-lookup"><span data-stu-id="3eeca-664">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="3eeca-665">Il livello di esecuzione richiesto deve essere presente per ogni file e dpiAware deve essere presente per almeno il file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-665">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="3eeca-666">aspirato thread 6,3-threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-666">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="3eeca-667">Questo strumento viene eseguito da un prompt dei comandi in cui si trova threadhijacker.exe.</span><span class="sxs-lookup"><span data-stu-id="3eeca-667">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="3eeca-668">Esempio:</span><span class="sxs-lookup"><span data-stu-id="3eeca-668">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="3eeca-669">Dove Str è il nome \_ del \_program.exe</span><span class="sxs-lookup"><span data-stu-id="3eeca-669">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="3eeca-670">Aprire Gestione attività, fare clic sulla scheda processi e individuare il nome del file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="3eeca-670">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="3eeca-671">Aprire un prompt dei comandi in modalità di amministrazione</span><span class="sxs-lookup"><span data-stu-id="3eeca-671">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="3eeca-672">Passare alla directory in cui threadhijacker.exe è</span><span class="sxs-lookup"><span data-stu-id="3eeca-672">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="3eeca-673">Tipo: **threadhijacker.exe/Process:** Str, dove Str è il nome del file eseguibile che si desidera raggiungere</span><span class="sxs-lookup"><span data-stu-id="3eeca-673">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="3eeca-674">6,4 Microsoft Games per Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="3eeca-674">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="3eeca-675">Questo strumento si trova in DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="3eeca-675">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="3eeca-676">Una volta installato l'SDK in un computer, il programma di installazione per lo strumento di test giochi per Windows può essere inserito nel computer di test e installato.</span><span class="sxs-lookup"><span data-stu-id="3eeca-676">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="3eeca-677">Individuare il programma di installazione di Microsoft Games for Windows Test Tool nel computer di sviluppo in cui è installato DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="3eeca-677">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="3eeca-678">Per impostazione predefinita, viene inserito nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="3eeca-678">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="3eeca-679">Copiare il programma di installazione (MicrosoftGFWTestTool.msi/setup.exe) nel computer di test.</span><span class="sxs-lookup"><span data-stu-id="3eeca-679">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="3eeca-680">Eseguire il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-680">Run the installer.</span></span>
3.  <span data-ttu-id="3eeca-681">Avviare lo strumento di test di Microsoft Games per Windows.</span><span class="sxs-lookup"><span data-stu-id="3eeca-681">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="3eeca-682">Nel campo **elenco progetti** sostituire **Crea nuovo progetto** con il nome del titolo e fare clic su **Crea nuovo**.</span><span class="sxs-lookup"><span data-stu-id="3eeca-682">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="3eeca-683">Attendere il completamento della linea di base.</span><span class="sxs-lookup"><span data-stu-id="3eeca-683">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="3eeca-684">Immettere le informazioni eventualmente disponibili nella sezione **informazioni sul gioco** e fare clic su **Aggiorna informazioni sul gioco**.</span><span class="sxs-lookup"><span data-stu-id="3eeca-684">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="3eeca-685">Fare clic sulla scheda **test case** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-685">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="3eeca-686">A partire dalla parte superiore, procedere con i test case, facendo clic su **superato** o **non superato** in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="3eeca-686">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="3eeca-687">Per informazioni dettagliate sull'inclusione di un bug nel report, vedere la sezione relativa alla scrittura di un bug, più avanti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="3eeca-687">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="3eeca-688">Tornare alla scheda **progetti** dopo aver esaminato il report controllando le schede **report** e **modifica bug** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-688">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="3eeca-689">Fare clic su **Compila report**.</span><span class="sxs-lookup"><span data-stu-id="3eeca-689">Click **Compile Report**.</span></span>

    <span data-ttu-id="3eeca-690">Una finestra verrà aperta al termine della compilazione del report.</span><span class="sxs-lookup"><span data-stu-id="3eeca-690">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="3eeca-691">Qui sarà disponibile un. Nome file ZIP *nomeprogetto* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="3eeca-691">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="3eeca-692">Questo file contiene tutti i log e i risultati raccolti durante il superamento del test.</span><span class="sxs-lookup"><span data-stu-id="3eeca-692">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="3eeca-693">Scrittura di un bug</span><span class="sxs-lookup"><span data-stu-id="3eeca-693">Writing a Bug</span></span>

<span data-ttu-id="3eeca-694">Per scrivere un report sui bug è possibile procedere in due modi: è possibile eseguire i test case e fare clic su **Fail** quando il titolo non riesce a test case oppure è possibile fare clic sulla scheda **modifica bug** e aggiungere manualmente un report sui bug.</span><span class="sxs-lookup"><span data-stu-id="3eeca-694">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="3eeca-695">Fare clic su Fail in un test case</span><span class="sxs-lookup"><span data-stu-id="3eeca-695">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="3eeca-696">Quando si fa clic su **Fail** in una test case, l'elenco a discesa **tipo di problema** verrà impostato automaticamente sul tipo di test case.</span><span class="sxs-lookup"><span data-stu-id="3eeca-696">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="3eeca-697">Aggiungere una breve descrizione al campo **title** che descrive brevemente il problema.</span><span class="sxs-lookup"><span data-stu-id="3eeca-697">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="3eeca-698">Aggiungere una descrizione dettagliata del problema al campo **comportamento osservato** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-698">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="3eeca-699">Se necessario, aggiungere il valore previsto (in contrapposizione a una descrizione del problema) al campo **comportamento previsto** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-699">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="3eeca-700">Aggiungere una descrizione dettagliata di come riprodurre il problema nel campo ripetizione dei **passaggi** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-700">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="3eeca-701">Al termine, fare clic sul pulsante **Salva** .</span><span class="sxs-lookup"><span data-stu-id="3eeca-701">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="3eeca-702">Aggiunta manuale di un bug</span><span class="sxs-lookup"><span data-stu-id="3eeca-702">Manually Adding a Bug</span></span>

<span data-ttu-id="3eeca-703">Questo processo equivale a fare clic su **Fail (errore**), ad eccezione dell'elenco a discesa popolato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3eeca-703">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="3eeca-704">In questo caso, selezionare il tipo di errore TCR appropriato oppure selezionare un **\* \* problema \* \* non TR** per i bug che non rientrano nell'intervallo TR, ma devono comunque essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="3eeca-704">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="3eeca-705">Risorse</span><span class="sxs-lookup"><span data-stu-id="3eeca-705">Resources</span></span>

<dl> <dt>

<span data-ttu-id="3eeca-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Giochi per Windows: requisiti tecnici</span><span class="sxs-lookup"><span data-stu-id="3eeca-706"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="3eeca-707">Giochi per i requisiti tecnici di Windows: procedure consigliate per giochi in Windows XP, Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eeca-707">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="3eeca-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3eeca-708"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="3eeca-709">SDK di Windows</span><span class="sxs-lookup"><span data-stu-id="3eeca-709">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="3eeca-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Linee guida per il controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="3eeca-710"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-711">[Requisiti per lo sviluppo di applicazioni Windows Vista per la compatibilità con controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3eeca-711">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Informazioni Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3eeca-712"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="3eeca-713">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3eeca-713">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="3eeca-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portale per sviluppatori WinQual</span><span class="sxs-lookup"><span data-stu-id="3eeca-714"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="3eeca-715">Servizi online di qualità Windows (Winqual)</span><span class="sxs-lookup"><span data-stu-id="3eeca-715">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="3eeca-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portale per sviluppatori DirectX</span><span class="sxs-lookup"><span data-stu-id="3eeca-716"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="3eeca-717">[Centro per sviluppatori DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3eeca-717">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="3eeca-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sui giochi per Windows e DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="3eeca-718"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="3eeca-719">Giochi per Windows e DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="3eeca-719">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="3eeca-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli su DirectX</span><span class="sxs-lookup"><span data-stu-id="3eeca-720"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="3eeca-721">Articoli tecnici su DirectX</span><span class="sxs-lookup"><span data-stu-id="3eeca-721">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

