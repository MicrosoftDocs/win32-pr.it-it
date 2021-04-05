---
title: 'Requisiti tecnici dei giochi di Windows: procedure consigliate per giochi su Windows XP, Windows Vista, Windows 7 e Windows 8'
description: Questo articolo fornisce i requisiti tecnici e le procedure consigliate per i giochi eseguiti in Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e38b9476a4ab2aad5edc6210f55bc4d2b85845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730047"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Giochi per i requisiti tecnici di Windows: procedure consigliate per giochi in Windows XP, Windows Vista, Windows 7 e Windows 8

Questo articolo fornisce i requisiti tecnici e le procedure consigliate per i giochi eseguiti in Windows. I requisiti tecnici e le procedure consigliate sono stati scritti principalmente per comprendere Windows Vista e Windows 7, nonché il sistema operativo Windows XP legacy. Queste procedure consigliate si applicano in genere anche ai giochi Win32 Desktop in Windows 8.

Questo articolo contiene le seguenti sezioni:

-   [Differenze per Windows 8](#differences-for-windows-8)
    -   [Informazioni aggiuntive](#additional-information)
-   [Giochi per Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [Integrazione di Esplora giochi 1,1](#11-games-explorer-integration)
    -   [1,2 supporto per la sicurezza della famiglia/controlli parentali](/windows)
    -   [1,3 supporto di giochi Rich salvati](#13-support-rich-saved-games)
    -   [1,4 supportare il requisito condizionale del controller comune di Xbox 360 per Windows \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 supportano più proporzioni e soluzioni](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1,6 supporto del lancio da Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [1,7 supporto Direct3D](#17-direct3d-support)
    -   [1,8 abilitare la compatibilità con DPI elevata](#18-enable-high-dpi-aware)
-   [Sicurezza e compatibilità](#security-and-compatibility)
    -   [2,1 seguire le linee guida per il controllo dell'account utente](#21-follow-user-account-control-guidelines)
    -   [2,2 supportano le versioni di Windows x64](#22-support-windows-x64-versions)
    -   [2,3 file di firma](#23-sign-files)
    -   [2,4 firmare i driver](#24-sign-drivers)
    -   [2,5 eseguire il controllo della versione corretto](#25-perform-proper-version-checking)
    -   [2,6 supportare sessioni utente simultanee](#26-support-concurrent-user-sessions)
    -   [2,7 supporto di nomi lunghi](#27-support-long-names)
-   [Installazione](#32-support-user-account-control-for-installation)
    -   [3,1 supporto dell'installazione semplificata](#31-support-easy-installation)
    -   [3,2 supporto del controllo dell'account utente per l'installazione](#32-support-user-account-control-for-installation)
    -   [3,3 installare in cartelle corrette](#33-install-to-correct-folders)
    -   [3,4 installare correttamente le risorse di Windows](#34-install-windows-resources-properly)
    -   [3,5 evitare il riavvio durante l'installazione](#35-avoid-reboots-during-installation)
    -   [3,6 usare correttamente il controllo delle versioni dei file](#36-use-file-versioning-correctly)
    -   [3,7 supporto \[ requisito condizionale Autorun\]](#37-support-autorun-conditional-requirement)
-   [Affidabilità](#reliability)
    -   [4,1 eliminare i riavvii non necessari](#41-eliminate-unnecessary-reboots)
    -   [4,2 eliminare Application Verifier errori](#42-eliminate-application-verifier-failures)
    -   [4,3 supporto di Segnalazione errori Windows e informazioni sulla versione del file](#43-support-windows-error-reporting-and-file-version-information)
-   [Terminologia del controller comune di Xbox 360 per Windows](#xbox-360-common-controller-for-windows-terminology)
-   [Linee guida per i prodotti middleware di gioco](#guidelines-for-game-middleware-products)
    -   [Introduzione](#introduction)
    -   [Suggerimenti aggiuntivi](#additional-recommendations)
    -   [Giochi per Windows showcases](#games-for-windows-showcases)
-   [Risorse](#resources)

## <a name="differences-for-windows-8"></a>Differenze per Windows 8

Di seguito è riportato un riepilogo delle principali differenze quando si applicano questi requisiti tecnici e le procedure consigliate a Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**L'interfaccia utente di Esplora giochi non è visibile**
</dt> <dd>

Tutti i giochi registrati con [Esplora giochi](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) vengono esposti come riquadri nella nuova interfaccia utente di Windows, ma la maggior parte dei metadati associati al titolo non è più visibile. Per creare i metadati è comunque possibile usare lo strumento per la creazione di file di definizione dei giochi (GDFMAKER.EXE), che ora è disponibile in Windows Software Development Kit (SDK). È inoltre possibile utilizzare i meccanismi esistenti per la distribuzione dei metadati. Continuare a testare la registrazione di Esplora giochi usando Windows 7 e verificare che il riquadro nuova interfaccia utente Windows venga visualizzato quando viene installato in Windows 8 (vedere l' [integrazione di 1,1 Games Explorer](#11-games-explorer-integration)).

Per scaricare Windows 8 SDK, vedere [download per lo sviluppo di applicazioni desktop](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**La registrazione con le API di Game Explorer continua a essere il meccanismo per registrare il gioco con i controlli padre di Windows**
</dt> <dd>

È consigliabile eseguire la versione Windows SDK di GDFMAKER sulla versione rilasciata di Windows 8 per assicurarsi che possa popolare tutti i sistemi di classificazione attualmente supportati.

> [!Note]  
> Questa versione di GDFMAKER richiede .NET 4,0.

 

Vedere [1,2 supporto per la sicurezza della famiglia/controlli parentali](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Sono ora disponibili tre opzioni per l'uso dell'API XINPUT in base ai requisiti**
</dt> <dd>

XINPUT 1,4 è integrato in Windows 8. Sia le app di Windows Store sia le app desktop Win32 possono usare XINPUT 1,4. Tutte le versioni di Windows possono usare XINPUT 9.1.0 per i controller comuni semplificati, ma non è presente alcun pacchetto di ridistribuzione con XINPUT 9.1.0. Tutte le versioni di Windows possono usare anche la versione esistente di DirectX SDK XINPUT 1,3, che richiede la distribuzione di DirectSetup.

Vedere [1,4 supporto del controller comune di Xbox 360 per Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**In Windows RT è supportato solo un set limitato di app desktop Win32**
</dt> <dd>

I giochi eseguiti in Windows 7 possono essere eseguiti correttamente nelle piattaforme Windows 8 x86 e x64.

Vedere [2,2 supporto delle versioni di Windows x64](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Assicurarsi che tutti i controlli del sistema operativo vengano eseguiti correttamente**
</dt> <dd>

La versione del sistema operativo Windows 8 è 6,2. Windows 8 passa i test della barra minima attualmente consigliati per la distribuzione dei giochi.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Il pacchetto di ridistribuzione DirectX End-User viene eseguito correttamente in Windows 8, come in Windows 7, per distribuire D3DX9, D3DX10, D3DX11, XINPUT 1,3, XAUDIO 2,7, XACTEngine e così via**
</dt> <dd>

Tuttavia, esiste un problema noto con DirectSetup nei sistemi in cui è installato solo .NET 4,0, a causa della gestione della distribuzione degli assembly DirectX 1,1 gestiti legacy. Questo problema si applica sia a Windows 8, che include .NET 4,5 per impostazione predefinita, sia ai computer Windows XP aggiornati in cui è installato il runtime di .NET 4,0. Tuttavia, questo problema non si applica a nessuna versione di .NET precedente a .NET 4,0. Sebbene Windows 8 abbia un comportamento di compatibilità delle applicazioni per risolvere automaticamente questo problema (che richiede l'accesso alla rete), è consigliabile che i giochi che continuano a distribuire l'aggiornamento di DirectSetup alla versione di DirectX SDK (giugno 2010) abbiano aggiornato i file REDIST. Come sempre, se si usa DirectSetup per il titolo, tagliare il titolo fino al set minimo necessario di CAB.

Vedere [3,4 installare correttamente le risorse di Windows](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Giochi che richiedono il runtime compatibile con .NET 2,0 (2,0, 3,0, 3,5) continuano a usare i meccanismi di distribuzione esistenti**
</dt> <dd>

Questi giochi attivano un comportamento di compatibilità delle applicazioni in Windows 8 per abilitare automaticamente il Runtime .NET 3,5 (che richiede l'accesso alla rete). Tuttavia, è consigliabile che gli sviluppatori .NET passino al runtime di .NET 4,0.

> [!Note]  
> Gli assembly DirectX 1,1 gestiti legacy non sono compatibili con il Runtime .NET 4. x.

 

Vedere [3,4 installare correttamente le risorse di Windows](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**L'uso di un Autorunner o di un'altra tecnologia di pre-installazione che si basa su .NET non è consigliato**
</dt> <dd>

Si può presupporre che in Windows Vista e Windows 7 siano presenti solo i Runtime compatibili con .NET 2,0 (2,0, 3,0, 3,5). Per impostazione predefinita, solo il runtime compatibile con .NET 4,0 è presente in Windows 8.

Vedere [3,7 supporto di autorun](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Application Verifier aggiornata per Windows 8**
</dt> <dd>

Windows 8 SDK include questa Application Verifier aggiornata.

Vedere [4,2 eliminare Application Verifier errori](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Informazioni aggiuntive

<dl>

[Cookbook sulla compatibilità con Windows 8 e Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Dov'è DirectX SDK?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Giochi per Windows

**Riepilogo dei requisiti dei giochi**

**Vantaggi dei clienti**

I giochi per computer sono un'esperienza di intrattenimento fondamentale in Windows, ma i problemi di semplicità d'uso hanno provocato frustrazione per i clienti nel corso degli anni. Tradizionalmente, i giochi vengono installati come le applicazioni, ma vengono usati più come i supporti di intrattenimento, ad esempio film o canzoni. Le innovazioni, ad esempio giochi Explorer, espongono giochi in modo coerente, diverse dalle applicazioni standard. Queste innovazioni offrono anche lo stato di un cittadino di prima classe in Windows, insieme a musica e immagini. I requisiti seguenti consentono di garantire che Windows Vista e Windows 7 forniscano un'esperienza di gioco migliorata, più accessibile e unificata. Allo stesso tempo, garantiscono la compatibilità con Windows XP.

### <a name="11-games-explorer-integration"></a>Integrazione di Esplora giochi 1,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco deve essere visibile all'interno di Games Explorer (la cartella **Games** ) in Windows Vista e Windows 7. Quando questa opzione è selezionata, il gioco deve anche visualizzare i metadati corretti, tra cui server di pubblicazione, sviluppatore, data di rilascio, versione, punteggi indice prestazioni Windows, classificazione (se applicabile) e collegamenti ipertestuali associati.

Se il gioco viene distribuito digitalmente tramite un servizio di gioco online, il provider di servizi deve essere visualizzato anche in Games Explorer. Per garantire la corretta gestione del provider e per consentire l'uso di feed RSS, è necessario usare la versione 2 dello schema per i file di definizione dei giochi (GDFs). Per ulteriori informazioni su GDFs, vedere informazioni aggiuntive.

Inoltre, i programmi di installazione dei giochi devono osservare le regole seguenti quando vengono eseguiti in Windows Vista e Windows 7:

-   L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altra posizione.
-   Le attività e i tasti di scelta rapida per la rimozione non devono essere creati.
-   Gli utenti devono essere in grado di rimuovere il gioco utilizzando programmi e funzionalità nel pannello di controllo in Windows Vista e Windows 7 oppure installazione applicazioni nel pannello di controllo in Windows XP.

In Windows XP e nelle versioni precedenti di Windows, il programma di installazione del gioco è libero di creare gruppi di programmi, icone desktop o collegamenti in base alle esigenze.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Windows Games Explorer è un concetto simile a quello delle cartelle di Windows XP **documenti** o **Immagini personali**. L'idea è quella di centralizzare contenuti simili in un'unica posizione e di semplificare l'organizzazione e le attività sensibili al contesto. Esplora giochi estende il concetto di **documenti** o **Immagini** , consentendo un'organizzazione e un controllo più completo sui giochi. Esplora giochi consente ai giocatori di visualizzare, organizzare e interagire con tutti i giochi installati nei propri sistemi. Consente inoltre agli editori di giochi di comunicare più efficacemente informazioni importanti sul gioco. Il sistema è basato sui dati, semplificando l'aggiornamento delle informazioni del gioco da parte di un editore di giochi per tutta la durata del prodotto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per l'integrazione con Game Explorer è necessario creare un file di definizione del gioco (GDF), ovvero un file di testo XML incorporato in un file binario (un file eseguibile o una DLL) come risorsa, insieme a un'icona di Windows. Il gioco deve quindi essere registrato con Game Explorer. Il GDF consente inoltre di esporre le informazioni fornite, ad esempio il titolo del gioco, l'editore, lo sviluppatore, i collegamenti ai siti Web e le attività facoltative. Si noti che le attività di supporto possono essere solo collegamenti a siti Web, ma è possibile usare le attività di riproduzione anche per le attività di supporto facoltative.

Esplora giochi può usare un'immagine bitmap di anteprima, ma è consigliabile specificare invece una risorsa icona Windows con icone grandi (256 256). La risorsa icona deve includere dimensioni di immagine pari a 256 256 48 48, 32 32 e 16 16 nei livelli di colore a 24 bit (true color) e a 8 bit (256). L'editor di icone fornito in Visual Studio 2008 e 2010 supporta questi formati di icone di grandi dimensioni, così come IconWorkshop Lite.

In DirectX SDK sono disponibili informazioni dettagliate sull'integrazione con **Esplora giochi di Windows** . DirectX SDK include un editor di file di definizione del gioco (GDF), nonché un esempio di GDF incluso in GDFExampleBinary, un esempio. Un altro esempio, GameUxInstallHelper, fornisce routine per l'integrazione delle funzionalità necessarie nei sistemi di installazione esistenti. Il validator del file di definizione del gioco (gdftrace.exe) fornisce il supporto per il debug per la valutazione di un GDF. Vedere anche "integrazione di Esplora risorse di Windows" nella documentazione di DirectX SDK per C++.

In Windows 7 è stato introdotto il supporto per la seconda versione di uno schema per i file GDF. La nuova versione include un metodo semplificato per la creazione di attività di riproduzione e il supporto per le notifiche di aggiornamento, i provider di servizi di gioco, le statistiche dei giochi e i feed RSS per i provider di servizi di La versione più recente di GameUxInstallHelper gestisce tutte le registrazioni e il supporto legacy necessari per l'utilizzo di un file GDF della versione 2 con Windows Vista. Usare gli strumenti e il codice di esempio di DirectX SDK da agosto 2009 o versione successiva. È consigliabile usare un file GDF della versione 2 per abilitare il supporto per i feed RSS, le statistiche dei giochi e le notifiche di aggiornamento. Vedere anche gli esempi ProviderGDFExampleBinary e GameStatisticsExample.

In Windows Vista Business Edition, Windows 7 Professional Edition ed Enterprise Edition di Windows Vista e Windows 7, il collegamento giochi nel menu Start è nascosto. Esplora giochi è ancora disponibile nel menu Start facendo clic su **tutti i programmi** e quindi su **giochi**.

Per le applicazioni associate installate con il gioco, ma non per i giochi, è possibile creare gruppi di programmi di menu Start, collegamenti e icone desktop in tutte le versioni di Windows, tra cui Windows Vista e Windows 7. Tali applicazioni associate devono superare i giochi applicabili per i requisiti di Windows; per informazioni dettagliate, vedere [linee guida per i prodotti middleware di gioco](#guidelines-for-game-middleware-products). I servizi di gioco sono invitati a eseguire la registrazione con giochi Explorer come provider di giochi per Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 supporto per la sicurezza della famiglia/controlli parentali

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi devono supportare completamente la protezione della famiglia di Windows attenendosi alle regole seguenti:

-   I giochi non devono richiedere che l'utente disponga delle credenziali amministrative per la riproduzione. L'installazione, l'applicazione di patch e la rimozione possono richiedere credenziali amministrative, in base ai requisiti indicati nella sezione 3. Per quanto riguarda il requisito 2,1, seguire le linee guida per il controllo dell'account utente.
-   I giochi classificati in base alle classificazioni supportate da Windows, ad esempio ESRB e PEGI, devono includere le informazioni relative alle classificazioni assegnate nel file di definizione del gioco (GDF). Tutti i dati di classificazione disponibili devono essere inclusi in ogni versione localizzata di GDF, così come nella versione indipendente dalla lingua.
-   I giochi devono elencare i file eseguibili in GDF per offrire un'esperienza utente ottimale per le restrizioni generali dell'applicazione, a meno che il gioco non usi una tecnologia anti-pirateria che crea eseguibili denominati in modo casuale in fase di esecuzione.
-   I giochi devono chiamare il metodo **VerifyAccess** dell'interfaccia di Esplora giochi durante l'avvio, se disponibile, e uscire se restituisce \* pfHasAccess come false.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Tutti i giochi devono essere eseguiti nel contesto di un account utente standard per consentire agli account controllati dai controlli padre di Windows di riprodurre il gioco. I genitori desiderano poter monitorare e controllare l'accesso dei propri figli ai giochi. Inoltre, numerosi gruppi di settore, governativi e sostenitore desiderano modi migliori per consentire ai genitori di monitorare e controllare i giochi per i quali vengono esposti i loro figli. Insieme all'architettura offerta da Game Explorer, Microsoft fornisce ai genitori questa possibilità tramite i controlli padre di Windows.

Anche per i giochi che non fanno parte di un programma di classificazione, la richiesta di privilegi elevati consente di creare un'esperienza di riproduzione insufficiente per la maggior parte degli account utente. Questa situazione si verifica in particolare se sono abilitati i controlli padre, che richiedono all'elemento padre di immettere la password di amministratore ogni volta che viene avviato il gioco.

Il sistema dei controlli padre di Windows consente agli utenti di selezionare le classificazioni che ritengono appropriate per gli elementi figlio. I controlli padre supportano molti dei sistemi di classificazione globali. I controlli padre consentono inoltre ai genitori di limitare l'accesso ai giochi in base ai descrittori di contenuto (se il sistema di classificazione applicabile li supporta) e di consentire o impedire l'accesso a singoli giochi.

La scelta predefinita del sistema di classificazione per i controlli padre di Windows è basata sulle impostazioni locali del sistema, ma può essere modificata dall'utente in **Opzioni internazionali e della lingua** nel **Pannello di controllo**. Pertanto, ogni lingua supportata deve fornire tutti i dati di classificazione disponibili, in modo che l'utente abbia la libertà di selezionare qualsiasi classificazione desiderata.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi senza classificazione devono comunque soddisfare i requisiti per supportare Play come utente standard e per chiamare **VerifyAccess**. Tali giochi hanno come impostazione predefinita la categoria senza classificazione, visualizzano il testo "Nessuna classificazione fornita" in Esplora giochi e sono soggetti all'impostazione **restrizioni del gioco** nei **controlli padre** per i giochi non classificati. L'impostazione delle **restrizioni** predefinite è Consenti.

Le informazioni sulla classificazione in GDF verranno ignorate se il file binario che lo contiene non è firmato correttamente con Authenticode. Vedere requisito 2,3.

Nell'editor di file di definizione del gioco in DirectX SDK sono inclusi tutti i sistemi di classificazione supportati e le informazioni vengono replicate correttamente in tutte le versioni localizzate di GDF, oltre a una versione indipendente dalla lingua. Lo strumento GDFTrace decodifica e verificherà tutte le informazioni sulle classificazioni presenti. Utilizzare la versione agosto 2009 o successiva di questi strumenti.

Il GDF per un provider di giochi non contiene in genere informazioni di classificazione ed è soggetto alle impostazioni per il contenuto senza frequenza.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Sistemi di classificazione supportati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (Giappone)</li>
<li>ESRB (STATI UNITI)</li>
<li>OFLC (Australia)</li>
<li>PEGI (Europa)</li>
<li>PEGI Finland (deprecato)</li>
<li>PEGI Portogallo</li>
<li>PEGI/BBFC (Regno Unito)</li>
<li>USK (Germania)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista con un Service Pack</td>
<td>I Service Pack per Windows Vista aggiungono il supporto per gli elementi seguenti:<br/>
<ul>
<li>GRB (Corea del Sud)</li>
<li>&quot;Descrittori di contenuto Variant lieve per ESRB &quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 supporta i sistemi di classificazione supportati da Windows Vista e aggiunge il supporto per gli elementi seguenti: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 supporta i sistemi di classificazione precedenti e aggiunge il supporto per gli elementi seguenti:<br/>
<ul>
<li>COB-AU (Australia)</li>
<li>DJCTQ (Brasile)</li>
<li>PFB (Sudafrica)</li>
<li>OFLC-NZ (Nuova Zelanda)</li>
</ul>
Windows 8 ritira il supporto per i sistemi deprecati seguenti:<br/>
<ul>
<li>PEGI-FI (Finlandia)</li>
<li>OFLC (Australia)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Qualsiasi titolo che includa i nuovi descrittori di contenuto Windows Vista Service Pack 1 (SP1) di ESRB viene visualizzato come non valutata in Windows Vista senza una Service Pack.

 

I dati di classificazione più recenti vengono ignorati nelle versioni dei sistemi operativi senza supporto. Il PEGI (Finlandia) variant è ora deprecato a favore del sistema di classificazione standard PEGI (Europe). Il sistema OFLC è ora deprecato a favore di COB-AU per l'Australia.

Per altre informazioni su come rendere un gioco compatibile con i privilegi utente standard, vedere l'articolo relativo al [controllo dell'account utente per gli sviluppatori di giochi](/windows/desktop/DxTechArts/user-account-control-for-game-developers)di DirectX.

Per ulteriori informazioni sul file di definizione del gioco (GDF), vedere requisito 1,1.

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 supporto di giochi Rich salvati

\[Questo requisito è stato ritirato\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 supportare il requisito condizionale del controller comune di Xbox 360 per Windows \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi che supportano i controller di gamepad devono supportare il controller Xbox 360 per Windows con l'API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Se sono supportate anche le periferiche DirectInput, è anche possibile usare DirectInput. Tuttavia, XInput deve essere l'API predefinita se viene usato un dispositivo compatibile con Xbox 360.

Tutti i riferimenti ai trigger e ai pulsanti comuni del controller devono usare i nomi di Xbox 360. Per informazioni dettagliate, vedere l'elenco delle [terminologie del controller comune di Xbox 360 per Windows](#xbox-360-common-controller-for-windows-terminology) .

La vibrazione del controller deve essere spenta quando il gioco è in uno stato sospeso o sospeso.

Il controllo mouse/tastiera non può essere completamente disabilitato in qualsiasi momento. Come minimo, è necessario che sia disponibile un'opzione per tornare ai menu di gioco.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Questo requisito offre ai giocatori la libertà di scelta di usare il controller Xbox 360 o la tastiera e il mouse, a seconda del metodo di input più naturale e intuitivo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Questo requisito non si applica ai giochi che usano solo il mouse e/o la tastiera.

Si consiglia di implementare la navigazione dei menu per usare i pulsanti del controller standard ampiamente accettati:

-   A-Accept
-   B-Annulla
-   Start: accetta o Sospendi
-   Back-Cancel, backup di una schermata o di un livello di menu

Per altre informazioni, vedere [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

L'argomento [XInput e DirectInput](/windows/desktop/xinput/xinput-and-directinput) illustra i problemi relativi all'uso di entrambe le API nello stesso momento.

Si consiglia di non usare DirectInput per implementare i controlli della tastiera o del mouse. I controlli tastiera e mouse devono essere implementati solo mediante messaggi di Windows e API Win32. Per informazioni dettagliate su come ottenere informazioni sul movimento del mouse ad alta risoluzione senza usare DirectInput, vedere [sfruttare i vantaggi di High-Definition movimento del mouse](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1,5 supportano più proporzioni e soluzioni

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco deve supportare almeno le proporzioni seguenti e le risoluzioni dello schermo associate:

-   4:3 normale (800 600 o 1024 768)
-   16:9 widescreen (1280 720)
-   16:10 widescreen (1152 720 o 1680 1050 o 800 480)

Per la configurazione e il rilevamento della risoluzione dello schermo, il gioco deve rispettare le regole seguenti:

-   Per impostazione predefinita, il gioco usa la risoluzione desktop del dispositivo di visualizzazione se è una risoluzione supportata. Le proporzioni desktop devono essere usate come criterio di ricerca se il gioco sceglie una risoluzione predefinita diversa.
-   Il gioco deve richiedere all'utente di confermare le nuove impostazioni di visualizzazione quando viene apportata una modifica. Se l'utente non accetta entro 15 secondi, la visualizzazione deve ripristinare l'impostazione precedente.
-   Il gioco non deve allungare i pixel o centrare una finestra di rendering 4:3 per supportare le proporzioni widescreen. Tuttavia, il letterbox è accettabile.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Con il desktop di Windows 3D, non è possibile ipotizzare una particolare proporzioni o risoluzioni, a causa dei seguenti fattori:

-   Supporto per la visualizzazione di dettagli elevati.
-   Aumento della quota di mercato dei monitoraggi widescreen.
-   Distribuzioni HDTV per Windows Media Center.
-   Requisiti di accessibilità.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Idealmente, per impostazione predefinita il gioco si riferisce alle proporzioni native dello schermo. Tuttavia, ottenere queste informazioni in modo affidabile può essere una sfida, quindi come soluzione più generale il gioco può presupporre che il desktop sia in esecuzione in proporzioni native. La risoluzione del desktop può essere ottenuta chiamando [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) con \_ le impostazioni del registro di sistema enum \_ .

Per altri dettagli, vedere le sezioni proporzioni e widescreen dell'articolo di DirectX [Introduzione all'esperienza a 10 piedi per gli sviluppatori di giochi Windows](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1,6 supporto del lancio da Windows Media Center

\[Questo requisito è stato ritirato.\]

### <a name="17-direct3d-support"></a>1,7 supporto Direct3D

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere il renderer predefinito selezionato.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'architettura grafica principale di Windows Vista e Windows 7 è stata progettata in Direct3D. Direct3D 8 e versioni precedenti sono supportate mediante la modifica del mapping delle interfacce legacy.

L'uso di versioni di Direct3D più recenti di Direct3D 9 è vivamente consigliato. Vedere i giochi per Windows Showcase S. 1. La richiesta di Direct3D 10 o Direct3D 11 è completamente conforme al requisito 1,7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 abilitare la compatibilità con DPI elevata

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando il ridimensionamento di punti per pollice (DPI) è abilitato (testato con 144 DPI per la scalabilità del 150% alla risoluzione dello schermo 1600 1200) in Windows Vista e Windows 7.

Questa operazione richiede in genere che l'eseguibile del gioco dichiari che è compatibile con DPI. Questa operazione viene eseguita incorporando un elemento manifesto: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I monitor LCD di alta qualità sono comuni come schermi di computer e sembrano migliori quando sono basati sulle risoluzioni native, in genere 1280 1024, 1600 1200 e così via. I clienti che hanno difficoltà a leggere il testo e a visualizzare le immagini in questa risoluzione spesso configurano i desktop dei computer a una risoluzione inferiore e presentano artefatti visivi dal ridimensionamento LCD. I clienti possono invece lasciare la risoluzione alla dimensione nativa e modificare il valore DPI dello schermo di Windows, in modo da rendere più grande l'aspetto dell'elemento e del testo senza sacrificare la qualità dell'immagine.

Sebbene questa funzionalità sia stata disponibile in alcune forme rispetto a Windows XP, è raramente abilitata dai clienti o dagli OEM. Attualmente, più della metà di tutti i computer vengono visualizzati con una risoluzione inferiore rispetto alla risoluzione nativa del monitor, in base ai suggerimenti dei clienti. Windows 7 rende questa funzionalità molto più visibile ai clienti durante la configurazione iniziale e quando si modificano le impostazioni di visualizzazione, incoraggiandoli a usare il ridimensionamento DPI anziché modificare la risoluzione del desktop.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

È invece possibile usare la funzione [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) , se viene chiamata prima nel codice di avvio del processo. È preferibile aggiungere al manifesto, per assicurarsi che non esistano race condition con elementi software, ad esempio dll, che potrebbero essere inizializzati prima che venga chiamato il punto di ingresso principale. Si noti che **SetProcessDPIAware** è presente solo in Windows Vista e Windows 7.

L'aggiunta dell'elemento manifest è facile da eseguire con Visual Studio 2005 e 2008; creare un file denominato DpiAware. manifest che contenga il testo seguente:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Quindi, all'interno di Visual Studio, aggiungere dpiware. manifest al progetto. Verificare che **Incorpora manifesto** sia impostato su **Sì** nelle proprietà del progetto. Si noti che le versioni precedenti dello strumento Manifesto (Mt.exe) genereranno un avviso non corretto con gli elementi manifesto compatibili con DPI. Per risolvere questo problema, aggiornare Mt.exe alla versione più recente dall'Windows SDK.

Visual Studio 2010 include un'impostazione nelle proprietà del progetto, denominata **Enable dpi Awareness**, che elimina la necessità di un file come DpiAware. manifest. Trovare **Enable dpi Awareness** espandendo le **proprietà di configurazione** e **lo strumento Manifesto**, quindi selezionando **input & output**.

Per impostazione predefinita, in Windows la modalità di visualizzazione tradizionale è 96 DPI, che era comune per i monitoraggi CRT.

Sebbene le applicazioni a schermo intero modifichino la risoluzione dello schermo, usano spesso messaggi e metriche della finestra quando si configurano i buffer e si visualizzano i rettangoli. Con la virtualizzazione DPI le modalità di visualizzazione a schermo intero vengono ritagliate e la dichiarazione di compatibilità DPI impedisce tali problemi. Per ulteriori informazioni, vedere [scrittura DPI-Aware applicazioni Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Sicurezza e compatibilità

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi dei clienti**

I requisiti seguenti migliorano la sicurezza complessiva dei giochi e assicurano che funzionino con Windows in architetture diverse, in configurazioni diverse e in modalità diverse.

### <a name="21-follow-user-account-control-guidelines"></a>2,1 seguire le linee guida per il controllo dell'account utente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Ogni file eseguibile, ovvero tutti i file con estensione exe, deve contenere un manifesto incorporato che ne definisce il livello di esecuzione includendo il tag seguente:

``` syntax
            <requestedExecutionLevel>
```

Per requisito 1,2, il gioco principale e l'eseguibile di autorun devono avere il livello di esecuzione asInvoker per supportare i contesti utente standard.

I file di dati utente che hanno associazioni di file registrate con **Esplora file** devono essere inseriti in una sottocartella della cartella specificata da CSIDL \_ Personal (detti anche **documenti** o **documenti**). Tutti gli altri file di dati utente devono essere archiviati in una sottocartella delle cartelle specificate da CSIDL \_ Local \_ AppData o CSIDL \_ Common \_ AppData. Queste directory sono nascoste per impostazione predefinita per i singoli utenti e per tutti gli utenti.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'esperienza Windows di un utente è più sicura se le applicazioni vengono eseguite solo con le autorizzazioni necessarie.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Se solo alcune funzionalità di un'applicazione richiedono privilegi amministrativi (ad esempio, un'applicazione che deve configurare un firewall), il processo principale dell'applicazione deve comunque essere eseguito usando i privilegi utente standard. Le funzionalità che richiedono privilegi amministrativi devono essere spostate in un processo distinto, ad esempio un programma di installazione o un'utilità di configurazione.

Se non sono necessari privilegi amministrativi, il file XML del manifesto incorporato deve includere quanto segue:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Se sono necessari privilegi amministrativi, il file XML del manifesto incorporato deve includere quanto segue:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Con Visual Studio 2005 questa operazione è facilmente incorporata aggiungendo un file manifesto (con estensione manifest) che contiene uno dei blocchi precedenti al progetto e assicurando che **Incorpora manifesto** sia impostato su **Sì** nelle proprietà del progetto per lo strumento Manifesto. Per Visual Studio 2008 e 2010, è possibile impostare le proprietà del controllo dell'account utente direttamente nelle proprietà del progetto per il linker nella pagina **file manifesto** . Si noti che le versioni precedenti dello strumento Manifesto (Mt.exe) generano un avviso non corretto con gli elementi manifesto del controllo dell'account utente. Per risolvere questo problema, aggiornare Mt.exe alla versione più recente dall'Windows SDK.

Vedere requisito 3,1 per informazioni dettagliate sui casi speciali di installazione, applicazione di patch e rimozione.

Le librerie a collegamento dinamico (dll) non richiedono tali manifesti.

Per ulteriori informazioni sul controllo dell'account utente, vedere [controllo dell'account utente per sviluppatori di giochi](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2,2 supportano le versioni di Windows x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per mantenere la compatibilità con le edizioni di Windows a 64 bit, i giochi devono soddisfare i requisiti seguenti.

-   I titoli e i programmi di installazione del titolo non devono contenere codice a 16 bit o basarsi su un componente a 16 bit.
-   Se il gioco dipende da driver in modalità kernel per l'operazione, è necessario che siano disponibili versioni x64 di questi driver. L'installazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni di Windows a 64 bit.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Molti utenti di Windows Vista e Windows 7 eseguiranno edizioni a 64 bit del sistema operativo per tutta la durata del prodotto, pertanto è fondamentale che le applicazioni siano compatibili con questo sistema operativo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Windows in Windows 64 (WOW64) consente l'esecuzione di codice a 32 bit nelle edizioni di Windows a 64 bit, pertanto non è necessario che l'applicazione sia codice nativo a 64 bit nelle edizioni di Windows a 64 bit. Il codice a 16 bit non viene eseguito nelle edizioni di Windows a 64 bit.

Il mantenimento della compatibilità con Windows XP Professional x64 Edition non è obbligatorio, ma è fortemente consigliato.

Per informazioni dettagliate, vedere [programmazione a 64 bit per sviluppatori di giochi](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>2,3 file di firma

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Tutti i file di codice eseguibile (in genere, i file con estensione exe o dll) devono essere firmati con un certificato Authenticode valido pubblicamente e devono disporre di un URL del server di timestamp valido per la firma di produzione.

Se il gioco usa Windows Installer, i file del pacchetto del programma di installazione (file con estensione msi) devono essere firmati.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

La firma di un file consente agli utenti di decidere se considerare attendibile un'applicazione e assicura agli utenti che i file non sono stati manomessi. Consente inoltre di eseguire correttamente le applicazioni in ambienti bloccati.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per informazioni dettagliate, vedere [firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Se il gioco usa Windows Installer, è consigliabile abilitare l'applicazione di patch UAC/LUA, includendo una tabella MsiPatchCertificate. Per ulteriori informazioni, vedere applicazione di [patch a controllo dell'account utente (UAC)](/windows/desktop/Msi/user-account-control--uac--patching).

Non è consigliabile firmare i file CAB (CAB), a meno che non siano relativamente piccoli (inferiori a 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2,4 firmare i driver

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente.

Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve disporre di una firma Microsoft, che può essere ottenuta da Windows Hardware Quality Labs (WHQL) o dal programma driver affidabilità Signature (DRS).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I driver non correttamente scritti o malware possono influenzare gravemente la stabilità e la sicurezza di un sistema. Nelle edizioni a 64 bit di Windows Vista e Windows 7 i driver non firmati non vengono caricati. Questo criterio può essere abilitato anche per le edizioni a 32 bit di Windows Vista e Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Sono necessarie entrambe le versioni native a 32 bit e a 64 bit di tutti i driver in modalità kernel per requisito 2,2.

Ulteriori informazioni sui programmi di firma dei driver Microsoft sono disponibili nel [portale per sviluppatori di hardware Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2,5 eseguire il controllo della versione corretto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi non devono essere eseguiti nei sistemi operativi futuri, come indicato dalle modifiche apportate al numero di versione di Windows, a meno che il contratto di licenza con l'utente finale non vieti l'uso nei sistemi operativi futuri. Se si suppone che il gioco abbia esito negativo, è necessario che venga visualizzato un messaggio appropriato all'utente.

Se vengono eseguiti i controlli della versione di Windows, è necessario utilizzare le API di controllo della versione ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) o [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) per controllare la versione del sistema operativo. Le chiavi del registro di sistema non devono essere lette per determinare la versione.

I controlli della versione espliciti per il runtime di DirectX non devono essere presenti nel gioco. Questi controlli della versione non devono essere presenti nell'installazione che avvia il programma di installazione di DirectX Runtime (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Quando gli utenti di Windows eseguono l'aggiornamento dei sistemi operativi, non devono essere bloccati dalla riproduzione dei giochi correnti semplicemente perché il numero di versione di Windows è aumentato. I controlli della versione scritti correttamente continuano a creare problemi per il software che, in caso contrario, funziona correttamente nelle versioni più recenti di Windows o semplicemente con l'aggiunta di un Service Pack di Windows.

La logica di confronto del controllo della versione fragile per DirectX Runtime ha creato numerose installazioni non riuscite quando viene eseguita in versioni diverse di Windows. Il numero di versione di DirectX si applica solo ai componenti principali del sistema operativo. Non si applica ai componenti di DirectX SDK affiancati usati da molti giochi.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

È piuttosto comune vedere che i programmi di installazione verificano la presenza di una versione minima del sistema operativo. Questo controllo, tuttavia, deve essere eseguito con cautela per verificare che il test sia maggiore o uguale a, anziché l'uguaglianza semplice, bloccando quindi a una versione specifica del sistema operativo. L'uso di Application Verifier test **HighVersionLie** è un modo rapido e semplice per determinare il modo in cui il programma di installazione reagirà a una modifica significativa nel numero di versione del sistema operativo.

L'uso corretto del pacchetto di ridistribuzione di DirectX Runtime (installazione di DirectX) comporta sempre l'avvio durante l'installazione, preferibilmente in modalità invisibile all'utente. Ciò consente al codice fornito da Microsoft di eseguire eventuali aggiornamenti della versione necessari. Consente inoltre di installare tutti i componenti facoltativi di DirectX SDK side-by-Side, ad esempio D3DX, XACT, MDX o XInput.

Per le procedure consigliate per la distribuzione di DirectX Runtime, vedere [installazione di DirectX per sviluppatori di giochi](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

Si consiglia ai giochi che supportano Windows XP di verificare la presenza di un livello di Service Pack 2 o superiore, poiché Service Pack 2 (SP2) e Service Pack 3 (SP3) forniscono miglioramenti significativi per la sicurezza, un requisito semplificato di ridistribuzione di DirectX Runtime e una distribuzione estremamente ampia. La maggior parte delle moderne tecnologie Microsoft che supportano Windows XP richiedono SP2 o SP3 (XAudio2, giochi per Windows-LIVE e così via).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2,6 supportare sessioni utente simultanee

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per i giochi basati su grafica 3D non è necessario usare una connessione Desktop remoto, ma l'utente deve ricevere un avviso quando il gioco non riesce.

I giochi devono supportare scenari multitasking standard di Windows attenendosi alle regole seguenti:

-   I giochi non devono bloccare l'uso di sessioni utente simultanee.
-   Un gioco deve essere eseguito in una nuova sessione utente quando è già in esecuzione in un'altra sessione.
-   Il suono del gioco in una sessione utente non deve essere ascoltato quando un altro utente è attivo in una sessione diversa.
-   I giochi devono supportare il cambio rapido utente.
-   I giochi non devono tentare di disabilitare il cambio di attività standard. I giochi non devono disabilitare il tasto di scelta rapida ALT + TAB. Ai giochi è consentito disabilitare le scelte rapide da tastiera di accessibilità, come descritto in [disabilitazione dei tasti di scelta rapida nei giochi](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Gli utenti di Windows devono essere in grado di eseguire sessioni simultanee senza conflitti o rotture. Si tratta di uno scenario comune per un computer Windows condiviso da una famiglia, da un compagno di gruppo o da altri.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per verificare se il gioco viene avviato in una sessione remota, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Un valore diverso da zero indica che la sessione è remota.

Per ulteriori informazioni, vedere [cambio rapido utente](/windows-hardware/drivers/display/fast-user-switching). Si noti che il cambio rapido utente si verifica se vengono abilitate le restrizioni temporali dei controlli padre quando il tempo dell'utente è attivo. Per ulteriori informazioni, vedere requisito 1,2.

</dd> </dl>

### <a name="27-support-long-names"></a>2,7 supporto di nomi lunghi

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Se un gioco supporta il salvataggio di file, deve essere in grado di salvare i file con nomi e percorsi lunghi. Il gioco deve gestire correttamente caratteri di file system speciali, ad esempio \\ /: \* ? " < >, in tutti i campi di input utente utilizzati per creare nomi file o percorsi.

I giochi devono funzionare correttamente quando un utente ha un nome utente lungo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I giocatori sono abituati a usare nomi lunghi nei percorsi profondi supportati dal sistema operativo sottostante.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I nomi lunghi sono definiti come quelli che contengono i valori massimi definiti nel Windows SDK.

</dd> </dl>

## <a name="installation"></a>Installazione

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi dei clienti**

I clienti possono essere sicuri che le applicazioni verranno installate in Windows senza degradare il sistema operativo o altre applicazioni se le applicazioni utilizzano metodi di distribuzione dei componenti di sistema ufficiali. Un'esperienza di installazione semplificata offre un'esperienza predefinita più accessibile e senza problemi per i giochi.

### <a name="31-support-easy-installation"></a>3,1 supporto dell'installazione semplificata

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi devono fornire un percorso semplificato nell'interfaccia utente del programma di installazione implementando quanto segue:

-   Visualizza al massimo una richiesta EULA.
-   Il percorso di installazione predefinito deve ignorare tutte le selezioni per l'installazione (ad esempio, la cartella di installazione o le selezioni dei componenti), presupporre le selezioni predefinite, quindi eseguire il gioco o l'utilità di avvio al completamento dell'installazione, senza ulteriori richieste. Se lo si desidera, è possibile specificare un'opzione di installazione personalizzata per le opzioni di configurazione avanzate.
-   Installare tutti i componenti del sistema operativo necessari, ad esempio i runtime di DirectX e Visual C, usando i pacchetti di ridistribuzione Microsoft corretti. L'installazione deve essere eseguita in modo invisibile all'utente senza chiedere conferma e senza essere sorvegliata dai controlli delle versioni dei componenti.
-   Fornire la rimozione tramite **programmi e funzionalità** nel **Pannello di controllo** sia per l'applicazione di gioco che per i file di lavoro generati. È consigliabile eliminare eventuali file di dati creati dall'utente. Il processo di rimozione deve garantire che tutti i file installati vengano rimossi e che vengano cancellate tutte le impostazioni, ad esempio le voci dell'elenco di eccezioni del firewall e le chiavi del registro di sistema. I componenti ridistribuiti del sistema operativo non devono essere rimossi.
-   Se il gioco richiede l'aggiunta di eccezioni alla Windows Firewall, il processo di installazione può richiedere agli utenti di indicare che questa modifica è necessaria. Questa richiesta dovrebbe essere visualizzata prima dell'inizio dell'installazione.

L'installazione e la rimozione possono richiedere diritti amministrativi. L'applicazione di patch può richiedere la richiesta di credenziali amministrative, a seconda della frequenza di aggiornamento. La riproduzione normale del gioco non deve richiedere diritti amministrativi, per requisito 2,1 seguire le linee guida per il controllo dell'account utente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'installazione semplificata è una filosofia di sviluppo di giochi incentrata su Windows progettata per semplificare e semplificare il processo di installazione dei giochi in computer che eseguono sistemi operativi Windows. L'installazione semplificata è abilitata usando un set di tecnologie e procedure consigliate che consentono di ridurre la complessità superflua e il rischio di installare giochi nei computer Windows.

Gli obiettivi principali sono i seguenti:

-   Ridurre la quantità di tempo per entrare nel gioco e iniziare la riproduzione.
-   Ridurre il numero di finestre di dialogo e scelte a pochissimi o nessuno per semplificare l'esperienza di installazione del gioco.

Alcune installazioni tradizionali hanno richieste che consentono installazioni non funzionali, anche se l'applicazione sembra essere installata correttamente. Ad esempio, un gioco può richiedere a un utente di accettare un contratto di licenza. Il gioco viene quindi installato e viene visualizzato il contratto di licenza DirectX. Questo EULA consente agli utenti di rifiutare e quindi ignorare l'installazione del runtime di DirectX. Questo scenario può causare un errore di esecuzione del gioco a causa di componenti mancanti.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per ulteriori informazioni sull'installazione dei giochi, le tecniche di installazione dei giochi non tradizionali, le soluzioni di patch compatibili con UAC e la gestione delle patch frequenti, vedere gli articoli DirectX seguenti:

-   [Semplificazione dell'installazione del gioco](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Installazione su richiesta per giochi](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Procedure consigliate per l'installazione per giochi multiplayer online](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> La rimozione di file di dati generati specifici dell'utente deve essere eseguita solo per l'utente corrente e per i percorsi utente condivisi comuni. Non esiste un modo efficace per eseguire la scansione del sistema per rimuovere i file specifici dell'utente per altri utenti, anche se la rimozione richiede credenziali amministrative.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 supporto del controllo dell'account utente per l'installazione

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente. I percorsi specifici dell'utente saranno diversi dal programma di installazione e dal lettore anche per i sistemi a utente singolo a causa dell'elevazione delle credenziali di amministratore. Pertanto, quando un gioco viene eseguito per la prima volta, deve eseguire attività specifiche dell'utente, separatamente rispetto al processo di installazione.

La finestra di dialogo Windows Firewall eccezione non deve essere visualizzata quando un utente ospita o partecipa a un gioco multiplayer. È necessario eseguire tutte le operazioni di configurazione necessarie al momento dell'installazione. Le istruzioni di installazione dovrebbero informare l'utente che l'operazione verrà eseguita come parte dell'installazione.

Il programma di installazione del gioco deve fornire un manifesto incorporato che definisce il livello di esecuzione richiesto, per requisito 2,1 seguire le linee guida per il controllo dell'account utente.

Se il gioco viene avviato dal programma di installazione al termine dell'installazione, è necessario avviarlo nel contesto dell'utente originale.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Una delle principali modifiche apportate al sistema operativo Windows in Windows Vista è l'aggiunta del controllo dell'account utente, che consente di eseguire le applicazioni con privilegi ridotti per impostazione predefinita. Di conseguenza, i programmi di installazione devono gestire i livelli di privilegio. Windows 7 USA anche il controllo dell'account utente. Sebbene Windows 7 migliori l'esperienza utente di UAC, i programmi di installazione devono comunque soddisfare gli stessi requisiti di Windows Vista per funzionare correttamente, senza basarsi sul comportamento di virtualizzazione potenzialmente confuso.

Il controllo dell'account utente è attivo per impostazione predefinita in Windows Vista e Windows 7 e la maggior parte dei clienti (88% o più, in base ai commenti e suggerimenti) lascia questa funzionalità abilitata.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per altri dettagli sulla configurazione della Windows Firewall, vedere l'articolo relativo a DirectX [Windows Firewall per sviluppatori di giochi](/windows/desktop/DxTechArts/games-and-firewalls) e l'esempio FirewallInstallHelper.

L'avvio standard del gioco alla fine del processo di installazione non è in grado di soddisfare l'ultimo aspetto di questo requisito se l'installazione viene avviata da un utente standard e se il processo di installazione richiede privilegi amministrativi (ovvero richiede credenziali di amministratore). Eredita inoltre i privilegi amministrativi, che rappresenta un potenziale rischio per la sicurezza. Al contrario, un caricatore bootstrap del programma di installazione deve avviare il gioco dopo il ritorno da una chiamata riuscita del programma di installazione. Per ulteriori informazioni, vedere l'articolo di MSDN Magazine per [insegnare alle app la riproduzione con il controllo dell'account utente di Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3,3 installare in cartelle corrette

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per impostazione predefinita, i giochi installati per tutti gli utenti devono essere installati nella cartella programmi. I dati utente devono essere scritti quando il gioco viene eseguito per la prima volta, non durante l'installazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Gli utenti devono avere la flessibilità necessaria per installare le applicazioni in cui sono necessari. Devono inoltre avere un'esperienza coerente e sicura con il percorso predefinito dei file.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi possono usare i vari percorsi di cartelle note, ad esempio quelli specificati da CSIDL \_ Local \_ AppData e CSIDL \_ Common \_ AppData, per archiviare quantità significative di dati di gioco e di supporto per i file eseguibili per implementare scenari avanzati di installazione su richiesta e applicazione di patch.

Poiché l'installazione può richiedere l'elevazione a un account utente diverso durante il processo di installazione di tutti gli utenti, non esiste una posizione utente corretta in cui archiviare i dati al momento dell'installazione. Inoltre, se la crittografia dei file è abilitata, i file crittografati possono essere accessibili solo dall'account utente che li ha creati.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3,4 installare correttamente le risorse di Windows

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Le applicazioni non devono tentare di installare file o chiavi del registro di sistema protetti da Protezione risorse di Windows (WRP). Se l'applicazione richiede versioni più recenti dei componenti di sistema, è necessario aggiornare questi componenti utilizzando un Microsoft Service Pack o un pacchetto di installazione approvato da Microsoft che contiene il componente di sistema. I componenti di sistema non devono mai essere riassemblati.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Protezione risorse di Windows (WRP) è progettato per garantire che le risorse di sistema protette vengano aggiornate solo utilizzando i meccanismi di installazione o aggiornamento approvati da Microsoft. WRP migliora l'affidabilità del sistema garantendo che i risultati di un'installazione siano prevedibili.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

WRP è il successore della protezione dei file di Windows, che protegge la maggior parte dei componenti di sistema installati nella cartella Windows. WRP protegge la maggior parte delle chiavi del registro di sistema per la creazione di oggetti COM. Riserva inoltre alcune cartelle per l'utilizzo esclusivo da parte del sistema operativo. I tentativi di accesso alle risorse protette causano in genere un errore di negazione dell'accesso.

Per informazioni dettagliate sulle procedure consigliate per la distribuzione di DirectX Runtime con un gioco, vedere l'articolo DirectX [installazione di DirectX per sviluppatori di giochi](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitare il riavvio durante l'installazione

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco non deve presupporre che l'installazione dei componenti di Windows dai pacchetti di ridistribuzione richieda un riavvio, a meno che il riavvio non sia indicato da un risultato restituito o dalla documentazione Microsoft.

Se il programma di installazione del gioco forza sempre un riavvio, questo deve essere approvato da Microsoft.

Le finestre di dialogo file in uso incluse nei pacchetti di Windows Installer devono contenere un'opzione per chiudere automaticamente le applicazioni e tentare di riavviarle al termine dell'installazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Il riavvio del sistema dopo un'installazione è un'operazione inopportuna per gli utenti e in genere non è necessario.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per ulteriori informazioni, vedere [utilizzo di Windows Installer con Gestione riavvio](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3,6 usare correttamente il controllo delle versioni dei file

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco deve verificare in modo corretto che siano installate le versioni dei file più recenti. L'installazione di un gioco non deve mai far regredire alcun file che non viene prodotto o condiviso da applicazioni che non vengono generate.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I componenti condivisi e i componenti di sistema vengono spesso aggiornati per le correzioni di sicurezza e le funzionalità espanse. Un'installazione che include una versione precedente dei componenti aggiornati non dovrebbe comportare la perdita di aggiornamenti e correzioni già applicati.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3,7 supporto \[ requisito condizionale Autorun\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per i giochi distribuiti su CD, DVD o altri supporti rimovibili che supportano l'esecuzione automatica, quando il disco viene inserito per la prima volta, l'applicazione deve eseguire automaticamente o richiedere all'utente di installare il gioco, a meno che l'utente non abbia disabilitato la funzionalità di avvio automatico.

Dopo che l'applicazione è stata installata correttamente, il reinserimento del disco nell'unità non deve causare l'avvio automatico dell'installazione. È accettabile richiedere agli utenti se vogliono aggiornare o modificare le opzioni di installazione.

L'applicazione di avvio automatico non deve richiedere l'elevazione (ovvero deve avere asInvoker nel manifesto, per requisito 2,1, anche se può avviare il programma di installazione o un'altra utilità che richiede diritti amministrativi. L'elevazione deve verificarsi solo se il gioco non è installato o se l'utente lo seleziona in modo specifico.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Autorun semplifica l'uso di applicazioni distribuite con supporti, ad esempio giochi che in genere richiedono che il disco sia presente nell'unità per riprodurre il gioco.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Non è accettabile richiedere all'utente di spostarsi in Esplora file per avviare l'installazione dal CD o dal DVD.

Per i giochi distribuiti su più dischi, i dischi successivi dovrebbero idealmente usare la funzionalità di avvio automatico oppure continuare l'installazione senza richiedere all'utente di premere un tasto o eseguire altre azioni.

Quando si crea un programma di autorun, assicurarsi che tutti i componenti necessari siano presenti in installazioni aggiornate di Windows. Le applicazioni tipiche si basano sulle tecnologie installate dal programma di installazione di, ma l'esecuzione automatica viene eseguita prima di tale configurazione. Un esempio comune è l'errore dei programmi di autorun perché le DLL di runtime di Visual C non sono state incluse come parte dell'installazione di Windows. Il programma di autorun, quindi, deve usare la distribuzione CRT locale dell'applicazione o collegare in modo statico la libreria CRT.

I programmi di avvio automatico scritti per l'utilizzo nelle versioni di Windows precedenti a Windows Vista non devono utilizzare il Runtime .NET perché questa tecnologia non è inclusa in Windows XP o nelle versioni precedenti di Windows. Windows Server 2003 e Windows Vista sono le prime versioni di Windows per includere il Runtime .NET come parte del sistema operativo.

Per motivi simili, i programmi di autorun non possono richiedere la presenza di componenti side-by-side facoltativi di DirectX SDK, ad esempio D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT e MDX 1,1.

Per un esempio dell'uso di autorun, vedere esempio di AutoRun.

</dd> </dl>

## <a name="reliability"></a>Affidabilità

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi dei clienti**

Questi requisiti rendono un'applicazione più affidabile riducendo al minimo il numero di arresti anomali, blocchi e riavvii. I requisiti di affidabilità consentono di garantire che il software sia più prevedibile, gestibile, resiliente e reversibile.

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminare i riavvii non necessari

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Tutti i programmi di installazione di applicazioni devono sfruttare le API di gestione riavvio per evitare il riavvio del sistema (vedere requisito 3,5).

I giochi non devono bloccare l'arresto.

Tutte le applicazioni devono rispondere a gestione riavvio ascoltando e rispondendo ai messaggi di chiusura seguenti:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Le applicazioni GUI devono rispondere (TRUE) immediatamente in preparazione al riavvio.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Le applicazioni devono restituire un valore 0 entro 5 secondi, quindi chiudere.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C 
</dt> <dd>

Le applicazioni console che ricevono questo messaggio devono essere chiuse immediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I riavvii del sistema rappresentano un'importante interferenza. Si tratta di un'esperienza utente non valida e deve essere ridotta a icona. Alcune operazioni, ad esempio gli aggiornamenti critici del sistema, possono richiedere il riavvio. Ascoltando i messaggi di chiusura, il gioco e altre applicazioni possono rispondere tempestivamente alle richieste da Gestione riavvio. In questo modo, è possibile evitare inutilmente ritardi nelle richieste di riavvio valide.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Se un programma di installazione di giochi usa la tecnologia Windows Installer (MSI) senza alcuna azione personalizzata, questa funzionalità viene fornita automaticamente. I pacchetti di ridistribuzione Microsoft supportano anche Gestione riavvio.

Per ulteriori informazioni su Gestione riavvio, vedere l'articolo MSDN [relativo a gestione riavvio](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminare Application Verifier errori

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco non deve generare errori con Microsoft Application Verifier (AppVerifier), versione 4,0 o successiva, nei test seguenti:

-   Nozioni fondamentali: handle, heap, blocchi, memoria, TLS
-   Varie: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

AppVerifier verifica la presenza di molti problemi noti che provocano arresti anomali e blocchi nelle applicazioni Windows, oltre a vulnerabilità di sicurezza note.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per ulteriori informazioni su Application Verifier, vedere [Application Verifier](/previous-versions/ms220948(v=vs.80)) e [utilizzo di Application Verifier all'interno del ciclo](/previous-versions/aa480483(v=msdn.10)) di vita di sviluppo del software su MSDN. È possibile scaricare Application Verifier dal [download dei dettagli: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) nell'area download Microsoft.

Questo requisito non si applica alle applicazioni gestite pure senza l'interoperabilità nativa.

Questi test devono essere eseguiti in una build di rilascio. Le compilazioni di debug possono generare falsi errori. Alcune tecnologie anti-pirateria e anti-cheat possono interferire con l'esecuzione di AppVerifier. Pertanto, questi test devono essere eseguiti senza tecnologie anti-pirateria e anti-cheat abilitate.

Potrebbe essere necessario impostare la proprietà completa del test nozioni di base: heaps su FALSE, perché la PageHeap completa aumenta significativamente la quantità di memoria dell'applicazione in esecuzione. Gli errori verranno comunque rilevati, ma potrebbe essere più difficile tenere traccia se si usa solo PageHeap parziali.

Se si usano i test correlati a UAC/LUA in Application Verifier per soddisfare i requisiti di controllo dell'account utente 2,1 e 3,2, è consigliabile usare l' [Analizzatore utente standard](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) per esaminare i risultati. Sono inoltre disponibili numerosi altri test utili offerti da Application Verifier che si consiglia di usare in fase di sviluppo e test per garantire un livello elevato di compatibilità con le versioni correnti e future di Windows. Il test **HighVersionLie** viene usato per verificare la conformità con il requisito 2,5.

Visual Studio Team System include un subset della funzionalità AppVerifier integrata nell'ambiente di debug. Questo può risultare utile per tenere traccia dei problemi e risolverli con le nozioni di base: heap, handle e blocchi test.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4,3 supporto di Segnalazione errori Windows e informazioni sulla versione del file

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per abilitare il supporto di Segnalazione errori Windows, è necessario che i giochi soddisfino i requisiti seguenti:

-   I giochi devono gestire solo le eccezioni note e previste. Segnalazione errori Windows non deve essere disabilitato. Se un errore, ad esempio una violazione di accesso, viene visualizzato in un gioco, deve consentire Segnalazione errori Windows di segnalare l'arresto anomalo.
-   Tutti i file eseguibili (ad esempio, file con estensione exe o dll) devono contenere un nome di prodotto, un nome della società e una versione del file accurati.
-   La normale uscita del gioco non può causare un errore di eccezione sconosciuto.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Le API Segnalazione errori Windows forniscono un feedback fondamentale a Microsoft per il rilevamento di arresti anomali e blocchi diffusi nelle applicazioni. Questo consente a Microsoft e ai suoi partner di rilevare e risolvere rapidamente i problemi di sistema e di driver che causano rapidamente errori dell'applicazione.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi possono includere gestori di eccezioni non gestite personalizzati per eseguire il supporto personalizzato e la funzionalità di creazione di report, ma devono passare qualsiasi errore per le funzioni **ReportFault** o **WerReportSubmit** .

È possibile verificare le informazioni sulla versione del file appropriate visualizzando le proprietà del file nell'interfaccia utente del desktop di Windows e controllando la pagina delle proprietà Version.

Per altre informazioni sulle API Segnalazione errori Windows e su come analizzare i dump di arresto anomalo del sistema generati quando si usa questo servizio, vedere l'articolo relativo all' [analisi dei dump di arresto anomalo](/windows/desktop/DxTechArts/crash-dump-analysis)dell'articolo DirectX.

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Terminologia del controller comune di Xbox 360 per Windows



|                                          |                                                                                                  |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| A                                        | Pulsante A                                                                                     |
| B                                        | Pulsante B                                                                                     |
| INDIETRO                                     | Pulsante indietro                                                                                  |
| (Right/Left) Bumper                      | Pulsante in alto a destra e al bordo sinistro del controller. Equivalente a un pulsante della spalla.    |
| Pad direzionale                          | Pad direzionale del controller                                                                   |
| D-Pad                                    | Abbreviazione accettata del pad direzionale                                                         |
| Punto di distribuzione (DP)                                       | Abbreviazione del pad direzionale e etichetta del controller                                                |
| RB, LB                                   | Abbreviazioni e etichette del controller a destra e a sinistra                                        |
| RS, LS                                   | Abbreviazioni e etichette del controller a destra e a sinistra                                         |
| RT, LT                                   | Abbreviazioni del trigger Right e Left e etichette del controller                                       |
| RSB, LSB                                 | Abbreviazioni e etichette del controller a destra e a sinistra                                         |
| START                                    | Il pulsante Start                                                                                 |
| (Right/Left) Stick                       | Il controller Stick. In precedenza levetta.                                                       |
| pulsante Stick (Right/Left)                | Pulsante della barra del controller. Pulsante levetta in precedenza.                                         |
| trigger (Right/Left)                     | Trigger del controller.                                                                          |
| Vibrazione                                | Feedback del gioco prodotto dal motore del controller. Non usare Rumble.                           |
| X                                        | Pulsante X                                                                                     |
| S                                        | Pulsante Y                                                                                     |
| Controller Xbox 360 per Windows          | Il gamepad Xbox 360 è stato venduto come SKU hardware del PC, incluso un disco driver di dispositivo Windows.          |
| Controller wireless Xbox 360 per Windows | Il gamepad Xbox 360 wireless è stato venduto come SKU hardware del PC, incluso un disco driver di dispositivo Windows. |



 

## <a name="guidelines-for-game-middleware-products"></a>Linee guida per i prodotti middleware di gioco

### <a name="introduction"></a>Introduzione

Affinché i giochi siano idonei per i giochi per il programma Windows, devono soddisfare un elenco di requisiti tecnici. Tutti i componenti di terze parti forniti con un titolo (file eseguibili, dll, driver e così via) devono soddisfare anche questi requisiti affinché il gioco sia idoneo. Questo documento evidenzia i requisiti più comuni che devono essere soddisfatti anche dai componenti di terze parti per il gioco per superare i test di conformità. I programmi di installazione e il motore di gioco completo e i pacchetti di produzione dovrebbero esaminare il documento giochi completi per i requisiti tecnici di Windows, poiché molti di questi requisiti sono interessati da questi strumenti.

### <a name="additional-recommendations"></a>Ulteriori indicazioni

Oltre ad assicurare che il componente supporti la creazione di titoli conformi ai requisiti per i giochi per Windows, è necessario tenere conto di alcune altre considerazioni durante la progettazione e la distribuzione di una libreria o di un'utilità di supporto per un gioco di Windows.

-   Per supportare gli sviluppatori che utilizzano applicazioni x64 native a 64 bit, fornire versioni native a 32 bit e 64 bit delle librerie. La versione a 32 bit deve essere compatibile con 64 bit per 2,2. Le librerie per le applicazioni a 32 bit non devono presupporre che il bit elevato di qualsiasi indirizzo a 32 bit non venga usato per supportare l'uso nelle applicazioni LARGEADDRESSAWARE x86.
-   Se si forniscono intestazioni di codice nativo (C/C++), usare la sintassi dell'attributo SAL (Standard Annotation Language) per decorare le routine API pubbliche. Ciò consentirà agli utenti della libreria di sfruttare al massimo i vantaggi derivanti dall'uso dell'analisi statica del codice (/Analyze), che fa parte di Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium e Visual Studio 2010 Ultimate, oltre agli strumenti del compilatore Windows SDK disponibili pubblicamente.
-   Se il prodotto crea thread all'interno del processo dell'utente, assicurarsi di assegnare un nome a ogni thread in modo che gli strumenti di debug possano annotare correttamente i thread in esecuzione.
-   Se si scrivono routine che devono essere chiamate all'interno di un ciclo principale del gioco, usare le routine D3DX D3DPERF \_ beginEvent/chiamata endEvent e D3DPERF \_ semarker per annotare le operazioni di alto livello per semplificare l'identificazione dei colli di bottiglia con Pix per Windows.
    > [!Note]  
    > Per la funzionalità di diagnostica grafica di Visual Studio 2012, le routine D3DX e PIX vengono sostituite dall'interfaccia [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) .

     

-   Per le librerie di rete, fornire implementazioni indipendenti da IP ed evitare routine solo IPv4 deprecate per supportare le tecnologie IPv6 e Teredo in Windows XP con Service Pack 2, Windows Vista e Windows 7.
-   I provider di servizi di gioco devono registrarsi con Game Explorer usando la versione 2 dello schema GDF e usare la funzionalità RSS per fornire notizie correlate ai servizi.

### <a name="games-for-windows-showcases"></a>Giochi per Windows showcases

### <a name="introduction"></a>Introduzione

Giochi per Windows Showcase oltre a offrire un'esperienza di gioco solida nei PC Windows. Implementando queste funzionalità, i giochi possono aggiungere più entusiasmo all'esperienza utente sulle piattaforme Windows più recenti.

I giochi per i titoli di Windows devono soddisfare tutti i requisiti tecnici elencati in questo articolo, ma le funzionalità Showcase sono facoltative. Questi titoli sono gratuiti per implementare alcuni, nessuno o tutti questi Showcase.

### <a name="s1-exploit-direct3d-11"></a>S. 1 exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Direct3D 11 è l'API di rendering di prossima generazione per Windows Vista e Windows 7. I giochi che sfruttano Direct3D 11 usano contenuto ottimizzato, tecniche di rendering avanzate e nuove funzionalità hardware per creare un'esperienza interessante su hardware che supporta 10, 10,1 e 11.

Se il gioco implementa anche Direct3D 9, un confronto affiancato dovrebbe dimostrare un miglioramento percettibile della qualità del contenuto, della fedeltà visiva, delle prestazioni, della complessità della scena e di altre aree di fedeltà grafica per Direct3D 11. Questo supporto è soggetto ai giochi per i requisiti tecnici di Windows 1,7.

La tecnologia Direct3D 10level9 può essere usata per supportare l'hardware video di Shader Model 2.0/3.0 Direct3D a 9 classi in Windows Vista e Windows 7, invece di usare un'implementazione affiancata di Direct3D 9 per un ampio supporto hardware. Tuttavia, questo non è sufficiente per dimostrare questa presentazione.

Nei computer che eseguono Windows Vista o Windows 7 con Direct3D 11 installato, per impostazione predefinita il gioco deve usare Direct3D 11.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'API Direct3D 11 si basa su Windows Display Driver Model (WDDM) e sull'infrastruttura Direct3D 10,1 per supportare nuove funzionalità: mosaico hardware, compute shader, rendering multithreading e creazione di risorse, nuovi formati di compressione di trama e un linguaggio shader più flessibile. Direct3D 11 fornisce il supporto hardware unificato per le schede video moderne, incluse le parti Direct3D 11 di ultima generazione, tutte le schede video Direct3D 10 e 10,1 e molte schede video Direct3D 9 di Shader Model 2.0/3.0, che è il minimo hardware video necessario per il desktop Aero 3D.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

La migrazione di un motore di rendering Direct3D 9 per l'utilizzo della nuova interfaccia Direct3D 11 è un'attività ben definita:

-   Eliminare tutte le operazioni a funzione fissa a favore degli shader programmabili.
-   Aggiornare tutti gli shader esistenti alla nuova sintassi del modello Shader 4. x/5.
-   Aggiornare Gestione risorse per supportare il nuovo modello di visualizzazione.
-   Convertire tutti gli asset in modo da usare un nuovo elenco di formati disponibili.
-   Aggiornare la gestione dello stato di rendering per usare blocchi di stato non modificabili e rielaborare le costanti dello shader in buffer costanti.

Questa conversione è essenziale per abilitare la vetrina Direct3D 11, sebbene il risultato non soddisfi i requisiti di presentazione per sfruttare la nuova API.

La nuova API e il modello di programmazione HLSL associato offrono molte opportunità per il contenuto migliorato:

-   Sfruttando le funzionalità hardware Direct3D 10 esistenti, ad esempio Geometry shader, Stream out, le matrici di trame e i formati di trama compressi BC4/BC5.
-   Sfruttando le funzionalità hardware Direct3D 10,1 esistenti, ad esempio le modalità di Blend per il rendering per singolo, il livello di lettura e la profondità MSAA, l'accesso allo shader per campione, le matrici della mappa del cubo e il rendering in formati con compressione a blocchi (BC).
-   Implementazione di algoritmi GPU avanzati con compute shader con CS4. x sulle schede video Direct3D 10/10.1 esistenti (abilitate dai driver video aggiornati) o CS 5,0 nelle schede video Direct3D 11 di prossima generazione.
-   Rendering su più thread mediante la creazione di risorse a thread libero e più contesti di dispositivo per migliorare le prestazioni nei sistemi multicore (con driver video aggiornati). Per ulteriori informazioni, vedere la pagina relativa ai giochi per Windows Showcase S. 3.
-   Utilizzo di nuove funzionalità dell'hardware video di Direct3D a 11 classi, ad esempio la suddivisione a mosaico hardware con Hull e Domain shader, il modello shader 5,0 HLSL shader features formati di trama BC6HBC7 e Dynamic shader collegamento.

Le tecniche che possono essere implementate con Direct3D 9 (in gran parte tramite un costo elevato della CPU) possono essere disattivate nella GPU in modo efficiente, liberando così risorse della CPU per supportare altre richieste di gioco.

Le API Direct3D 11, gli strumenti di supporto e gli esempi sono disponibili in DirectX SDK. Vedere anche API grafiche in Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 exploit x64 nativo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco include un file eseguibile nativo a 64 bit che offre una nuova esperienza interessante abilitata dalle edizioni x64 di Windows in esecuzione su hardware compatibile con x64. Un confronto affiancato con la versione a 32 bit del gioco dovrebbe mostrare un miglioramento percettibile della complessità del contenuto, riducendo i tempi di caricamento complessivi e le prestazioni.

Nelle edizioni di Windows a 64 bit, l'installazione deve sempre configurare la versione nativa del gioco a 64 bit come impostazione predefinita per i collegamenti in Games Explorer e Windows XP Professional x64 Edition. Se si desidera eseguire l'installazione doppia, è possibile specificare un'attività di riproduzione aggiuntiva per Game Explorer in Windows Vista e Windows 7 che punta alla versione a 32 bit, ma il valore predefinito deve rimanere la versione nativa a 64 bit.

Si noti che il gioco deve supportare le edizioni a 64 bit di Windows Vista e Windows 7 per soddisfare questa raccomandazione di presentazione. Il supporto per Windows XP Professional x64 Edition è consigliato, ma non obbligatorio.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

la tecnologia x64 offre funzionalità di indirizzamento a 64 bit sia per i mercati consumer che per i mercati server che includono compatibilità con le versioni precedenti a 32 bit per le applicazioni esistenti. x64 è una parte essenziale della roadmap per AMD (AMD64) e Intel (EMT64) e, fatta eccezione per le CPU ultra-mobili, supporta la tecnologia per tutti i processori di generazione correnti e futuri.

Windows XP Professional x64 Edition era il primo sistema operativo Windows orientato ai consumatori a supportare la tecnologia x64 e Windows Vista e Windows 7 ampliano in modo sostanziale la disponibilità dell'abilitazione del sistema operativo per l'elaborazione di consumer a 64 bit. Con 2 GB di RAM come standard in molti nuovi computer, i miglioramenti apportati alla scalabilità della memoria non trarranno vantaggio dalle singole applicazioni a 32 bit che non sono in grado di gestire più di 2 GB di RAM fisica. Molti giochi attuali affrontano le difficoltà che consentono di adattare tutto il contenuto disponibile ai vincoli di 2 GB di spazio degli indirizzi virtuali, specialmente quando vengono combinati con le grandi memorie video disponibili sulle GPU di fascia alta e il passaggio alla tecnologia x64 aumenta significativamente i livelli di dettaglio supportati.

la compatibilità x64 per i giochi a 32 bit è un requisito tecnico per Windows (2,2), ma per sfruttare appieno le nuove tecnologie è necessaria un'implementazione nativa a 64 bit.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Il vantaggio principale dell'indirizzamento a 64 bit è la possibilità di accedere direttamente a più di 2 GB di memoria fisica e virtuale. Lo spazio degli indirizzi della memoria virtuale di grandi dimensioni consente un uso estensivo dell'I/O mappato alla memoria senza preoccupazioni per i problemi di esaurimento dello spazio degli indirizzi della macchina virtuale prevalentemente nella programmazione a 32 bit. I giochi possono sfruttare il nuovo spazio per migliorare significativamente i tempi di caricamento o, in alcuni casi, per eliminare le pause per il caricamento del contenuto.

Le applicazioni a 32 bit esistenti possono trarre vantaggio dalle edizioni x64 grazie alla possibilità di elaborare gli indirizzi con dati 32 bit completi quando vengono compilati con l'opzione del linker Abilita indirizzi di grandi dimensioni (**/LARGEADDRESSAWARE**). Nelle versioni a 32 bit di Windows XP, le modalità di avvio speciali hanno consentito a tali applicazioni di soddisfare fino a 3 GB di RAM e le edizioni x64 forniscono accesso fino a 4 GB di RAM per le app di tipo large address Aware (LAA). Sebbene l'uso di LAA in un'applicazione a 32 bit non soddisfi i requisiti di questo Showcase, questa tecnologia Bridge è un modo estremamente utile per offrire vantaggi di scalabilità aggiuntivi nelle versioni x64 di Windows per coloro che non implementano completamente questo requisito di presentazione.

Per ulteriori informazioni, vedere [la pagina relativa alla programmazione a 64 bit per sviluppatori di giochi](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) e [RAM, VRAM e altre RAM: il gioco a 64 bit è](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) disponibile in Gamasutra.

> [!Note]  
> Una sfida fondamentale per questa presentazione è la garanzia che tutti i componenti o le librerie di terze parti su cui si basa il gioco siano disponibili per lo sviluppo nativo a 64 bit. Molte API Microsoft legacy sono state anche eliminate dall'ambiente nativo a 64 bit, che può dimostrare una sfida per le basi di codice del motore che contengono implementazioni precedenti dei sistemi principali.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 Many-Core processori exploit

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco implementa funzionalità che sfruttano i processori multicore, ridimensionando a 3, 4 o più core, quando disponibili.

Se il gioco supporta sistemi a processore singolo o dual core, un confronto affiancato con un sistema quad-core dovrebbe illustrare nuove funzionalità percettibili, effetti interessanti aggiuntivi, miglioramento della qualità del contenuto e/o miglioramento delle prestazioni.

Poiché il ridimensionamento Dual Core è già ampiamente supportato dai giochi, nonché usato automaticamente da diversi miglioramenti del driver Direct3D, la scalabilità Dual Core non è sufficiente per dimostrare questa presentazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

La continua crescita delle prestazioni per le CPU è cambiata dai miglioramenti della frequenza di clock all'aggiunta di core di calcolo. Le roadmap AMD e Intel sono basate su progettazioni multicore scalabili. Tutte le piattaforme di gioco di nuova generazione hanno CPU multicore a causa di questo cambiamento fondamentale nell'evoluzione dei processori. Le applicazioni a thread singolo non vedranno più significativi guadagni dalle CPU di nuova generazione. Anche il multithreading semplice non riuscirà a ridimensionarsi perché il numero di core CPU in uso comune cresce a tre o più.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Si noti che i conteggi di base non devono essere una potenza di due, quindi i giochi devono essere ridimensionati in modo lineare e gestire i conteggi dei core di 3, 4, 5, 6, 7, 8 e così via.

La scalabilità aumentando il numero di thread in un'applicazione fornisce solo un valore restituito se il costo di comunicazione e la sincronizzazione dei thread vengono mantenuti sotto controllo. La scalabilità basata sulle funzionalità può dimostrare una soluzione più semplice a breve termine, consentendo al gioco di funzionare normalmente senza i thread aggiuntivi nei sistemi single core e di abilitarli quando è disponibile la potenza di CPU aggiuntiva.

Per ulteriori informazioni, vedere la pagina relativa alla [codifica per più core in xbox 360 e Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) e [considerazioni sulla programmazione non bloccate per Xbox 360 e Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) negli articoli DirectX, nonché l'utilità DXUTLockFreePipe e l'esempio CoreDetection.

Usare la creazione di risorse con thread libero Direct3D 11 e i contesti di dispositivo sono utili per ottenere una scalabilità di molti core per il rendering e il caricamento di risorse grafiche. Vedere giochi per Windows Showcase S. 1.

Si noti che l'uso diretto dell'istruzione della CPU RDTSC, invece di usare le API di Windows per calcolare l'intervallo nei sistemi multicore, può causare problemi in alcune configurazioni hardware e del sistema operativo. vedere la pagina relativa alla [temporizzazione dei giochi e ai processori multicore](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) negli articoli DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S. 4 giochi di supporto per Windows-LIVE

Games for Windows-LIVE non è più supportato da Microsoft.

### <a name="s5-support-windows-touch"></a>S. 5 supporto per Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi compatibili con Windows Touch sono riproducibili mediante tocco e/o movimenti nei computer che eseguono Windows 7 con un tocco. È anche possibile usare l'input da tastiera, ma l'interfaccia di riproduzione primaria deve essere basata sul tocco.

L'abilitazione del tocco non deve impedire l'uso del mouse o del controller comune, in base ai requisiti tecnici 1,4.

Non è previsto che il programma di installazione del gioco supporti la funzionalità Windows Touch.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Le visualizzazioni con supporto multitocco per i computer sono disponibili per computer portatili e desktop e rappresentano una funzionalità hardware chiave da promuovere con il rilascio di Windows 7. Windows 7 supporta Windows Touch in tutto il desktop e le interfacce dei controlli comuni.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Le applicazioni con codice nativo possono accedere a più touch attraverso i \_ messaggi WM touch, in combinazione con la funzione [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) . Vedere anche le modifiche e l'API di inerzia.

Windows Presentation Foundation (WPF) 4,0 fornisce una soluzione gestita per le interfacce multitocco.

Per ulteriori informazioni, vedere Windows Touch SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S. 6 supporta il colore elevato

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi che supportano un colore elevato usano il formato 10:10:10:2 (DXGI \_ Format \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) o 16:16:16:16 (DXGI \_ Format \_ R16G16B16A16, D3DFMT A16B16G16R16 \_ ) per la modalità di visualizzazione a schermo intero e buffer di rendering.

Usando una destinazione di rendering a colore elevato, è possibile eseguire il rendering del contenuto di High-Dynamic Range (HDR) con una gamma estesa o ampia durante l'esecuzione del mapping dei toni a un intervallo a 10 bit o a 16 bit.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I monitoraggi sono stati in grado di visualizzare più di 256 livelli di colore per canale per molti anni, anche quando le visualizzazioni CRT erano prevalenti. L'hardware di analisi sulle schede video è stato il fattore di limitazione. Le GPU moderne, tra cui la maggior parte dei componenti hardware di Direct3D 9 e tutti i componenti hardware Direct3D 10 e di qualità superiore, hanno hardware di analisi che supportano almeno 10 bit per canale e la capacità hardware è impostata per l'aumento fino a 16 bit per canale di colore in futuro. I sistemi di interconnessione HD TV (HDMI, DisplayPort) sono stati progettati per gestire oltre 8 bit per canale e il VGA analogico porta già tali segnali.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Si noti che il colore alto, o il colore Hi, si riferisce storicamente al passaggio da un colore a 256 (8 bit) a una visualizzazione a 15 o a 16 bit. La maggior parte dei sistemi di visualizzazione è stata spostata su un colore reale a 24 bit o a 8 bit per canale di colore rosso, verde e blu. In base a un colore elevato, significa che una nuova generazione di Visualizza i sistemi che possono funzionare con più di 8 bit per singolo canale di colori. Viene anche definito colore profondo.

</dd> </dl>

### <a name="recommended-best-practices"></a>Procedure consigliate

### <a name="introduction"></a>Introduzione

Oltre a soddisfare i requisiti tecnici e ad adottare una o più Showcase nel titolo, è consigliabile seguire alcune procedure consigliate per tutti i giochi di Windows. Sebbene queste raccomandazioni non rientrino nell'ambito dei requisiti tecnici di base, si consiglia di impiegarle per tutti i giochi per i titoli di Windows.

### <a name="additional-recommendations"></a>Ulteriori indicazioni

-   Usare il compilatore e il runtime di Visual Studio più recenti. Le versioni più recenti del compilatore implementano miglioramenti significativi per la qualità del codice generato e per i problemi di sicurezza e utilizzano strategie di ottimizzazione del processore moderne. L'aggiornamento del compilatore e l'utilizzo della versione più recente del runtime C è un modo semplice per eseguire la migrazione alle moderne procedure di codifica.
-   Utilizzare la versione della libreria di collegamento dinamico (DLL) del runtime di C, anziché il collegamento statico, e utilizzare CRT protetto. (Le eccezioni possono essere eseguite in casi speciali di pre-installazione, ad esempio per un programma di Autorun o per il programma di installazione stesso).
-   Per l'audio del gioco, usare XAudio2, X3DAudio e/o XACT, anziché DirectSound. Per i motori audio che eseguono tutte le operazioni di combinazione e conversione della frequenza del codice sorgente e necessitano solo di una soluzione a bassa latenza per l'output audio, utilizzare DirectSound in Windows XP (solo) e WASAPI in Windows Vista e Windows 7.
-   Evitare di usare le API legacy e deprecate: DirectDraw, DirectSound, DirectPlay, il livello di prestazioni di DirectMusic, la voce di DirectPlay e la modalità di conservazione di Direct3D. Si noti che DirectPlay Voice e la modalità mantenuta di Direct3D non sono disponibili in Windows Vista o Windows 7. Il livello di prestazioni di DirectPlay e DirectMusic non è disponibile per le applicazioni x64 native.
-   Ottimizzare l'uso di set di istruzioni SIMD SSE/SSE2. Vedere l'API [DirectXMath](/windows/desktop/dxmath/directxmath-portal) nel Windows SDK come soluzione multipiattaforma per operazioni matematiche ottimizzate per SIMD.
-   Usare le procedure consigliate moderne per la sicurezza di Windows (incluse le opzioni del compilatore e del linker come **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DynamicBase**, **/SDL** e così via). Per altre informazioni, vedere procedure consigliate per la [sicurezza nello sviluppo di giochi](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Usare i componenti e le librerie di Windows SDK più recenti. Rimuovere le dipendenze dai componenti legacy DirectSetup distribuiti fuori banda, ad esempio D3DX9, D3DX10 e D3DX11. Provare a usare [DirectXTex](https://github.com/Microsoft/DirectXTex) o [DirectXTK](https://github.com/Microsoft/DirectXTK) o entrambi.
-   Evitare di usare il compilatore HLSL precedente e usare invece il compilatore HLSL moderno. Se per l'applicazione è richiesto il supporto per pixel shader 1. x, usare l'assembly dello shader anziché HLSL oppure limitare l'uso del compilatore precedente solo a questi scenari.

## <a name="resources"></a>Risorse



| Termine                                                                                                                                                                                                                         | Descrizione                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Giochi per Windows: test case <br/>                              | Procedure consigliate per i giochi in Windows XP, Windows Vista e Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [SDK di Windows](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Linee guida per il controllo dell'account utente <br/>                      | [Requisiti per lo sviluppo di applicazioni Windows Vista per la compatibilità con controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portale per sviluppatori WinQual <br/>                                                  | [Servizi online di qualità Windows (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>Portale per sviluppatori DirectX <br/>                                                  | [Centro per sviluppatori DirectX](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog sui giochi per Windows e DirectX SDK<br/> | [Giochi per Windows e DirectX SDK](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli su DirectX<br/>                                             | [Articoli tecnici su DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

