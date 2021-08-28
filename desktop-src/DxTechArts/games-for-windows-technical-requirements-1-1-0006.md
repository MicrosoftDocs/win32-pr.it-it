---
title: 'Requisiti tecnici dei giochi di Windows: procedure consigliate per giochi su Windows XP, Windows Vista, Windows 7 e Windows 8'
description: Questo articolo fornisce i requisiti tecnici e le procedure consigliate per i giochi eseguiti in Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0723c5da09d011111b0064ef689025d7ddcac85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887061"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Giochi per Windows tecnici: procedure consigliate per i giochi in Windows XP, Windows Vista, Windows 7 e Windows 8

Questo articolo fornisce i requisiti tecnici e le procedure consigliate per i giochi eseguiti in Windows. Questi requisiti tecnici e procedure consigliate sono stati scritti principalmente per Windows Vista e Windows 7, nonché per il sistema operativo Windows XP legacy. Queste procedure consigliate si applicano in genere anche ai giochi Win32 desktop Windows 8.

Questo articolo contiene le sezioni seguenti:

-   [Differenze per Windows 8](#differences-for-windows-8)
    -   [Informazioni aggiuntive](#additional-information)
-   [Giochi per Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [1.1 Integrazione Games Explorer](#11-games-explorer-integration)
    -   [1.2 Supporto Family Safety/Controllo genitori](/windows)
    -   [1.3 Supporto di giochi salvati con funzionalità rich](#13-support-rich-saved-games)
    -   [1.4 Supportare il Xbox 360 Common Controller per Windows \[ requisito condizionale\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1.5 Supporto di più proporzioni e risoluzioni](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1.6 Avvio del supporto da Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [1.7 Supporto Direct3D](#17-direct3d-support)
    -   [1.8 Abilitare il supporto per DPI elevato](#18-enable-high-dpi-aware)
-   [Sicurezza e compatibilità](#security-and-compatibility)
    -   [2.1 Seguire le linee guida per il controllo dell'account utente](#21-follow-user-account-control-guidelines)
    -   [2.2 Supporto delle Windows x64](#22-support-windows-x64-versions)
    -   [2.3 Firmare i file](#23-sign-files)
    -   [2.4 Driver di firma](#24-sign-drivers)
    -   [2.5 Eseguire il controllo della versione corretto](#25-perform-proper-version-checking)
    -   [2.6 Supporto di sessioni utente simultanee](#26-support-concurrent-user-sessions)
    -   [2.7 Supporto dei nomi lunghi](#27-support-long-names)
-   [Installazione](#32-support-user-account-control-for-installation)
    -   [3.1 Supporto dell'installazione semplice](#31-support-easy-installation)
    -   [3.2 Supporto del controllo dell'account utente per l'installazione](#32-support-user-account-control-for-installation)
    -   [3.3 Eseguire l'installazione in cartelle corrette](#33-install-to-correct-folders)
    -   [3.4 Installare correttamente Windows risorse](#34-install-windows-resources-properly)
    -   [3.5 Evitare riavvii durante l'installazione](#35-avoid-reboots-during-installation)
    -   [3.6 Usare correttamente il controllo delle versioni dei file](#36-use-file-versioning-correctly)
    -   [3.7 Supporto del requisito condizionale di esecuzione \[ automatica\]](#37-support-autorun-conditional-requirement)
-   [Affidabilità](#reliability)
    -   [4.1 Eliminare i riavvii non necessari](#41-eliminate-unnecessary-reboots)
    -   [4.2 Eliminare Application Verifier errori](#42-eliminate-application-verifier-failures)
    -   [4.3 Supporto delle Segnalazione errori Windows e delle versioni dei file](#43-support-windows-error-reporting-and-file-version-information)
-   [Xbox 360 Common Controller per Windows terminologia](#xbox-360-common-controller-for-windows-terminology)
-   [Linee guida per i prodotti middleware di gioco](#guidelines-for-game-middleware-products)
    -   [Introduzione](#introduction)
    -   [Altre Consigli](#additional-recommendations)
    -   [Giochi per Windows Showcase](#games-for-windows-showcases)
-   [Risorse](#resources)

## <a name="differences-for-windows-8"></a>Differenze per Windows 8

Ecco un riepilogo delle differenze principali quando si applicano questi requisiti tecnici e procedure consigliate Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**L Games Explorer'interfaccia utente non è visibile**
</dt> <dd>

Tutti i giochi registrati [](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) con il Games Explorer vengono eretto come riquadri nella nuova interfaccia utente di Windows, ma gran parte dei metadati associati al titolo non è più visibile. Si usa ancora lo strumento Games Definition File Maker (GDFMAKER.EXE), ora disponibile in Windows Software Development Kit (SDK), per creare i metadati. Si usano anche i meccanismi esistenti per la distribuzione dei metadati. Continuare a testare la registrazione Games Explorer usando Windows 7 e verificare che il nuovo riquadro dell'interfaccia utente di Windows sia visualizzato quando lo si installa in Windows 8 (vedere [1.1 Games Explorer Integration).](#11-games-explorer-integration)

Per scaricare l'SDK Windows 8, vedere [Download per lo sviluppo di app desktop.](https://msdn.microsoft.com/windows/desktop/aa904949)

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**La registrazione con le API di Game Explorer continua a essere il meccanismo per registrare il gioco Windows Controllo genitori**
</dt> <dd>

È consigliabile eseguire la versione Windows SDK di GDFMAKER nella versione rilasciata di Windows 8 per assicurarsi che possa popolare tutti i sistemi di classificazione attualmente supportati.

> [!Note]  
> Questa versione di GDFMAKER richiede .NET 4.0.

 

Vedere [1.2 Supporto Family Safety/Controllo genitori](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Sono ora disponibili tre opzioni per l'uso dell'API XINPUT a seconda dei requisiti**
</dt> <dd>

XINPUT 1.4 è integrato in Windows 8. Sia Windows app di Store che app Win32 desktop possono usare XINPUT 1.4. Tutte le versioni di Windows possono usare XINPUT 9.1.0 per i controller comuni semplificati, ma non esiste alcun pacchetto di ridistribuzione con XINPUT 9.1.0. Tutte le versioni Windows possono anche usare la versione XINPUT 1.3 di DirectX SDK esistente, che richiede la distribuzione di DirectSetup.

Vedere [1.4 Support the Xbox 360 Common Controller per Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Solo un set limitato di app Win32 desktop è supportato Windows RT**
</dt> <dd>

I giochi eseguiti Windows 7 possono e devono essere eseguiti correttamente Windows 8 nelle piattaforme x86 e x64.

Vedere [2.2 Supporto Windows versioni x64](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Verificare che i controlli del sistema operativo vengano eseguiti correttamente**
</dt> <dd>

La Windows 8 del sistema operativo è 6.2. Windows 8 i test a barre minimi correnti consigliati per la distribuzione del gioco.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Il pacchetto DirectX End-User Redistribution viene eseguito correttamente in Windows 8, come in Windows 7, per distribuire D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine e così via**
</dt> <dd>

Tuttavia, esiste un problema noto con DirectSetup nei sistemi in cui è installato solo .NET 4.0 a causa della gestione della distribuzione degli assembly DirectX 1.1 gestiti legacy. Questo problema si applica Windows 8, che viene fornito con .NET 4.5 per impostazione predefinita, e ai nuovi computer Windows XP in cui è installato il runtime di .NET 4.0. Ma questo problema non si applica a nessuna versione di .NET precedente a .NET 4.0. Anche se Windows 8 ha un comportamento di compatibilità delle applicazioni per risolvere automaticamente questo problema (che richiede l'accesso alla rete), è consigliabile che i giochi che continuano a distribuire l'aggiornamento DirectSetup nella versione aggiornata di DirectX SDK (giugno 2010) dei file REDIST. Come sempre, se si usa DirectSetup per il titolo, ridurre il titolo al set minimo richiesto di CAB.

Vedere [3.4 Installare Windows risorse correttamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**I giochi che richiedono il runtime compatibile con .NET 2.0 (2.0, 3.0, 3.5) continuano a usare i meccanismi di distribuzione esistenti**
</dt> <dd>

Questi giochi attivano un comportamento di compatibilità Windows 8 per abilitare automaticamente il runtime .NET 3.5 (che richiede l'accesso alla rete). Tuttavia, è consigliabile che gli sviluppatori .NET si spostino nel runtime .NET 4.0.

> [!Note]  
> Gli assembly DirectX 1.1 gestiti legacy non sono compatibili con il runtime .NET 4.x.

 

Vedere [3.4 Installare Windows risorse correttamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Non è consigliabile usare una funzionalità di esecuzione automatica o un'altra tecnologia di preinstallazione basata su .NET**
</dt> <dd>

È possibile presupporre che in Windows Vista e Windows 7 siano presenti solo runtime compatibili con .NET 2.0 (2.0, 3.0, 3.5). Solo il runtime compatibile con .NET 4.0 è presente Windows 8 per impostazione predefinita.

Vedere [3.7 Support Autorun (Esecuzione automatica del supporto 3.7).](#37-support-autorun-conditional-requirement)

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**È disponibile un aggiornamento Application Verifier per Windows 8**
</dt> <dd>

L Windows 8 SDK include questo aggiornamento Application Verifier.

Vedere [4.2 Eliminare Application Verifier errori .](#42-eliminate-application-verifier-failures)

</dd> </dl>

### <a name="additional-information"></a>Informazioni aggiuntive

<dl>

[Windows 8 e Windows Server 2012 di compatibilità](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Dov'è DirectX SDK?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Giochi per Windows

**Riepilogo dei requisiti dei giochi**

**Vantaggi per i clienti**

I giochi per computer sono un'esperienza di intrattenimento chiave Windows, ma i problemi di facilità d'uso hanno causato la frustrazione dei clienti nel corso degli anni. Tradizionalmente, i giochi vengono installati come le applicazioni, ma vengono usati più come supporti di intrattenimento (film o brani musicali, ad esempio). Le innovazioni, ad esempio Games Explorer, espongono i giochi in modo coerente, diverso dalle applicazioni standard. Queste innovazioni offrono anche ai giochi lo stato di primo livello dei Windows, insieme a Musica e Pictures. I requisiti seguenti garantiscono che Windows Vista e Windows 7 forniranno un'esperienza di gioco migliorata, più accessibile e unificata. Allo stesso tempo, garantiscono la compatibilità con Windows XP.

### <a name="11-games-explorer-integration"></a>1.1 Integrazione Games Explorer

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco deve essere visibile all'interno Games Explorer (cartella **Giochi)** in Windows Vista e Windows 7. Quando questa opzione è selezionata, il gioco deve anche visualizzare i metadati corretti, inclusi editore, sviluppatore, data di rilascio, versione, punteggi dell'indice dell'esperienza Windows, classificazione (se applicabile) e collegamenti ipertestuali associati.

Se il gioco viene distribuito digitalmente tramite un servizio di gioco online, anche il provider di servizi dovrebbe essere visualizzato in Games Explorer. Per garantire una corretta gestione del provider e abilitare l'uso di feed RSS, è necessario usare la versione 2 dello schema per i file di definizione del gioco (GDF). Per altre informazioni sui file GDF, vedere Informazioni aggiuntive.

Inoltre, i programmi di installazione dei giochi devono osservare le regole seguenti quando vengono eseguiti Windows Vista e Windows 7:

-   L'installazione non deve creare un collegamento per avviare il gioco sul desktop, nel menu Start o in qualsiasi altra posizione.
-   Non è necessario creare attività e collegamenti per la rimozione.
-   Gli utenti devono essere in grado di rimuovere il gioco usando Programmi e funzionalità in Pannello di controllo in Windows Vista e Windows 7 o Installazione applicazioni in Pannello di controllo in Windows XP.

In Windows XP e nelle versioni precedenti di Windows, il programma di installazione del gioco è gratuito per creare gruppi di programmi, icone del desktop o collegamenti in base alle esigenze.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Windows Games Explorer concetto è simile a quello delle cartelle Windows XP **Documenti** **o Immagini** personali . L'idea è quella di centralizzare contenuti simili in un'unica posizione e di semplificare l'organizzazione e le attività sensibili al contesto. Games Explorer estende il concetto **Documenti** **o Immagini** personali consentendo un'organizzazione e un controllo più completo sui giochi. Games Explorer consente ai giocatori di visualizzare, organizzare e interagire con tutti i giochi installati nei propri sistemi. Consente anche agli editori di giochi di comunicare informazioni importanti sui giochi in modo più efficace. Il sistema è basato sui dati, rendendo più semplice per un editore di giochi aggiornare le informazioni sui giochi nel corso della durata del prodotto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

L'integrazione con Games Explorer richiede la creazione di un file di definizione del gioco (GDF), ovvero un file di testo XML incorporato in un file binario (un file eseguibile o una DLL) come risorsa, insieme a un'icona Windows. Il gioco deve quindi essere registrato con Games Explorer. La funzione GDF consente anche l'esposizione di informazioni fornite, ad esempio titolo del gioco, editore, sviluppatore, collegamenti a siti Web e attività facoltative. Si noti che le attività di supporto possono essere solo collegamenti a siti Web, ma le attività di riproduzione possono essere usate anche per attività di supporto facoltative.

Games Explorer possibile usare un'immagine bitmap di anteprima, ma è consigliabile fornire una risorsa icona Windows con icone grandi (256 256). La risorsa icona deve includere dimensioni di immagine di 256 256 48 48, 32 32 e 16 16 in profondità di colore a 24 bit (True Color) e a 8 bit (256). L'editor di icone fornito Visual Studio 2008 e 2010 supporta questi formati di icone di grandi dimensioni, così come IconWorkshop Lite.

Informazioni dettagliate **sull'integrazione con Windows Games Explorer** sono disponibili in DirectX SDK. DirectX SDK include un editor del file di definizione del gioco (GDF), nonché un esempio di GDF incluso in GDFExampleBinary, un esempio. Un altro esempio, GameUxInstallHelper, fornisce routine per l'integrazione delle funzionalità necessarie nei sistemi di installazione esistenti. Game Definition File Validator (gdftrace.exe) fornisce il supporto per il debug per la valutazione di una funzione definita dall'utente. Vedere anche "Windows Games Explorer Integration" nella documentazione di DirectX SDK per C++.

Windows 7 introduce il supporto per la seconda versione di uno schema per i file GDF. La nuova versione include un metodo semplificato per la creazione di attività di riproduzione e il supporto per le notifiche di aggiornamento, i provider di servizi di gioco, le statistiche dei giochi e i feed RSS per i provider di servizi di gioco. La versione più recente di GameUxInstallHelper gestisce tutto il supporto legacy e di registrazione necessario per usare un file GDF versione 2 con Windows Vista. Usare gli strumenti e il codice di esempio di DirectX SDK di agosto 2009 o versione successiva. È consigliabile usare un file GDF versione 2 per abilitare il supporto per feed RSS, statistiche del gioco e notifiche di aggiornamento. Vedere anche gli esempi ProviderGDFExampleBinary e GameStatisticsExample.

In Windows Vista Business Edition, Windows 7 Professional Edition e edizione Enterprise di Windows Vista e Windows 7, il collegamento Giochi nel menu Start è nascosto. Games Explorer è ancora disponibile nel menu Start facendo clic su **Tutti** i programmi e quindi su **Giochi**.

Per le applicazioni associate installate con il gioco, ma non i giochi stessi, è possibile creare gruppi di programmi, collegamenti e icone del desktop menu Start in tutte le versioni di Windows, tra cui Windows Vista e Windows 7. Tali applicazioni associate devono superare i giochi applicabili per Windows requisiti; Per informazioni dettagliate, vedere [Linee guida per i prodotti middleware di gioco.](#guidelines-for-game-middleware-products) I servizi di gioco sono invitati a registrarsi Games Explorer come provider di giochi per Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 Supporto Family Safety/Controllo genitori

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi devono supportare Windows Family Safety rispettando le regole seguenti:

-   I giochi non devono richiedere che l'utente abbia credenziali amministrative per la riproduzione. L'installazione, l'applicazione di patch e la rimozione possono richiedere credenziali amministrative, in base ai requisiti della sezione 3. In relazione a questo requisito 2.1, seguire le linee guida per il controllo dell'account utente.
-   I giochi classificati da Windows classificazioni supportate, ad esempio ESRB e PEGI, devono includere le informazioni sulle classificazioni assegnate nel file di definizione del gioco (GDF). Tutti i dati delle classificazioni disponibili devono essere inclusi in ogni versione localizzata della funzione definita dall'utente, nonché nella versione indipendente dalla lingua.
-   I giochi devono elencare i file eseguibili nella funzione definita dall'utente per offrire un'esperienza utente ottimale per le restrizioni generali delle applicazioni, a meno che il gioco non usi una tecnologia antipirateria che crea file eseguibili denominati in modo casuale in fase di esecuzione.
-   I giochi devono chiamare il **metodo VerifyAccess** dell'interfaccia Games Explorer durante l'avvio, se disponibile, e uscire se restituisce \* pfHasAccess come FALSE.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Tutti i giochi devono essere eseguiti nel contesto di un account utente Standard per consentire agli account controllati Windows Controllo genitori di eseguire il gioco. I genitori vogliono la possibilità di monitorare e controllare l'accesso dei figli ai giochi. Inoltre, numerosi gruppi di settore, enti pubblici e di difesa desiderano modi migliori per consentire ai genitori di monitorare e controllare i giochi a cui sono esposti i figli. In combinazione con l'architettura offerta da Games Explorer, Microsoft offre ai genitori questa possibilità Windows Controllo genitori.

Anche per i giochi che non partecipano a un programma della bacheca delle classificazioni, la necessità di privilegi elevati crea un'esperienza di gioco scadente per la maggior parte degli account utente. Questo è in particolare il caso in cui è abilitato Controllo genitori, che richiederebbe all'elemento padre di immettere la password dell'amministratore ogni volta che viene avviato il gioco.

Il Windows controllo genitori consente agli elementi padre di selezionare le classificazioni che ritengono appropriate per i figli. Controllo genitori supporta molti dei sistemi di classificazione in tutto il mondo. Controllo genitori consente inoltre agli elementi padre di limitare l'accesso ai giochi in base ai descrittori di contenuto (se supportati dal sistema di classificazione applicabile) e di consentire o impedire l'accesso ai singoli giochi.

La scelta predefinita del sistema di classificazione Windows Controllo genitori è basata sulle impostazioni locali del sistema, ma può essere modificata dall'utente **in** Opzioni internazionali e della lingua in **Pannello di controllo**. Pertanto, ogni lingua supportata deve fornire tutti i dati delle classificazioni disponibili in modo che l'utente abbia la libertà di selezionare qualsiasi scheda di classificazione desiderata.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi senza classificazione devono comunque soddisfare i requisiti per supportare il gioco come utente Standard e chiamare **VerifyAccess**. Per impostazione predefinita, tali giochi sono la categoria Non classificati, visualizzano il testo  "Nessuna classificazione fornita" in Games Explorer e sono soggetti all'impostazione Restrizioni di gioco in **Controllo** genitori per i giochi non classificati. **L'impostazione predefinita Restrizioni** è Consenti.

Le informazioni di classificazione nella funzione definita dall'utente verranno ignorate se il file binario contenitore non è firmato correttamente con Authenticode. Vedere il requisito 2.3.

L'Editor file di definizione del gioco in DirectX SDK include tutti i sistemi di classificazione supportati e replica correttamente queste informazioni in tutte le versioni localizzate della funzione definita dall'utente, nonché in una versione indipendente dalla lingua. Lo strumento GDFTrace decodifica e verifica tutte le informazioni sulle classificazioni presenti. Usare la versione di agosto 2009 o successiva di questi strumenti.

La funzione GDF per un provider di giochi in genere non contiene informazioni sulla classificazione ed è soggetta alle impostazioni per il contenuto non classificato.




| Sistema operativo | Sistemi di classificazione supportati | 
|------------------|--------------------------|
| Windows Vista | <ul><li>CERO (Giappone)</li><li>ESRB (USA)</li><li>OFLC (Australia)</li><li>PEGI (Europa)</li><li>PEGI (deprecato)</li><li>PEGI Portogallo</li><li>PEGI/BBFC (Regno Unito)</li><li>USK (Germania)</li></ul> | 
| Windows Vista con un Service Pack | I Service Pack per Windows Vista aggiungono il supporto per gli elementi seguenti:<br /><ul><li>GRB (Corea del Sud)</li><li>Descrittori di contenuto delle varianti ESRB "Lievi"</li></ul> | 
| Windows 7 | Windows 7 supporta i sistemi di classificazione supportati da Windows Vista e aggiunge il supporto per gli elementi seguenti: <br /><ul><li>CSRR (Taiwan)</li></ul> | 
| Windows 8 | Windows 8 supporta i sistemi di classificazione precedenti e aggiunge il supporto per gli elementi seguenti:<br /><ul><li>COB-AU (Australia)</li><li>DJCTQ (Brasile)</li><li>PFB (Sudafrica)</li><li>OFLC-NZ (Nuova Zelanda)</li></ul>Windows 8 ritira il supporto per i sistemi ora deprecati seguenti:<br /><ul><li>PEGI-FI (Portogallo)</li><li>OFLC (Australia)</li></ul> | 




 

> [!Note]  
> Qualsiasi titolo che include i nuovi descrittori di contenuto di ESRB Windows Vista Service Pack 1 (SP1) verrà visualizzato come Senzarate in Windows Vista senza Service Pack.

 

I dati delle classificazioni più recenti vengono ignorati nelle versioni dei sistemi operativi senza supporto. La variante PEGI (Norvegia) è ora deprecata a favore del sistema di classificazione STANDARD PEGI (Europa). Il sistema OFLC è ora deprecato a favore di COB-AU per l'Australia.

Per altre informazioni su come rendere un gioco compatibile con i privilegi utente standard, vedere l'articolo di DirectX [Controllo dell'account utente per sviluppatori di giochi.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

Vedere il requisito 1.1 per altri dettagli sul file di definizione del gioco (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 Supportare giochi salvati con contenuto rtf

\[Questo requisito è stato ritirato\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Supportare il controller comune Xbox 360 per il Windows \[ condizionale\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi che supportano i controller del game pad devono supportare controller Xbox 360 per Windows l'API [XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal) Se sono supportate anche periferiche DirectInput, è possibile usare anche DirectInput. Tuttavia, XInput deve essere l'API predefinita se viene Xbox 360 un dispositivo compatibile.

Tutti i riferimenti ai trigger e ai pulsanti del controller comuni devono usare Xbox 360 nomi. Per informazioni [dettagliate, Xbox 360 l'elenco](#xbox-360-common-controller-for-windows-terminology) Windows terminologia comune.

La vibrazione del controller deve essere disattivata quando il gioco è in stato sospeso o sospeso.

Il controllo mouse/tastiera non può essere completamente disabilitato in qualsiasi momento. Come minimo, deve essere disponibile un'opzione per tornare ai menu di gioco.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Questo requisito offre ai giocatori la libertà di scegliere se usare il controller Xbox 360 o la tastiera e il mouse, a seconda del metodo di input più naturale e intuitivo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Questo requisito non si applica ai giochi che usano solo il mouse e/o la tastiera.

È consigliabile che la navigazione nei menu sia implementata per usare i pulsanti del controller standard ampiamente accettati:

-   A - Accetta
-   B - Annulla
-   Start - Accetta o sospendi
-   Indietro - Annulla, indietro di una schermata o un livello di menu superiore

Per altre informazioni, vedere [XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal)

[L'argomento XInput e DirectInput](/windows/desktop/xinput/xinput-and-directinput) illustrano i problemi relativi all'uso di entrambe le API contemporaneamente.

È consigliabile non usare DirectInput per implementare i controlli della tastiera o del mouse. I controlli della tastiera e del mouse devono essere implementati solo Windows messaggi e API Win32. Per informazioni dettagliate su come ottenere informazioni sullo spostamento del mouse ad alta risoluzione senza usare DirectInput, vedere Sfruttare [High-Definition spostamento del mouse.](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 Supporto di più proporzioni e risoluzioni

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco deve supportare almeno le proporzioni seguenti e le risoluzioni dello schermo associate:

-   Normale 4:3 (800 600 o 1024 768)
-   Widescreen 16:9 (1280 720)
-   Widescreen 16:10 (1152 720 o 1680 1050 o 800 480)

Per la configurazione e il rilevamento della risoluzione dello schermo, il gioco deve rispettare le regole seguenti:

-   Il gioco usa la risoluzione desktop del dispositivo di visualizzazione per impostazione predefinita, se è una risoluzione supportata. Le proporzioni del desktop devono essere usate come criterio di ricerca se il gioco sceglie una risoluzione predefinita diversa.
-   Il gioco deve richiedere all'utente di confermare le nuove impostazioni di visualizzazione quando viene apportata una modifica. Se l'utente non accetta entro 15 secondi, la visualizzazione deve ripristinare l'impostazione precedente.
-   Il gioco non deve estendere i pixel o centrare una finestra di rendering 4:3 per supportare le proporzioni widescreen. Tuttavia, il letterboxing è accettabile.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Con il Windows desktop 3D, non è possibile presunirsi proporzioni o risoluzioni particolari, a causa dei fattori seguenti:

-   Supporto per schermi con dettagli elevati.
-   Maggiore quota di mercato dei monitor widescreen.
-   Distribuzioni HDTV per Windows Media Center.
-   Requisiti di accessibilità.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Idealmente, per impostazione predefinita il gioco ha le proporzioni native dello schermo. Tuttavia, ottenere queste informazioni in modo affidabile può essere una sfida, quindi come soluzione più generale il gioco può presupporre che il desktop sia in esecuzione con le proporzioni native. La risoluzione desktop può essere ottenuta chiamando [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) con ENUM \_ REGISTRY \_ SETTINGS.

Per altri dettagli, vedere le sezioni Proporzioni e Widescreen dell'articolo di DirectX [Introduction to the 10-Foot Experience for Windows Game Developers](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 Supporto dell'avvio da Windows Media Center

\[Questo requisito è stato ritirato.\]

### <a name="17-direct3d-support"></a>1.7 Supporto Direct3D

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Se il gioco usa Direct3D, la versione minima supportata deve essere Direct3D 9 e Direct3D deve essere il renderer predefinito selezionato.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'Windows grafica di base Windows Vista e Windows 7 core è progettata per Direct3D. Direct3D 8 e versioni precedenti sono supportati tramite la modifica del mapping delle interfacce legacy.

È vivamente consigliato l'uso di versioni di Direct3D più recenti di Direct3D 9. Vedere Games for Windows Showcase S.1 (Giochi per Windows Showcase S.1). La richiesta di Direct3D 10 o Direct3D 11 è completamente conforme al requisito 1.7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 Abilitare il supporto per valori DPI elevati

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi e i relativi programmi di installazione devono essere eseguiti correttamente senza problemi visivi quando è abilitato il ridimensionamento DPI (Dots per Inch) (testato con 144 DPI per una scalabilità del 150% alla risoluzione dello schermo di 1600 1200) in Windows Vista e Windows 7.

Ciò richiede in genere che l'eseguibile del gioco dichiari di essere in grado di riconoscere DPI. Questa operazione viene eseguita incorporando un elemento manifesto: &lt; dpiAware &gt; true &lt; dpiAware &gt; .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I monitor LCD di alta qualità sono comuni come gli schermi dei computer e hanno un aspetto ottimale se sono guidati dalle risoluzioni native (in genere 1280 1024, 1600 1200 e così via). I clienti che hanno difficoltà a leggere il testo e visualizzare le immagini a questa risoluzione spesso impostano i desktop dei computer su una risoluzione inferiore e subiscono artefatti visivi dal ridimensionamento LCD. Al contrario, i clienti possono lasciare la risoluzione alle dimensioni native e modificare il valore DPI della visualizzazione Windows, rendendo più grande l'aspetto di elementi e testo senza compromettere la qualità dell'immagine.

Anche se questa funzionalità è disponibile in qualche modo Windows XP, raramente è abilitata dai clienti o dagli OEM. Attualmente più della metà di tutti gli schermi del computer è impostata su una risoluzione inferiore rispetto alla risoluzione nativa del monitor, in base ai commenti e suggerimenti dei clienti. Windows 7 rende questa funzionalità molto più visibile ai clienti durante la configurazione iniziale e quando si modificano le impostazioni di visualizzazione, incoraggiandoli a usare il ridimensionamento DPI invece di modificare la risoluzione del desktop.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

È invece possibile usare la funzione [**SetProcessDPIAware,**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) se chiamata all'inizio del codice di avvio del processo. È preferibile aggiungere al manifesto per assicurarsi che non siano presenti race conditions con elementi software (ad esempio DLL) che potrebbero essere inizializzati prima della chiamata al punto di ingresso principale. Si noti **che SetProcessDPIAware** è presente solo in Windows Vista e Windows 7.

L'aggiunta dell'elemento manifesto è facile da Visual Studio 2005 e 2008; creare un file denominato dpiaware.manifest contenente il testo seguente:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Quindi, all'Visual Studio, aggiungere dpiware.manifest al progetto. Assicurarsi che **l'opzione Incorpora** manifesto **sia impostata su Sì** nelle proprietà del progetto. Si noti che le versioni precedenti dello strumento manifesto (Mt.exe) genereranno un avviso non valido con gli elementi manifesto che sono in grado di riconoscere DPI. Per risolvere il problema, aggiornare Mt.exe alla versione più recente da Windows SDK.

Visual Studio 2010 include un'impostazione nelle proprietà del progetto, denominata Abilita riconoscimento **DPI,** che elimina la necessità di un file come dpiaware.manifest. Trovare **Abilita riconoscimento DPI** espandendo **Proprietà** di configurazione e **Strumento Manifesto** e quindi selezionando Input **& Output**.

In Windows, il valore predefinito della modalità di visualizzazione tradizionale è 96 DPI, che era comune per i monitor CRT.

Anche se le applicazioni a schermo intero modificano la risoluzione dello schermo, spesso usano i messaggi e le metriche delle finestre durante la configurazione di buffer e rettangoli di visualizzazione. La virtualizzazione DPI fa sì che queste modalità di visualizzazione a schermo intero vengano ritagliate e dichiarando che è in grado di riconoscere DPI si evitano questi problemi. Per altre informazioni, vedere [Writing DPI-Aware Win32 Applications](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Sicurezza e compatibilità

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi per i clienti**

I requisiti seguenti migliorano la sicurezza complessiva dei giochi e consentono di garantire che funzionino con Windows in architetture diverse, in configurazioni diverse e in modalità diverse.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Seguire le linee guida per il controllo dell'account utente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Ogni file eseguibile, ovvero ogni file con estensione .exe, deve contenere un manifesto incorporato che ne definisce il livello di esecuzione includendo il tag seguente:

``` syntax
            <requestedExecutionLevel>
```

Per requisito 1.2, il gioco principale e l'eseguibile di esecuzione automatica devono avere il livello di esecuzione asInvoker per supportare i contesti utente standard.

I file di dati utente con associazioni di file registrati con **Esplora file** devono essere inseriti in una sottocartella della cartella specificata da CSIDL PERSONAL (denominata anche Documenti \_ o **Documenti**).  Tutti gli altri file di dati utente devono essere archiviati in una sottocartella delle cartelle specificate da CSIDL \_ LOCAL \_ APPDATA o CSIDL \_ COMMON \_ APPDATA. Queste directory sono nascoste per impostazione predefinita per i singoli utenti e per tutti gli utenti.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'esperienza Windows utente è più sicura se le applicazioni vengono eseguite solo con le autorizzazioni necessarie.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Se solo alcune funzionalità di un'applicazione richiedono privilegi amministrativi(ad esempio, un'applicazione che deve configurare un firewall), il processo principale dell'applicazione deve comunque essere eseguito usando privilegi utente standard. Le funzionalità che richiedono privilegi amministrativi devono essere spostate in un processo separato, ad esempio un programma di installazione o un'utilità di configurazione.

Se non sono necessari privilegi amministrativi, il codice XML del manifesto incorporato deve includere quanto segue:

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

Se sono necessari privilegi amministrativi, il codice XML del manifesto incorporato deve includere quanto segue:

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

Con Visual Studio 2005 questa funzionalità è facilmente incorporabile semplicemente aggiungendo un file manifesto (con estensione manifest)  che contiene uno dei blocchi precedenti al progetto e verificando che Incorpora manifesto sia impostato su **Sì** nelle proprietà del progetto per lo strumento manifesto. Per Visual Studio 2008 e 2010, le proprietà del controllo dell'account utente possono essere impostate direttamente nelle proprietà del progetto per il linker nella pagina **File** manifesto. Si noti che le versioni precedenti dello strumento manifesto (Mt.exe) generano un avviso non valido con gli elementi manifesto del controllo dell'account utente. Per risolvere il problema, aggiornare Mt.exe alla versione più recente da Windows SDK.

Vedere il requisito 3.1 per informazioni dettagliate sui casi speciali di installazione, applicazione di patch e rimozione.

Le LIBRERIE (Dynamic Link Libraries) non richiedono manifesti di questo tipo.

Per altre informazioni sul controllo dell'account utente, vedere [Controllo dell'account utente per sviluppatori di giochi.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 Supporto delle Windows x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per mantenere la compatibilità con le edizioni a 64 bit Windows, i giochi devono soddisfare i requisiti seguenti.

-   I programmi di installazione di titoli e titoli non devono contenere codice a 16 bit o basarsi su componenti a 16 bit.
-   Se il gioco dipende dai driver in modalità kernel per il funzionamento, le versioni x64 di questi driver devono essere disponibili. La configurazione del gioco deve rilevare e installare i driver e i componenti appropriati per le edizioni a 64 bit di Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Molti utenti Windows Vista e Windows 7 eseguiranno edizioni a 64 bit del sistema operativo nel corso del ciclo di vita del prodotto, quindi è fondamentale che le applicazioni siano compatibili con questo sistema operativo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Windows in Windows 64 (WOW64) consente l'esecuzione di codice a 32 bit in edizioni a 64 bit di Windows, pertanto non è necessario che l'applicazione sia codice nativo a 64 bit nelle edizioni a 64 bit di Windows. Il codice a sedici bit non viene eseguito in edizioni a 64 bit di Windows.

La compatibilità con Windows XP Professional x64 Edition non è necessaria, ma è fortemente consigliabile.

Per informazioni dettagliate, vedere [Programmazione a 64 bit per sviluppatori di giochi](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Firmare i file

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Tutti i file di codice eseguibile (in genere i file con estensione .exe o .dll) devono essere firmati con un certificato Authenticode valido pubblicamente e devono avere un URL del server timestamp valido per la firma di produzione.

Se il gioco usa Windows installer, i file del pacchetto del programma di installazione (.msi file) devono essere firmati.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

La firma di un file consente agli utenti di decidere se considerare attendibile un'applicazione e garantisce agli utenti che i file non sono stati manomissionati. Consente inoltre alle applicazioni di essere eseguite correttamente in ambienti bloccati.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per informazioni dettagliate, vedere [Firma Authenticode per sviluppatori di giochi.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Se il gioco usa Windows installer, è consigliabile abilitare l'applicazione di patch UAC/LUA, includendo una tabella MsiPatchCertificate. Per altre informazioni, vedere [Controllo dell'account utente ( Controllo](/windows/desktop/Msi/user-account-control--uac--patching)dell'account utente) Applicazione di patch .

Non è consigliabile firmare file cab (.cab), a meno che non siano relativamente piccoli (meno di 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Driver di firma

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Qualsiasi driver in modalità kernel installato dal gioco deve essere firmato con un certificato Authenticode valido pubblicamente.

Qualsiasi driver di dispositivo hardware in modalità kernel installato dal gioco deve avere una firma Microsoft, che può essere ottenuta da Windows Hardware Quality Labs (WHQL) o dal programma Driver Reliability Signature (DRS).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I driver di malware o scritti in modo non corretti possono influire gravemente sulla stabilità e sulla sicurezza di un sistema. Nelle edizioni a 64 bit di Windows Vista e Windows 7, i driver non firmati non vengono caricati. Questo criterio può essere abilitato anche per le edizioni a 32 bit di Windows Vista e Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Entrambe le versioni native a 32 bit e a 64 bit di tutti i driver in modalità kernel sono necessarie per ogni requisito 2.2.

Altre informazioni sui programmi di firma dei driver Microsoft sono disponibili nel portale per sviluppatori [Windows hardware.](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Eseguire il controllo della versione corretto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi non devono essere eseguiti nei sistemi operativi futuri, come indicato dalle modifiche nel numero di versione Windows, a meno che il Contratto di licenza con l'utente finale non proibisca l'uso nei sistemi operativi futuri. Se si suppone che il gioco non riesca, deve farlo normalmente visualizzando un messaggio appropriato per l'utente.

Se Windows vengono eseguiti controlli di versione, è necessario usare le API di controllo della versione ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) [**o VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) per controllare la versione del sistema operativo. Le chiavi del Registro di sistema non devono essere lette per determinare la versione.

I controlli espliciti della versione per il runtime DirectX non devono essere presenti nel gioco. Questi controlli della versione non devono essere presenti nell'installazione che avvia l'installazione del runtime DirectX (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Quando Windows gli utenti aggiornano i sistemi operativi, non devono essere bloccati dalla riproduzione dei giochi correnti semplicemente perché il numero di Windows versione è aumentato. I controlli delle versioni scritti in modo non corretta continuano a creare problemi per il software che, in caso contrario, funziona correttamente nelle versioni più recenti di Windows o semplicemente con l'aggiunta di un Service Pack Windows.

La logica di confronto del controllo delle versioni per il runtime DirectX ha creato numerose installazioni non riuscite quando viene eseguito in versioni diverse Windows. Il numero di versione di DirectX si applica solo ai componenti principali del sistema operativo. Non si applica ai componenti di DirectX SDK side-by-side usati da molti giochi.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

È piuttosto comune vedere che i programmi di installazione verificano la presenza di una versione minima del sistema operativo. Questo controllo, tuttavia, deve essere eseguito con cautela per assicurarsi che il test sia maggiore o uguale a, anziché alla semplice uguaglianza, bloccando in tal modo una versione specifica del sistema operativo. L Application Verifier test **HighVersionLie** di Application Verifier è un modo rapido e semplice per determinare in che modo il programma di installazione reagirà a una modifica significativa del numero di versione del sistema operativo.

L'uso corretto del pacchetto di ridistribuzione del runtime DirectX (programma di installazione di DirectX) comporta sempre l'avvio durante l'installazione, preferibilmente in modalità invisibile all'utente. Ciò consente al codice fornito da Microsoft di eseguire gli aggiornamenti della versione necessari. Consente anche l'installazione di tutti i componenti facoltativi di DirectX SDK side-by-side, ad esempio D3DX, XACT, MDX o XInput.

Per le procedure consigliate per la distribuzione del runtime DirectX, vedere [Installazione di DirectX per sviluppatori di giochi](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

È consigliabile che i giochi che supportano Windows XP controllino la presenza di un livello di Service Pack 2 o superiore, perché Service Pack 2 (SP2) e Service Pack 3 (SP3) offrono miglioramenti significativi della sicurezza, un requisito di ridistribuzione del runtime DirectX semplificato e una distribuzione estremamente ampia. La maggior parte delle tecnologie Microsoft moderne che supportano Windows XP richiede SP2 o SP3 (XAudio2, Games for Windows - LIVE e così via).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Supporto di sessioni utente simultanee

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi che si basano sulla grafica 3D non devono funzionare su una connessione desktop remoto, ma l'utente deve essere avvisato quando il gioco ha esito negativo.

I giochi devono supportare Windows multitasking standard rispettando le regole seguenti:

-   I giochi non devono bloccare l'uso di sessioni utente simultanee.
-   Un gioco deve essere eseguito in una nuova sessione utente quando è già in esecuzione in un'altra sessione.
-   Il suono del gioco in una sessione utente non deve essere ascoltato quando un altro utente è attivo in una sessione diversa.
-   I giochi devono supportare il cambio rapido utente.
-   I giochi non devono tentare di disabilitare il cambio di attività standard. I giochi non devono disabilitare il tasto di scelta rapida ALT+TAB. I giochi sono autorizzati a disabilitare i tasti di scelta rapida per l'accessibilità, come descritto in [Disabilitazione dei tasti di scelta rapida in Giochi](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Windows utenti devono essere in grado di eseguire sessioni simultanee senza conflitti o interruzioni. Si tratta di uno scenario comune per un computer Windows condiviso da una famiglia, da coinquilino o da altri.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per verificare se il gioco viene avviato in una sessione remota, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Un valore diverso da zero indica che la sessione è remota.

Per altre informazioni, vedere [Cambio rapido utente.](/windows-hardware/drivers/display/fast-user-switching) Si noti che cambio rapido utente si verifica se le restrizioni di tempo di Controllo genitori sono abilitate quando il tempo dell'utente è attivo. Per altri dettagli, vedere il requisito 1.2.

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 Supporto dei nomi lunghi

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Se un gioco supporta il salvataggio di file, deve essere in grado di salvare i file con nomi e percorsi lunghi. Il gioco deve gestire correttamente caratteri file system speciali, ad esempio \\ / : \* ? " < >, in tutti i campi di input utente usati per creare nomi di file o percorsi.

I giochi devono funzionare correttamente quando un utente ha un nome utente lungo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I lettori sono abituati a usare nomi lunghi in percorsi approfonditi supportati dal sistema operativo sottostante.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I nomi lunghi sono definiti come quelli che contengono i valori massimi definiti in Windows SDK.

</dd> </dl>

## <a name="installation"></a>Installazione

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi per i clienti**

I clienti possono essere certi che le applicazioni verranno installate in Windows senza degradare il sistema operativo o altre applicazioni se le applicazioni usano metodi ufficiali di distribuzione dei componenti di sistema. Un'esperienza di installazione semplificata offre un'esperienza predefinita più accessibile e senza problemi per i giochi.

### <a name="31-support-easy-installation"></a>3.1 Supporto dell'installazione semplice

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi devono fornire un percorso semplificato nell'interfaccia utente di configurazione implementando quanto segue:

-   Visualizzare un massimo di un prompt EULA.
-   Il percorso di installazione predefinito deve ignorare tutte le selezioni per l'installazione ,ad esempio la cartella di installazione o le selezioni di componenti, presupporre le selezioni predefinite e quindi eseguire il gioco o l'utilità di avvio al termine dell'installazione, senza richieste aggiuntive. Se si desidera, è possibile specificare un'opzione di installazione personalizzata per le opzioni di configurazione avanzate.
-   Installare tutti i componenti del sistema operativo necessari,ad esempio i runtime DirectX e Visual C, usando i pacchetti di ridistribuzione Microsoft corretti. L'installazione deve essere eseguita in modo invisibile all'utente, senza chiedere conferma e senza essere sorvegliata dai controlli della versione del componente.
-   Fornire la rimozione **tramite Programmi e funzionalità** in Pannello di controllo per l'applicazione di gioco e i file di lavoro generati.  È consigliabile eliminare tutti i file di dati creati dall'utente. Il processo di rimozione deve garantire che tutti i file installati siano rimossi e che tutte le impostazioni , ad esempio le voci dell'elenco eccezioni del firewall e le chiavi del Registro di sistema, siano cancellate. I componenti del sistema operativo ridistribuiti non devono essere rimossi.
-   Se il gioco richiede l'aggiunta di eccezioni al firewall Windows, il processo di configurazione può richiedere di informare gli utenti che questa modifica è necessaria. Questa richiesta dovrebbe essere visualizzata prima dell'inizio dell'installazione.

L'installazione e la rimozione possono richiedere diritti amministrativi. L'applicazione di patch può richiedere credenziali amministrative, a seconda della frequenza di aggiornamento. Il normale gioco non deve richiedere diritti amministrativi, in base al requisito 2.1 Seguire le linee guida di controllo dell'account utente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'installazione semplice è una filosofia di sviluppo di giochi incentrata su Windows progettata per semplificare e semplificare il processo talvolta noioso e confuso di installazione di giochi nei computer che eseguono sistemi operativi Windows sistema operativo. L'installazione semplice viene abilitata usando un set di tecnologie e procedure consigliate che riducono la complessità non necessaria e il rischio percepito di installare giochi nei computer Windows computer.

Gli obiettivi principali sono:

-   Ridurre la quantità di tempo per entrare nel gioco e iniziare a giocare.
-   Ridurre il numero di finestre di dialogo e scelte a pochissime, o nessuna, per semplificare l'esperienza di installazione del gioco.

Alcune installazioni tradizionali hanno richieste che consentono installazioni non funzionali, anche se l'applicazione sembra essere stata installata correttamente. Ad esempio, un gioco può richiedere a un utente di accettare un contratto di licenza. Il gioco viene quindi installato e quindi viene visualizzato il codice EULA di DirectX. Questo EULA consente agli utenti di rifiutare e quindi ignorare l'installazione del runtime DirectX. Questo scenario può causare un gioco che non viene eseguito a causa di componenti mancanti.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per altre informazioni sull'installazione del gioco, sulle tecniche di installazione di giochi non tradizionali, sulle soluzioni di applicazione di patch compatibili con il controllo dell'account utente e sulla gestione di patch frequenti, vedere gli articoli di DirectX seguenti:

-   [Semplificazione dell'installazione del gioco](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Installare su richiesta per i giochi](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Applicazione di patch al software di gioco in Windows XP, Windows Vista e Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Procedure consigliate per l'installazione di giochi online Massively Multiplayer](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> La rimozione di file di dati generati specifici dell'utente deve essere eseguita solo per l'utente corrente e per i percorsi utente condivisi comuni. Non esiste un modo efficace per analizzare il sistema per rimuovere file specifici dell'utente per altri utenti, anche se la rimozione richiede credenziali amministrative.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 Supporto del controllo dell'account utente per l'installazione

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco non deve presupporre che sia in esecuzione nello stesso contesto dell'utente. Le posizioni specifiche dell'utente saranno diverse dal programma di installazione e dal lettore anche per i sistemi a utente singolo a causa dell'elevazione delle credenziali di amministratore. Pertanto, quando un gioco viene eseguito per la prima volta, deve eseguire attività specifiche dell'utente, separatamente dal processo di installazione.

La Windows di eccezione firewall non deve essere visualizzata quando un utente ospita o partecipa a un gioco multiplayer. Qualsiasi configurazione richiesta deve essere eseguita in fase di installazione. Le istruzioni di installazione devono informare l'utente che questa operazione verrà eseguita come parte dell'installazione.

Il programma di installazione del gioco deve fornire un manifesto incorporato che definisce il livello di esecuzione richiesto, in base al requisito 2.1 Seguire le linee guida per il controllo dell'account utente.

Se il gioco viene avviato dal programma di installazione al termine dell'installazione, deve essere avviato nel contesto dell'utente originale.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Una delle principali modifiche al sistema operativo Windows in Windows Vista è l'aggiunta del controllo dell'account utente, che esegue applicazioni con privilegi ridotti per impostazione predefinita. Di conseguenza, i programmi di installazione devono gestire i livelli di privilegi di conseguenza. Windows 7 usa anche il controllo dell'account utente. Anche se Windows 7 migliora l'esperienza utente del controllo dell'account utente, i programmi di installazione devono comunque soddisfare gli stessi requisiti di Windows Vista per funzionare correttamente, senza basarsi sul comportamento di virtualizzazione potenzialmente confuso.

Il controllo dell'account utente è attivo per impostazione predefinita in Windows Vista e Windows 7 e la maggior parte dei clienti (88% o più, in base ai commenti e suggerimenti) lascia abilitata questa funzionalità.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per altre informazioni sulla configurazione del firewall Windows, vedere l'articolo di DirectX [Windows Firewall per](/windows/desktop/DxTechArts/games-and-firewalls) sviluppatori di giochi e l'esempio FirewallInstallHelper.

L'avvio standard del gioco alla fine del processo di installazione non soddisfa l'ultimo aspetto di questo requisito se l'installazione viene avviata da un utente standard e se il processo di installazione richiede privilegi amministrativi, ovvero richiede credenziali di amministratore. Eredita anche i privilegi amministrativi, che rappresenta un potenziale rischio per la sicurezza. Un caricatore bootstrap del programma di installazione dovrebbe invece avviare il gioco dopo la restituzione da una chiamata riuscita del programma di installazione. Per altre informazioni, vedere l'articolo di MSDN Magazine [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 Eseguire l'installazione in cartelle corrette

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi installati per tutti gli utenti devono essere installati nella cartella Programmi per impostazione predefinita. I dati utente devono essere scritti quando il gioco viene eseguito per la prima volta, non durante l'installazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Gli utenti devono avere la flessibilità necessaria per installare le applicazioni laddove necessario. Devono anche avere un'esperienza coerente e sicura con il percorso predefinito dei file.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi possono usare i vari percorsi di cartelle note (ad esempio quelli specificati da CSIDL LOCAL APPDATA e \_ \_ CSIDL \_ COMMON APPDATA) per archiviare quantità significative di dati di gioco e file eseguibili di supporto per implementare scenari avanzati di installazione su richiesta e applicazione di \_ patch.

Poiché l'installazione può richiedere l'elevazione a un account utente diverso durante il processo di installazione di tutti gli utenti, non esiste un percorso utente corretto in cui archiviare i dati in fase di installazione. Inoltre, se la crittografia dei file è abilitata, i file crittografati possono essere accessibili solo dall'account utente che li ha creati.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 Installare correttamente Windows risorse

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Le applicazioni non devono tentare di installare file o chiavi del Registro di sistema protette Windows Resource Protection (WRP). Se l'applicazione richiede versioni più recenti dei componenti di sistema, deve aggiornare questi componenti usando un Microsoft Service Pack o un pacchetto di installazione approvato da Microsoft che contiene il componente di sistema. I componenti di sistema non devono mai essere ripacchedati.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Windows Resource Protection (WRP) è progettato per garantire che le risorse di sistema protette siano aggiornate solo usando meccanismi di installazione o aggiornamento approvati da Microsoft. WRP migliora l'affidabilità del sistema assicurando che i risultati di un'installazione siano prevedibili.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

WRP è il successore Windows Protezione file, che protegge la maggior parte dei componenti di sistema installati nella Windows cartella. WRP protegge la maggior parte delle chiavi del Registro di sistema che archiviano le impostazioni per la creazione di oggetti COM. Riserva inoltre alcune cartelle per l'uso esclusivo da parte del sistema operativo. I tentativi di accesso alle risorse protette in genere comportano un errore di negazione dell'accesso.

Per informazioni dettagliate sulle procedure consigliate per la distribuzione del runtime DirectX con un gioco, vedere l'articolo DirectX Installation for Game Developers (Installazione [di DirectX per sviluppatori di giochi).](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 Evitare riavvii durante l'installazione

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco non deve presupporre che l'installazione di componenti Windows da pacchetti di ridistribuzione richieda un riavvio, a meno che il riavvio non sia indicato da un risultato restituito o dalla documentazione Microsoft.

Se il programma di installazione del gioco impone sempre un riavvio, questo deve essere approvato da Microsoft.

Le finestre di dialogo file in uso incluse nei pacchetti Windows Installer devono contenere un'opzione per chiudere automaticamente le applicazioni e tentare di riavviarle al termine dell'installazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Il riavvio del sistema dopo un'installazione è un'interruzione non necessaria per gli utenti e in genere non è necessaria.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per altre informazioni, vedere [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 Usare correttamente il controllo delle versioni dei file

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il programma di installazione del gioco deve verificare correttamente che siano installate le versioni più recenti dei file. L'installazione di un gioco non deve mai regredire i file non prodotti o condivisi da applicazioni non producete.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I componenti condivisi e i componenti di sistema vengono spesso aggiornati per le correzioni di sicurezza e le funzionalità espanse. Un'installazione che include una versione precedente dei componenti aggiornati non dovrebbe comportare la perdita di aggiornamenti e correzioni già applicate.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Supporto del requisito condizionale di esecuzione \[ automatica\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per i giochi distribuiti su CD, DVD o altri supporti rimovibili che supportano l'esecuzione automatica, quando il disco viene inserito per la prima volta, l'applicazione deve eseguire automaticamente o richiedere all'utente di installare il gioco, a meno che l'utente non abbia disabilitato la funzionalità di esecuzione automatica.

Al termine dell'installazione dell'applicazione, il nuovo inserimento del disco nell'unità non deve causare il nuovo avvio automatico dell'installazione. È accettabile chiedere agli utenti se vogliono aggiornare o modificare le opzioni di installazione.

L'applicazione di esecuzione automatica non deve richiedere l'elevazione dei privilegi, ovvero deve avere asInvoker nel manifesto, in base al requisito 2.1, anche se può avviare il programma di installazione o un'altra utilità che richiede diritti amministrativi. L'elevazione dei privilegi deve verificarsi solo se il gioco non è installato o se l'utente lo seleziona in modo specifico.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'esecuzione automatica semplifica l'esperienza di utilizzo di applicazioni distribuite su supporti, ad esempio i giochi che in genere richiedono che il disco sia presente nell'unità per poter riprodurre il gioco.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Non è accettabile richiedere all'utente di spostarsi Esplora file avviare l'installazione dal CD o dal DVD.

Per i giochi distribuiti su più dischi, i dischi successivi dovrebbero usare idealmente la funzionalità Di esecuzione automatica o continuare l'installazione senza chiedere all'utente di premere un tasto o di eseguire altre azioni.

Quando si crea un programma di esecuzione automatica, assicurarsi che tutti i componenti necessari siano presenti nelle nuove installazioni di Windows. Le applicazioni tipiche si basano su tecnologie installate dal programma di installazione, ma l'esecuzione automatica viene eseguita prima di qualsiasi configurazione di questo tipo. Un esempio comune è l'errore dei programmi di esecuzione automatica perché le DLL di runtime di Visual C non sono state incluse nell'Windows configurazione. Il programma di esecuzione automatica, pertanto, deve usare la distribuzione CRT locale dell'applicazione o collegare in modo statico il CRT.

I programmi di esecuzione automatica scritti per l'uso nelle versioni di Windows prima di Windows Vista non devono usare il runtime .NET perché questa tecnologia non è inclusa in Windows XP o versioni precedenti di Windows. Windows Server 2003 e Windows Vista sono le prime versioni di Windows includere il runtime .NET come parte del sistema operativo.

Per motivi simili, i programmi di esecuzione automatica non possono richiedere la presenza di componenti side-by-side facoltativi di DirectX SDK, ad esempio D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT e MDX 1.1.

Per un esempio di uso dell'esecuzione automatica, vedere Esempio di esecuzione automatica.

</dd> </dl>

## <a name="reliability"></a>Affidabilità

**Riepilogo dei requisiti di sicurezza e compatibilità**

**Vantaggi per i clienti**

Questi requisiti rendono un'applicazione più affidabile riducendo al minimo il numero di arresti anomali, blocchi e riavvii. I requisiti di affidabilità consentono di garantire che il software sia più prevedibile, gestibile, resiliente e recuperabile.

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Eliminare i riavvii non necessari

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Tutti i programmi di installazione dell'applicazione devono sfruttare le API di Gestione riavvio per evitare riavvii del sistema (vedere il requisito 3.5).

I giochi non devono bloccare l'arresto.

Tutte le applicazioni devono rispondere al gestore riavvii in ascolto e rispondendo ai messaggi di arresto seguenti:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Le applicazioni GUI devono rispondere (TRUE) immediatamente in preparazione del riavvio.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Le applicazioni devono restituire un valore 0 entro 5 secondi e quindi chiudere.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL+C 
</dt> <dd>

Le applicazioni console che ricevono questo messaggio devono chiudersi immediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I riavvii del sistema sono un'interruzione importante. Conducono a un'esperienza utente non ottimale e devono essere ridotte al minimo. Alcune operazioni, ad esempio gli aggiornamenti critici del sistema, possono richiedere riavvii. In ascolto dei messaggi di arresto, il gioco e altre applicazioni possono reagire prontamente alle richieste di Gestione riavvio. In questo modo, possono evitare ritardi inutilmente nelle richieste di riavvio valide.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Se il programma di installazione di un gioco usa Windows installer senza azioni personalizzate, questa funzionalità viene fornita automaticamente. I pacchetti di ridistribuzione Microsoft supportano anche Gestione riavvio.

Per altre informazioni su Gestione riavvio, vedere l'articolo MSDN [Informazioni su Gestione riavvio](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Eliminare Application Verifier errori

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco non deve generare errori in esecuzione in Microsoft Application Verifier (AppVerifier), versione 4.0 o successiva, nei test seguenti:

-   Nozioni di base: Handle, Heap, Blocchi, Memoria, TLS
-   Varie: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

AppVerifier verifica molti problemi noti che causano arresti anomali e si blocca Windows applicazioni, nonché vulnerabilità di sicurezza note.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Per altre informazioni sui Application Verifier, [](/previous-versions/ms220948(v=vs.80)) vedere Application Verifier [e Uso Application Verifier ciclo](/previous-versions/aa480483(v=msdn.10)) di vita dello sviluppo software in MSDN. È possibile scaricare Application Verifier [dettagli del download: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) nell'Area download Microsoft.

Questo requisito non si applica alle applicazioni gestite pure senza interoperabilità nativa.

Questi test devono essere eseguiti in una build di versione. Il debug delle compilazioni può generare errori falsi. Alcune tecnologie antipirateria e anti-trucchi possono interferire con l'esecuzione di AppVerifier. Pertanto, questi test devono essere eseguiti senza tecnologie antipirateria e anti-cheat abilitate.

Potrebbe essere necessario impostare la proprietà Full del test Basics:Heaps su FALSE, perché l'intero pageHeap aumenta notevolmente la quantità di memoria dell'applicazione in esecuzione. Gli errori verranno comunque rilevati, ma potrebbero essere più difficili da rilevare se si usa solo pageHeap parziale.

Se si usano i test correlati a UAC/LUA in Application Verifier per soddisfare i requisiti di controllo dell'account utente 2.1 e 3.2, è consigliabile usare l'analizzatore utente [standard](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) per esaminare i risultati. Esistono anche numerosi altri test utili forniti da Application Verifier che è consigliabile usare nello sviluppo e nei test per garantire un livello elevato di compatibilità con le versioni correnti e future di Windows. Il **test HighVersionLie** viene usato per verificare la conformità con il requisito 2.5.

Visual Studio Team System include un subset della funzionalità AppVerifier integrata nell'ambiente di debug. Ciò può risultare utile per tenere traccia e risolvere i problemi relativi ai test di base: heap, handle e blocchi.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 Supporto delle Segnalazione errori Windows e della versione del file

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Per abilitare il supporto di Segnalazione errori Windows, i giochi devono soddisfare i requisiti seguenti:

-   I giochi devono gestire solo le eccezioni note e previste. Segnalazione errori Windows deve essere disabilitato. Se in un gioco viene visualizzato un errore, ad esempio una violazione di accesso, Segnalazione errori Windows segnalare l'arresto anomalo.
-   Tutti i file eseguibili, ad esempio .exe file o DLL, devono contenere un nome di prodotto, un nome di società e una versione del file accurati.
-   L'uscita normale del gioco non deve generare un errore di eccezione sconosciuto.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Le SEGNALAZIONE ERRORI WINDOWS forniscono feedback essenziale a Microsoft per rilevare arresti anomali e blocchi diffusi nelle applicazioni. Ciò consente a Microsoft e ai suoi partner di rilevare e risolvere rapidamente i problemi di sistema e driver che causano errori dell'applicazione.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

I giochi possono includere gestori di eccezioni non gestiti personalizzati per eseguire funzionalità di supporto e creazione di report personalizzate, ma devono passare qualsiasi errore alle funzioni **ReportFault** o **WerReportSubmit.**

Le informazioni corrette sulla versione del file possono essere verificate visualizzando le proprietà dei file nell'interfaccia Windows desktop e controllando la pagina delle proprietà Versione.

Per altre informazioni sulle API Segnalazione errori Windows e su come analizzare i dump di arresto anomalo generati quando si usa questo servizio, vedere l'articolo directX [Crash Dump Analysis](/windows/desktop/DxTechArts/crash-dump-analysis).

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller per Windows terminologia



| Nome                                          | Descrizione                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| A                                        | Pulsante A.                                                                                     |
| B                                        | Pulsante B.                                                                                     |
| INDIETRO                                     | Pulsante Indietro.                                                                                  |
| Paraurti (destra/sinistra)                      | Pulsante in alto a destra e a sinistra del controller. Equivale a un pulsante della barra.    |
| pad direzionale                          | Pad direzionale del controller.                                                                   |
| D-pad                                    | Abbreviazione accettata del riempimento direzionale.                                                         |
| Punto di distribuzione (DP)                                       | Abbreviazione del pad direzionale e etichetta del controller.                                                |
| RB, LB                                   | Abbreviazioni dei paraurti destro e sinistro ed etichette del controller.                                        |
| RS, LS                                   | Abbreviazioni di bastoni a destra e a sinistra e etichette del controller.                                         |
| RT, LT                                   | Abbreviazioni dei trigger destro e sinistro ed etichette del controller.                                       |
| RSB, LSB                                 | Abbreviazioni di bastoni a destra e a sinistra e etichette del controller.                                         |
| START                                    | Oggetto pulsante Start.                                                                                 |
| (destra/sinistra) stick                       | La levetta del controller. In precedenza la levetta personale.                                                       |
| (destra/sinistra) stick button (A destra/sinistra) stick button (A destra/Sinistra) stick button                | Pulsante della levetta del controller. Pulsante della levetta in precedenza.                                         |
| Trigger (destra/sinistra)                     | Trigger del controller.                                                                          |
| Vibrazione                                | Feedback di gioco prodotto dal motore del controller. Non usare rumble.                           |
| X                                        | Pulsante X.                                                                                     |
| S                                        | Pulsante Y.                                                                                     |
| controller Xbox 360 per Windows          | Il Xbox 360 gamepad venduto come SKU hardware del PC, incluso un disco Windows del driver di dispositivo.          |
| controller wireless Xbox 360 per Windows | Il Xbox 360 gamepad wireless venduto come SKU hardware del PC, incluso un disco Windows del driver di dispositivo. |



 

## <a name="guidelines-for-game-middleware-products"></a>Linee guida per i prodotti middleware di gioco

### <a name="introduction"></a>Introduzione

Perché i giochi siano idonei per il programma Games for Windows, devono soddisfare un elenco di requisiti tecnici. Anche i componenti di terze parti forniti con un titolo (file eseguibili, DLL, driver e così via) devono soddisfare questi requisiti affinché il gioco sia idoneo. Questo documento evidenzia i requisiti più comuni che devono essere soddisfatti anche dai componenti di terze parti perché il gioco superi i test di conformità. I programmi di installazione e i pacchetti di produzione/motore di gioco completi devono esaminare la documentazione completa dei giochi per Windows requisiti tecnici, perché molti di questi requisiti sono interessati da questi strumenti.

### <a name="additional-recommendations"></a>Ulteriori indicazioni

Oltre a garantire che il componente supporti la creazione di titoli conformi ai requisiti per Giochi per Windows, è necessario tenere conto di alcune altre considerazioni durante la progettazione e la distribuzione di una libreria o di un'utilità di supporto per un gioco Windows.

-   Per supportare gli sviluppatori che lavorano su applicazioni x64 native a 64 bit, fornire entrambe le versioni native a 32 e 64 bit delle librerie. La versione a 32 bit deve essere compatibile a 64 bit per 2.2. Le librerie per le applicazioni a 32 bit non devono presupporre che il bit alto di qualsiasi indirizzo a 32 bit non sia usato per supportare l'uso all'interno di applicazioni LARGEADDRESSAWARE x86.
-   Se si forniscono intestazioni di codice nativo (C/C++), usare la sintassi degli attributi SAL (Standard Annotation Language) per decorare le routine API pubbliche. In questo modo gli utenti della libreria potranno usufruire del massimo vantaggio dell'uso di Static Code Analysis (/analyze), che fa parte di Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium e Visual Studio 2010 Ultimate, nonché degli strumenti del compilatore Windows SDK disponibili pubblicamente.
-   Se il prodotto crea thread all'interno del processo dell'utente, assicurarsi di assegnare un nome a ogni thread in modo che gli strumenti di debug possano annotare correttamente i thread in esecuzione.
-   Se si scrivono routine che devono essere chiamate all'interno del ciclo principale di un gioco, usare le routine D3DX D3DPERF \_ BeginEvent/EndEvent e D3DPERF SetMarker per annotare le operazioni di alto livello per identificare più facilmente i colli di bottiglia usando PIX per \_ Windows.
    > [!Note]  
    > Per la Visual Studio diagnostica grafica di 2012, queste routine D3DX e PIX vengono sostituite [**dall'interfaccia ID3DUserDefinedAnnotation.**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)

     

-   Per le librerie di rete, fornire implementazioni indipendenti da IP ed evitare routine deprecate solo IPv4 per supportare le tecnologie IPv6 e Teredo in Windows XP con Service Pack 2, Windows Vista e Windows 7.
-   I provider di servizi di gioco devono registrarsi con Games Explorer usando la versione 2 dello schema GDF e usare la funzionalità RSS per fornire notizie correlate al servizio.

### <a name="games-for-windows-showcases"></a>Giochi per Windows Showcase

### <a name="introduction"></a>Introduzione

Le vetrine Windows games for Windows offrono un'esperienza di gioco solida Windows PC. Implementando queste funzionalità, i giochi possono aggiungere maggiore entusiasmo all'esperienza utente nelle Windows più recenti.

I giochi per Windows devono soddisfare tutti i requisiti tecnici elencati in questo articolo, ma le funzionalità della vetrina sono facoltative. Questi titoli sono gratuiti per implementare alcune, nessuna o tutte queste vetrine.

### <a name="s1-exploit-direct3d-11"></a>S.1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Direct3D 11 è l'API di rendering di nuova generazione per Windows Vista e Windows 7. I giochi che sfruttano Direct3D 11 usano contenuto ottimizzato, tecniche di rendering avanzate e nuove funzionalità hardware per creare un'esperienza accattivante nell'hardware che supporta 10, 10.1 e 11.

Se il gioco implementa anche Direct3D 9, un confronto side-by-side dovrebbe dimostrare un miglioramento percettibile della qualità del contenuto, della fedeltà visiva, delle prestazioni, della complessità della scena e di altre aree di fedeltà grafica per Direct3D 11. Questo supporto è soggetto ai giochi per Windows requisito tecnico 1.7.

La tecnologia Direct3D 10level9 può essere usata per supportare l'hardware video direct3D 9 classe Shader Model 2.0/3.0 in Windows Vista e Windows 7, anziché usare un'implementazione Direct3D 9 side-by-side per un ampio supporto hardware. Tuttavia, questo non è sufficiente per illustrare questa vetrina.

Nei computer che eseguono Windows Vista o Windows 7 con Direct3D 11 installato, per impostazione predefinita il gioco deve usare Direct3D 11.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

L'API Direct3D 11 si basa sull'infrastruttura WDDM (Windows Display Driver Model) e Direct3D 10.1 per supportare nuove funzionalità: tessellazione hardware, shader di calcolo, rendering multithreading e creazione di risorse, nuovi formati di compressione della trama e un linguaggio shader più flessibile. Direct3D 11 offre supporto hardware unificato per le schede video moderne, incluse le parti Direct3D 11 di ultima generazione, tutte le schede video Direct3D 10 e 10.1 e molte schede video Direct3D 9 Direct3D 2.0/3.0 shader Model 2.0/3.0, ovvero l'hardware video minimo necessario per il desktop 3D Di Aero.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

La migrazione di un motore di rendering Direct3D 9 per l'uso della nuova interfaccia Direct3D 11 è un'attività ben definita:

-   Eliminare tutte le operazioni a funzione fissa a favore degli shader programmabili.
-   Aggiornare tutti gli shader esistenti alla nuova sintassi di Shader Model 4.x/5.
-   Aggiornare la gestione delle risorse per supportare il nuovo modello di visualizzazione.
-   Convertire tutti gli asset per usare un nuovo elenco di formati disponibili.
-   Aggiornare la gestione dello stato di rendering per usare blocchi di stato non modificabili e rielaborare le costanti dello shader in buffer costanti.

Questa conversione è essenziale per abilitare la vetrina Direct3D 11, anche se il risultato non soddisfa il requisito di vetrina per sfruttare la nuova API.

La nuova API e il modello di programmazione HLSL associato offrono molte opportunità per il contenuto avanzato:

-   Sfruttando le funzionalità hardware Direct3D 10 esistenti, ad esempio Geometry Shader, Stream Out, matrici di trame e i formati di trama compressi BC4/BC5.
-   Sfruttando le funzionalità hardware Direct3D 10.1 esistenti, ad esempio modalità di fusione indipendenti per destinazione di rendering, read back di profondità MSAA, accesso MSAA per campione dello shader, matrici di mappe del cubo e rendering in formati compressi a blocchi (BC).
-   Implementazione di algoritmi GPU avanzati con Compute Shader con CS4.x su schede video Direct3D 10/10.1 esistenti (abilitate dai driver video aggiornati) o CS 5.0 su schede video Direct3D 11 di nuova generazione.
-   Rendering su più thread usando la creazione di risorse a thread libero e più contesti di dispositivo per migliorare le prestazioni nei sistemi multicore (con driver video aggiornati). Per altre informazioni, vedere Giochi per Windows Showcase S.3.
-   L'uso di nuove funzionalità dell'hardware video di classe Direct3D 11, ad esempio la tessellazione hardware con hull e shader di dominio, l'hardware dello shader HLSL shader Shader 5.0 offre formati di trama compressi BC6HBC7 e Dynamic Shader Linkage.

Le tecniche che possono essere implementate con Direct3D 9 (in gran parte tramite un costo elevato della CPU) possono essere scaricate nella GPU in modo efficiente, liberando così le risorse della CPU per supportare altre richieste di gioco.

Le API, gli strumenti di supporto e gli esempi di Direct3D 11 sono disponibili in DirectX SDK. Vedere anche API grafiche in Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S.2 Exploit x64 Nativo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco include un eseguibile nativo a 64 bit che offre una nuova esperienza accattivante abilitata dalle edizioni x64 di Windows in esecuzione su hardware con supporto x64. Un confronto side-by-side con la versione a 32 bit del gioco dovrebbe mostrare un miglioramento percettibile nella complessità del contenuto, tempi di caricamento complessivi ridotti e prestazioni.

Nelle edizioni a 64 bit di Windows l'installazione deve sempre configurare la versione nativa a 64 bit del gioco come impostazione predefinita per i collegamenti in Games Explorer e Windows XP Professional x64 Edition. Se si desidera una doppia installazione, è possibile specificare un'attività di riproduzione aggiuntiva per Games Explorer in Windows Vista e Windows 7 che punta alla versione a 32 bit, ma il valore predefinito deve rimanere la versione nativa a 64 bit.

Si noti che il gioco deve supportare le edizioni a 64 bit di Windows Vista e Windows 7 per soddisfare questa raccomandazione di dimostrazione. Il supporto Windows XP Professional x64 Edition è consigliato, ma non obbligatorio.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

La tecnologia x64 offre funzionalità di indirizzamento a 64 bit per i mercati consumer e server che include la compatibilità con le versioni precedenti a 32 bit a velocità completa per le applicazioni esistenti. x64 è una parte fondamentale della roadmap sia per AMD (AMD64) che per Intel (EMT64) e, ad eccezione delle CPU ultra-mobili, supporta la tecnologia per tutti i processori di generazione corrente e futura.

Windows XP Professional x64 Edition è stato il primo sistema operativo Windows orientato agli utenti a supportare la tecnologia x64 e Windows Vista e Windows 7 ampliano notevolmente la disponibilità dell'abilitazione del sistema operativo per l'elaborazione consumer a 64 bit. Con 2 GB di RAM come standard in molti nuovi computer, ulteriori miglioramenti al ridimensionamento della memoria non trarranno vantaggio dalle singole applicazioni a 32 bit che non sono in grado di risolvere più di 2 GB di RAM fisica. Molti giochi attualmente affrontano difficoltà nell'adattamento di tutto il contenuto disponibile ai vincoli di 2 GB di spazio degli indirizzi virtuali, soprattutto se combinati con le grandi memorie video disponibili nelle GPU di fascia alta e il passaggio alla tecnologia x64 aumenta notevolmente i livelli di dettaglio supportati.

La compatibilità x64 per i giochi a 32 bit è un requisito tecnico di Games for Windows (2.2), ma l'utilizzo completo delle nuove tecnologie richiede un'implementazione nativa a 64 bit.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Il vantaggio principale dell'indirizzamento a 64 bit è la possibilità di accedere direttamente a più di 2 GB di memoria fisica e virtuale. Lo spazio di indirizzi della memoria virtuale di grandi dimensioni consente un uso esteso di I/O mappato alla memoria senza problemi di esaurimento dello spazio degli indirizzi della macchina virtuale prevalenti nella programmazione a 32 bit. I giochi possono sfruttare il nuovo spazio per migliorare notevolmente i tempi di caricamento o, in alcuni casi, per eliminare le pause per il caricamento del contenuto.

Le applicazioni a 32 bit esistenti possono trarre vantaggio dalle edizioni x64 grazie alla possibilità di elaborare indirizzi con dati completi a 32 bit quando vengono compilate con l'opzione del linker Abilita indirizzi di grandi dimensioni (**/LARGEADDRESSAWARE**). Nelle versioni a 32 bit di Windows XP, le modalità di avvio speciali consentiranno alle applicazioni di risolvere fino a 3 GB di RAM e le edizioni x64 forniscono l'accesso fino a 4 GB di RAM per le app large address aware (LAA). Sebbene l'uso di LAA in un'applicazione a 32 bit non soddisfi questo requisito di dimostrazione, questa tecnologia bridge è un modo estremamente utile per offrire vantaggi di scalabilità aggiuntivi nelle versioni x64 di Windows per coloro che non implementano completamente questo requisito di dimostrazione.

Per altre informazioni, vedere Programmazione a [64 bit](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) per sviluppatori di giochi e RAM, VRAM e altra [RAM: 64-bit Gaming Is Here](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra ( Giochi a 64 bit in Gamasutra).

> [!Note]  
> Una sfida fondamentale per questa dimostrazione è garantire che tutte le librerie o i componenti di terze parti su cui si basa il gioco siano disponibili per lo sviluppo nativo a 64 bit. Molte API Microsoft legacy sono state eliminate anche dall'ambiente nativo a 64 bit, che può rivelarsi una sfida per le codebase del motore contenenti implementazioni precedenti di sistemi chiave.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S.3 Exploit Many-Core Processori

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Il gioco implementa funzionalità che sfruttano i processori multicore, con scalabilità a 3, 4 o più core, se disponibili.

Se il gioco supporta sistemi a processore singolo o dual core, un confronto side-by-side con un sistema quad-core deve dimostrare nuove funzionalità percettibili, effetti accattivanti aggiuntivi, miglioramento della qualità del contenuto e/o prestazioni migliorate.

Poiché la scalabilità dual-core è già ampiamente supportata dai giochi, nonché usata automaticamente da vari miglioramenti dei driver Direct3D, la scalabilità dual-core non è sufficiente per illustrare questa dimostrazione.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

La continua crescita delle prestazioni per le CPU è passata dai miglioramenti della frequenza di clock all'aggiunta di core di calcolo. Le roadmap di AMD e Intel si basano su progettazioni multicore scalabili. Tutte le piattaforme di gioco di prossima generazione hanno CPU multicore a causa di questo cambiamento fondamentale nell'evoluzione dei processori. Le applicazioni a thread singolo non oseranno più vantaggi significativi dalle CPU di nuova generazione. Anche il multithreading semplice non verrà ridimensionato man mano che il numero di core CPU in uso comune aumenta fino a tre o più.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Si noti che il numero di core non deve essere una potenza di due, quindi i giochi devono essere ridimensionati in modo lineare e gestire i conteggi dei core di 3, 4, 5, 6, 7, 8 e così via.

Il ridimensionamento aumentando il numero di thread in un'applicazione restituisce un valore restituito solo se i costi di comunicazione e sincronizzazione dei thread vengono mantenuti sotto controllo. La scalabilità basata sulle funzionalità può rivelarsi una soluzione più semplice a breve termine, consentendo al gioco di funzionare normalmente senza i thread aggiuntivi nei sistemi a core singolo e abilitandoli quando è disponibile la potenza aggiuntiva della CPU.

Per altre informazioni, vedere [Coding For Multiple Cores on Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) and Lockless Programming Considerations for Xbox 360 and Microsoft Windows (Considerazioni sulla programmazione senza blocco per Xbox 360 e Microsoft [Windows)](/windows/desktop/DxTechArts/lockless-programming) negli articoli di DirectX, nonché l'utilità DXUTLockFreePipe e l'esempio CoreDetection.

L'uso della creazione di risorse a thread libero Direct3D 11 e dei contesti di dispositivo è utile per ottenere la scalabilità molti-core nel rendering e nel caricamento delle risorse grafiche. Vedere Giochi per Windows Showcase S.1.

Si noti che l'uso diretto dell'istruzione della CPU rdtsc, invece di usare le API Windows per calcolare i tempi nei sistemi multicore, può causare problemi in alcune configurazioni hardware e del sistema operativo. vedere [Game Timing and Multicore Processors (Tempo di gioco e processori multicore)](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) negli articoli di DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S.4 Support Games for Windows - LIVE

Games for Windows - LIVE non è più supportato da Microsoft.

### <a name="s5-support-windows-touch"></a>Supporto di S.5 Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

Windows giochi che supportano il tocco sono riproducibili tramite tocco e/o movimenti nei computer che eseguono Windows 7 con un display touch. È possibile usare anche l'input da tastiera, ma l'interfaccia di riproduzione principale deve essere basata sul tocco.

L'abilitazione del tocco non deve impedire l'uso del mouse o del controller comune, in base al requisito tecnico 1.4.

Non è previsto che il programma di installazione del gioco supporti Windows Touch.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

Gli schermi con supporto per il multitocchetto per computer sono disponibili per portatili e desktop e rappresentano una funzionalità hardware chiave in fase di promozione con il rilascio di Windows 7. Windows 7 supporta l Windows Touch in tutte le interfacce di controlli comuni e desktop.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Le applicazioni di codice nativo possono accedere al multitocco tramite i messaggi WM \_ TOUCH, in combinazione con la [**funzione RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) Vedere anche l'API Manipulations and Inertia (Manipolazioni e inerzia).

Windows Presentation Foundation (WPF) 4.0 offre una soluzione gestita per le interfacce multitocchetto.

Per altre informazioni, vedere l'Windows Touch SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S.6 Supporto di colori elevati

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requisito**
</dt> <dd>

I giochi che supportano colori alti usano 10:10:10:2 (FORMATO DXGI \_ \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) o 16:16:16:16 (formato DXGI \_ \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) per il rendering della modalità di visualizzazione back-buffer e schermo intero.

Usando una destinazione di rendering a colori elevati, è possibile eseguire il rendering del contenuto High-Dynamic Range (HDR) con una gamma estesa o ampia quando si esegue il mapping del tono a un intervallo a 10 o 16 bit.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Logica**
</dt> <dd>

I monitor sono stati in grado di visualizzare più di 256 livelli di colore per canale per molti anni, anche quando gli schermi CRT erano prevalenti. L'hardware di analisi nelle schede video è stato il fattore limitante. Le GPU moderne, tra cui la maggior parte dell'hardware di classe Direct3D 9 e tutti i componenti hardware di classe 10 Direct3D e migliori, hanno hardware di analisi in grado di almeno 10 bit per canale e la capacità hardware è impostata per crescere a 16 bit per canale di colore in futuro. I sistemi hd-tv interconnettori (HDMI, DisplayPort) sono stati progettati per gestire anche più di 8 bit per canale e la VGA analoga conporterà già tali segnali.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informazioni aggiuntive**
</dt> <dd>

Si noti che Il colore alto, o Hi Color, si riferisce in cronologia allo spostamento da schermi a colori a 256 (8 bit) a schermi a 15 o 16 bit. La maggior parte dei sistemi di visualizzazione è passata da tempo a True Color, che è a 24 bit o a 8 bit per canale di colore per rosso, verde e blu. Per Colore elevato in questo caso si intende una nuova generazione di sistemi di visualizzazione che possono operare con più di 8 bit per ogni singolo canale di colore. L'oggetto è detto anche colore scuro.

</dd> </dl>

### <a name="recommended-best-practices"></a>Procedure consigliate

### <a name="introduction"></a>Introduzione

Oltre a soddisfare i requisiti tecnici e ad adottare una o più showcase nel titolo, è consigliabile seguire una serie di procedure consigliate per tutti i Windows giochi. Anche se queste raccomandazioni non rientrano nell'ambito dei requisiti tecnici di base, è vivamente consigliabile impiegarle per tutti i giochi Windows titoli.

### <a name="additional-recommendations"></a>Ulteriori indicazioni

-   Usare il compilatore e il runtime Visual Studio più recenti. Le versioni più recenti del compilatore implementano miglioramenti significativi per la qualità del codice generato e per i problemi di sicurezza e adottano strategie moderne di ottimizzazione del processore. L'aggiornamento del compilatore e l'uso del runtime C più recente sono un modo semplice per eseguire la migrazione a procedure di codifica moderne.
-   Usare la versione della libreria a collegamento dinamico (DLL) del runtime C, anziché il collegamento statico, e usare Secure CRT. Le eccezioni possono essere effettuate in casi speciali di preinstallazione, ad esempio per un programma di esecuzione automatica o per il programma di installazione stesso.
-   Per l'audio del gioco, usare XAudio2, X3DAudio e/o XACT anziché DirectSound. Per i motori audio che eseguono tutte le conversioni di combinazione e velocità di origine e necessitano solo di una soluzione a bassa latenza per l'output audio, usare DirectSound in Windows XP (solo) e WASAPI in Windows Vista e Windows 7.
-   Evitare di usare API legacy e deprecate: DirectDraw, DirectSound, DirectPlay, il livello di prestazioni di DirectMusic, DirectPlay Voice e la modalità mantenuta Direct3D. Si noti che DirectPlay Voice e la modalità mantenuta Direct3D non sono affatto disponibili in Windows Vista o Windows 7. Il livello di prestazioni di DirectPlay e DirectMusic non è disponibile per le applicazioni native x64.
-   Ottimizzare usando set di istruzioni SIMD SSE/SSE2. Vedere [l'API DirectXMath](/windows/desktop/dxmath/directxmath-portal) in Windows SDK come soluzione multipiattaforma per operazioni matematiche ottimizzate per SIMD.
-   Usare le procedure consigliate moderne per la sicurezza Windows ( incluse le opzioni del compilatore e del linker come **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DYNAMICBASE**, **/SDL** e così via). Per altre informazioni, vedere [Procedure di sicurezza consigliate per lo sviluppo di giochi.](/windows/desktop/DxTechArts/best-security-practices-in-game-development)
-   Usare i componenti e le librerie Windows SDK più recenti. Rimuovere le dipendenze dai componenti legacy di DirectSetup distribuiti fuori banda, ad esempio D3DX9, D3DX10 e D3DX11. Provare a [usare DirectXTex](https://github.com/Microsoft/DirectXTex) o [DirectXTK](https://github.com/Microsoft/DirectXTK) o entrambi.
-   Evitare di usare il compilatore HLSL meno recente e usare invece il compilatore HLSL moderno. Se l'applicazione richiede il supporto per Pixel Shader 1.x, usare l'assembly dello shader anziché HLSL oppure limitare l'uso del compilatore precedente solo a questi scenari.

## <a name="resources"></a>Risorse



| Termine                                                                                                                                                                                                                         | Descrizione                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Giochi per Windows: test case <br/>                              | Procedure consigliate per i giochi Windows XP, Windows Vista e Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Linee guida per il controllo dell'account utente <br/>                      | [Windows Requisiti di sviluppo delle applicazioni di Vista per la compatibilità del controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual portale per sviluppatori <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX portale per sviluppatori <br/>                                                  | [Centro per sviluppatori Directx](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog di Games for Windows e DirectX SDK<br/> | [Giochi per Windows e DirectX SDK](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Altri articoli di DirectX<br/>                                             | [Articoli tecnici su DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

