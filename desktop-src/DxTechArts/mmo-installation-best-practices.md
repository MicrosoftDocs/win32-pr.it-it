---
title: Procedure consigliate per l'installazione per giochi multiplayer online
description: Questo articolo descrive la creazione di una catena di progettazione di attendibilità per l'installazione client di MMOG (Massively multiplayer online) e sistemi di aggiornamento dei giochi personalizzati che funzionano bene con Windows e con il modello di sicurezza di Windows Vista e Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81003a434b830f046c29d606355104fe618d1f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046978"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Procedure consigliate per l'installazione per giochi multiplayer online

Questo articolo descrive la creazione di una catena di progettazione di attendibilità per l'installazione client di MMOG (Massively multiplayer online) e sistemi di aggiornamento dei giochi personalizzati che funzionano bene con Windows e con il modello di sicurezza di Windows Vista e Windows 7. Questo approccio è progettato per consentire l'applicazione di patch ai titoli MMOG, supportando gli account utente standard, che hanno accesso limitato al disco rigido e al registro di sistema.

-   [Perché i client MMOG hanno requisiti diversi per i tradizionali giochi acquistati al dettaglio](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Panoramica di una catena di approcci di attendibilità](#overview-of-a-chain-of-trust-approach)
-   [Tutti gli elementi vengono convalidati sul server, perché è necessario preoccuparsi se il client viene hackerato?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Creazione dell'applicazione Trust-Worthy Loader](#construction-of-the-trust-worthy-loader-application)
    -   [Lettura in background](#background-reading)
    -   [Installazione del caricatore attendibile e del Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Installazione dei file eseguibili, delle dll e dei dati del gioco](#installation-of-the-game-executables-dlls-and-data)
    -   [Codice di modifica dell'elenco di controllo di accesso](#access-control-list-modification-code)
    -   [Installazioni per utenti avanzati](#installations-for-advanced-users)
    -   [Verifica dell'attendibilità del caricatore](#the-loaders-verification-of-trust)
    -   [Convalida dei dati](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Perché i client MMOG hanno requisiti diversi per i tradizionali giochi acquistati al dettaglio

La natura costantemente connessa e in evoluzione di MMOG rende un requisito fondamentale per fornire aggiornamenti regolari del codice client e del contenuto per correggere le vulnerabilità di sicurezza ed estendere l'esperienza di gioco. Con la possibilità di aggiornamenti quasi giornalieri, lo scenario MMOG richiede una gestione attenta per garantire un'esperienza intuitiva. Questo comportamento è diverso rispetto al modello di acquisto al dettaglio tradizionale, in cui è possibile fornire un numero ridotto di patch vicino alla data di spedizione al dettaglio del prodotto. La Windows Installer tecnologia limitata per l'applicazione di patch per gli utenti fornita con il sistema operativo è progettata per gestire un numero ridotto di patch per le applicazioni e non per la grande quantità e la massima frequenza richiesta da MMOG. Spesso è necessario che i sistemi di applicazione di patch personalizzati vengano sviluppati per soddisfare le esigenze di MMOG, inclusi i requisiti speciali specifici per il particolare MMOG sviluppato.

Poiché molti computer sono connessi a Internet, Windows Vista e Windows 7 presentano restrizioni e misure di sicurezza più complesse per gli utenti, che limitano l'accesso alle applicazioni per le varie aree del disco rigido. A differenza di Windows XP, queste restrizioni sono abilitate per la modalità predefinita per gli account utente. Queste restrizioni devono essere prese in considerazione quando si progetta il layout di un gioco, un file eseguibile e i dati e il sistema di applicazione delle patch associato. Per altri dettagli sulle misure di sicurezza fornite dal sistema operativo, vedere [controllo dell'account utente per sviluppatori di giochi](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Panoramica di una catena di approcci di attendibilità

L'approccio di aggiornamento personalizzato presentato in questo white paper si basa sul fatto che un'applicazione di caricatore attendibile è installata nella cartella programmi protetti, mantenendo i file eseguibili dei giochi e i dati in un'area condivisa accessibile da tutti gli utenti. Una catena di trust inizia con il caricatore che esegue controlli di validità sui file binari e sui dati del gioco prima dell'avvio.

![la catena di attendibilità inizia con un caricatore attendibile](images/mmo-installation-best-practices-01.gif)

Il caricatore attendibile deve avere una logica sufficiente per essere in grado di verificare che l'eseguibile del gioco e altri file binari non siano stati manomessi prima di avviare il gioco. Il caricatore può inoltre verificare i dati del gioco con la frequenza necessaria. Tuttavia, le dimensioni dei dati del gioco sono in genere troppo grandi per consentire la verifica ogni volta in un singolo passaggio. Un approccio alternativo consiste nell'usare un modello di campionamento che garantisce che la verifica dell'intero set di dati venga eseguita in un periodo di tempo prolungato. L'applicazione Loader può contenere un motore di patch del gioco, che fornisce un metodo di attendibilità degno da per integrare gli aggiornamenti con il gioco installato.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Tutti gli elementi vengono convalidati sul server, perché è necessario preoccuparsi se il client viene hackerato?

Non è possibile considerare attendibile che il client non sia stato compromesso; è pertanto comune per i server MMOG convalidare tutti i dati ricevuti dal client. Sebbene questa elaborazione possa identificare i client di gioco compromessi o barare nell'universo del gioco, il server non è in grado di identificare facilmente tutti i problemi a cui è possibile esporre il client di gioco. È importante rafforzare la protezione da hacker che vogliono usare il client come piattaforma per gli attacchi al servizio, ad altri utenti o anche semplicemente come vettore per attaccare i computer client. L'applicazione delle tecniche di firma del codice e di verifica dei dati consente di rilevare i client compromessi prima di essere eseguiti. Poiché il meccanismo di applicazione delle patch richiede l'esposizione di file binari eseguibili e DLL non protetti dalle autorizzazioni di sola lettura standard per i file di programma, la convalida di questi file prima dell'avvio è importante per la sicurezza complessiva del sistema.

Questo modello non tenta di gestire lo scenario utente malintenzionato di amministrazione in cui il caricatore stesso potrebbe diventare compromesso ma è incentrato sulla protezione degli utenti standard dal codice alterato per l'esecuzione accidentale. Le tecniche di convalida dei client server tradizionali sono in realtà l'unica possibile mitigazione per gli amministratori di sistema client dannosi.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Creazione dell'applicazione Trust-Worthy Loader

### <a name="background-reading"></a>Lettura in background

I lettori devono acquisire familiarità con la seguente documentazione, che fornisce i dettagli della tecnologia di base per garantire la procedura consigliata per l'attendibilità basata su software.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Firma del codice
</dt> <dd>

[Firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) su MSDN

</dd> </dl>

La sezione seguente illustra in dettaglio le API che devono essere usate per costruire l'applicazione Loader, che supporta il layout del disco per l'installazione e la verifica del controllo di attendibilità.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Installazione del caricatore attendibile e del Patcher

Il caricatore attendibile e la versione di base dell'utilità Patcher devono essere installati nella cartella programmi protetti sul disco rigido come nelle installazioni tradizionali. Per l'installazione e l'applicazione di patch dell'applicazione Loader sono necessari i diritti di amministratore ed è quindi importante ridurre al minimo la frequenza di aggiornamento per il caricatore, in modo da garantire che gli utenti finali non debbano elevare spesso il numero di patch per l'utente, anche Windows Installer se è possibile usare l'applicazione di patch per i caricatori.

Vedere l'articolo patching Game software in Windows XP, Windows Vista e Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Installazione dei file eseguibili, delle dll e dei dati del gioco

Per semplificare gli aggiornamenti standard degli utenti del gioco senza privilegi amministrativi, è necessario installare l'eseguibile dei giochi, le dll e i dati in un'area del disco rigido che sia accessibile in scrittura per tutti gli utenti. Il sistema operativo fornisce un'area "tutti gli utenti dati dell'applicazione" che può essere usata come percorso predefinito per l'installazione. [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) deve essere usato con la \_ \_ chiave AppData comune CSIDL per determinare il percorso del file per quest'area. È importante che non venga fatta alcuna ipotesi sul percorso a cui viene restituita la chiave, perché può essere configurabile dall'utente.

L'installazione deve modificare o gestire le autorizzazioni per la cartella in modo da ottenere l'accesso all-user-Shared-Write necessario per l'aggiornamento del titolo. Con le autorizzazioni corrette, la funzionalità di aggiornamento del gioco del programma di caricamento può facilmente applicare patch al gioco senza la necessità di privilegi speciali da parte di un account utente, inclusi i tempi di avvio da parte degli utenti standard.

### <a name="access-control-list-modification-code"></a>Codice di modifica dell'elenco di controllo di accesso

Per Windows XP, è necessario eseguire il codice per modificare manualmente l'elenco di controllo di accesso (ACL). di seguito è riportato un esempio di funzione che illustra come eseguire questa operazione:

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

Questo esempio di codice funziona anche per Windows Vista e Windows 7; Tuttavia, forniscono anche l'utilità della riga di comando icacls per modificare gli ACL dei file che è possibile scegliere di usare.

Lo strumento fornisce una guida dettagliata quando viene eseguito, tuttavia, un esempio di utilizzo per lo strumento è:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Questo utilizzo consentirà all'utente le autorizzazioni di eliminazione e scrittura DAC per la cartella di gioco archiviate nelle aree tutti gli utenti del disco rigido.

### <a name="installations-for-advanced-users"></a>Installazioni per utenti avanzati

Per gli scenari di installazione avanzata degli utenti, è possibile che un utente desideri specificare il percorso di installazione dei giochi manualmente. La selezione della directory deve essere limitata a uno all'esterno dei file di programma per assicurarsi che la cartella si trovi in un'area realmente condivisibile del disco rigido. Il percorso selezionato dall'utente deve essere usato solo per i file exe e i dati dei giochi, perché il caricatore del gioco e gli exe delle patch devono sempre essere installati nella cartella programmi protetti per una maggiore sicurezza.

### <a name="the-loaders-verification-of-trust"></a>Verifica dell'attendibilità del caricatore

Windows fornisce la funzione [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) per verificare la validità del codice firmato ed è basata sui servizi di crittografia nel sistema operativo. La funzione è completamente documentata in MSDN: **WinVerifyTrust** function.

Il programma di esempio seguente su MSDN descrive in dettaglio l'uso della funzione per determinare se un eseguibile del programma è firmato con un certificato valido: [esempio C programma: verifica della firma di un file PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).

Ai fini della verifica che l'eseguibile del gioco firmato sia attendibile per l'esecuzione dall'interno del caricatore, sarà sufficiente l'azione di verifica generica:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

\_ \_ Verifica generica azione Wintrust \_ \_ v2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Significato
</dt> <dd>

Verificare un file o un oggetto utilizzando il provider di criteri Authenticode.

</dd> </dl>

La funzione accetta un argomento della struttura di input che contiene le informazioni necessarie al provider di attendibilità per elaborare l'azione specificata. In genere, come nel caso di esempio precedente, la struttura include informazioni che identificano l'oggetto che deve essere valutato dal provider di attendibilità.

Il formato della struttura è specifico dell'identificatore dell'azione. Nell'argomento seguente su MSDN viene illustrata la struttura di esempio per la struttura di [**\_ dati**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) Wintrust provider: wintrust.

Se il provider di attendibilità verifica che l'oggetto sia considerato attendibile per l'azione specificata, il valore restituito è zero. Nessun altro valore oltre a zero deve essere considerato un risultato positivo.

### <a name="data-validation"></a>Convalida dei dati

Il meccanismo di coprogettazione supporta solo la firma di alcuni tipi specifici di file, inclusi i file eseguibili, le dll, i pacchetti Windows Installer (file con estensione msi) e i file CAB (CAB). L'API [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) non deve essere usata per verificare che i file di dati di grandi dimensioni (ad esempio file con estensione cab) non siano stati manomessi, in quanto si verificano problemi di prestazioni e stabilità durante la convalida di file di grandi dimensioni. Gli eseguibili di programma tendono a essere sufficientemente piccoli da consentire l'esecuzione di un controllo di attendibilità totale usando il provider WinTrust, ma i file di dati per i giochi sono spesso dell'area di autenticazione di molti gigabyte. L'approccio adottato dal caricatore per la verifica dei dati del gioco deve essere quello in cui viene testato un piccolo campione del set di dati in fase di esecuzione del gioco. Questo approccio consente di distribuire il costo dei test di verifica rispetto alla durata dell'esperienza di gioco e di offrire un'esperienza utente uniforme senza tempi di attesa prolungati. Per ottenere questo risultato, potrebbe essere necessaria un'attenta organizzazione dei dati. Alcuni MMOG adottano un approccio basato su database per gestire, gestire e verificare la correttezza delle risorse dei giochi nel tempo.

Dal punto di vista della sicurezza, il codice client deve essere progettato in modo da non considerare attendibili i file di dati anche se si usa un tipo di convalida dei dati di base con il caricatore attendibile. Devono essere usati controlli di intestazione, hash e altri controlli di integrità tradizionali. Il lavoro per la protezione avanzata del codice i/O del client deve essere eseguito anche usando tecniche quali i test fuzzy, oltre a sfruttare gli strumenti di analisi del codice statico automatici, ad esempio l'opzione **/Analyze** in visual Studio 2005 e visual Studio 2008 (disponibile in Visual Studio Team System e il compilatore gratuito fornito con il Windows SDK).

Per ulteriori informazioni sulla sicurezza del software, vedere procedure consigliate per la [sicurezza nello sviluppo di giochi](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 