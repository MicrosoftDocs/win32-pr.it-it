---
title: 'Test case dei giochi di Windows: procedure consigliate per giochi su Windows XP, Windows Vista, Windows 7 e Windows 8'
description: Questo articolo fornisce test case per giochi per Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120276"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="1e0bd-103">Test case di Giochi per Windows: procedure consigliate per i giochi in Windows XP, Windows Vista, Windows 7 e Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e0bd-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="1e0bd-104">Questo articolo fornisce test case per giochi per Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="1e0bd-105">Come usare questo articolo</span><span class="sxs-lookup"><span data-stu-id="1e0bd-105">How to Use This Article</span></span>

<span data-ttu-id="1e0bd-106">Questo articolo contiene tre sezioni principali:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="1e0bd-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisiti di test**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-108">Ogni requisito di test in questo documento ha quattro sezioni principali: un titolo e una tabella con tre sezioni di primo piano (colonna a sinistra, in alto a destra, in basso a destra).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="1e0bd-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo</span><span class="sxs-lookup"><span data-stu-id="1e0bd-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-110">Nome dell'test case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Casella, colonna all'estrema sinistra</span><span class="sxs-lookup"><span data-stu-id="1e0bd-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-112">Nomi dei sistemi operativi a cui si test case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Casella, in alto a destra</span><span class="sxs-lookup"><span data-stu-id="1e0bd-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-114">Breve riepilogo del test case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Casella, in basso a destra</span><span class="sxs-lookup"><span data-stu-id="1e0bd-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-116">Dettagli dell'effettiva test case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1e0bd-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script di test di esempio**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-118">Questa sezione è un esempio della sequenza che verrebbe seguito da un tipico passaggio di test se si usano i requisiti di test come guida.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Note dello strumento di test**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-120">Questa sezione contiene note dettagliate su ognuno degli strumenti di test usati per verificare le condizioni di superati o non superati nei requisiti di test.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="1e0bd-121">Requisiti di test</span><span class="sxs-lookup"><span data-stu-id="1e0bd-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="1e0bd-122">1. Requisiti del gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="1e0bd-123">1.1 Windows Games Explorer</span><span class="sxs-lookup"><span data-stu-id="1e0bd-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-124">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-126">Il gioco deve essere visibile all'interno Games Explorer in Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="1e0bd-127">Quando questa opzione è selezionata, il gioco deve visualizzare anche i metadati corretti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="1e0bd-128">L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altra posizione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="1e0bd-129">Non è necessario creare attività e collegamenti per la rimozione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-130">Dopo aver installato il gioco, aprire Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="1e0bd-131">Verificare che l'icona del gioco sia visualizzata Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="1e0bd-132">Fare clic con il pulsante destro del mouse sull'icona e testare ogni attività di & di supporto.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="1e0bd-133">Fare clic sull'icona e verificare che i metadati (editore, sviluppatore, genere, data di rilascio, versione) nella parte inferiore siano visualizzati e siano corretti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="1e0bd-134">Verificare che l'icona del gioco visualizzi Indice prestazioni Windows (WEI) in Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="1e0bd-135">Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="1e0bd-136">Se i collegamenti ipertestuali non vengono visualizzati, è possibile che il file exe non sia firmato. Vedere la sezione <a href="#23-sign-files">2.3.</a></span><span class="sxs-lookup"><span data-stu-id="1e0bd-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="1e0bd-137">Verificare che il gioco visualizzi una valutazione accurata del controllo genitori Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="1e0bd-138">Se viene indicato che non è stata impostata larate, verificare che si tratta di un gioco senzarate. In caso contrario, si tratta di un indicatore che indica che l'exe non è firmato; vedere la sezione <a href="#23-sign-files">2.3.</a></span><span class="sxs-lookup"><span data-stu-id="1e0bd-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="1e0bd-139">Verificare che il gioco non inseri i collegamenti di avvio sul desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="1e0bd-140">Fare clic su Start -> Tutti i programmi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="1e0bd-141">Verificare che il gioco non inseri i collegamenti di avvio nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="1e0bd-142">Verificare che il gioco non posiziona i collegamenti di disinstallazione nel menu Start all'esterno Pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="1e0bd-143">Se il gioco viene distribuito digitalmente, verificare che il provider di servizi sia visualizzato in Windows Games Explorer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="1e0bd-144">1.2 Windows Family Safety/Controllo genitori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-145">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-147">Il gioco deve essere eseguito nel contesto di un &quot; utente &quot; standard.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="1e0bd-148">Controllo genitori deve essere in grado di bloccare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="1e0bd-149">Verificare che la funzione definita dall'utente abbia nomi EXE.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-150">Creare un account utente standard in Windows Vista o Windows 7 denominato Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="1e0bd-151">Start -> Pannello di controllo -> Add or Remove User Accounts -> Create New Account</span><span class="sxs-lookup"><span data-stu-id="1e0bd-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="1e0bd-152">Come Jane, dall'account amministratore configurare Controllo genitori per il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="1e0bd-153">Start -> Pannello di controllo -> Set up Parental Controls for Any User -> Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="1e0bd-154">Verificare che il gioco sia avviato dall'Games Explorer di avvio.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="1e0bd-155">Verificare che il gioco visualizzi una valutazione accurata di Controllo genitori sotto il titolo del gioco nell'Pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="1e0bd-156">Prima di applicare Controllo genitori, verificare che il gioco non richiedi credenziali di amministratore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="1e0bd-157">Impostare Controllo genitori su &quot; On &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e0bd-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="1e0bd-158">Nella sezione Impostazioni di Windows fare clic su Giochi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="1e0bd-159">Fare clic su OK (l'impostazione dovrebbe ora &quot; essere AO/tutti i &quot; giochi).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="1e0bd-160">Verificare che il gioco venga eseguito con queste impostazioni come User Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-161">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1e0bd-162">Verificare che il gioco venga eseguito con queste impostazioni come User Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="1e0bd-163">Disconnettersi come Toby e accedere come Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-164">Tornare alla schermata precedente e selezionare &quot; Imposta classificazioni di gioco &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e0bd-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="1e0bd-165">Selezionare una classificazione inferiore alla classificazione ESRB del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-166">Se il gioco non è valutato, ignorare questo passaggio e passare alla parte successiva di questo test.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="1e0bd-167">Potrebbe essere necessario scegliere un sistema di classificazione diverso per trovare una classificazione del gioco, a seconda delle impostazioni locali della lingua dello SKU testato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="1e0bd-168">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1e0bd-169">Verificare che il gioco non si avvii per User Toby quando ESRB è bloccato dall'utente Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-170">Disconnettersi come Toby e accedere come Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-171">Se modificato in precedenza, ripristinare le impostazioni ESRB.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="1e0bd-172">Se non sono presenti impostazioni ESRB, selezionare Blocca o Consenti giochi specifici &quot; e selezionare il gioco in base al &quot; nome.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="1e0bd-173">Disconnettersi come Jane e accedere come Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="1e0bd-174">Verificare che il gioco non si avvii per User Toby quando EXE/Name è bloccato dall'utente Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-175">Disconnettersi come Toby e accedere di nuovo come Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-176">Come Jane, aprire Controlli utente -> restrizioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="1e0bd-177">Fare clic su Toby per usare solo i programmi consentiti e fare clic su &quot; &quot; OK(ovvero, non consentire exe).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="1e0bd-178">Passare a Controlli utente | Games Controlla e consente il gioco specifico usando la classificazione ESRB.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="1e0bd-179">Disconnettersi come Jane e accedere come Toby e provare a eseguire il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="1e0bd-180">Verificare che il gioco NON sia bloccato e che Toby possa riprodurlo quando non sono impostati &quot; file &quot; exe consentiti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="1e0bd-181">1.3 Windows Vista Rich Saved Games</span><span class="sxs-lookup"><span data-stu-id="1e0bd-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="1e0bd-182">Questo requisito è stato ritirato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="1e0bd-183">1.4 Xbox 360 requisito condizionale di Common Controller per \[ Windows\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-184">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-185">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-187">I giochi che supportano i controller gamepad devono supportare il controller Xbox 360 per Windows usando l'API XInput.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="1e0bd-188">Tutti i riferimenti ai trigger e ai pulsanti comuni del controller devono usare Xbox 360 nomi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-189">Avviare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-189">Launch the game.</span></span></li>
<li><span data-ttu-id="1e0bd-190">Passare alle opzioni del controller.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="1e0bd-191">Verificare che il gioco riconosca Xbox 360 controller per Windows come dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="1e0bd-192">Riprodurre il gioco e verificare che il gioco e il sistema di menu siano controllabili con Xbox 360 Controller per Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="1e0bd-193">Verificare che il Xbox 360 controller per Windows si comporti in base agli standard accettati.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="1e0bd-194">(B per back, A per accept, Start for in game menu/pause or accept, etc.)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="1e0bd-195">Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando Xbox 360 nomi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-196">Se il gioco non supporta un controller di gioco e/o supporta solo tastiera/mouse, ignorare questa test case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="1e0bd-197">\*\* Le impostazioni per il controller potrebbero trovarsi all'esterno del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="1e0bd-198">1.5 Proporzioni e risoluzioni multiple</span><span class="sxs-lookup"><span data-stu-id="1e0bd-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-199">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-200">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-202">Il gioco deve supportare almeno le proporzioni seguenti e le risoluzioni dello schermo associate:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="1e0bd-203">4:3 &quot; normale &quot; (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="1e0bd-204">Widescreen 16:9 &quot; &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="1e0bd-205">Widescreen 16:10 &quot; &quot; (1152 720, 1680 1050 o 800 480)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-206">Individuare le opzioni video per il gioco (potrebbe essere fuori gioco).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-207">I test seguenti devono essere eseguiti su un monitor widescreen.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="1e0bd-208">Nella sezione risoluzione video selezionare 800 600 o 1024 768.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="1e0bd-209">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 4:3.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1e0bd-210">Nella sezione risoluzione video selezionare 1280 720.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="1e0bd-211">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:9.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1e0bd-212">Nella sezione risoluzione video selezionare 1680 1050, 800 480 o 1152 720.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="1e0bd-213">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:10.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="1e0bd-214">Verificare che il gioco non estenda l'immagine e a sua volta presenti un'area di visualizzazione più ampia.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="1e0bd-215">Verificare che il gioco chiede all'utente quando viene apportata una modifica alla risoluzione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="1e0bd-216">Se l'utente non accetta entro 15 secondi, verificare che lo schermo torni all'impostazione precedente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="1e0bd-217">Verificare che il gioco non attava le barre nere a sinistra e a destra dell'area di gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="1e0bd-218">In questo caso, l'area del gioco sarà ancora in un rapporto 4:3 al centro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="1e0bd-219">1.6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="1e0bd-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="1e0bd-220">Questo requisito è stato ritirato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="1e0bd-221">1.7 Requisito condizionale \[ Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="1e0bd-222">OS</span><span class="sxs-lookup"><span data-stu-id="1e0bd-222">OS</span></span>                                                                    | <span data-ttu-id="1e0bd-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0bd-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0bd-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-224">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-225">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-226">Windows XP</span></span><br/> | <span data-ttu-id="1e0bd-227">Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere l'impostazione predefinita per qualsiasi opzione di configurazione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="1e0bd-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt></span><span class="sxs-lookup"><span data-stu-id="1e0bd-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="1e0bd-229">Avviare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-229">Launch the game.</span></span> <span data-ttu-id="1e0bd-230">Nelle opzioni video verificare se sono disponibili opzioni di rendering, D3D e/o OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="1e0bd-231">In caso contrario, verificare che le opzioni di rendering del gioco siano direct3D per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="1e0bd-232">Se non è possibile verificare che D3D9 sia la versione di DirectX in uso, passare a Test automatizzato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="1e0bd-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt></span><span class="sxs-lookup"><span data-stu-id="1e0bd-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="1e0bd-234">Usare lo strumento: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="1e0bd-235">1.8 Abilitare il supporto per valori DPI alti</span><span class="sxs-lookup"><span data-stu-id="1e0bd-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-236">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-238">I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando è abilitato il ridimensionamento DPI.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1e0bd-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1e0bd-240">Impostare il sistema su DPI 150%:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="1e0bd-241">Windows Vista: Pannello di controllo: Personalizzazione, Regola dimensioni carattere (DPI), DPI personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="1e0bd-242">Impostare su 150%.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-242">Set to 150%.</span></span><br/> <span data-ttu-id="1e0bd-243">Windows 7: Pannello di controllo: Schermo, Impostato su Più grande - 150%.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="1e0bd-244">Eseguire il processo di installazione e il gioco per verificare che non siano presenti problemi con le schermate ritagliate o le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="1e0bd-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="1e0bd-246">Verificare che <dpiAware>l'elemento true</dpiAware> sia contenuto nel manifesto incorporato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="1e0bd-247">Usare lo strumento: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="1e0bd-248">2. Sicurezza e compatibilità</span><span class="sxs-lookup"><span data-stu-id="1e0bd-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="1e0bd-249">2.1 Seguire le linee guida per il controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="1e0bd-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-250">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-252">Ogni file eseguibile (.EXE)incluso in un'applicazione deve avere un manifesto incorporato che ne definisce il livello di esecuzione:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-253">Per i giochi e i programmi di installazione di giochi, uiAccess deve sempre essere impostato su &quot; &quot; false.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-254">Verificare che i file eseguibili del gioco contengano manifesti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="1e0bd-255">Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel &quot; sia AsInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="1e0bd-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="1e0bd-256">Usare lo strumento: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="1e0bd-257">2.2 Supporto delle versioni x64 di Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-258">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-260">Per mantenere la compatibilità con le versioni x64 di Windows:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="1e0bd-261">I programmi di installazione dei titoli e dei titoli non devono contenere codice a 16 bit o basarsi su componenti a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="1e0bd-262">Se il gioco dipende dai driver in modalità kernel per il funzionamento, è necessario che siano disponibili versioni x64 di questi driver.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="1e0bd-263">La configurazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni a 64 bit di Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-264">Il supporto per l'edizione a 64 bit di Windows XP Professional è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-265">Test manuale</span><span class="sxs-lookup"><span data-stu-id="1e0bd-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-266">Eseguire il gioco nelle edizioni a 64 bit di Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="1e0bd-267">Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="1e0bd-268">Verificare che il gioco non verifichi un errore in seguito a file eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="1e0bd-269">L'errore menziona l'applicazione a 16 bit nella finestra degli errori.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="1e0bd-270">Se il gioco ha un eseguibile nativo a 64 bit, usare anche questo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="1e0bd-271">2.3 Firmare i file</span><span class="sxs-lookup"><span data-stu-id="1e0bd-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-272">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-273">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-275">Tutti i file di codice eseguibile ( ad esempio, .exe e .dll) devono essere firmati con un certificato Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="1e0bd-276">Se si usa un Windows Installer, i file di pacchetto del programma di installazione (.msi file) devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-277">Test manuale</span><span class="sxs-lookup"><span data-stu-id="1e0bd-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-278">Passare alla directory del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="1e0bd-279">Individuare tutti i file .exe e .dll file.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="1e0bd-280">Fare clic con il pulsante destro del mouse su Proprietà in ogni file.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="1e0bd-281">Verificare che i file eseguibili del gioco contengano una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="1e0bd-282">2.4 Firmare i driver</span><span class="sxs-lookup"><span data-stu-id="1e0bd-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-283">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-284">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-286">Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="1e0bd-287">Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve avere una firma Microsoft ottenuta tramite il programma Windows Hardware Quality Labs (WHQL) o DrS (Driver Reliability Signature).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-288">Test manuale</span><span class="sxs-lookup"><span data-stu-id="1e0bd-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-289">Installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-289">Install the game.</span></span></li>
<li><span data-ttu-id="1e0bd-290">Verificare che il processo di installazione del gioco non visualizza le finestre di dialogo del driver non firmate.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="1e0bd-291">2.5 Eseguire correttamente il controllo della versione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-292">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-293">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-295">I giochi non devono essere eseguiti nei sistemi operativi futuri come indicato dalle modifiche nel numero di versione di Windows, a meno che il Contratto di licenza con l'utente finale non proibisca l'uso nei sistemi operativi futuri.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="1e0bd-296">Se si suppone che il gioco non riesca, deve farlo normalmente visualizzando un messaggio all'utente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1e0bd-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1e0bd-298">Installare il gioco in Windows XP, nelle edizioni a 32 bit di Windows Vista e Windows 7 e nelle edizioni a 64 bit di Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="1e0bd-299">Verificare che il processo di installazione del gioco non verifichi un errore relativo alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="1e0bd-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="1e0bd-301">Usare lo strumento: Application Verifier</span><span class="sxs-lookup"><span data-stu-id="1e0bd-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-302">Avviare Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="1e0bd-303">Abilitare il test Compatibility:HighVersionLie dopo aver selezionato il INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="1e0bd-304">Installare il gioco e assicurarsi che non blocchi l'installazione in base alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="1e0bd-305">Abilitare il test Compatibility:HighVersionLie dopo aver selezionato il GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="1e0bd-306">Eseguire il gioco e assicurarsi che non blocchi l'esecuzione in base alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="1e0bd-307">2.6 Supporto di sessioni utente simultanee</span><span class="sxs-lookup"><span data-stu-id="1e0bd-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-308">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-309">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-311">I giochi devono supportare scenari multitasking windows standard.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-312">Creare un account utente standard in Windows Vista o Windows 7 denominato Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="1e0bd-313">Start -> Pannello di controllo -> Add or Remove User Accounts -> Create New Account</span><span class="sxs-lookup"><span data-stu-id="1e0bd-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="1e0bd-314">Avviare il gioco come User Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-315">ALT+TAB per tornare al desktop.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="1e0bd-316">Verificare che il gioco sia correttamente ALT+TAB sul desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="1e0bd-317">Fare clic su Start -> [freccia a destra di Blocca] -> Cambia utente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="1e0bd-318">Accedere come Utente Toby.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="1e0bd-319">Verificare che il gioco sia avviato come User Toby mentre è ancora in esecuzione come User Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="1e0bd-320">Verificare che nel gioco non si verifichino errori per User Toby o User Jane durante il processo user switch.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="1e0bd-321">Se è possibile avviare un'altra sessione di gioco, verificare che non sia possibile ascoltare l'audio dalla sessione di gioco originale.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="1e0bd-322">Chiudere il gioco e tornare all'utente e al gioco originali.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="1e0bd-323">2.7 Supporto dei nomi lunghi</span><span class="sxs-lookup"><span data-stu-id="1e0bd-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-324">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-325">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-327">Se un gioco supporta il salvataggio di file, deve essere in grado di salvare file con nomi e percorsi lunghi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="1e0bd-328">Il gioco deve gestire correttamente i caratteri file system, ad esempio \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="1e0bd-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="1e0bd-329">&quot; < o > campi di input utente usati per creare nomi di file o percorsi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-330">Avviare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-330">Launch the game.</span></span></li>
<li><span data-ttu-id="1e0bd-331">Avviare un nuovo gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-331">Start a new game.</span></span></li>
<li><span data-ttu-id="1e0bd-332">Salvare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-332">Save the game.</span></span> <span data-ttu-id="1e0bd-333">Durante il processo di salvataggio, verificare che il gioco sia salvato usando il nome di salvataggio My First Save Game.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="1e0bd-334">Tornare al menu principale.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="1e0bd-335">Provare a caricare il gioco appena salvato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="1e0bd-336">Verificare che nel gioco non si verifichino errori durante la gestione di caratteri file system non supportati, ad esempio \ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="1e0bd-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="1e0bd-337">&quot; < o > se il gioco lo consente, assegnare un nome al gioco salvato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="1e0bd-338">Se all'utente è consentito assegnare un nome al profilo e/o al carattere o salvare giochi, verificare che il gioco non presenti errori anche quando si usano nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="1e0bd-339">3. Installazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="1e0bd-340">3.1 Installazione semplice</span><span class="sxs-lookup"><span data-stu-id="1e0bd-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-341">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-342">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-344">I giochi con un'installazione tradizionale devono fornire un percorso semplificato nell'interfaccia utente di installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-345">Inserire il disco del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="1e0bd-346">Verificare che nel gioco non siano visualizzati più End-User di licenza.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="1e0bd-347">Se il gioco supporta un'opzione di installazione personalizzata o avanzata, verificare che questa opzione sia accessibile durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="1e0bd-348">Verificare che l'opzione Installazione predefinita bypassi tutte le selezioni di input utente per il processo di installazione (selezione della cartella di installazione, selezione dei componenti e così via).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="1e0bd-349">Verificare che il processo di installazione del gioco non richiede l'installazione del componente del sistema operativo (installazione di DirectX, Runtime di Visual C e così via).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="1e0bd-350">Verificare che il processo di installazione del gioco non richiede l'interazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="1e0bd-351">Verificare che il gioco venga eseguito automaticamente o che al termine del processo di installazione sia presente un menu di avvio.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="1e0bd-352">Verificare che il processo di disinstallazione del gioco rimova tutti i file dei componenti del sistema operativo non ridistribuiti installati e cancella tutte le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="1e0bd-353">La pulizia di tutte le impostazioni e i dati per utente (ad esempio i giochi salvati) non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="1e0bd-354">3.2 Supporto del controllo dell'account utente per l'installazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-355">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="1e0bd-357">Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="1e0bd-358">I giochi devono quindi eseguire attività per utente alla prima esecuzione separatamente dall'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-359">Verificare che sia possibile installare il gioco come User Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="1e0bd-360">Questa operazione richiederà diritti elevati durante il processo di installazione/installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="1e0bd-361">Verificare che il processo di installazione del gioco richiede all'utente Jane di elevare il livello tramite credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="1e0bd-362">La richiesta di elevazione dei privilegi verrà visualizzata quando l'utente tenta di eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="1e0bd-363">Scegliere di eseguire automaticamente il gioco al termine dell'installazione, se non lo fa già, o avviarlo dal menu visualizzato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="1e0bd-364">Una volta in gioco, creare un nuovo profilo, riprodurre e salvare un gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="1e0bd-365">Uscire dal gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-365">Exit the game.</span></span></li>
<li><span data-ttu-id="1e0bd-366">Riavviare il gioco e verificare che Profili utente e Giochi salvati siano accessibili dall'account User Jane.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="1e0bd-367">3.3 Installare in cartelle corrette</span><span class="sxs-lookup"><span data-stu-id="1e0bd-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-368">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-369">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-371">I giochi devono essere installati nella cartella Programmi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="1e0bd-372">I dati utente devono essere scritti alla prima esecuzione e non durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-373">Installare il gioco usando il tipo di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="1e0bd-374">Verificare che il gioco sia stato installato in Programmi.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-375">Se il test ha esito negativo, verificare che il gioco sia destinato all'installazione per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="1e0bd-376">In tal caso, si tratta di un errore.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="1e0bd-377">3.4 Installare correttamente le risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-378">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-379">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-381">Le applicazioni non devono tentare di installare file o chiavi del Registro di sistema protette da Protezione risorse di Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="1e0bd-382">Verificare che non vengano Protezione risorse di Windows finestre di dialogo WRP durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="1e0bd-383">3.5 Evitare riavvii durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-384">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-385">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-387">Il programma di installazione del gioco non deve presupporre che l'installazione dei componenti di Windows dai pacchetti di ridistribuzione richieda un riavvio, a meno che il riavvio non sia indicato da un risultato restituito o dalla documentazione Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-388">Installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-388">Install the game.</span></span></li>
<li><span data-ttu-id="1e0bd-389">Verificare che il gioco non richieda il riavvio del sistema dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-390">Se un aggiornamento del sistema Microsoft REDIST richiede un riavvio, eseguire le operazioni seguenti: Completare l'installazione del gioco, disinstallare il gioco e reinstallarlo una seconda volta.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="1e0bd-391">Il processo di installazione del gioco non deve richiedere un riavvio in questa seconda installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="1e0bd-392">3.6 Usare correttamente il controllo delle versioni dei file</span><span class="sxs-lookup"><span data-stu-id="1e0bd-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-393">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-394">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-396">Il programma di installazione del gioco deve verificare correttamente che siano installate le versioni più recenti dei file.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="1e0bd-397">L'installazione di un gioco non deve mai regredire i file non prodotti o condivisi da applicazioni non producete.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-398">Prima di installare il gioco, creare uno snapshot di preinstallazione di System32.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-399">Creare una directory denominata G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="1e0bd-400">Visualizzare una finestra di comando (Start -> Run -> cmd).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="1e0bd-401">Passare a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="1e0bd-402">Digitare dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="1e0bd-403">Creare uno snapshot post-installazione di System32.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="1e0bd-404">Visualizzare una finestra di comando (Avvia -> Esegui -> cmd).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="1e0bd-405">Passare a c:\windows\system32.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="1e0bd-406">Digitare dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="1e0bd-407">Verificare che il gioco non regredi le versioni dei file che il gioco non ha prodotto (... dei file elencati nei due documenti confrontando pregame.txt con postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="1e0bd-408">3.7 Supporto dei requisiti condizionali di esecuzione \[ automatica\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-409">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-410">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-412">Per i giochi distribuiti su CD, DVD o altri supporti rimovibili che supportano l'esecuzione automatica, quando il disco viene inserito per la prima volta, l'applicazione deve essere eseguita automaticamente o richiedere all'utente di installare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-413">I programmi di esecuzione automatica scritti per l'uso in versioni di Windows precedenti a Windows Vista non devono usare il runtime .NET, perché questa tecnologia non è inclusa in Windows XP o versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="1e0bd-414">Per altre indicazioni, vedere <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun (Giochi per Windows Technical Requirements 3.7, Esecuzione automatica del supporto).</span><span class="sxs-lookup"><span data-stu-id="1e0bd-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="1e0bd-415">Inserire il disco del gioco o i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="1e0bd-416">Verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="1e0bd-417">Windows Vista o Windows 7: verificare che il programma di esecuzione automatica del gioco stesso non chiede all'utente Jane di elevare i privilegi tramite credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="1e0bd-418">Verificare che il file eseguibile di esecuzione automatica non necessiti di componenti REDIST, ad esempio .NET 3.5, librerie Run-Time C e così via.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="1e0bd-419">Verificare che il nuovo inserimento del disco nell'unità dopo l'installazione non causerà il nuovo avvio automatico dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="1e0bd-420">4. Affidabilità</span><span class="sxs-lookup"><span data-stu-id="1e0bd-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="1e0bd-421">4.1 Eliminare i riavvii non necessari</span><span class="sxs-lookup"><span data-stu-id="1e0bd-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="1e0bd-422">OS</span><span class="sxs-lookup"><span data-stu-id="1e0bd-422">OS</span></span>                                              | <span data-ttu-id="1e0bd-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0bd-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0bd-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-424">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-425">Windows Vista</span></span><br/> | <span data-ttu-id="1e0bd-426">Tutti i programmi di installazione delle applicazioni devono sfruttare le API di Gestione riavvio per evitare riavvii del sistema (vedere [il requisito 3.5).](#35-avoid-reboots-during-installation)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="1e0bd-427">4.2 Eliminare Application Verifier errori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-428">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-429">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-431">Il gioco non deve generare errori in esecuzione in Microsoft Application Verifier (AppVerifier), versione 4.0 o successiva, nei test seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="1e0bd-432">Nozioni di base: handle, heap, blocchi, memoria, TLS</span><span class="sxs-lookup"><span data-stu-id="1e0bd-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="1e0bd-433">Varie: DangerousAPIs, DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="1e0bd-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-434">Usare lo strumento: AppVerifier 4.0 (o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="1e0bd-435">Installare AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="1e0bd-436">Avviare AppVerifier e selezionare File -> Aggiungi applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="1e0bd-437">Individuare il file eseguibile del gioco, selezionarlo e fare clic sul &quot; pulsante &quot; Apri.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="1e0bd-438">Nella sezione &quot; Applicazioni selezionare il file &quot; eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="1e0bd-439">Nella sezione Test selezionare i test elencati in precedenza nelle categorie Nozioni di base e Varie (deselezionare ThreadPool e &quot; &quot; &quot; &quot; &quot; &quot; TimeRollOver) e assicurarsi che tutti gli altri test non siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="1e0bd-440">Avviare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-440">Launch the game.</span></span></li>
<li><span data-ttu-id="1e0bd-441">Verificare che il gioco non generi errori quando viene eseguito in Application Verifier.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="1e0bd-442">Alcuni test richiedono l'esecuzione completa di un debugger.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="1e0bd-443">Potrebbe essere necessaria una versione non protetta del file eseguibile del gioco, perché la tecnologia anti-cheat/anti-piracy può interferire con AppVerifer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="1e0bd-444">4.3 Supporto Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e0bd-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-445">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-446">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-448">I giochi devono gestire solo le eccezioni note e previste e Segnalazione errori Windows non devono essere disabilitate.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="1e0bd-449">Se un errore (ad esempio una violazione di accesso) viene inserito in un gioco, deve consentire Segnalazione errori Windows segnalare l'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="1e0bd-450">Usare lo strumento: Hijacker thread</span><span class="sxs-lookup"><span data-stu-id="1e0bd-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="1e0bd-451">Se l'applicazione si arresta in modo anomalo durante il test, verificare che il gioco Segnalazione errori Windows correttamente e raccoglie i dati di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
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
<td><span data-ttu-id="1e0bd-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-452">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-453">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-455">Tutti i file eseguibili( ad esempio, .exe o .dll) devono contenere un nome di prodotto, un nome società e una versione del file accurati.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="1e0bd-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuale:</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="1e0bd-457">Fare clic con il pulsante destro del mouse sui file eseguibili del gioco sia nel supporto di installazione che in quelli installati nel disco rigido del computer.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="1e0bd-458">Selezionare Proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-458">Select Properties.</span></span></li>
<li><span data-ttu-id="1e0bd-459">Windows XP: fare clic sulla <strong>scheda</strong> Versione. Verificare che i campi Product Name (Nome prodotto), Company Name (Nome società) e File Version (Versione file) siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="1e0bd-460">Windows Vista o Windows 7: fare clic sulla <strong>scheda</strong> Dettagli. Verificare che i campi Nome prodotto e Versione file siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="1e0bd-461">Nome società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="1e0bd-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatizzato:</dt> </span><span class="sxs-lookup"><span data-stu-id="1e0bd-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="1e0bd-463">Usare lo strumento di test di Microsoft Games for Windows; vedere <a href="#64-microsoft-games-for-windows-test-tool">la sezione 6.4</a>.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
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
<td><span data-ttu-id="1e0bd-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-464">Windows 7</span></span><br/> <span data-ttu-id="1e0bd-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e0bd-465">Windows Vista</span></span><br/> <span data-ttu-id="1e0bd-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="1e0bd-467">La normale uscita del gioco non deve generare un errore di eccezione sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="1e0bd-468">Dopo aver riprodotto il gioco per una normale sessione di gioco, verificare che il gioco non generi errori all'uscita.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="1e0bd-469">5. Script di test di esempio</span><span class="sxs-lookup"><span data-stu-id="1e0bd-469">5. Sample Test Script</span></span>

<span data-ttu-id="1e0bd-470">Questo è un esempio di un test superato tipico usando i requisiti di test precedenti come guida.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="1e0bd-471">5.1 Strumenti</span><span class="sxs-lookup"><span data-stu-id="1e0bd-471">5.1 Tools</span></span>

-   <span data-ttu-id="1e0bd-472">Edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="1e0bd-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="1e0bd-473">Edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="1e0bd-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="1e0bd-474">Edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="1e0bd-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="1e0bd-475">Edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="1e0bd-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="1e0bd-476">Edizione a 32 bit di Windows XP SP2 in una CPU AMD</span><span class="sxs-lookup"><span data-stu-id="1e0bd-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="1e0bd-477">Edizione a 32 bit di Windows XP SP2 in una CPU Intel</span><span class="sxs-lookup"><span data-stu-id="1e0bd-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="1e0bd-478">Monitor wide screen che supporta 1680 1050</span><span class="sxs-lookup"><span data-stu-id="1e0bd-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="1e0bd-479">Xbox 360 controller per Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="1e0bd-480">5.2 Preinstallazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="1e0bd-481">Windows Vista e Windows 7: Creare due utenti standard: Jane e Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="1e0bd-482">Windows Vista e Windows 7: verificare che Controllo dell'account utente sia abilitato</span><span class="sxs-lookup"><span data-stu-id="1e0bd-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="1e0bd-483">Creare uno snapshot di preinstallazione di System32</span><span class="sxs-lookup"><span data-stu-id="1e0bd-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="1e0bd-484">Creare una directory denominata G4Wtest</span><span class="sxs-lookup"><span data-stu-id="1e0bd-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="1e0bd-485">Visualizzare una finestra di comando (Start -> Esegui -> cmd)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="1e0bd-486">Passare a c: \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="1e0bd-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="1e0bd-487">Digitare dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="1e0bd-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="1e0bd-488">Windows Vista e Windows 7: impostare su 150% DPI \[ 1.8\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="1e0bd-489">Procedere con [l'installazione](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="1e0bd-490">5.3 Installare</span><span class="sxs-lookup"><span data-stu-id="1e0bd-490">5.3 Install</span></span>

1.  <span data-ttu-id="1e0bd-491">Accedere come Utente Jane</span><span class="sxs-lookup"><span data-stu-id="1e0bd-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="1e0bd-492">Inserire il disco del gioco nell'unità CD/DVD, verificare che la finestra di dialogo di installazione/esecuzione venga visualizzata automaticamente \[ 3.7\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="1e0bd-493">Verificare che il processo di installazione del gioco richiede all'utente Jane di elevare le credenziali di amministratore \[ 3.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="1e0bd-494">Verificare che il programma di esecuzione automatica del gioco stesso non chiede all'utente Jane di elevare i privilegi tramite credenziali di amministratore \[ 3.7\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="1e0bd-495">Verificare che il gioco non visualizza più di un contratto End-User licenza \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="1e0bd-496">Verificare che nel gioco siano visualizzate le opzioni di installazione predefinita/semplice e personalizzata/avanzata \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="1e0bd-497">Verificare che l'opzione di installazione Predefinita/Semplice ignora tutte le selezioni di input dell'utente per il processo di installazione (selezione della cartella di installazione, selezione dei componenti e così via). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="1e0bd-498">Verificare che il processo di installazione del gioco non richiede la configurazione dei componenti del sistema operativo (installazione di DirectX, librerie Run-Time C e così via). \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="1e0bd-499">Verificare che il processo di installazione del gioco non richiede l'interazione con il firewall \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="1e0bd-500">Verificare che il processo di installazione del gioco non verifichi un errore relativo alla versione del sistema operativo \[ 2.5 \] \[ 4.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="1e0bd-501">Verificare che nel processo di installazione del gioco non siano visualizzate finestre di dialogo del driver \[ non firmate 2.4\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="1e0bd-502">Verificare che non vengano Protezione risorse di Windows (WRP) durante il processo di installazione \[ 3.4\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="1e0bd-503">Verificare che il nuovo inserimento del disco nell'unità dopo l'installazione non causa il nuovo avvio automatico dell'installazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="1e0bd-504">Verificare che il gioco non richieda il riavvio del sistema dopo \[ l'installazione 3.5\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="1e0bd-505">Verificare che sia possibile installare il gioco come User Jane \[ 3.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="1e0bd-506">Verificare che il gioco venga eseguito automaticamente o che sia presente un menu di avvio alla fine del processo di installazione \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="1e0bd-507">Se il gioco viene eseguito automaticamente dopo l'installazione, passare a [Runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="1e0bd-508">Se il gioco ha lasciato un menu di avvio o non è stato possibile disinstallare, vedere la sezione [Post-installazione](#54-post-install)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="1e0bd-509">5.4 Post-installazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="1e0bd-510">Verificare che il gioco non posiziona i collegamenti di avvio sul desktop dell'utente \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="1e0bd-511">Verificare che il gioco non posiziona i collegamenti di avvio nel menu Start \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="1e0bd-512">Verificare che l'icona del gioco sia visualizzata Windows Games Explorer \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="1e0bd-513">Verificare che i metadati (editore, sviluppatore, genere, data di rilascio, versione) nella parte inferiore visualizzino la \[ versione 1.1 corretta\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="1e0bd-514">Verificare che l'icona del gioco visualizzi Indice prestazioni Windows (WEI) in Windows Games Explorer \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="1e0bd-515">Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Windows Games Explorer \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="1e0bd-516">Verificare che il gioco visualizzi una valutazione accurata del controllo genitori in Windows Games Explorer \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="1e0bd-517">Creare uno snapshot post-installazione di System32</span><span class="sxs-lookup"><span data-stu-id="1e0bd-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="1e0bd-518">Visualizzare una finestra di comando (Start -> Run -> cmd)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="1e0bd-519">Passare a c: \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="1e0bd-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="1e0bd-520">Digitare dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="1e0bd-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="1e0bd-521">Verificare che il gioco non regredisca con le versioni dei file elencati nei due documenti confrontando pregame.txt con postgame.txt \[ 3.6\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="1e0bd-522">Passare al [runtime](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="1e0bd-523">5.5 Runtime</span><span class="sxs-lookup"><span data-stu-id="1e0bd-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="1e0bd-524">RUNTIME 1: se il menu di avvio è presente, avviare il gioco da qui.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="1e0bd-525">Se il gioco è stato eseguito automaticamente o è stato avviato dal menu dell'utilità di avvio del gioco dopo l'installazione, seguire questa procedura. In caso contrario, passare a RUNTIME 2:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="1e0bd-526">Creare un profilo (se il gioco lo consente)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="1e0bd-527">Avviare un nuovo gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-527">Start a new game</span></span>
    3.  <span data-ttu-id="1e0bd-528">Salvare il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-528">Save the game</span></span>
    4.  <span data-ttu-id="1e0bd-529">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-529">Exit the game</span></span>
    5.  <span data-ttu-id="1e0bd-530">Avviare il gioco da Games Explorer</span><span class="sxs-lookup"><span data-stu-id="1e0bd-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="1e0bd-531">Verificare che il gioco sia avviato dall'icona Games Explorer \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="1e0bd-532">Verificare che il gioco non richiede credenziali di amministratore \[ all'avvio 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="1e0bd-533">Verificare che Profili utente e Salva giochi siano accessibili dall'account User Jane \[ 3.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="1e0bd-534">Passare a RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="1e0bd-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="1e0bd-535">RUNTIME 2: se il gioco non è stato eseguito automaticamente o non è stato visualizzato un avvio dal menu dell'utilità di avvio del gioco, si tratta di un errore \[ 3.1. Tuttavia, i test possono \] continuare normalmente:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="1e0bd-536">Avviare il gioco da Games Explorer</span><span class="sxs-lookup"><span data-stu-id="1e0bd-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="1e0bd-537">Verificare che il gioco sia avviato dall'icona Games Explorer \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="1e0bd-538">Verificare che il gioco non richiede credenziali di amministratore \[ all'avvio 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="1e0bd-539">Passare a RUNTIME 3</span><span class="sxs-lookup"><span data-stu-id="1e0bd-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="1e0bd-540">RUNTIME 3: se il gioco supporta un game pad, verificare che il gioco riconosca Xbox 360 Controller per Windows come dispositivo di input \[ 1.4\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="1e0bd-541">Se necessario, abilitare il controller tramite il menu delle opzioni</span><span class="sxs-lookup"><span data-stu-id="1e0bd-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="1e0bd-542">Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando Xbox 360 nomi</span><span class="sxs-lookup"><span data-stu-id="1e0bd-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="1e0bd-543">Verificare che il gioco e il sistema di menu siano controllabili con il controller Xbox 360 per Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="1e0bd-544">Verificare che il Xbox 360 per Windows si comporti in base agli standard accettati</span><span class="sxs-lookup"><span data-stu-id="1e0bd-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="1e0bd-545">Impostare il video su \[ 1.5: \]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="1e0bd-546">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 4:3 (800 600 o 1024 768)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="1e0bd-547">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:9 (1280 720)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="1e0bd-548">Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:10 (1680 1050, 800 480 o 1152 720)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="1e0bd-549">Verificare che il gioco richiede all'utente quando viene apportata una modifica alla risoluzione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="1e0bd-550">Verificare che la visualizzazione ripristina l'impostazione precedente se non si accetta entro 15 secondi</span><span class="sxs-lookup"><span data-stu-id="1e0bd-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="1e0bd-551">Verificare che il gioco non estensa l'immagine e a sua volta presenti un'area di visualizzazione più ampia</span><span class="sxs-lookup"><span data-stu-id="1e0bd-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="1e0bd-552">Verificare che il gioco non aggiunge barre nere a sinistra e a destra dell'area di gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="1e0bd-553">Se disponibile nelle impostazioni video, verificare che per impostazione predefinita le opzioni di rendering del gioco siano Direct3D \[ 1.7. In caso \] contrario, passare [a Test automatizzati](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="1e0bd-554">Se richiesto o se l'opzione è disponibile, creare un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="1e0bd-555">Verificare che nel gioco non si verifichino errori quando si usano nomi di file lunghi \[ 2.7\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="1e0bd-556">Avviare un nuovo gioco, creare un salvataggio del gioco e verificare che non si verifichino errori durante la gestione dei caratteri file system non supportati \[ 2.7\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="1e0bd-557">Verificare che il gioco sia correttamente ALT+TAB sul desktop di Windows \[ 2.6\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="1e0bd-558">Cambiare utente con il gioco in esecuzione facendo clic su Start -> Cambia utente</span><span class="sxs-lookup"><span data-stu-id="1e0bd-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="1e0bd-559">Accedere come Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="1e0bd-560">Verificare che il gioco sia avviato come User Toby mentre è ancora in esecuzione come User Jane \[ 2.6\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="1e0bd-561">Verificare che nel gioco non si verifichino errori per User Toby o User Jane durante il processo user switch \[ 2.6\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="1e0bd-562">Verificare che non sia possibile ascoltare l'audio dalla sessione di gioco \[ originale 2.6\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="1e0bd-563">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-563">Exit the game</span></span>
    7.  <span data-ttu-id="1e0bd-564">Disconnettersi da Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-564">Log off Toby</span></span>
    8.  <span data-ttu-id="1e0bd-565">Tornare all'utente originale in cui è in esecuzione il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="1e0bd-566">ALT+TAB torna al gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="1e0bd-567">Uscire dal gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-567">Exit the game</span></span>
10. <span data-ttu-id="1e0bd-568">Passare al [post-runtime](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="1e0bd-569">5.6 Post-Runtime</span><span class="sxs-lookup"><span data-stu-id="1e0bd-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="1e0bd-570">Verificare che il gioco non generi errori all'uscita \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="1e0bd-571">Verificare che il gioco sia installato in Programmi \[ 3.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="1e0bd-572">Passare a [Controllo genitori](/windows)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="1e0bd-573">5.7 Controllo genitori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="1e0bd-574">Aprire Controllo genitori in Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="1e0bd-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="1e0bd-575">Verificare che il gioco visualizzi una valutazione accurata di Controllo genitori sotto il titolo del gioco in Controllo genitori Pannello di controllo \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="1e0bd-576">Per i test seguenti, vedere Test case \[ 1.2: \]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="1e0bd-577">Dopo aver impostato Controllo genitori su "On", verificare che il gioco venga eseguito con queste impostazioni come User Jane \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="1e0bd-578">Disconnettersi e accedere come Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="1e0bd-579">Verificare che il gioco venga eseguito con queste impostazioni come User Toby \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="1e0bd-580">Disconnettersi e accedere come Jane</span><span class="sxs-lookup"><span data-stu-id="1e0bd-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="1e0bd-581">Nella sezione Controllo genitori impedire a User Toby di visualizzare i giochi di un livello ESRB sempre superiore rispetto al gioco appena installato</span><span class="sxs-lookup"><span data-stu-id="1e0bd-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="1e0bd-582">Esempio: se il gioco è valutato E, impostarlo in modo che Toby possa solo riprodurre giochi classificati in C</span><span class="sxs-lookup"><span data-stu-id="1e0bd-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="1e0bd-583">Verificare che il gioco venga eseguito con queste impostazioni come User Jane \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="1e0bd-584">Disconnettersi e accedere come utente Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="1e0bd-585">Verificare che il gioco non si avvii in User Toby quando ESRB è bloccato dall'utente Jane \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="1e0bd-586">Disconnettersi come utente Toby e accedere di nuovo come utente Jane</span><span class="sxs-lookup"><span data-stu-id="1e0bd-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="1e0bd-587">Se modificato in precedenza, ripristinare le impostazioni ESRB</span><span class="sxs-lookup"><span data-stu-id="1e0bd-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="1e0bd-588">Se non sono presenti impostazioni ESRB, selezionare "Blocca o Consenti giochi specifici" e selezionare il gioco in base al nome</span><span class="sxs-lookup"><span data-stu-id="1e0bd-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="1e0bd-589">Disconnettersi come Jane e accedere come Toby</span><span class="sxs-lookup"><span data-stu-id="1e0bd-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="1e0bd-590">Verificare che il gioco non si avvii in User Toby quando EXE/Name è bloccato dall'utente Jane \[ 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="1e0bd-591">Disconnettersi come Toby e accedere di nuovo come Jane</span><span class="sxs-lookup"><span data-stu-id="1e0bd-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="1e0bd-592">Come Jane, aprire Controlli utente -> restrizioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="1e0bd-593">Fare clic su "Toby can only use the programs I allow" (Toby può usare solo i programmi consentiti) e quindi fare clic su OK (ad esempio, non consentire exe)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="1e0bd-594">Fare clic sulla casella Deseleziona tutto e quindi fare clic su OK</span><span class="sxs-lookup"><span data-stu-id="1e0bd-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="1e0bd-595">Passare a Controlli utente \| Games Controls e consentire il gioco specifico usando la classificazione ESRB</span><span class="sxs-lookup"><span data-stu-id="1e0bd-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="1e0bd-596">Disconnettersi come Jane e accedere come Toby e provare a eseguire il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="1e0bd-597">Verificare che il gioco NON sia bloccato e che Toby possa riprodurlo quando "allow no exes" è impostato \[ su 1.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="1e0bd-598">Disconnettersi come utente Toby e accedere di nuovo come utente Jane</span><span class="sxs-lookup"><span data-stu-id="1e0bd-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="1e0bd-599">Passare a Controllo genitori in Pannello di controllo e rimuovere le restrizioni</span><span class="sxs-lookup"><span data-stu-id="1e0bd-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="1e0bd-600">Verificare che entrambi gli utenti possano ora riprodurre il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="1e0bd-601">Passare a [Test automatizzati](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="1e0bd-602">5.8 Test automatizzati</span><span class="sxs-lookup"><span data-stu-id="1e0bd-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="1e0bd-603">Verificare che il gioco non generi errori quando viene eseguito in Application Verifier- Vedere la documentazione dello strumento di test di personalizzazione \[ 4.2\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="1e0bd-604">Verificare che i file eseguibili del gioco contengano manifesti. Vedere la documentazione dello strumento di test della personalizzazione \[ 2.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="1e0bd-605">Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia "AsInvoker". Vedere la documentazione dello strumento di test di personalizzazione \[ 2.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="1e0bd-606">Passare ad [Altri test](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="1e0bd-607">5.9 Altri test</span><span class="sxs-lookup"><span data-stu-id="1e0bd-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="1e0bd-608">Verificare che i file eseguibili del gioco contengano una firma \[ digitale 2.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="1e0bd-609">Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="1e0bd-610">Verificare che il gioco non verifichi un errore in seguito a file eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="1e0bd-611">Forzare l'arresto anomalo dell'applicazione durante il test e verificare che il gioco Segnalazione errori Windows correttamente e raccoglie i dati di arresto \[ anomalo 4.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="1e0bd-612">Verificare i riepiloghi dei file \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="1e0bd-613">Fare clic su Start -> Computer</span><span class="sxs-lookup"><span data-stu-id="1e0bd-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="1e0bd-614">Passare alla directory del gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="1e0bd-615">Nella finestra di ricerca digitare \*.dll</span><span class="sxs-lookup"><span data-stu-id="1e0bd-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="1e0bd-616">Per ogni file: fare clic con il pulsante destro del mouse sul file e scegliere Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e0bd-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="1e0bd-617">In Windows XP: fare clic sulla scheda Versione . Verificare che i campi Product Name (Nome prodotto), Company Name (Nome società) e File Version (Versione file) siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="1e0bd-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-618">\[4.3\]</span></span>
        -   <span data-ttu-id="1e0bd-619">In Windows Vista e Windows 7: fare clic sulla scheda Dettagli. Verificare che i campi Nome prodotto e Versione file siano popolati correttamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="1e0bd-620">Nome società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7 \[ 4.3\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="1e0bd-621">Ripetere questo controllo per .exe file</span><span class="sxs-lookup"><span data-stu-id="1e0bd-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="1e0bd-622">Avviare il gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-622">Launch the game.</span></span>

    1.  <span data-ttu-id="1e0bd-623">Premere CTRL+ALT+CANC</span><span class="sxs-lookup"><span data-stu-id="1e0bd-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="1e0bd-624">Fare clic sulla freccia "Opzioni di arresto"</span><span class="sxs-lookup"><span data-stu-id="1e0bd-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="1e0bd-625">Fare clic su Riavvia</span><span class="sxs-lookup"><span data-stu-id="1e0bd-625">Click Restart</span></span>
    4.  <span data-ttu-id="1e0bd-626">Verificare che il gioco non blocchi \[ l'arresto 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="1e0bd-627">Procedere alla [disinstallazione](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="1e0bd-628">5.10 Disinstallazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="1e0bd-629">Verificare che il processo di disinstallazione del gioco rimova tutti i file dei componenti del sistema operativo installati e non ridistribuiti e cancella tutte le impostazioni \[ 3.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="1e0bd-630">Verificare in Windows Vista o Windows 7 che Pannello di controllo sia l'unico modo per rimuovere il programma \[ 1.1\]</span><span class="sxs-lookup"><span data-stu-id="1e0bd-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="1e0bd-631">Note dello strumento di test</span><span class="sxs-lookup"><span data-stu-id="1e0bd-631">Test Tool Notes</span></span>

<span data-ttu-id="1e0bd-632">Queste sono note per ognuno degli strumenti di test elencati nei requisiti di test precedenti.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="1e0bd-633">6.1 Appverifier 4.0 (o versione successiva)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="1e0bd-634">**Test case: 2.5, 4.2**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="1e0bd-635">Alcune applicazioni non vengono eseguite con AppVerifier in esecuzione a causa della protezione della copia.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="1e0bd-636">Questo problema può essere risolto eseguendo con una versione di rilascio non protetta del file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="1e0bd-637">Installare AppVerifier 4.0 (o versione successiva) in un computer che esegue Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e0bd-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="1e0bd-638">Avviare AppVerifier e fare clic su File -> Aggiungi applicazione</span><span class="sxs-lookup"><span data-stu-id="1e0bd-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="1e0bd-639">Individuare il file eseguibile del gioco, selezionarlo e fare clic su Apri</span><span class="sxs-lookup"><span data-stu-id="1e0bd-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="1e0bd-640">Nella sezione "Applicazioni" selezionare il file eseguibile del gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="1e0bd-641">Selezionare i test seguenti nella sezione "Nozioni di base":</span><span class="sxs-lookup"><span data-stu-id="1e0bd-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="1e0bd-642">Selettori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-642">Handles</span></span>
    -   <span data-ttu-id="1e0bd-643">Heap</span><span class="sxs-lookup"><span data-stu-id="1e0bd-643">Heaps</span></span>
    -   <span data-ttu-id="1e0bd-644">Locks</span><span class="sxs-lookup"><span data-stu-id="1e0bd-644">Locks</span></span>
    -   <span data-ttu-id="1e0bd-645">Memoria</span><span class="sxs-lookup"><span data-stu-id="1e0bd-645">Memory</span></span>
    -   <span data-ttu-id="1e0bd-646">TLS</span><span class="sxs-lookup"><span data-stu-id="1e0bd-646">TLS</span></span>

6.  <span data-ttu-id="1e0bd-647">Selezionare i test seguenti nella sezione "Varie":</span><span class="sxs-lookup"><span data-stu-id="1e0bd-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="1e0bd-648">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="1e0bd-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="1e0bd-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="1e0bd-649">DirtyStacks</span></span>

7.  <span data-ttu-id="1e0bd-650">Verificare che tutti gli altri test non siano selezionati</span><span class="sxs-lookup"><span data-stu-id="1e0bd-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="1e0bd-651">Avviare il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-651">Launch the game</span></span>
9.  <span data-ttu-id="1e0bd-652">Riprodurre il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-652">Play the game</span></span>
10. <span data-ttu-id="1e0bd-653">Chiudere il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-653">Close the game</span></span>
11. <span data-ttu-id="1e0bd-654">In AppVerifier selezionare Visualizza -> log</span><span class="sxs-lookup"><span data-stu-id="1e0bd-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="1e0bd-655">Nella sezione "Applicazioni" selezionare il file di .exe app</span><span class="sxs-lookup"><span data-stu-id="1e0bd-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="1e0bd-656">Nella sezione "Log" selezionare il file di log e osservare il numero di errori.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="1e0bd-657">Se non sono presenti errori, terminare i test di AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="1e0bd-658">Se sono presenti errori, fare clic sul pulsante Visualizza</span><span class="sxs-lookup"><span data-stu-id="1e0bd-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="1e0bd-659">Cercare Gravità="Errore nel documento (CTRL+F)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="1e0bd-660">Creare bug in base alla parte LayerName= dell'errore</span><span class="sxs-lookup"><span data-stu-id="1e0bd-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="1e0bd-661">6.2 Test manifesto - mt.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="1e0bd-662">**Test case: 1.8, 2.1**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="1e0bd-663">Questo strumento viene eseguito da un prompt dei comandi in MT.exe si trova.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="1e0bd-664">Esempio:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="1e0bd-665">Fare clic su Start -> Run -> digitare cmd e fare clic sul pulsante OK</span><span class="sxs-lookup"><span data-stu-id="1e0bd-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="1e0bd-666">Eseguire lo mt.exe per generare un file manifesto per ogni file .exe che viene installato con il gioco</span><span class="sxs-lookup"><span data-stu-id="1e0bd-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="1e0bd-667">Aprire il file manifesto generato</span><span class="sxs-lookup"><span data-stu-id="1e0bd-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="1e0bd-668">Assicurarsi che ogni .exe file contenga quanto segue (richiesto:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-668">Ensure that each .exe file contains the following (requested:</span></span>

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
> <span data-ttu-id="1e0bd-669">Il livello di esecuzione richiesto deve essere presente per ogni file e dpiAware deve essere presente per almeno il file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="1e0bd-670">6.3 Thread Hijacker - threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="1e0bd-671">Questo strumento viene eseguito da un prompt dei comandi in threadhijacker.exe si trova.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="1e0bd-672">Esempio:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="1e0bd-673">Dove str è il nome \_ di \_program.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="1e0bd-674">Visualizzare Gestione attività, fare clic sulla scheda Processi e individuare il nome del file eseguibile del gioco.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="1e0bd-675">Aprire un prompt dei comandi in modalità amministratore</span><span class="sxs-lookup"><span data-stu-id="1e0bd-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="1e0bd-676">Passare alla directory in cui si trova threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="1e0bd-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="1e0bd-677">Tipo: **threadhijacker.exe /process:** str, dove str è il nome del file eseguibile che si vuole selezionare</span><span class="sxs-lookup"><span data-stu-id="1e0bd-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="1e0bd-678">6.4 Microsoft Games for Windows Test Tool</span><span class="sxs-lookup"><span data-stu-id="1e0bd-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="1e0bd-679">Questo strumento si trova in DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="1e0bd-680">Dopo aver installato l'SDK in un computer, il programma di installazione dello strumento di test di Games for Windows può essere inserito nel computer di test e installato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="1e0bd-681">Individuare il programma di installazione dello strumento di test di Microsoft Games for Windows nel computer di sviluppo in cui è installato DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="1e0bd-682">Per impostazione predefinita, viene inserito nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="1e0bd-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="1e0bd-683">Copiare il programma di MicrosoftGFWTestTool.msi /setup.exe) nel computer di test.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="1e0bd-684">Eseguire il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-684">Run the installer.</span></span>
3.  <span data-ttu-id="1e0bd-685">Avviare lo strumento di test di Microsoft Games for Windows.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="1e0bd-686">Nel campo **Project List (Elenco** progetti) sostituire **Create New Project (Crea nuovo progetto)** con il nome del titolo e fare clic **su Create New (Crea nuovo).**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="1e0bd-687">Attendere il completamento della baseline.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="1e0bd-688">Immettere tutte le informazioni disponibili nella sezione **Game Information (Informazioni** sul gioco) e fare clic **su Update Game Information (Aggiorna informazioni sul gioco).**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="1e0bd-689">Fare clic **sulla scheda Test** case.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="1e0bd-690">A partire dall'alto, procedere con i test case, facendo clic su **Supera** o **Non superato in** base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="1e0bd-691">Per informazioni dettagliate sull'inclusione di un bug nel report, vedere "Scrittura di un bug" più avanti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="1e0bd-692">Tornare alla scheda **Progetti** dopo aver esaminato il report (selezionando le **schede Report** e **Modifica bug).**</span><span class="sxs-lookup"><span data-stu-id="1e0bd-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="1e0bd-693">Fare clic **su Compila report**.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="1e0bd-694">Al termine della compilazione del report verrà aperta una finestra.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="1e0bd-695">Qui è possibile trovare un nome .ZIP nome file *ProjectName* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="1e0bd-696">Questo file contiene tutti i log e i risultati raccolti durante il test superato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="1e0bd-697">Scrittura di un bug</span><span class="sxs-lookup"><span data-stu-id="1e0bd-697">Writing a Bug</span></span>

<span data-ttu-id="1e0bd-698">Esistono due modi per scrivere un report sui bug:  è possibile scorrere i test case e fare clic su Non riuscito quando il titolo ha esito negativo per un test case oppure è possibile fare clic sulla scheda **Modifica** bug e aggiungere manualmente un report sui bug.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="1e0bd-699">Fare clic su Non riuscito in un test case</span><span class="sxs-lookup"><span data-stu-id="1e0bd-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="1e0bd-700">Quando si fa **clic su** Non  riuscito in test case, l'elenco a discesa Tipo di problema verrà impostato automaticamente sul tipo test case problema.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="1e0bd-701">Aggiungere una breve descrizione al **campo Titolo** che descrive brevemente il problema.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="1e0bd-702">Aggiungere una descrizione dettagliata del problema al **campo Comportamento** osservato.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="1e0bd-703">In base alle esigenze, aggiungere ciò che era previsto (anziché una descrizione del problema) al **campo Comportamento** previsto.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="1e0bd-704">Aggiungere una descrizione dettagliata di come riprodurre il problema nel **campo Passaggi di** riproduzione.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="1e0bd-705">Al termine, fare clic sul **pulsante** Salva.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="1e0bd-706">Aggiunta manuale di un bug</span><span class="sxs-lookup"><span data-stu-id="1e0bd-706">Manually Adding a Bug</span></span>

<span data-ttu-id="1e0bd-707">Questo processo è identico a quello in cui si fa clic su **Non** riuscito , ad eccezione dell'elenco a discesa popolato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="1e0bd-708">In questo caso, selezionare il tipo di errore TCR appropriato o selezionare **\* \* Problema non \* \* TR** per i bug che non rientrano nell'intervallo TR ma che devono comunque essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="1e0bd-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="1e0bd-709">Risorse</span><span class="sxs-lookup"><span data-stu-id="1e0bd-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="1e0bd-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Giochi per Windows: requisiti tecnici</span><span class="sxs-lookup"><span data-stu-id="1e0bd-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="1e0bd-711">Requisiti tecnici di Games for Windows: procedure consigliate per i giochi in Windows XP, Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e0bd-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="1e0bd-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1e0bd-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="1e0bd-713">SDK di Windows</span><span class="sxs-lookup"><span data-stu-id="1e0bd-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="1e0bd-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Linee guida per il controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="1e0bd-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-715">[Requisiti di sviluppo delle applicazioni di Windows Vista per la compatibilità del controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1e0bd-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer informazioni</span><span class="sxs-lookup"><span data-stu-id="1e0bd-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="1e0bd-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1e0bd-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="1e0bd-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="1e0bd-719">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="1e0bd-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="1e0bd-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX portale per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1e0bd-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="1e0bd-721">[Centro per sviluppatori DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="1e0bd-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="1e0bd-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog di Games for Windows e DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="1e0bd-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="1e0bd-723">Giochi per Windows e DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="1e0bd-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="1e0bd-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli di DirectX</span><span class="sxs-lookup"><span data-stu-id="1e0bd-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="1e0bd-725">Articoli tecnici su DirectX</span><span class="sxs-lookup"><span data-stu-id="1e0bd-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

