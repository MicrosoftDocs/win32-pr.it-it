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
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Giochi per i test case di Windows: procedure consigliate per i giochi in Windows XP, Windows Vista, Windows 7 e Windows 8

Questo articolo fornisce i test case per i giochi per Windows.

## <a name="how-to-use-this-article"></a>Come usare questo articolo

Questo articolo include tre sezioni principali:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisiti di test**
</dt> <dd>

Ogni requisito di test in questo documento è costituito da quattro sezioni principali: un titolo e una tabella con tre sezioni rilevanti (colonna sinistra, a destra in alto, a destra in basso).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Nome del test case.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, colonna all'estrema sinistra
</dt> <dd>

Nomi dei sistemi operativi a cui si applica il test case.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, a destra in alto
</dt> <dd>

Breve riepilogo del test case.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, a destra in basso
</dt> <dd>

Dettagli del test case effettivo.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script di test di esempio**
</dt> <dd>

Questa sezione è un esempio della sequenza che dovrebbe essere seguita da un passaggio di test tipico se si usano i requisiti di test come guida.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Note sugli strumenti di test**
</dt> <dd>

Questa sezione contiene le note dettagliate su ciascuno degli strumenti di test usati per verificare le condizioni di superamento o di errore nei requisiti di test.

</dd> </dl>

## <a name="test-requirements"></a>Requisiti di test

### <a name="1-game-requirements"></a>1. requisiti del gioco

### <a name="11-windows-games-explorer"></a>1,1 Esplora giochi di Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il gioco deve essere visibile all'interno di Esplora giochi in Windows Vista e Windows 7. Quando questa opzione è selezionata, il gioco deve anche visualizzare i metadati corretti. L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altra posizione. Le attività e i tasti di scelta rapida per la rimozione non devono essere creati.</td>
</tr>
<tr class="even">

