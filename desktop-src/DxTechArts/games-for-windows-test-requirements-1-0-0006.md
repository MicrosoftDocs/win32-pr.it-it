---
title: 'Test case dei giochi di Windows: procedure consigliate per giochi su Windows XP, Windows Vista, Windows 7 e Windows 8'
description: Questo articolo fornisce test case per i giochi per Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9848131cae57e1f456f2ca7a497f10c8865fad146aa82c7b73f99180dcb75aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107581"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8

Questo articolo fornisce test case per i giochi per Windows.

## <a name="how-to-use-this-article"></a>Come usare questo articolo

Questo articolo contiene tre sezioni principali:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Requisiti di test**
</dt> <dd>

Ogni requisito di test in questo documento include quattro sezioni principali: un titolo e una tabella con tre sezioni principali (colonna sinistra, in alto a destra, in basso a destra).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Nome del test case.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, colonna all'estrema sinistra
</dt> <dd>

Nomi dei sistemi operativi a cui si test case sistema operativo.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Casella, in alto a destra
</dt> <dd>

Breve riepilogo del test case.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Casella, in basso a destra
</dt> <dd>

Dettagli dell'effettivo test case.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Script di test di esempio**
</dt> <dd>

Questa sezione è un esempio della sequenza che verrebbe seguito da un tipico test superato se si usano i requisiti di test come guida.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Note dello strumento di test**
</dt> <dd>

Questa sezione contiene note dettagliate su ognuno degli strumenti di test usati per verificare le condizioni di superati o non superati nei requisiti di test.

</dd> </dl>

## <a name="test-requirements"></a>Requisiti di test

### <a name="1-game-requirements"></a>1. Requisiti del gioco

### <a name="11-windows-games-explorer"></a>1.1 Windows Games Explorer



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il gioco deve essere visibile all'interno Games Explorer in Windows Vista e Windows 7. Quando questa opzione è selezionata, il gioco deve visualizzare anche i metadati corretti. L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altro percorso. Le attività e i collegamenti per la rimozione non devono essere creati.</td>
</tr>
<tr class="even">

<td><ol>
<li>Dopo aver installato il gioco, aprire Games Explorer.</li>
<li>Verificare che l'icona del gioco sia visualizzata Games Explorer.</li>
<li>Fare clic con il pulsante destro del mouse sull'icona e testare ogni attività di riproduzione definita dall'& supporto tecnico.</li>
<li>Fare clic sull'icona e verificare che i metadati (editore, sviluppatore, genere, data di rilascio, versione) nella parte inferiore siano visualizzati e siano corretti.</li>
<li>Verificare che l'icona del gioco Windows informazioni sull'indice dell'esperienza utente (WEI) Games Explorer.</li>
<li>Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Games Explorer. Se i collegamenti ipertestuali non vengono visualizzati, questo è un possibile segno che il file exe non è firmato. Vedere la sezione <a href="#23-sign-files">2.3.</a></li>
<li>Verificare che il gioco visualizzi una classificazione di controllo genitori accurata Games Explorer. Se viene visualizzato un messaggio senzarate, verificare che si tratta di un gioco senzarate. In caso contrario, si tratta di un indicatore che indica che il file exe non è firmato. Vedere la sezione <a href="#23-sign-files">2.3.</a></li>
<li>Verificare che il gioco non posiziona i tasti di scelta rapida di avvio sul desktop dell'utente.</li>
<li>Fare clic su Start -> Tutti i programmi.</li>
<li>Verificare che il gioco non posiziona i tasti di scelta rapida di avvio nel menu Start.</li>
<li>Verificare che i tasti di scelta rapida di disinstallazione non siano posizionati nel menu Start all'esterno Pannello di controllo.</li>
<li>Se il gioco viene distribuito digitalmente, verificare che il provider di servizi sia visualizzato Windows Games Explorer.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1.2 Windows Family Safety/Controllo genitori



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il gioco deve essere eseguito nel contesto di un &quot; utente &quot; standard. Il controllo genitori deve essere in grado di bloccare il gioco. Verificare che la funzione GDF abbia nomi EXE.</td>
</tr>
<tr class="even">

<td><ol>
<li>Creare un account utente standard in Windows Vista o Windows 7 denominato Toby. Avviare -> Pannello di controllo -> Aggiungi o rimuovi account utente -> Crea nuovo account</li>
<li>Come Jane, dall'account amministratore configurare Controllo genitori per il gioco. Start -> Pannello di controllo -> Set Up Parent Controls for Any User -> Toby
<ol>
<li>Verificare che il gioco si avvii dall Games Explorer icona.</li>
<li>Verificare che il gioco visualizzi una valutazione accurata di Controllo genitori sotto il titolo del gioco nella scheda Controllo genitori Pannello di controllo.</li>
<li>Prima di applicare il controllo genitori, verificare che il gioco non richiedi credenziali di amministratore all'avvio.</li>
<li>Impostare Controllo genitori su &quot; On &quot; .</li>
<li>Nella sezione Windows Impostazioni fare clic su Giochi.</li>
<li>Fare clic su OK (l'impostazione dovrebbe &quot; ora essere AO/tutti i &quot; giochi).</li>
<li>Verificare che il gioco venga eseguito con queste impostazioni come User Jane.</li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco venga eseguito con queste impostazioni come User Toby.</li>
<li>Disconnettersi come Toby e accedere come Jane.</li>
<li>Tornare alla schermata precedente e selezionare &quot; Set Game Ratings (Imposta classificazioni &quot; gioco).</li>
<li><p>Selezionare una classificazione inferiore alla classificazione ESRB del gioco.</p>
<blockquote>
[!Note]<br />
Se il gioco non viene valutato, ignorare questo passaggio e passare alla parte successiva di questo test. Potrebbe essere necessario scegliere un sistema di classificazione diverso per trovare una classificazione del gioco, a seconda delle impostazioni locali della lingua dello SKU testato.
</blockquote>
<p><br/></p></li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco non si avvii per User Toby quando ESRB è bloccato dall'utente Jane.</li>
<li>Disconnettersi come Toby e accedere come Jane.</li>
<li>Se è stato modificato in precedenza, ripristinare le impostazioni di ESRB.</li>
<li>Se non sono presenti impostazioni ESRB, selezionare Blocca o Consenti &quot; giochi specifici e selezionare il gioco in base al &quot; nome.</li>
<li>Disconnettersi come Jane e accedere come Toby.</li>
<li>Verificare che il gioco non si avvii per User Toby quando EXE/Name è bloccato dall'utente Jane.</li>
<li>Disconnettersi come Toby e accedere di nuovo come Jane.</li>
<li>Come Jane, aprire Controlli utente -> restrizioni dell'applicazione.</li>
<li>Fare clic su Toby può usare solo i programmi consentiti e fare clic &quot; su OK &quot; ,ovvero non consentire alcun file exe.</li>
<li>Passare a Controlli utente | Games Controlla e consente il gioco specifico usando la classificazione ESRB.</li>
<li>Disconnettersi come Jane e accedere come Toby e provare a eseguire il gioco.</li>
<li>Verificare che il gioco NON sia bloccato e che Toby possa riprodurlo quando non sono impostati &quot; file &quot; exe consentiti.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1.3 Windows Rich Saved Games di Vista

Questo requisito è stato ritirato.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Xbox 360 Common Controller for Windows \[ Conditional Requirement\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi che supportano i controller del game pad devono supportare controller Xbox 360 per Windows l'API XInput. Tutti i riferimenti ai trigger e ai pulsanti del controller comuni devono usare Xbox 360 nomi.</td>
</tr>
<tr class="even">

<td><ol>
<li>Avviare il gioco.</li>
<li>Passare alle opzioni del controller. **</li>
<li>Verificare che il gioco riconosca controller Xbox 360 per Windows come dispositivo di input.</li>
<li>Riprodurre il gioco e verificare che il sistema di gioco e menu sia controllabile con controller Xbox 360 per Windows.</li>
<li>Verificare che il controller Xbox 360 per Windows si comporti in base agli standard accettati. (B per back, A per accept, Start for in game menu/pause or accept, etc.)</li>
<li>Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller Xbox 360 nomi.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Se il gioco non supporta un controller di gioco e/o supporta solo tastiera/mouse, ignorare questo test case.
</blockquote>
<br/> ** Impostazioni per il controller potrebbe trovarsi all'esterno del gioco. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1.5 Proporzioni e risoluzioni multiple



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
<li>Schermo widescreen 16:9 &quot; &quot; (1280 720)</li>
<li>Widescreen 16:10 &quot; &quot; (1152 720, 1680 1050 o 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Individuare le opzioni video per il gioco (potrebbe essere fuori gioco).<br/>
<blockquote>
[!Note]<br />
I test seguenti devono essere eseguiti su un monitor widescreen.
</blockquote>
<br/>
<ol>
<li>Nella sezione risoluzione video selezionare 800 600 o 1024 768.</li>
<li>Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 4:3.</li>
<li>Nella sezione risoluzione video selezionare 1280 720.</li>
<li>Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:9.</li>
<li>Nella sezione risoluzione video selezionare 1680 1050, 800 480 o 1152 720.</li>
<li>Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:10.</li>
<li>Verificare che il gioco non estensa l'immagine e a sua volta presenti un'area di visualizzazione più ampia.</li>
<li>Verificare che il gioco richiede all'utente quando viene apportata una modifica alla risoluzione.</li>
<li>Se l'utente non accetta entro 15 secondi, verificare che lo schermo torni all'impostazione precedente.</li>
<li>Verificare che il gioco non aggiunge barre nere a sinistra e a destra dell'area di gioco. In questo caso, l'area del gioco sarà ancora in un rapporto 4:3 al centro dello schermo.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1.6 Windows Media Center

Questo requisito è stato ritirato.

### <a name="17-direct3d-conditional-requirement"></a>1.7 Requisito condizionale \[ Direct3D\]



| Sistema operativo                                                                    | Requisito                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere l'impostazione predefinita per qualsiasi opzione di configurazione dello schermo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd> Avviare il gioco. Nelle opzioni video verificare se sono disponibili opzioni di rendering, D3D e/o OpenGL. In caso contrario, verificare che per impostazione predefinita le opzioni di rendering del gioco siano Direct3D. Se non è possibile verificare che D3D9 sia la versione di DirectX in uso, passare a Test automatizzato. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Usare lo strumento: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1.8 Abilitare il supporto per valori DPI elevati



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando è abilitato il ridimensionamento DPI.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd>
<ol>
<li>Impostare il sistema su DPI 150%: <br/> Windows Vista: Pannello di controllo: Personalizzazione, Regola dimensioni carattere (DPI), DPI personalizzato. Impostare su 150%.<br/> Windows 7: Pannello di controllo: Display, Set to Larger - 150%.<br/></li>
<li>Eseguire il processo di installazione e il gioco per verificare che non siano presenti problemi con schermate ritagliate o finestre di dialogo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Verificare che <dpiAware>l'elemento true</dpiAware> sia contenuto nel manifesto incorporato.<br/> Usare lo strumento: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. Sicurezza e compatibilità

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Seguire le linee guida per il controllo dell'account utente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Ogni file eseguibile (.EXE) incluso in un'applicazione deve avere un manifesto incorporato che ne definisce il livello di esecuzione:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Per i giochi e i programmi di installazione dei giochi, uiAccess deve sempre essere impostato su &quot; &quot; false.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Verificare che i file eseguibili del gioco contengano manifesti.</li>
<li>Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia &quot; AsInvoker &quot; .</li>
</ol>
Usare lo strumento: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2.2 Supporto delle versioni x64 di Windows



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
<li>I programmi di installazione di titoli e titoli non devono contenere codice a 16 bit o basarsi su componenti a 16 bit.</li>
<li>Se il gioco dipende dai driver in modalità kernel per il funzionamento, le versioni x64 di questi driver devono essere disponibili. La configurazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni a 64 bit di Windows.</li>
</ul>
<blockquote>
[!Note]<br />
Il supporto per l'edizione a 64 bit di Windows XP Professional facoltativo.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Eseguire il gioco in edizioni a 64 bit di Windows. Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista o Windows 7.</li>
<li>Verificare che il gioco non verifichi un errore in seguito a eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista o Windows 7. L'errore menziona l'applicazione a 16 bit nella finestra di errore.</li>
<li>Se il gioco ha un eseguibile nativo a 64 bit, usare anche questo.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2.3 Firmare i file



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Tutti i file di codice eseguibile (ad esempio, .exe e .dll) devono essere firmati con un certificato Authenticode. <br/> Se si usa il Windows, i file del pacchetto del programma di installazione (.msi file) devono essere firmati. <br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Passare alla directory del gioco.</li>
<li>Individuare tutti i .exe e .dll file.</li>
<li>Fare clic con il pulsante destro del mouse su Proprietà in ogni file.</li>
<li>Verificare che i file eseguibili del gioco contengano una firma digitale.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2.4 Driver di firma



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente. <br/> Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve avere una firma Microsoft ottenuta tramite il programma Windows Hardware Quality Labs (WHQL) o Driver Reliability Signature (DRS). <br/></td>
</tr>
<tr class="even">

<td>Test manuale<br/>
<ol>
<li>Installare il gioco.</li>
<li>Verificare che nel processo di installazione del gioco non siano visualizzate finestre di dialogo del driver non firmate.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2.5 Eseguire correttamente il controllo della versione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi non devono essere eseguiti nei sistemi operativi futuri, come indicato dalle modifiche nel numero di versione Windows, a meno che il Contratto di licenza con l'utente finale non proibisca l'uso nei sistemi operativi futuri. Se si suppone che il gioco non riesca, deve farlo normalmente visualizzando un messaggio all'utente.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuale</dt> <dd>
<ol>
<li>Installare il gioco in Windows XP, nelle edizioni a 32 bit di Windows Vista e Windows 7 e nelle edizioni a 64 bit di Windows Vista e Windows 7.</li>
<li>Verificare che il processo di installazione del gioco non verifichi un errore relativo alla versione del sistema operativo.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Test automatizzato</dt> <dd> Usare lo strumento: Application Verifier<br/>
<ol>
<li>Avviare Application Verifier.</li>
<li>Abilitare il test Compatibility:HighVersionLie dopo aver selezionato il INSTALL.EXE.</li>
<li>Installare il gioco e assicurarsi che non blocchi l'installazione in base alla versione del sistema operativo.</li>
<li>Abilitare il test Compatibility:HighVersionLie dopo aver selezionato il GAME.EXE.</li>
<li>Eseguire il gioco e assicurarsi che non blocchi l'esecuzione in base alla versione del sistema operativo.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2.6 Supporto di sessioni utente simultanee



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi devono supportare scenari Windows multitasking standard.</td>
</tr>
<tr class="even">

<td>Creare un account utente standard in Windows Vista o Windows 7 denominato Toby. Avviare -> Pannello di controllo -> Aggiungi o rimuovi account utente -> Crea nuovo account <br/>
<ol>
<li>Avviare il gioco come User Jane.</li>
<li>ALT+TAB torna al desktop.</li>
<li>Verificare che il gioco venga eseguito correttamente con ALT+TAB Windows desktop.</li>
<li>Fare clic su Start -> [freccia a destra di Blocca] -> Cambia utente.</li>
<li>Accedere come User Toby.</li>
<li>Verificare che il gioco si avvii come User Toby mentre è ancora in esecuzione come User Jane.</li>
<li>Verificare che il gioco non presenti errori per User Toby o User Jane durante il processo user switch.</li>
<li>Se è possibile avviare un'altra sessione di gioco, verificare che non sia possibile ascoltare l'audio dalla sessione di gioco originale.</li>
<li>Chiudere il gioco e tornare all'utente e al gioco originali.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2.7 Supporto dei nomi lunghi



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Se un gioco supporta il salvataggio di file, deve essere in grado di salvare i file con nomi e percorsi lunghi. Il gioco deve gestire correttamente i file system speciali, ad esempio \ / : * ? &quot; < o > in tutti i campi di input utente usati per creare percorsi o nomi di file.</td>
</tr>
<tr class="even">

<td><ol>
<li>Avviare il gioco.</li>
<li>Avviare un nuovo gioco.</li>
<li>Salvare il gioco. Durante il processo di salvataggio, verificare che il gioco sia salvato usando il nome di salvataggio My First Save Game.</li>
<li>Tornare al menu principale.</li>
<li>Provare a caricare il gioco appena salvato.</li>
<li>Verificare che nel gioco non si verifichino errori durante la gestione di caratteri file system non supportati, ad esempio \ / : * ? &quot; < o > se il gioco lo consente, assegnare un nome al gioco salvato.</li>
<li>Se l'utente è autorizzato a assegnare un nome al proprio profilo e/o al carattere o salvare giochi, verificare che il gioco non presenti errori anche quando si usano nomi di file lunghi.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. Installazione

### <a name="31-easy-install"></a>3.1 Installazione semplice



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi con un'installazione tradizionale devono fornire un percorso semplificato nell'interfaccia utente di installazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Inserire il disco del gioco.</li>
<li>Verificare che il gioco non visualizza più di un contratto End-User licenza.</li>
<li>Se il gioco supporta un'opzione di installazione personalizzata o avanzata, verificare che questa opzione sia accessibile durante il processo di installazione.</li>
<li>Verificare che l'opzione installazione predefinita ignora tutte le selezioni di input dell'utente per il processo di installazione (selezione della cartella di installazione, selezione dei componenti e così via).</li>
<li>Verificare che il processo di installazione del gioco non richiede l'installazione del componente del sistema operativo (installazione di DirectX, runtime di Visual C e così via).</li>
<li>Verificare che il processo di installazione del gioco non richiede l'interazione con il firewall.</li>
<li>Verificare che il gioco venga eseguito automaticamente o che al termine del processo di installazione sia presente un menu di avvio.</li>
<li>Verificare che il processo di disinstallazione del gioco rimova tutti i file dei componenti del sistema operativo installati e non ridistribuiti e cancella tutte le impostazioni. Non è necessario pulire tutte le impostazioni e i dati per utente, ad esempio i giochi salvati.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3.2 Supporto del controllo dell'account utente per l'installazione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente. I giochi devono quindi eseguire attività per utente alla prima esecuzione separatamente dall'installazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Verificare che sia possibile installare il gioco come User Jane. Questa operazione richiede diritti elevati durante il processo di installazione/installazione.</li>
<li>Verificare che il processo di installazione del gioco richiede all'utente Jane di elevare i privilegi tramite credenziali di amministratore. Quando l'utente tenta di eseguire l'installazione, verrà visualizzata la richiesta di elevazione dei privilegi.</li>
<li>Scegliere di eseguire automaticamente il gioco al termine dell'installazione, se non lo fa già, oppure avviarlo dal menu visualizzato.</li>
<li>Una volta nel gioco, crea un nuovo profilo, riproduci e salva un gioco.</li>
<li>Uscire dal gioco.</li>
<li>Riavviare il gioco e verificare che i profili utente e i giochi salvati siano accessibili dall'account User Jane.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3.3 Eseguire l'installazione nelle cartelle corrette



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi devono essere installati nella cartella Programmi per impostazione predefinita. I dati utente devono essere scritti alla prima esecuzione e non durante l'installazione.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installare il gioco usando il tipo di installazione Predefinito.</li>
<li>Verificare che il gioco sia stato installato in Programmi.</li>
</ol>
<blockquote>
[!Note]<br />
Se il test ha esito negativo, verificare che il gioco sia destinato all'installazione per Tutti gli utenti. In caso contrario, si tratta di un errore.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3.4 Installare Windows risorse in modo corretto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Le applicazioni non devono tentare di installare file o chiavi del Registro di sistema protette da Windows Resource Protection (WRP).</td>
</tr>
<tr class="even">

<td><ul>
<li>Verificare che non vengano Windows finestra di dialogo WRP di Protezione risorse durante il processo di installazione.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3.5 Evitare i riavvii durante l'installazione



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
Se un aggiornamento del sistema Microsoft REDIST richiede un riavvio, eseguire le operazioni seguenti: Completare l'installazione del gioco, disinstallare il gioco e reinstallare il gioco una seconda volta. Il processo di installazione del gioco non deve richiedere un riavvio in questa seconda installazione.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3.6 Usare correttamente il controllo delle versioni dei file



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il programma di installazione del gioco deve verificare correttamente che siano installate le versioni più recenti dei file. L'installazione di un gioco non deve mai regredire per i file non prodotti o condivisi da applicazioni che non vengono prodotti.</td>
</tr>
<tr class="even">

<td><ol>
<li>Prima di installare il gioco, creare uno snapshot di preinstallazione di System32.<br/>
<ol>
<li>Creare una directory denominata G4Wtest.</li>
<li>Visualizzare una finestra di comando (Avvia -> Esegui -> cmd).</li>
<li>Passare a c:\windows\system32.</li>
<li>Digitare dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</li>
</ol></li>
<li>Creare uno snapshot post-installazione di System32. <br/>
<ol>
<li>Visualizzare una finestra di comando (Avvia -> Esegui -> cmd).</li>
<li>Passare a c:\windows\system32.</li>
<li>Digitare dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</li>
<li>Verificare che il gioco non regredi le versioni dei file che il gioco non ha prodotto (... dei file elencati nei due documenti confrontando pregame.txt con postgame.txt).</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Supporto dei requisiti condizionali di esecuzione \[ automatica\]



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
I programmi di esecuzione automatica scritti per l'uso in versioni di Windows precedenti a Windows Vista non devono usare il runtime .NET, perché questa tecnologia non è inclusa in Windows XP o versioni precedenti di Windows.
</blockquote>
<br/> Per altre indicazioni, fare riferimento a <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun (Requisiti tecnici 3.7, Esecuzione automatica del supporto). <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Inserire il disco del gioco o i file multimediali.</li>
<li>Verificare che la finestra di dialogo Installa/Esegui venga visualizzata automaticamente.</li>
<li>Windows Vista o Windows 7: verificare che il programma di esecuzione automatica del gioco stesso non chiede all'utente Jane di elevare i privilegi tramite credenziali di amministratore.</li>
<li>Verificare che il file eseguibile di esecuzione automatica non necessiti di componenti REDIST, ad esempio .NET 3.5, librerie Run-Time C e così via.</li>
<li>Verificare che se si inserisce nuovamente il disco nell'unità dopo l'installazione, l'installazione non verrà avviata di nuovo automaticamente.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. Affidabilità

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Eliminare i riavvii non necessari



| Sistema operativo                                              | Requisito                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Tutti i programmi di installazione delle applicazioni devono sfruttare le API di Gestione riavvio per evitare riavvii del sistema (vedere [il requisito 3.5).](#35-avoid-reboots-during-installation) |



 

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Eliminare Application Verifier errori



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Il gioco non deve generare errori in esecuzione in Microsoft Application Verifier (AppVerifier), versione 4.0 o successiva, nei test seguenti: <br/>
<ul>
<li>Nozioni di base: handle, heap, blocchi, memoria, TLS</li>
<li>Varie: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Usare lo strumento: AppVerifier 4.0 (o versione successiva)<br/>
<ol>
<li>Installare AppVerifier.</li>
<li>Avviare AppVerifier e selezionare File -> Aggiungi applicazione.</li>
<li>Individuare il file eseguibile del gioco, selezionarlo e fare clic sul &quot; pulsante &quot; Apri.</li>
<li>Nella sezione &quot; Applicazioni selezionare il file &quot; eseguibile del gioco.</li>
<li>Nella sezione Test selezionare i test elencati in precedenza nelle categorie Informazioni di base e Varie (deselezionare ThreadPool e &quot; &quot; &quot; &quot; &quot; &quot; TimeRollOver) e assicurarsi che tutti gli altri test non siano selezionati.</li>
<li>Avviare il gioco.</li>
<li>Verificare che il gioco non generi errori quando viene eseguito in Application Verifier.</li>
</ol>
<blockquote>
[!Note]<br />
Alcuni test richiedono l'esecuzione completa di un debugger. Potrebbe essere necessaria una versione non protetta del file eseguibile del gioco, perché la tecnologia anti-cheat/anti-piracy può interferire con AppVerifer.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4.3 Supporto Segnalazione errori Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>I giochi devono gestire solo le eccezioni note e previste e Segnalazione errori Windows non devono essere disabilitate. Se un errore (ad esempio una violazione di accesso) viene inserito in un gioco, deve consentire Segnalazione errori Windows segnalare l'arresto anomalo.</td>
</tr>
<tr class="even">

<td>Usare lo strumento: Hijacker thread <br/>
<ul>
<li>Se l'applicazione si arresta in modo anomalo durante il test, verificare che il gioco Segnalazione errori Windows correttamente e raccoglie i dati di arresto anomalo.</li>
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
<td>Tutti i file eseguibili( ad esempio, .exe o .dll) devono contenere un nome di prodotto, un nome società e una versione del file accurati.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Test manuale:</dt> <dd>
<ol>
<li>Fare clic con il pulsante destro del mouse sui file eseguibili del gioco sia nel supporto di installazione che in quelli installati nel disco rigido del computer.</li>
<li>Selezionare Proprietà.</li>
<li>Windows XP: fare clic <strong>sulla scheda</strong> Versione. Verificare che i campi Product Name (Nome prodotto), Company Name (Nome società) e File Version (Versione file) siano popolati correttamente.</li>
<li>Windows Vista o Windows 7: fare clic sulla <strong>scheda</strong> Dettagli. Verificare che i campi Nome prodotto e Versione file siano popolati correttamente. Nome società non è visibile nella pagina Windows Vista o Windows 7.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Test automatizzato:</dt> <dd>
<ul>
<li>Usare Microsoft Games for Windows Test Tool; vedere <a href="#64-microsoft-games-for-windows-test-tool">la sezione 6.4</a>.</li>
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
<td>La normale uscita del gioco non deve generare un errore di eccezione sconosciuto.</td>
</tr>
<tr class="even">

<td><ul>
<li>Dopo aver riprodotto il gioco per una normale sessione di gioco, verificare che il gioco non generi errori all'uscita.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. Script di test di esempio

Questo è un esempio di un test superato tipico usando i requisiti di test precedenti come guida.

### <a name="51-tools"></a>5.1 Strumenti

-   Edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD
-   Edizione a 32 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel
-   Edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU AMD
-   Edizione a 64 bit di Windows Vista SP1 e/o Windows 7 in una CPU Intel
-   Edizione a 32 bit Windows XP SP2 in una CPU AMD
-   Edizione a 32 bit Windows XP SP2 in una CPU Intel
-   Monitor wide screen che supporta 1680 1050
-   controller Xbox 360 per Windows

### <a name="52-pre-install"></a>5.2 Preinstallazione

1.  Windows Vista e Windows 7: Creare due utenti standard: Jane e Toby
2.  Windows Vista e Windows 7: Verificare che controllo dell'account utente sia abilitato
3.  Creare uno snapshot di preinstallazione di System32

    1.  Creare una directory denominata G4Wtest
    2.  Visualizzare una finestra di comando (Start -> Esegui -> cmd)
    3.  Passare a c: \\ windows \\ system32
    4.  Digitare dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista e Windows 7: impostare su 150% DPI \[ 1,8\]
5.  Procedere con [l'installazione](#3-installation)

### <a name="53-install"></a>5.3 Installare

1.  Accedere come Utente Jane
2.  Inserire il disco del gioco nell'unità CD/DVD, verificare che la finestra di dialogo di installazione/esecuzione venga visualizzata automaticamente \[ 3.7\]
3.  Verificare che il processo di installazione del gioco richiede all'utente Jane di elevare le credenziali di amministratore \[ 3.2\]
4.  Verificare che il programma di esecuzione automatica del gioco stesso non chiede all'utente Jane di elevare i privilegi tramite credenziali di amministratore \[ 3.7\]
5.  Verificare che il gioco non visualizza più di un contratto End-User licenza \[ 3.1\]
6.  Verificare che nel gioco siano visualizzate le opzioni di installazione predefinita/semplice e personalizzata/avanzata \[ 3.1\]
7.  Verificare che l'opzione di installazione Predefinita/Semplice ignora tutte le selezioni di input dell'utente per il processo di installazione (selezione della cartella di installazione, selezione dei componenti e così via). \[ 3.1\]
8.  Verificare che il processo di installazione del gioco non richiede la configurazione dei componenti del sistema operativo (installazione di DirectX, librerie Run-Time C e così via). \[ 3.1\]
9.  Verificare che il processo di installazione del gioco non richiede l'interazione con il firewall \[ 3.1\]
10. Verificare che il processo di installazione del gioco non verifichi un errore relativo alla versione del sistema operativo \[ 2.5 \] \[ 4.2\]
11. Verificare che nel processo di installazione del gioco non siano visualizzate finestre di dialogo del driver \[ non firmate 2.4\]
12. Verificare che non vengano Windows finestre di dialogo WRP (Resource Protection) durante il processo di installazione \[ 3.4\]
13. Verificare che il nuovo inserimento del disco nell'unità dopo l'installazione non causa il nuovo avvio automatico dell'installazione
14. Verificare che il gioco non richieda il riavvio del sistema dopo \[ l'installazione 3.5\]
15. Verificare che sia possibile installare il gioco come User Jane \[ 3.2\]
16. Verificare che il gioco venga eseguito automaticamente o che sia presente un menu di avvio alla fine del processo di installazione \[ 3.1\]
17. Se il gioco viene eseguito automaticamente dopo l'installazione, passare a [Runtime](#55-runtime)
18. Se il gioco ha lasciato un menu di avvio o non è stato possibile disinstallare, vedere la sezione [Post-installazione](#54-post-install)

### <a name="54-post-install"></a>5.4 Post-installazione

1.  Verificare che il gioco non posiziona i collegamenti di avvio sul desktop \[ dell'utente 1.1\]
2.  Verificare che il gioco non posiziona i collegamenti di avvio nel menu Start \[ 1.1\]
3.  Verificare che l'icona del gioco sia visualizzata Windows Games Explorer \[ 1.1\]
4.  Verificare che i metadati (editore, sviluppatore, genere, data di rilascio, versione) nella parte inferiore visualizzino la \[ versione 1.1 corretta\]
5.  Verificare che l'icona del gioco visualizzi Windows informazioni sull'indice dell'esperienza (WEI) Windows Games Explorer \[ 1.1\]
6.  Verificare che i collegamenti ipertestuali del gioco per i metadati funzionino correttamente in Windows Games Explorer \[ 1.1\]
7.  Verificare che il gioco visualizzi una valutazione accurata del controllo genitori Windows Games Explorer \[ 1.1\]
8.  Creare uno snapshot post-installazione di System32

    1.  Visualizzare una finestra di comando (Start -> Run -> cmd)
    2.  Passare a c: \\ windows \\ system32
    3.  Digitare dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Verificare che il gioco non regredisca con le versioni dei file elencati nei due documenti confrontando pregame.txt con postgame.txt \[ 3.6\]

9.  Passare al [runtime](#55-runtime)

### <a name="55-runtime"></a>5.5 Runtime

1.  RUNTIME 1: se il menu di avvio è presente, avviare il gioco da qui. Se il gioco è stato eseguito automaticamente o è stato avviato dal menu dell'utilità di avvio del gioco dopo l'installazione, seguire questa procedura. In caso contrario, passare a RUNTIME 2:

    1.  Creare un profilo (se il gioco lo consente)
    2.  Avviare un nuovo gioco
    3.  Salvare il gioco
    4.  Uscire dal gioco
    5.  Avviare il gioco da Games Explorer
    6.  Verificare che il gioco sia avviato dall'icona Games Explorer \[ 1.2\]
    7.  Verificare che il gioco non richiede credenziali di amministratore \[ all'avvio 1.2\]
    8.  Verificare che Profili utente e Salva giochi siano accessibili dall'account User Jane \[ 3.2\]
    9.  Passare a RUNTIME 3

2.  RUNTIME 2: se il gioco non è stato eseguito automaticamente o non è stato visualizzato un avvio dal menu dell'utilità di avvio del gioco, si tratta di un errore \[ 3.1. Tuttavia, i test possono \] continuare normalmente:

    1.  Avviare il gioco da Games Explorer
    2.  Verificare che il gioco sia avviato dall'icona Games Explorer \[ 1.2\]
    3.  Verificare che il gioco non richiede credenziali di amministratore \[ all'avvio 1.2\]
    4.  Passare a RUNTIME 3

3.  RUNTIME 3: se il gioco supporta un game pad, verificare che il gioco riconosca controller Xbox 360 per Windows come dispositivo di input \[ 1.4\]

    1.  Se necessario, abilitare il controller tramite il menu delle opzioni
    2.  Verificare che il gioco faccia riferimento ai pulsanti e ai trigger del controller usando Xbox 360 nomi
    3.  Verificare che il gioco e il sistema di menu siano controllabili con il controller Xbox 360 per Windows
    4.  Verificare che il controller Xbox 360 per Windows si comporti in base agli standard accettati

4.  Impostare il video su \[ 1.5: \]

    1.  Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 4:3 (800 600 o 1024 768)
    2.  Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:9 (1280 720)
    3.  Verificare che il gioco venga eseguito con una risoluzione delle proporzioni 16:10 (1680 1050, 800 480 o 1152 720)
    4.  Verificare che il gioco richiede all'utente quando viene apportata una modifica alla risoluzione
    5.  Verificare che la visualizzazione ripristina l'impostazione precedente se non si accetta entro 15 secondi
    6.  Verificare che il gioco non estensa l'immagine e a sua volta presenti un'area di visualizzazione più ampia
    7.  Verificare che il gioco non aggiunge barre nere a sinistra e a destra dell'area di gioco

5.  Se disponibile nelle impostazioni video, verificare che per impostazione predefinita le opzioni di rendering del gioco siano Direct3D \[ 1.7. In caso \] contrario, passare [a Test automatizzati](#58-automated-tests)
6.  Se richiesto o se l'opzione è disponibile, creare un profilo utente. Verificare che nel gioco non si verifichino errori quando si usano nomi di file lunghi \[ 2.7\]
7.  Avviare un nuovo gioco, creare un salvataggio del gioco e verificare che non si verifichino errori durante la gestione di caratteri file system non supportati \[ 2.7\]
8.  Verificare che il gioco sia correttamente ALT+TAB Windows desktop \[ 2.6\]

    1.  Cambiare utente con il gioco in esecuzione facendo clic su Start -> Cambia utente
    2.  Accedere come Toby
    3.  Verificare che il gioco sia avviato come User Toby mentre è ancora in esecuzione come User Jane \[ 2.6\]
    4.  Verificare che nel gioco non si verifichino errori per User Toby o User Jane durante il processo user switch \[ 2.6\]
    5.  Verificare che non sia possibile ascoltare l'audio dalla sessione di gioco \[ originale 2.6\]
    6.  Uscire dal gioco
    7.  Disconnettersi da Toby
    8.  Tornare all'utente originale in cui è in esecuzione il gioco
    9.  ALT+TAB torna al gioco

9.  Uscire dal gioco
10. Passare al [post-runtime](#56-post-runtime)

### <a name="56-post-runtime"></a>5.6 Post-Runtime

1.  Verificare che il gioco non generi errori all'uscita \[ 4.3\]
2.  Verificare che il gioco sia installato in Programmi \[ 3.3\]
3.  Passare a [Controllo genitori](/windows)

### <a name="57-parental-controls"></a>5.7 Controllo genitori

1.  Aprire Controllo genitori in Pannello di controllo
2.  Verificare che il gioco visualizzi una valutazione accurata di Controllo genitori sotto il titolo del gioco in Controllo genitori Pannello di controllo \[ 1.2\]
3.  Per i test seguenti, vedere Test case \[ 1.2: \]

    1.  Dopo aver impostato Controllo genitori su "On", verificare che il gioco venga eseguito con queste impostazioni come User Jane \[ 1.2\]
    2.  Disconnettersi e accedere come Toby
    3.  Verificare che il gioco venga eseguito con queste impostazioni come User Toby \[ 1.2\]
    4.  Disconnettersi e accedere come Jane
    5.  Nella sezione Controllo genitori impedire a User Toby di visualizzare i giochi di un livello ESRB sempre superiore rispetto al gioco appena installato

        Esempio: se il gioco è valutato E, impostarlo in modo che Toby possa solo riprodurre giochi classificati in C

    6.  Verificare che il gioco venga eseguito con queste impostazioni come User Jane \[ 1.2\]
    7.  Disconnettersi e accedere come utente Toby
    8.  Verificare che il gioco non si avvii in User Toby quando ESRB è bloccato dall'utente Jane \[ 1.2\]
    9.  Disconnettersi come utente Toby e accedere di nuovo come utente Jane
    10. Se modificato in precedenza, ripristinare le impostazioni ESRB
    11. Se non sono presenti impostazioni ESRB, selezionare "Blocca o Consenti giochi specifici" e selezionare il gioco in base al nome
    12. Disconnettersi come Jane e accedere come Toby
    13. Verificare che il gioco non si avvii in User Toby quando EXE/Name è bloccato dall'utente Jane \[ 1.2\]
    14. Disconnettersi come Toby e accedere di nuovo come Jane
    15. Come Jane, aprire Controlli utente -> restrizioni dell'applicazione
    16. Fare clic su "Toby can only use the programs I allow" (Toby può usare solo i programmi consentiti) e quindi fare clic su OK (ad esempio, non consentire exe)
    17. Fare clic sulla casella Deseleziona tutto e quindi fare clic su OK
    18. Passare a Controlli utente \| Games Controls e consentire il gioco specifico usando la classificazione ESRB
    19. Disconnettersi come Jane e accedere come Toby e provare a eseguire il gioco
    20. Verificare che il gioco NON sia bloccato e che Toby possa riprodurlo quando "allow no exes" è impostato \[ su 1.2\]
    21. Disconnettersi come utente Toby e accedere di nuovo come utente Jane
    22. Passare a Controllo genitori in Pannello di controllo e rimuovere le restrizioni
    23. Verificare che entrambi gli utenti possano ora riprodurre il gioco

4.  Passare a [Test automatizzati](#58-automated-tests)

### <a name="58-automated-tests"></a>5.8 Test automatizzati

1.  Verificare che il gioco non generi errori quando viene eseguito in Application Verifier- Vedere la documentazione dello strumento di test di personalizzazione \[ 4.2\]
2.  Verificare che i file eseguibili del gioco contengano manifesti. Vedere la documentazione dello strumento di test della personalizzazione \[ 2.1\]
3.  Verificare che il manifesto del file eseguibile del gioco requestedExecutionLevel sia "AsInvoker". Vedere la documentazione dello strumento di test di personalizzazione \[ 2.1\]
4.  Passare ad [Altri test](#59-other-tests)

### <a name="59-other-tests"></a>5.9 Altri test

1.  Verificare che i file eseguibili del gioco contengano una firma \[ digitale 2.3\]
2.  Verificare che il processo di installazione del gioco venga eseguito normalmente nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2.3\]
3.  Verificare che il gioco non verifichi un errore in seguito a file eseguibili a 16 bit nelle edizioni a 64 bit di Windows Vista e/o Windows 7 \[ 2.3\]
4.  Forzare l'arresto anomalo dell'applicazione durante i test e verificare che il gioco Segnalazione errori Windows correttamente e raccoglie i dati di arresto \[ anomalo 4.3\]
5.  Assicurarsi che i riepiloghi dei file \[ 4.3 siano adeguati\]

    1.  Fare clic su Start -> Computer
    2.  Passare alla directory del gioco
    3.  Nella finestra di ricerca digitare \*.dll
    4.  Per ogni file: fare clic con il pulsante destro del mouse sul file e scegliere Proprietà

        -   In Windows XP: fare clic sulla scheda Versione. Verificare che i campi Product Name (Nome prodotto), Company Name (Nome società) e File Version (Versione file) siano popolati correttamente. \[4.3\]
        -   In Windows Vista e Windows 7: fare clic sulla scheda Dettagli. Verificare che i campi Nome prodotto e Versione file siano popolati correttamente. Nome società non è visibile nella pagina Windows Vista o Windows 7 \[ 4.3\]

    5.  Ripetere questo controllo per .exe file

6.  Avviare il gioco.

    1.  Premere CTRL+ALT+CANC
    2.  Fare clic sulla freccia "Opzioni di arresto"
    3.  Fare clic su Riavvia
    4.  Verificare che il gioco non blocchi \[ l'arresto 3.1\]

7.  Procedere alla [disinstallazione](#510-uninstall)

### <a name="510-uninstall"></a>5.10 Disinstallazione

-   Verificare che il processo di disinstallazione del gioco rimova tutti i file dei componenti del sistema operativo installati e non ridistribuiti e cancella tutte le impostazioni \[ 3.1\]

    -   Verificare in Windows Vista o Windows 7 che Pannello di controllo sia l'unico modo per rimuovere il programma \[ 1.1\]

## <a name="test-tool-notes"></a>Note dello strumento di test

Queste sono note per ognuno degli strumenti di test elencati nei requisiti di test precedenti.

### <a name="61-appverifier-40-or-higher"></a>6.1 Appverifier 4.0 (o versione successiva)

**Test case: 2.5, 4.2**

> [!Note]  
> Alcune applicazioni non vengono eseguite con AppVerifier in esecuzione a causa della protezione della copia. Questo problema può essere risolto eseguendo con una versione di rilascio non protetta del file eseguibile del gioco.

 

1.  Installare AppVerifier 4.0 (o versione successiva) in un computer che esegue Windows XP
2.  Avviare AppVerifier e fare clic su File -> Aggiungi applicazione
3.  Individuare il file eseguibile del gioco, selezionarlo e fare clic su Apri
4.  Nella sezione "Applicazioni" selezionare il file eseguibile del gioco
5.  Selezionare i test seguenti nella sezione "Nozioni di base":

    -   Selettori
    -   Heap
    -   Locks
    -   Memoria
    -   TLS

6.  Selezionare i test seguenti nella sezione "Varie":

    -   DangerousAPIs
    -   DirtyStacks

7.  Assicurarsi che tutti gli altri test non siano selezionati
8.  Avviare il gioco
9.  Riprodurre il gioco
10. Chiudere il gioco
11. In AppVerifier selezionare Visualizza -> log
12. Nella sezione "Applicazioni" selezionare il file di .exe app
13. Nella sezione "Log" selezionare il file di log e osservare il numero di errori. Se non sono presenti errori, terminare i test di AppVerifier. Se sono presenti errori, fare clic sul pulsante Visualizza
14. Cercare Gravità="Errore nel documento (CTRL+F)
15. Creare bug in base alla parte LayerName= dell'errore

### <a name="62-manifest-test---mtexe"></a>6.2 Test manifesto - mt.exe

**Test case: 1.8, 2.1**

Questo strumento viene eseguito da un prompt dei comandi in MT.exe si trova.

Esempio:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Fare clic su Start -> Run -> digitare cmd e fare clic sul pulsante OK
2.  Eseguire lo mt.exe per generare un file manifesto per ogni file .exe che viene installato con il gioco
3.  Aprire il file manifesto generato
4.  Assicurarsi che ogni .exe file contenga quanto segue (richiesto:

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

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6.3 Thread Hijacker - threadhijacker.exe

Questo strumento viene eseguito da un prompt dei comandi in threadhijacker.exe si trova.

Esempio:

``` syntax
threadhijacker.exe /process:str
```

Dove str è il nome \_ di \_program.exe

1.  Visualizzare Gestione attività, fare clic sulla scheda Processi e individuare il nome del file eseguibile del gioco.
2.  Aprire un prompt dei comandi in modalità amministratore
3.  Passare alla directory in cui si trova threadhijacker.exe
4.  Tipo: **threadhijacker.exe /process:** str, dove str è il nome del file eseguibile che si vuole selezionare

### <a name="64-microsoft-games-for-windows-test-tool"></a>6.4 Microsoft Games for Windows Test Tool

Questo strumento si trova in DirectX SDK. Dopo aver installato l'SDK in un computer, il programma di installazione dello strumento di test games per Windows può essere inserito nel computer di test e installato.

Individuare il programma di installazione di Microsoft Games for Windows Test Tool nel computer di sviluppo in cui è installato DirectX SDK. Per impostazione predefinita, viene inserito nel percorso seguente:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Copiare il programma di MicrosoftGFWTestTool.msi /setup.exe) nel computer di test.
2.  Eseguire il programma di installazione.
3.  Avviare Microsoft Games for Windows Test Tool.
4.  Nel campo **Project elenco sostituire** Create New **Project** con il nome del titolo e fare clic su Create New ( **Crea nuovo).**

    Attendere il completamento della baseline.

5.  Immettere le informazioni disponibili nella sezione **Game Information (Informazioni** sul gioco) e fare clic **su Update Game Information (Aggiorna informazioni sul gioco).**
6.  Fare clic **sulla scheda Test** case.
7.  A partire dall'alto, procedere con i test case, facendo clic su **Supera** o **Non superato in** base alle esigenze.

    Per informazioni dettagliate sull'inclusione di un bug nel report, vedere "Scrittura di un bug" più avanti in questa sezione.

8.  Tornare alla scheda **Progetti** dopo aver esaminato il report (selezionando le **schede Report** e **Modifica bug).**
9.  Fare clic **su Compila report**.

    Al termine della compilazione del report verrà aperta una finestra. Qui è possibile trovare un nome .ZIP nome file *ProjectName* \_report.zip. Questo file contiene tutti i log e i risultati raccolti durante il test superato.

### <a name="writing-a-bug"></a>Scrittura di un bug

Esistono due modi per scrivere un report sui bug:  è possibile scorrere i test case e fare clic su Non riuscito quando il titolo ha esito negativo in un test case oppure è possibile fare clic sulla scheda **Modifica** bug e aggiungere manualmente un report sui bug.

### <a name="clicking-fail-on-a-test-case"></a>Fare clic su Non riuscito in un test case

1.  Quando si fa **clic su** Non  riuscito in test case, l'elenco a discesa Tipo di problema verrà impostato automaticamente sul tipo test case problema.
2.  Aggiungere una breve descrizione al **campo Titolo** che descrive brevemente il problema.
3.  Aggiungere una descrizione dettagliata del problema al **campo Comportamento** osservato.
4.  In base alle esigenze, aggiungere ciò che era previsto (anziché una descrizione del problema) al **campo Comportamento** previsto.
5.  Aggiungere una descrizione dettagliata di come riprodurre il problema nel **campo Passaggi di** riproduzione.
6.  Al termine, fare clic sul **pulsante** Salva.

### <a name="manually-adding-a-bug"></a>Aggiunta manuale di un bug

Questo processo è identico a quello in cui si fa clic su **Non** riuscito , ad eccezione dell'elenco a discesa popolato automaticamente. In questo caso, selezionare il tipo di errore TCR appropriato o selezionare **\* \* Problema non \* \* TR** per i bug che non rientrano nell'intervallo TR ma che devono comunque essere segnalati.

## <a name="resources"></a>Risorse

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Giochi per Windows: requisiti tecnici
</dt> <dd>

[Requisiti tecnici di Games for Windows: Procedure consigliate per i giochi in Windows XP, Windows Vista e Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows Sdk
</dt> <dd>

[Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Linee guida per il controllo dell'account utente
</dt> <dd>

[Windows Requisiti di sviluppo delle applicazioni di Vista per la compatibilità del controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Informazioni sul programma di installazione
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual portale per sviluppatori 
</dt> <dd>

[Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX portale per sviluppatori
</dt> <dd>

[Centro per sviluppatori DirectX](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog di Games for Windows e DirectX SDK
</dt> <dd>

[Giochi per Windows e DirectX SDK](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli di DirectX
</dt> <dd>

[Articoli tecnici su DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