<td><ol>
<li>Dopo l'installazione del gioco, aprire giochi Explorer.</li>
<li>Verificare che l'icona del gioco sia visualizzata in Games Explorer.</li>
<li>Fare clic con il pulsante destro del mouse sull'icona e testare tutte le attività di riproduzione & del supporto definite dall'applicazione.</li>
<li>Fare clic sull'icona e verificare che i metadati (Publisher, Developer, genre, data di rilascio, versione) nella parte inferiore visualizzino e siano corretti.</li>
<li>Verificare che nell'icona del gioco siano visualizzate le informazioni sugli indici di Windows Experience (WEI) in Games Explorer.</li>
<li>Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Game Explorer. Se non vengono visualizzati collegamenti ipertestuali, questo è un possibile segno che il file exe non è firmato. vedere la <a href="#23-sign-files">sezione 2,3</a>.</li>
<li>Verificare che il gioco visualizzi una classificazione di controllo parentale accurata in Games Explorer. Se viene indicato senza classificazione, verificare che si tratta di un gioco senza classificazione. in caso contrario, si tratta di un indicatore indicante che il file exe non è firmato. vedere la <a href="#23-sign-files">sezione 2,3</a>.</li>
<li>Verificare che il gioco non disponga dei collegamenti di avvio sul desktop dell'utente.</li>
<li>Fare clic su Start-> tutti i programmi.</li>
<li>Verificare che il gioco non disponga dei collegamenti di avvio nel menu Start.</li>
<li>Verificare che il gioco non disponga dei collegamenti di disinstallazione nel menu Start esterno al pannello di controllo.</li>
<li>Se il gioco è distribuito in formato digitale, verificare che il provider di servizi sia visualizzato in Esplora giochi di Windows.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1,2 sicurezza della famiglia di Windows/controlli padre



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il gioco deve essere eseguito nel contesto di un &quot; utente standard &quot; . I controlli padre devono essere in grado di bloccare il gioco. Verificare che l'oggetto GDF abbia nomi EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>Creare un account utente standard in Windows Vista o Windows 7 denominato Toby. Start-> pannello di controllo-> aggiungere o rimuovere account utente-> creare un nuovo account</li>
<li>Come Jane, dall'account amministratore impostare i controlli padre per il gioco. Start-> pannello di controllo-> configurare i controlli padre per qualsiasi utente-> Toby
<ol>
<li>Verificare che il gioco venga avviato dall'icona di Esplora giochi.</li>
<li>Verificare che il gioco visualizzi una valutazione accurata del controllo parentale sotto il titolo del gioco nel pannello di controllo dei controlli padre.</li>
<li>Prima di applicare i controlli padre, verificare che il gioco non richieda le credenziali di amministratore all'avvio.</li>
<li>Impostare i controlli padre &quot; su on &quot; .</li>
<li>Nella sezione impostazioni di Windows fare clic su giochi.</li>
<li>Fare clic su OK (l'impostazione dovrebbe essere ora &quot; Ao/tutti i giochi &quot; ).</li>
<li>Verificare che il gioco venga eseguito con queste impostazioni come utente Jane.</li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco venga eseguito con queste impostazioni come utente Toby.</li>
<li>Disconnettersi come Toby e accedere come Jane.</li>
<li>Tornare alla schermata precedente e selezionare &quot; imposta classificazioni giochi &quot; .</li>
<li><p>Selezionare una classificazione inferiore alla classificazione ESRB del gioco.</p>
<blockquote>
[!Note]<br />
Se il gioco non viene valutato, ignorare questo passaggio e passare alla parte successiva di questo test. Potrebbe essere necessario scegliere un sistema di classificazione diverso per trovare una classificazione del gioco, a seconda delle impostazioni locali della lingua dello SKU testato.
</blockquote>
<p><br/></p></li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco non venga avviato per l'utente Toby quando ESRB è bloccato dall'utente Jane.</li>
<li>Disconnettersi come Toby e accedere come Jane.</li>
<li>Se è stato modificato in precedenza, ripristinare le impostazioni di ESRB.</li>
<li>Se non sono presenti impostazioni di ESRB, selezionare &quot; blocca o Consenti giochi specifici &quot; e selezionare il gioco in base al nome.</li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco non venga avviato per l'utente Toby quando il nome di file EXE/nome è bloccato dall'utente Jane.</li>
<li>Disconnettersi da Toby e viceversa come Jane.</li>
<li>Come Jane, aprire controlli utente-> restrizioni dell'applicazione.</li>
<li>Fare clic su &quot; Toby è possibile utilizzare solo i programmi consentiti &quot; e fare clic su OK, ovvero non consentire alcun exe.</li>
<li>Vai a controlli utente | I giochi controllano e consentono al gioco specifico di usare la classificazione ESRB.</li>
<li>Disconnettersi da Jane e accedere come Toby e provare a riprodurre il gioco.</li>
<li>Verificare che il gioco non sia bloccato e che Toby possa riprodurlo quando non è &quot; impostato alcun exe &quot; .</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1,3 giochi Rich salvati di Windows Vista

Questo requisito è stato ritirato.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 controller comune di Xbox 360 per \[ requisito condizionale di Windows\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi che supportano i controller di gamepad devono supportare il controller Xbox 360 per Windows con l'API XInput. Tutti i riferimenti ai trigger e ai pulsanti comuni del controller devono usare i nomi di Xbox 360.</td>
</tr>
<tr class="even">

<td><ol>
<li>Avvia il gioco.</li>
<li>Passare alle opzioni del controller. **</li>
<li>Verificare che il gioco riconosca il controller Xbox 360 per Windows come dispositivo di input.</li>
<li>Riprodurre il gioco e verificare che il sistema di gioco e menu siano controllabili con il controller Xbox 360 per Windows.</li>
<li>Verificare che il controller Xbox 360 per Windows si comportano in base agli standard accettati. (B per indietro, A per accettazione, avvio per nel menu del gioco/pausa o accettazione e così via)</li>
<li>Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando i nomi di Xbox 360.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Se il gioco non supporta un controller di gioco e/o supporta solo tastiera/mouse, ignorare questo test case.
</blockquote>
<br/> * * Le impostazioni per il controller potrebbero trovarsi all'esterno del gioco. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1,5 più proporzioni e risoluzioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il gioco deve supportare almeno le proporzioni seguenti e le risoluzioni dello schermo associate: <br/>
<ul>
<li>4:3 &quot; normale &quot; (800 600 o 1024 768)</li>
<li>16:9 &quot; widescreen &quot; (1280 720)</li>
<li>16:10 &quot; widescreen &quot; (1152 720, 1680 1050 o 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Individuare le opzioni video per il gioco. è possibile che si trovino in gioco.<br/>
<blockquote>
[!Note]<br />
I test seguenti devono essere eseguiti su un monitor widescreen.
</blockquote>
<br/>
<ol>
<li>Nella sezione risoluzione del video selezionare 800 600 o 1024 768.</li>
<li>Verificare che il gioco venga eseguito a una risoluzione di 4:3 proporzioni.</li>
<li>Nella sezione risoluzione del video selezionare 1280 720.</li>
<li>Verificare che il gioco venga eseguito a una risoluzione di 16:9 proporzioni.</li>
<li>Nella sezione risoluzione del video selezionare 1680 1050, 800 480 o 1152 720.</li>
<li>Verificare che il gioco venga eseguito a una risoluzione di 16:10 proporzioni.</li>
<li>Verificare che il gioco non estenda l'immagine e a sua volta presenta un'area di visualizzazione più ampia.</li>
<li>Verificare che il gioco chieda all'utente quando viene apportata una modifica alla risoluzione.</li>
<li>Se l'utente non accetta entro 15 secondi, verificare che venga ripristinata l'impostazione precedente.</li>
<li>Verificare che il gioco non aggiunga barre nere a sinistra e a destra dell'area giochi. (In questo caso, l'area del gioco sarà ancora in un rapporto 4:3 al centro dello schermo).</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1,6 Windows Media Center

Questo requisito è stato ritirato.

### <a name="17-direct3d-conditional-requirement"></a>1,7 \[ requisito condizionale Direct3D\]



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere l'impostazione predefinita per qualsiasi opzione di configurazione di visualizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd> Avvia il gioco. Nelle opzioni video verificare se sono presenti opzioni di rendering, D3D e/o OpenGL. Se sono presenti, verificare che le opzioni di rendering del gioco siano predefinite in Direct3D. Se non si riesce a verificare che D3D9 sia la versione di DirectX in uso, procedere con il test automatizzato. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Usare lo strumento: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1,8 Abilita compatibilità DPI elevata



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando è abilitata la scalabilità DPI.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd>
<ol>
<li>Impostare il sistema su DPI 150%: <br/> Windows Vista: Pannello di controllo: personalizzazione, regolazione della dimensione del carattere (DPI), DPI personalizzato. Impostare su 150%.<br/> Windows 7: Pannello di controllo: visualizzazione, impostata su un numero di 150% superiore.<br/></li>
<li>Eseguire il processo di installazione e il gioco per verificare che non vi siano problemi con schermate o finestre di dialogo ritagliate.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Verificare che l'elemento <dpiAware>true</dpiAware> sia contenuto nel manifesto incorporato.<br/> Usare lo strumento: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. sicurezza e compatibilità

### <a name="21-follow-user-account-control-guidelines"></a>2,1 seguire le linee guida per il controllo dell'account utente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Ogni file eseguibile (. Estensione EXE) inclusa in un'applicazione deve avere un manifesto incorporato che ne definisce il livello di esecuzione:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Per i programmi di installazione dei giochi e dei giochi, uiAccess deve essere sempre impostato su &quot; false &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Verificare che i file eseguibili del gioco contengano manifesti.</li>
<li>Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia &quot; asInvoker &quot; .</li>
</ol>
Usare lo strumento: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2,2 supportano le versioni x64 di Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Per mantenere la compatibilità con le versioni x64 di Windows: <br/>
<ul>
<li>I titoli e i programmi di installazione del titolo non devono contenere codice a 16 bit o basarsi su un componente a 16 bit.</li>
<li>Se il gioco dipende da driver in modalità kernel per l'operazione, è necessario che siano disponibili versioni x64 di questi driver. L'installazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni di Windows a 64 bit.</li>
</ul>
<blockquote>
[!Note]<br />
Il supporto per l'edizione a 64 bit di Windows XP Professional è facoltativo.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Esegui il gioco nelle edizioni di Windows a 64 bit. Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista o Windows 7.</li>
<li>Verificare che il gioco non riscontri un errore a causa di eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista o Windows 7. Nell'errore verrà citata l'applicazione a 16 bit nella finestra di errore.</li>
<li>Se il gioco ha un eseguibile nativo a 64 bit, usare anche tale file.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2,3 file di firma



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tutti i file di codice eseguibile (ad esempio, con estensione exe e dll) devono essere firmati con un certificato Authenticode. <br/> Se si utilizza Windows Installer, i file del pacchetto del programma di installazione (file con estensione msi) devono essere firmati. <br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Passare alla directory del gioco.</li>
<li>Individuare tutti i file con estensione exe e dll.</li>
<li>Fare clic con il pulsante destro del mouse su proprietà per ogni file.</li>
<li>Verificare che i file eseguibili del gioco contengano una firma digitale.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2,4 firmare i driver



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente. <br/> Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve avere una firma Microsoft ottenuta tramite il programma Windows Hardware Quality Labs (WHQL) o driver affidabilità Signature (DRS). <br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Installare il gioco.</li>
<li>Verificare che il processo di installazione del gioco non visualizzi finestre di dialogo di driver non firmate.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2,5 eseguire correttamente il controllo della versione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi non devono essere eseguiti nei sistemi operativi futuri, come indicato dalle modifiche apportate al numero di versione di Windows, a meno che il contratto di licenza con l'utente finale non vieti l'uso nei sistemi operativi futuri. Se si suppone che il gioco abbia esito negativo, è necessario che venga visualizzato un messaggio all'utente.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd>
<ol>
<li>Installare il gioco in Windows XP, nelle edizioni a 32 bit di Windows Vista e Windows 7 e nelle edizioni a 64 bit di Windows Vista e Windows 7.</li>
<li>Verificare che il processo di installazione del gioco non riscontri un errore relativo alla versione del sistema operativo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Usare lo strumento: Application Verifier<br/>
<ol>
<li>Avviare Application Verifier.</li>
<li>Abilitare il test Compatibility: HighVersionLie dopo aver selezionato il INSTALL.EXE.</li>
<li>Installare il gioco e assicurarsi che non blocchi l'installazione in base alla versione del sistema operativo.</li>
<li>Abilitare il test Compatibility: HighVersionLie dopo aver selezionato il GAME.EXE.</li>
<li>Eseguire il gioco e assicurarsi che non blocchi l'esecuzione in base alla versione del sistema operativo.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2,6 supportare sessioni utente simultanee



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi devono supportare scenari multitasking standard di Windows.</td>
</tr>
<tr class="even">

<td>Creare un account utente standard in Windows Vista o Windows 7 denominato Toby. Start-> pannello di controllo-> aggiungere o rimuovere account utente-> creare un nuovo account <br/>
<ol>
<li>Avviare il gioco come utente Jane.</li>
<li>ALT + TAB per tornare al desktop.</li>
<li>Verificare che il gioco ALT + TAB sia corretto al desktop di Windows.</li>
<li>Fare clic su Start-> [freccia a destra di Lock]-> switch user.</li>
<li>Accedere come utente Toby.</li>
<li>Verificare che il gioco venga avviato come utente Toby mentre è ancora in esecuzione come utente Jane.</li>
<li>Verificare che il gioco non riscontri errori per l'utente Toby o l'utente Jane durante il processo switch utente.</li>
<li>Se è possibile avviare un'altra sessione del gioco, verificare che non sia possibile ascoltare audio dalla sessione del gioco originale.</li>
<li>Chiudere il gioco e tornare all'utente e al gioco originali.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2,7 supporto di nomi lunghi



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Se un gioco supporta il salvataggio di file, deve essere in grado di salvare i file con nomi e percorsi lunghi. Il gioco deve gestire correttamente caratteri di file system speciali, ad esempio \/: *? &quot; < o > in tutti i campi di input utente utilizzati per creare nomi file o percorsi.</td>
</tr>
<tr class="even">

<td><ol>
<li>Avvia il gioco.</li>
<li>Inizia una nuova partita.</li>
<li>Salvare il gioco. Durante il processo di salvataggio, verificare che il gioco venga salvato usando il nome Salva: il primo gioco Salva.</li>
<li>Tornare al menu principale.</li>
<li>Provare a caricare il gioco appena salvato.</li>
<li>Verificare che il gioco non riscontri errori durante la gestione di caratteri file system non supportati, ad esempio \/: *? &quot; < o > se il gioco ti consente, denominare il gioco salvato.</li>
<li>Se l'utente è autorizzato a assegnare un nome al profilo e/o a un carattere o a salvare le partite, verificare che il gioco non riscontri errori quando si usano nomi di file lunghi.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. installazione

### <a name="31-easy-install"></a>3,1 installazione semplificata



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi con un'installazione tradizionale devono fornire un percorso semplificato nell'interfaccia utente di configurazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inserire il disco del gioco.</li>
<li>Verificare che il gioco non visualizzi più di un contratto di licenza End-User (EULA).</li>
<li>Se il gioco supporta un'opzione di installazione personalizzata o avanzata, verificare che questa opzione sia accessibile durante il processo di installazione.</li>
<li>Verificare che l'opzione di installazione predefinita ignori tutte le selezioni di input dell'utente per il processo di installazione (selezione cartella di installazione, selezione componenti e così via).</li>
<li>Verificare che il processo di installazione del gioco non richieda la configurazione del componente del sistema operativo (installazione di DirectX, Runtime di Visual C e così via).</li>
<li>Verificare che il processo di installazione del gioco non richieda l'interazione del firewall.</li>
<li>Verificare che il gioco venga eseguito automaticamente o che al termine del processo di installazione sia presente un menu di avvio.</li>
<li>Verificare che il processo di disinstallazione del gioco rimuova tutti i file dei componenti del sistema operativo non ridistribuiti e installati e cancelli tutte le impostazioni. La pulizia di tutti i dati e le impostazioni per utente (ad esempio giochi salvati) non è necessaria.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3,2 supporto del controllo dell'account utente per l'installazione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente. I giochi devono pertanto eseguire attività per singolo utente durante la prima esecuzione separatamente dall'installazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Verificare che sia possibile installare il gioco come utente Jane. Questa operazione richiederà diritti elevati durante il processo di installazione/installazione.</li>
<li>Verificare che il processo di installazione del gioco chieda all'utente Jane di elevare le credenziali di amministratore. La richiesta di elevazione verrà rilevata quando l'utente tenta di installare.</li>
<li>Scegliere di eseguire l'autorun del gioco al termine dell'installazione, se non è già stato fatto, o di avviarlo dal menu visualizzato.</li>
<li>Una volta in gioco, creare un nuovo profilo, riprodurre e salvare un gioco.</li>
<li>Uscire dal gioco.</li>
<li>Riavviare il gioco e verificare che l'account utente Jane possa accedere a profili utente e giochi salvati.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3,3 installare in cartelle corrette



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Per impostazione predefinita, i giochi devono essere installati nella cartella programmi. I dati utente devono essere scritti alla prima esecuzione e non durante l'installazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installare il gioco usando il tipo di installazione predefinito.</li>
<li>Verificare che il gioco sia stato installato nei file di programma.</li>
</ol>
<blockquote>
[!Note]<br />
Se il test non riesce, verificare che il gioco sia destinato all'installazione per tutti gli utenti. In caso affermativo, si tratta di un errore.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3,4 installare correttamente le risorse di Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Le applicazioni non devono tentare di installare file o chiavi del registro di sistema protetti da Protezione risorse di Windows (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>Verificare che durante il processo di installazione non vengano visualizzate finestre di dialogo Protezione risorse di Windows WRP.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitare il riavvio durante l'installazione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il programma di installazione del gioco non deve presupporre che l'installazione dei componenti di Windows dai pacchetti di ridistribuzione richieda un riavvio, a meno che il riavvio non sia indicato da un risultato restituito o dalla documentazione Microsoft.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installare il gioco.</li>
<li>Verificare che il gioco non richieda il riavvio del sistema dopo l'installazione.</li>
</ol>
<blockquote>
[!Note]<br />
Se un Microsoft System Update REDIST richiede un riavvio, procedere come segue: completare l'installazione del gioco, disinstallare il gioco e reinstallare il gioco una seconda volta. Il processo di installazione del gioco non deve richiedere un riavvio in questa seconda installazione.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3,6 usare correttamente il controllo delle versioni dei file



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il programma di installazione del gioco deve verificare in modo corretto che siano installate le versioni dei file più recenti. L'installazione di un gioco non deve mai far regredire alcun file che non viene prodotto o condiviso da applicazioni che non vengono generate.</td>
</tr>
<tr class="even">

<td><ol>
<li>Prima di installare il gioco, creare uno snapshot di pre-installazione di system32.<br/>
<ol>
<li>Creare una directory denominata G4Wtest.</li>
<li>Visualizzare una finestra di comando (Start-> Run-> cmd).</li>
<li>Passare a c:\Windows\System32.</li>
<li>Digitare dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Creare uno snapshot di post-installazione di system32. <br/>
<ol>
<li>Visualizzare una finestra di comando (Start-> Run-> cmd).</li>
<li>Passare a c:\Windows\System32.</li>
<li>Digitare dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</li>
<li>Verificare che il gioco non regressioni le versioni di file dei file non prodotte dal gioco (... dei file elencati nei due documenti confrontando pregame.txt postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3,7 supporto \[ requisito condizionale Autorun\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Per i giochi distribuiti su CD, DVD o altri supporti rimovibili che supportano l'esecuzione automatica, quando il disco viene inserito per la prima volta, l'applicazione deve essere eseguita automaticamente o richiedere all'utente di installare il gioco. <br/>
<blockquote>
[!Note]<br />
I programmi di avvio automatico scritti per l'utilizzo nelle versioni di Windows precedenti a Windows Vista non devono utilizzare il Runtime .NET, perché questa tecnologia non è inclusa in Windows XP o nelle versioni precedenti di Windows.
</blockquote>
<br/> Per ulteriori informazioni, fare riferimento a <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">giochi per i requisiti tecnici di Windows</a> 3,7, supporto di autorun. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Inserire il disco del gioco o il supporto.</li>
<li>Verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente.</li>
<li>Windows Vista o Windows 7: verificare che il programma di avvio automatico del gioco non chieda all'utente Jane di elevare le credenziali di amministratore.</li>
<li>Verificare che l'eseguibile di autorun non richieda componenti predefiniti di REDIST, ad esempio .NET 3,5, librerie di Run-Time C e così via.</li>
<li>Verificare che la reinserimento del disco nell'unità dopo l'installazione non riavvii automaticamente l'installazione.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. affidabilità

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminare i riavvii non necessari



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Tutti i programmi di installazione di applicazioni devono sfruttare le API di gestione riavvio per evitare il riavvio del sistema (vedere [requisito 3,5](#35-avoid-reboots-during-installation)). |



 

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminare Application Verifier errori



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il gioco non deve generare errori con Microsoft Application Verifier (AppVerifier), versione 4,0 o successiva, nei test seguenti: <br/>
<ul>
<li>Nozioni fondamentali: handle, heap, blocchi, memoria, TLS</li>
<li>Varie: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Usare lo strumento: AppVerifier 4,0 (o versione successiva)<br/>
<ol>
<li>Installare AppVerifier.</li>
<li>Avviare AppVerifier e selezionare file-> Aggiungi applicazione.</li>
<li>Individuare l'eseguibile del gioco, selezionarlo e fare clic sul &quot; &quot; pulsante Apri.</li>
<li>Nella &quot; sezione applicazioni &quot; selezionare l'eseguibile del gioco.</li>
<li>Nella &quot; sezione test &quot; selezionare i test sopra elencati sotto le categorie &quot; nozioni di &quot; base &quot; e &quot; varie (deselezionare ThreadPool e TimeRollOver) e assicurarsi che tutti gli altri test non siano selezionati.</li>
<li>Avvia il gioco.</li>
<li>Verificare che il gioco non generi errori quando viene eseguito in Application Verifier.</li>
</ol>
<blockquote>
[!Note]<br />
Per alcuni test è necessario eseguire completamente un debugger. Potrebbe essere necessaria una versione di rilascio non protetta del file eseguibile del gioco, perché la tecnologia anti-cheat/anti-pirateria potrebbe interferire con AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4,3 supporto Segnalazione errori Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi devono gestire solo le eccezioni note e previste e Segnalazione errori Windows non devono essere disabilitate. Se un errore, ad esempio una violazione di accesso, viene inserito in un gioco, deve consentire Segnalazione errori Windows di segnalare l'arresto anomalo.</td>
</tr>
<tr class="even">

<td>Usare lo strumento: thread hijacker <br/>
<ul>
<li>Se l'applicazione si arresta in modo anomalo durante il test, verificare che il gioco venga visualizzato Segnalazione errori Windows correttamente e raccolga i dati di arresto anomalo.</li>
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
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tutti i file eseguibili (ad esempio, file con estensione exe o dll) devono contenere un nome di prodotto, un nome della società e una versione del file accurati.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuale:</dt> <dd>
<ol>
<li>Fare clic con il pulsante destro del mouse sui file eseguibili del gioco nel supporto di installazione di e in quelli installati sul disco rigido del computer.</li>
<li>Selezionare Proprietà.</li>
<li>Windows XP: fare clic sulla scheda <strong>versione</strong> . Verificare che il nome del prodotto, il nome della società e i campi della versione del file siano stati popolati correttamente.</li>
<li>Windows Vista o Windows 7: fare clic sulla scheda <strong>Dettagli</strong> . Verificare che i campi nome prodotto e versione file siano popolati correttamente. Il nome della società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatizzato:</dt> <dd>
<ul>
<li>Usare lo strumento di test di Microsoft Games per Windows; vedere la <a href="#64-microsoft-games-for-windows-test-tool">sezione 6,4</a>.</li>
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
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>La normale uscita del gioco non può causare un errore di eccezione sconosciuto.</td>
</tr>
<tr class="even">

<td><ul>
<li>Dopo aver giocato il gioco per una normale sessione di gioco, verificare che il gioco non generi errori all'uscita.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. script di test di esempio

Questo è un esempio di un test tipico che usa i requisiti di test precedenti come guida.

### <a name="51-tools"></a>strumenti di 5,1

-   edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD
-   edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel
-   edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD
-   edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel
-   edizione a 32 bit di Windows XP SP2 in una CPU AMD
-   edizione a 32 bit di Windows XP SP2 in una CPU Intel
-   Monitor a schermo intero che supporta 1680 1050
-   Controller Xbox 360 per Windows

### <a name="52-pre-install"></a>5,2 pre-installazione

1.  Windows Vista e Windows 7: creazione di due utenti standard: Jane e Toby
2.  Windows Vista e Windows 7: verificare che il controllo dell'account utente sia abilitato
3.  Creare uno snapshot di pre-installazione di system32

    1.  Creare una directory denominata G4Wtest
    2.  Visualizzare una finestra di comando (Start-> Run-> cmd)
    3.  Passare a c: \\ Windows \\ system32
    4.  Digitare dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista e Windows 7: impostare su 150% DPI \[ 1,8\]
5.  Procedere con l' [installazione](#3-installation)

### <a name="53-install"></a>5,3 installazione

1.  Accedi come utente Jane
2.  Inserire il disco del gioco nell'unità CD/DVD, verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente \[ 3,7\]
3.  Verificare che il processo di installazione del gioco chieda all'utente Jane di elevare le credenziali di amministratore \[ 3,2\]
4.  Verificare che il programma di avvio automatico del gioco non chieda all'utente Jane di elevare le credenziali di amministratore \[ 3,7\]
5.  Verificare che il gioco non visualizzi più di un contratto di licenza di End-User (EULA) \[ 3,1\]
6.  Verificare che il gioco visualizzi le opzioni di installazione predefinite/semplici e personalizzate/avanzate \[ 3,1\]
7.  Verificare che l'opzione di installazione predefinita/semplice ignori tutte le selezioni di input dell'utente per il processo di installazione (selezione cartella di installazione, selezione componenti e così via) \[ . 3,1\]
8.  Verificare che il processo di installazione del gioco non richieda la configurazione del componente del sistema operativo (installazione di DirectX, librerie di Run-Time C e così via) \[ . 3,1\]
9.  Verificare che il processo di installazione del gioco non richieda l'interazione del firewall \[ 3,1\]
10. Verificare che il processo di installazione del gioco non riscontri un errore relativo alla versione del sistema operativo \[ 2,5 \] \[ 4,2\]
11. Verificare che il processo di installazione del gioco non visualizzi finestre di dialogo di driver non firmate \[ 2,4\]
12. Verificare che non venga visualizzata alcuna finestra di dialogo Protezione risorse di Windows (WRP) durante il processo di installazione \[ 3,4\]
13. Verificare che il nuovo inserimento del disco nell'unità dopo l'installazione non riavvii automaticamente l'installazione
14. Verificare che il gioco non richieda il riavvio del sistema dopo l'installazione \[ 3,5\]
15. Verificare che sia possibile installare il gioco come utente Jane \[ 3,2\]
16. Verificare che venga eseguito automaticamente il gioco o che sia presente un menu di avvio al termine del processo di installazione \[ 3,1\]
17. Se il gioco viene eseguito automaticamente dopo l'installazione, passare al [Runtime](#55-runtime)
18. Se il gioco ha lasciato un menu di avvio o non è stato possibile disinstallarlo, vedere la sezione [post-installazione](#54-post-install)

### <a name="54-post-install"></a>5,4 post-installazione

1.  Verificare che il gioco non disponga dei collegamenti di avvio sul desktop dell'utente \[ 1,1\]
2.  Verificare che il gioco non disponga dei collegamenti di avvio nel menu Start \[ 1,1\]
3.  Verificare che l'icona del gioco sia visualizzata in Windows Games Explorer \[ 1,1\]
4.  Verificare che i metadati (Publisher, Developer, genre, data di rilascio, versione) nella parte inferiore visualizzino e siano corretti \[ 1,1\]
5.  Verificare che nell'icona del gioco siano visualizzate le informazioni sugli indici Windows Experience (WEI) in Windows Games Explorer \[ 1,1\]
6.  Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Esplora giochi di Windows \[ 1,1\]
7.  Verificare che il gioco visualizzi una classificazione di controllo parentale accurata in Windows Games Explorer \[ 1,1\]
8.  Creare uno snapshot di post-installazione di system32

    1.  Visualizzare una finestra di comando (Start-> Run-> cmd)
    2.  Passare a c: \\ Windows \\ system32
    3.  Digitare dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Verificare che il gioco non regressione le versioni dei file elencate nei due documenti confrontando pregame.txt con postgame.txt \[ 3,6\]

9.  Vai al [Runtime](#55-runtime)

### <a name="55-runtime"></a>5,5 Runtime

1.  RUNTIME 1: se il menu Launch è presente, avviare il gioco da questa posizione. Se il gioco è stato eseguito automaticamente o è stato avviato dal menu di avvio del gioco dopo l'installazione, eseguire le operazioni seguenti: in caso contrario, passare a RUNTIME 2:

    1.  Crea un profilo (se il gioco lo consente)
    2.  Avvia un nuovo gioco
    3.  Salva il gioco
    4.  Uscire dal gioco
    5.  Avvia il gioco da Esplora giochi
    6.  Verificare che il gioco venga avviato dall'icona di Esplora giochi \[ 1,2\]
    7.  Verificare che il gioco non richieda le credenziali di amministratore all'avvio \[ 1,2\]
    8.  Verificare che sia possibile accedere ai profili utente e salvare le partite dall'account utente Jane \[ 3,2\]
    9.  Vai al RUNTIME 3

2.  RUNTIME 2: se il gioco non è stato eseguito automaticamente o Visualizza un avvio dal menu di avvio del gioco, si tratta di un errore \[ 3,1 \] . Tuttavia, il test può continuare normalmente:

    1.  Avvia il gioco da Esplora giochi
    2.  Verificare che il gioco venga avviato dall'icona di Esplora giochi \[ 1,2\]
    3.  Verificare che il gioco non richieda le credenziali di amministratore all'avvio \[ 1,2\]
    4.  Vai al RUNTIME 3

3.  RUNTIME 3: se il gioco supporta un riquadro del gioco, verificare che il gioco riconosca il controller Xbox 360 per Windows come dispositivo di input \[ 1,4\]

    1.  Se necessario, abilitare il controller tramite il menu opzioni
    2.  Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando i nomi di Xbox 360
    3.  Verificare che il sistema di gioco e menu siano controllabili con il controller Xbox 360 per Windows
    4.  Verificare che il controller Xbox 360 per Windows si comportano in base agli standard accettati

4.  Impostare il video su \[ 1,5 \] :

    1.  Verificare che il gioco venga eseguito a una risoluzione di 4:3 proporzioni (800 600 o 1024 768)
    2.  Verificare che il gioco venga eseguito a una risoluzione di 16:9 proporzioni (1280 720)
    3.  Verificare che il gioco venga eseguito a una risoluzione di 16:10 proporzioni (1680 1050, 800 480 o 1152 720)
    4.  Verificare che il gioco chieda all'utente quando viene apportata una modifica alla risoluzione
    5.  Se non si accettano entro 15 secondi, verificare che venga ripristinata l'impostazione precedente.
    6.  Verificare che il gioco non estenda l'immagine e a sua volta presenta un'area di visualizzazione più ampia
    7.  Verificare che il gioco non aggiunga barre nere a sinistra e a destra dell'area giochi

5.  Se disponibile nelle impostazioni video, verificare che le opzioni di rendering del gioco siano predefinite per Direct3D \[ 1,7 \] . in caso contrario, procedere con i [test automatizzati](#58-automated-tests)
6.  Se richiesto o se l'opzione è disponibile, creare un profilo utente. Verificare che il gioco non riscontri errori durante l'uso di nomi di file lunghi \[ 2,7\]
7.  Avviare un nuovo gioco, creare un gioco e verificare che nel gioco non si verifichino errori durante la gestione di caratteri file system non supportati \[ 2,7\]
8.  Verificare che il gioco ALT + TAB sia corretto al desktop di Windows \[ 2,6\]

    1.  Cambiare gli utenti con il gioco in esecuzione facendo clic su Start-> utente switch
    2.  Accedi come Toby
    3.  Verificare che il gioco venga avviato come utente Toby mentre è ancora in esecuzione come utente Jane \[ 2,6\]
    4.  Verificare che il gioco non riscontri errori per l'utente Toby o l'utente Jane durante il passaggio dell'utente processo \[ 2,6\]
    5.  Verificare che non sia possibile ascoltare audio dalla sessione di gioco originale \[ 2,6\]
    6.  Uscire dal gioco
    7.  Disconnetti Toby
    8.  Tornare all'utente originale in cui è in esecuzione il gioco
    9.  ALT + TAB di nuovo nel gioco

9.  Uscire dal gioco
10. Passa a [post-Runtime](#56-post-runtime)

### <a name="56-post-runtime"></a>5,6 post-Runtime

1.  Verificare che il gioco non generi errori all'uscita \[ 4,3\]
2.  Verificare che il gioco sia installato nei file di programma \[ 3,3\]
3.  Passare a [controlli padre](/windows)

### <a name="57-parental-controls"></a>5,7 controlli parentali

1.  Aprire i controlli padre nel pannello di controllo
2.  Verificare che il gioco visualizzi una valutazione del controllo parentale accurata sotto il titolo del gioco nel pannello di controllo dei controlli padre \[ 1,2\]
3.  Vedere il test case \[ 1,2 \] per i test seguenti:

    1.  Dopo aver impostato i controlli padre su "on", verificare che il gioco venga eseguito con queste impostazioni come utente Jane \[ 1,2\]
    2.  Disconnettersi e accedere come Toby
    3.  Verificare che il gioco venga eseguito con queste impostazioni come utente Toby \[ 1,2\]
    4.  Disconnettersi e accedere come Jane
    5.  Nella sezione Parental Control (controllo parentale) impedire all'utente Toby di visualizzare i giochi un livello di ESRB superiore e superiore del gioco appena installato

        Esempio: se il gioco è classificato E, impostarlo in modo che Toby possa riprodurre solo giochi con classificazione C

    6.  Verificare che il gioco venga eseguito con queste impostazioni come utente Jane \[ 1,2\]
    7.  Disconnetti e accedi come utente Toby
    8.  Verificare che il gioco non venga avviato all'utente Toby quando ESRB è bloccato dall'utente Jane \[ 1,2\]
    9.  Disconnetti come utente Toby e viceversa come utente Jane
    10. Se è stato modificato in precedenza, ripristinare le impostazioni di ESRB
    11. Se non sono presenti impostazioni di ESRB, selezionare "blocca o Consenti giochi specifici" e selezionare il gioco per nome
    12. Disconnettersi come Jane e come Toby
    13. Verificare che il gioco non venga avviato all'utente Toby quando il nome del file/EXE è bloccato dall'utente Jane \[ 1,2\]
    14. Disconnettersi come Toby e tornare indietro come Jane
    15. Come Jane, aprire controlli utente-> restrizioni applicazione
    16. Fare clic su "Toby può utilizzare solo i programmi consentiti", quindi fare clic su OK, ovvero non consentire alcun exe
    17. Fare clic sulla casella Deseleziona tutto, quindi fare clic su OK.
    18. Passare a controlli utente \| giochi controlli e consentire il gioco specifico usando la classificazione ESRB
    19. Disconnettersi con Jane e accedere come Toby e provare a riprodurre il gioco
    20. Verificare che il gioco non sia bloccato e che Toby possa riprodurlo quando l'impostazione "Consenti nessun exe" è impostata su \[ 1,2\]
    21. Disconnetti come utente Toby e viceversa come utente Jane
    22. Passare a controlli padre nel pannello di controllo e rimuovere le restrizioni
    23. Verificare che entrambi gli utenti possano ora riprodurre il gioco

4.  Procedi ai [test automatizzati](#58-automated-tests)

### <a name="58-automated-tests"></a>5,8 test automatizzati

1.  Verificare che il gioco non generi errori quando viene eseguito in Application Verifier. vedere la documentazione dello strumento di test di personalizzazione \[ 4,2\]
2.  Verificare che i file eseguibili del gioco contengano manifesti. vedere la documentazione dello strumento di test di personalizzazione \[ 2,1\]
3.  Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia "AsInvoker". vedere la documentazione dello strumento di test di personalizzazione \[ 2,1\]
4.  Procedi ad [altri test](#59-other-tests)

### <a name="59-other-tests"></a>5,9 altri test

1.  Verificare che i file eseguibili del gioco contengano una firma digitale \[ 2,3\]
2.  Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2,3\]
3.  Verificare che il gioco non riscontri un errore a causa di eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2,3\]
4.  Forzare l'arresto anomalo dell'applicazione durante il test e verificare che il gioco venga visualizzato Segnalazione errori Windows correttamente e raccoglie i dati di arresto anomalo \[ 4,3\]
5.  Verificare che i riepiloghi di file 4,3 siano corretti \[\]

    1.  Fare clic su Start-> computer
    2.  Passare alla directory del gioco
    3.  Nella finestra di ricerca digitare \* . dll
    4.  Per ogni file: fare clic con il pulsante destro del mouse sul file e scegliere Proprietà.

        -   In Windows XP: fare clic sulla scheda versione. Verificare che il nome del prodotto, il nome della società e i campi della versione del file siano stati popolati correttamente. \[4,3\]
        -   In Windows Vista e Windows 7: fare clic sulla scheda Dettagli. Verificare che i campi nome prodotto e versione file siano popolati correttamente. Il nome della società non è visibile nella pagina delle proprietà di Windows Vista o Windows 7 \[ 4,3\]

    5.  Ripeti questo controllo per i file exe

6.  Avvia il gioco.

    1.  Premere CTRL + ALT + CANC
    2.  Fare clic sulla freccia "opzioni di arresto"
    3.  Fare clic su Riavvia
    4.  Verify Game non blocca l'arresto \[ 3,1\]

7.  Procedere alla [disinstallazione](#510-uninstall)

### <a name="510-uninstall"></a>5,10 Disinstalla

-   Verificare che il processo di disinstallazione del gioco elimini tutti i file dei componenti del sistema operativo installati e non ridistribuiti e elimini tutte le impostazioni \[ 3,1\]

    -   Verificare in Windows Vista o Windows 7 che il pannello di controllo sia l'unico modo per rimuovere il programma \[ 1,1\]

## <a name="test-tool-notes"></a>Note sugli strumenti di test

Si tratta di note per ciascuno degli strumenti di test elencati nei requisiti di test precedenti.

### <a name="61-appverifier-40-or-higher"></a>6,1 AppVerifier 4,0 (o versione successiva)

**Test case: 2,5, 4,2**

> [!Note]  
> Alcune applicazioni non vengono eseguite con AppVerifier in esecuzione, a causa della protezione della copia. Questo problema può essere risolto eseguendo con una versione di rilascio non protetta del file eseguibile del gioco.

 

1.  Installare AppVerifier 4,0 (o versione successiva) in un computer che esegue Windows XP
2.  Avviare AppVerifier e fare clic su file-> Aggiungi applicazione
3.  Individuare il file eseguibile del gioco, selezionarlo e fare clic su Apri
4.  Nella sezione "applicazioni" selezionare il file eseguibile del gioco
5.  Nella sezione "Nozioni di base" selezionare i test seguenti:

    -   Selettori
    -   Heap
    -   Locks
    -   Memoria
    -   TLS

6.  Nella sezione "varie" selezionare i test seguenti:

    -   DangerousAPIs
    -   DirtyStacks

7.  Assicurarsi che tutti gli altri test non siano selezionati
8.  Avvia il gioco
9.  Gioca il gioco
10. Chiudere il gioco
11. In AppVerifier selezionare Visualizza-> log
12. Nella sezione "applicazioni" selezionare il file app. exe
13. Nella sezione "log" selezionare il file di log e osservare il numero di errori. Se non sono presenti errori, terminare i test di AppVerifier. Se sono presenti errori, fare clic sul pulsante Visualizza.
14. Eseguire una ricerca nel documento (CTRL + F) per gravità = "errore
15. Crea bug in base alla parte dell'errore LayerName =

### <a name="62-manifest-test---mtexe"></a>Test del manifesto 6,2-mt.exe

**Test case: 1,8, 2,1**

Questo strumento viene eseguito da un prompt dei comandi in cui si trova MT.exe.

Esempio:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Fare clic su Start-> Esegui-> digitare cmd e fare clic sul pulsante OK
2.  Eseguire lo strumento mt.exe per generare un file con estensione manifest per ogni file exe che viene installato con il gioco
3.  Aprire il file con estensione manifest generato
4.  Verificare che ogni file con estensione exe includa le seguenti richieste:

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
> Il livello di esecuzione richiesto deve essere presente per ogni file e dpiAware deve essere presente per almeno il file eseguibile del gioco.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>aspirato thread 6,3-threadhijacker.exe

Questo strumento viene eseguito da un prompt dei comandi in cui si trova threadhijacker.exe.

Esempio:

``` syntax
threadhijacker.exe /process:str
```

Dove Str è il nome \_ del \_program.exe

1.  Aprire Gestione attività, fare clic sulla scheda processi e individuare il nome del file eseguibile del gioco.
2.  Aprire un prompt dei comandi in modalità di amministrazione
3.  Passare alla directory in cui threadhijacker.exe è
4.  Tipo: **threadhijacker.exe/Process:** Str, dove Str è il nome del file eseguibile che si desidera raggiungere

### <a name="64-microsoft-games-for-windows-test-tool"></a>6,4 Microsoft Games per Windows Test Tool

Questo strumento si trova in DirectX SDK. Una volta installato l'SDK in un computer, il programma di installazione per lo strumento di test giochi per Windows può essere inserito nel computer di test e installato.

Individuare il programma di installazione di Microsoft Games for Windows Test Tool nel computer di sviluppo in cui è installato DirectX SDK. Per impostazione predefinita, viene inserito nel percorso seguente:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copiare il programma di installazione (MicrosoftGFWTestTool.msi/setup.exe) nel computer di test.
2.  Eseguire il programma di installazione.
3.  Avviare lo strumento di test di Microsoft Games per Windows.
4.  Nel campo **elenco progetti** sostituire **Crea nuovo progetto** con il nome del titolo e fare clic su **Crea nuovo**.

    Attendere il completamento della linea di base.

5.  Immettere le informazioni eventualmente disponibili nella sezione **informazioni sul gioco** e fare clic su **Aggiorna informazioni sul gioco**.
6.  Fare clic sulla scheda **test case** .
7.  A partire dalla parte superiore, procedere con i test case, facendo clic su **superato** o **non superato** in base alle esigenze.

    Per informazioni dettagliate sull'inclusione di un bug nel report, vedere la sezione relativa alla scrittura di un bug, più avanti in questa sezione.

8.  Tornare alla scheda **progetti** dopo aver esaminato il report controllando le schede **report** e **modifica bug** .
9.  Fare clic su **Compila report**.

    Una finestra verrà aperta al termine della compilazione del report. Qui sarà disponibile un. Nome file ZIP *nomeprogetto* \_report.zip. Questo file contiene tutti i log e i risultati raccolti durante il superamento del test.

### <a name="writing-a-bug"></a>Scrittura di un bug

Per scrivere un report sui bug è possibile procedere in due modi: è possibile eseguire i test case e fare clic su **Fail** quando il titolo non riesce a test case oppure è possibile fare clic sulla scheda **modifica bug** e aggiungere manualmente un report sui bug.

### <a name="clicking-fail-on-a-test-case"></a>Fare clic su Fail in un test case

1.  Quando si fa clic su **Fail** in una test case, l'elenco a discesa **tipo di problema** verrà impostato automaticamente sul tipo di test case.
2.  Aggiungere una breve descrizione al campo **title** che descrive brevemente il problema.
3.  Aggiungere una descrizione dettagliata del problema al campo **comportamento osservato** .
4.  Se necessario, aggiungere il valore previsto (in contrapposizione a una descrizione del problema) al campo **comportamento previsto** .
5.  Aggiungere una descrizione dettagliata di come riprodurre il problema nel campo ripetizione dei **passaggi** .
6.  Al termine, fare clic sul pulsante **Salva** .

### <a name="manually-adding-a-bug"></a>Aggiunta manuale di un bug

Questo processo equivale a fare clic su **Fail (errore**), ad eccezione dell'elenco a discesa popolato automaticamente. In questo caso, selezionare il tipo di errore TCR appropriato oppure selezionare un **\* \* problema \* \* non TR** per i bug che non rientrano nell'intervallo TR, ma devono comunque essere segnalati.

## <a name="resources"></a>Risorse

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Giochi per Windows: requisiti tecnici
</dt> <dd>

[Giochi per i requisiti tecnici di Windows: procedure consigliate per giochi in Windows XP, Windows Vista e Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[SDK di Windows](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Linee guida per il controllo dell'account utente
</dt> <dd>

[Requisiti per lo sviluppo di applicazioni Windows Vista per la compatibilità con controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Informazioni Windows Installer
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portale per sviluppatori WinQual 
</dt> <dd>

[Servizi online di qualità Windows (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Portale per sviluppatori DirectX
</dt> <dd>

[Centro per sviluppatori DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sui giochi per Windows e DirectX SDK
</dt> <dd>

[Giochi per Windows e DirectX SDK](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli su DirectX
</dt> <dd>

[Articoli tecnici su DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

