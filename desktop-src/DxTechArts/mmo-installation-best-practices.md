---
title: Procedure consigliate per l'installazione di giochi online massively multiplayer
description: Questo articolo descrive la creazione di una catena di progettazione di trust per l'installazione client massively multiplayer online games (MMOG) e sistemi di aggiornamento dei giochi personalizzati che funzionano bene con Windows e il modello di sicurezza di Windows Vista e Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b574bdf2ae98b28fabed97340d6aa38b1a864c24519bb6532d0aa4069882efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815437"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Procedure consigliate per l'installazione di giochi online massively multiplayer

Questo articolo descrive la creazione di una catena di progettazione di trust per l'installazione client massively multiplayer online games (MMOG) e sistemi di aggiornamento dei giochi personalizzati che funzionano bene con Windows e il modello di sicurezza di Windows Vista e Windows 7. L'approccio è progettato per abilitare l'applicazione di patch ai titoli MMOG, supportando al tempo stesso gli account utente standard, che hanno accesso limitato al disco rigido e al Registro di sistema.

-   [Perché i clienti MMOG hanno requisiti diversi rispetto ai giochi tradizionali acquistati al dettaglio](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Panoramica di un approccio a catena di attendibilità](#overview-of-a-chain-of-trust-approach)
-   [Tutto viene convalidato nel server, perché è necessario preoccuparsi se il client viene violato?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Costruzione dell'applicazione Trust-Worthy Loader](#construction-of-the-trust-worthy-loader-application)
    -   [Lettura in background](#background-reading)
    -   [Installazione di Trusted Loader e Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Installazione di file eseguibili, DLL e dati del gioco](#installation-of-the-game-executables-dlls-and-data)
    -   [Codice di modifica dell'elenco di controllo di accesso](#access-control-list-modification-code)
    -   [Installazioni per utenti avanzati](#installations-for-advanced-users)
    -   [Verifica dell'attendibilità del caricatore](#the-loaders-verification-of-trust)
    -   [Convalida dei dati](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Perché i clienti MMOG hanno requisiti diversi rispetto ai giochi tradizionali acquistati al dettaglio

La natura costantemente connessa e in continua evoluzione dei gruppi di gestione dei dispositivi di gestione dei dispositivi di gestione dei contenuti costituisce un requisito fondamentale per fornire aggiornamenti regolari del codice client e del contenuto per correggere le vulnerabilità di sicurezza ed estendere l'esperienza di gioco. Con la possibilità di aggiornamenti quasi giornalieri, lo scenario MMOG richiede un'attenta gestione per garantire un'esperienza facile da usare. Ciò differisce dal modello di acquisto al dettaglio tradizionale in cui un numero ridotto di patch può essere fornito vicino alla data di spedizione al dettaglio del prodotto. La tecnologia di applicazione di patch limitate del programma di installazione di Windows fornita con il sistema operativo è progettata per gestire un numero ridotto di patch dell'applicazione e non la quantità elevata e l'alta frequenza necessarie per gli MMOG. È quindi spesso necessario sviluppare sistemi di applicazione di patch personalizzati per soddisfare le esigenze degli MMOG, inclusi eventuali requisiti speciali specifici per il particolare MMOG in fase di sviluppo.

Poiché molti computer sono connessi a Internet, Windows Vista e Windows 7 hanno restrizioni di sicurezza e misure di sicurezza più complesse per gli utenti, che limitano l'accesso delle applicazioni a diverse aree del disco rigido. A Windows XP, queste restrizioni sono abilitate per la modalità predefinita per gli account utente. Queste restrizioni devono essere prese in considerazione durante la progettazione del layout di un gioco, di un eseguibile e di dati e del sistema di applicazione delle patch associato. Per altre informazioni sulle misure di sicurezza fornite dal sistema operativo, vedere [Controllo dell'account utente per sviluppatori di giochi](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Panoramica di un approccio a catena di attendibilità

L'approccio di aggiornamento personalizzato presentato in questo white paper si basa sull'installazione di un'applicazione del caricatore attendibile nella cartella Programmi protetta mantenendo i file eseguibili dei giochi e i dati in un'area condivisa accessibile all'utente. Una catena di attendibilità inizia con il caricatore che esegue controlli di validità sui file binari e sui dati del gioco prima dell'avvio.

![la catena di attendibilità inizia con un caricatore attendibile](images/mmo-installation-best-practices-01.gif)

Il caricatore attendibile deve avere una logica sufficiente per poter verificare che l'eseguibile del gioco e altri file binari non siano stati manomissionati prima di avviare il gioco. Il caricatore può anche verificare i dati del gioco con la frequenza necessaria, tuttavia le dimensioni dei dati del gioco sono in genere troppo grandi per consentirne il controllo ogni volta in un singolo passaggio. Un approccio alternativo consiste nell'usare un modello di campionamento che garantisca che la verifica dell'intero set di dati si verifichi in un periodo di tempo prolungato. L'applicazione del caricatore può contenere un motore di applicazione di patch per il gioco, che fornisce un metodo affidabile per integrare gli aggiornamenti con il gioco installato.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Tutto viene convalidato nel server, perché è necessario preoccuparsi se il client viene violato?

Non è possibile considerare attendibile che il client non sia stato compromesso. pertanto è comune per i server MMOG convalidare tutti i dati ricevuti dal client. Anche se questa elaborazione può identificare i client di gioco compromessi o barati all'interno dell'universo di gioco, il server non può identificare facilmente tutti i problemi a cui il client di gioco può essere esposto. È importante rafforzare la protezione dagli hacker che vogliono usare il client come piattaforma per gli attacchi al servizio, ad altri utenti o anche semplicemente come vettore per attaccare i computer client stessi. L'applicazione di tecniche di firma del codice e verifica dei dati consente di rilevare i client compromessi prima di essere eseguiti. Poiché il meccanismo di applicazione delle patch richiede l'esposizione di file binari eseguibili e DLL non protetti dalle autorizzazioni standard di sola lettura nei file di programma, la convalida di questi file prima di avviarli è importante per la sicurezza complessiva del sistema.

Questo modello non tenta di gestire lo scenario utente amministratore dannoso in cui il caricatore stesso potrebbe essere compromesso, ma si concentra sulla protezione degli utenti standard dall'esecuzione accidentale di codice manomesso. Le tecniche tradizionali di convalida server-client sono in realtà l'unica possibile mitigazione per gli amministratori di sistema client dannosi.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Costruzione dell'applicazione Trust-Worthy Loader

### <a name="background-reading"></a>Lettura in background

I lettori devono acquisire familiarità con la documentazione seguente, che fornisce informazioni dettagliate sulla tecnologia di base per garantire le procedure consigliate per l'attendibilità basata su software.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Firma del codice
</dt> <dd>

[Firma Authenticode per sviluppatori di giochi](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>Signtool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) su MSDN

</dd> </dl>

Nella sezione seguente vengono fornite informazioni dettagliate sulle API da usare per costruire l'applicazione loader, che supportano il layout del disco per l'installazione e la verifica del controllo dell'attendibilità.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Installazione di Trusted Loader e Patcher

Il caricatore attendibile e la versione di base dell'utilità patcher devono essere installati nella cartella Programmi protetti nel disco rigido come nelle installazioni tradizionali. L'installazione e l'applicazione di patch dell'applicazione del caricatore richiedono diritti di amministratore, quindi è importante ridurre al minimo la frequenza di aggiornamento per il caricatore per garantire che gli utenti finali non devono elevare spesso, anche se è possibile usare l'applicazione di patch utente limitate del programma di installazione di Windows per evitare l'elevazione delle patch del caricatore.

Vedere l'articolo Patching Game Software in Windows XP, Windows Vista e Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Installazione di file eseguibili, DLL e dati del gioco

Per facilitare gli aggiornamenti degli utenti Standard del gioco senza privilegi amministrativi, l'eseguibile, le DLL e i dati dei giochi devono essere installati in un'area del disco rigido accessibile in scrittura per tutti gli utenti. Il sistema operativo fornisce un'area "All Users Application Data" che può essere usata come percorso predefinito per l'installazione. [**SHGetFolderPath deve**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) essere usato con la chiave CSIDL \_ COMMON \_ APPDATA per determinare il percorso del file per questa area. È importante non fare ipotesi sul percorso restituito da questa chiave perché può essere configurabile dall'utente.

L'installazione deve modificare o gestire le autorizzazioni della cartella per ottenere l'accesso all-user-shared-write necessario per aggiornare il titolo. Con le autorizzazioni corrette, la funzionalità di aggiornamento del gioco del programma caricatore può facilmente applicare patch al gioco senza la necessità di privilegi speciali da qualsiasi account utente, inclusi gli orari in cui vengono avviati dagli utenti standard.

### <a name="access-control-list-modification-code"></a>Codice di modifica dell'elenco di controllo di accesso

Per Windows XP, è necessario eseguire codice per modificare manualmente l'elenco di controllo di accesso (ACL), ecco una funzione di esempio che illustra come eseguire questa operazione:

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

Questo esempio di codice funziona anche per Windows Vista e Windows 7; Tuttavia, forniscono anche gli icacl dell'utilità della riga di comando per modificare gli ACL dei file che è possibile scegliere di usare.

Lo strumento fornisce una guida dettagliata quando viene eseguito, tuttavia, un esempio di utilizzo per lo strumento è:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Questo utilizzo concederà all'utente le autorizzazioni Rex Delete e Write DAC nella cartella game archiviata nelle aree Tutti gli utenti del disco rigido.

### <a name="installations-for-advanced-users"></a>Installazioni per utenti avanzati

Per gli scenari di installazione utente avanzata, un utente potrebbe voler specificare manualmente il percorso di installazione dei giochi. La selezione della directory deve essere limitata a una all'esterno dei file di programma per assicurarsi che la cartella si trova in un'area realmente gestibile del disco rigido. Il percorso selezionato dall'utente deve essere usato solo per i file exe dei giochi e i dati, perché i game Loader e Patcher exe devono sempre essere installati nella cartella Programmi sicuri per una maggiore sicurezza.

### <a name="the-loaders-verification-of-trust"></a>Verifica dell'attendibilità del caricatore

Windows fornisce la [**funzione WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) per controllare la validità del codice firmato ed è basata sui servizi di crittografia nel sistema operativo. La funzione è completamente documentata in MSDN: **Funzione WinVerifyTrust.**

Il programma di esempio seguente in MSDN illustra in dettaglio l'uso della funzione per determinare se un eseguibile del programma è firmato con un certificato valido: Programma C di esempio: verifica della firma di [un file PE.](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)

Ai fini della verifica dell'attendibilità dell'esecuzione del file eseguibile del gioco firmato dall'interno del caricatore, l'azione Di verifica generica sarà sufficiente:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

WINTRUST \_ ACTION \_ GENERIC \_ VERIFY \_ V2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Significato
</dt> <dd>

Verificare un file o un oggetto usando il provider di criteri Authenticode.

</dd> </dl>

La funzione accetta un argomento della struttura di input che contiene informazioni necessarie al provider di attendibilità per elaborare l'azione specificata. In genere, come nel caso dell'esempio precedente, la struttura include informazioni che identificano l'oggetto che il provider di attendibilità deve valutare.

Il formato della struttura è specifico dell'identificatore di azione. L'argomento seguente in MSDN illustra in dettaglio la struttura di esempio per il provider WinTrust: [**WINTRUST \_ DATA**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) Structure.

Se il provider di attendibilità verifica che l'oggetto sia attendibile per l'azione specificata, il valore restituito è zero. Nessun altro valore oltre a zero deve essere considerato un risultato positivo.

### <a name="data-validation"></a>Convalida dei dati

Il meccanismo di assegnazione del codice supporta solo la firma di alcuni tipi specifici di file, tra cui file eseguibili, DLL, pacchetti del programma di installazione di Windows (file .msi) e file cab (.cab). L'API [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) non deve essere usata per verificare che file di dati di grandi dimensioni (ad esempio file .cab) non siano stati manomissioni, in quanto si verificano alcuni problemi di prestazioni e stabilità durante la convalida di file di dimensioni molto grandi. I file eseguibili del programma tendono a essere sufficientemente piccoli da poter eseguire un controllo di attendibilità totale usando il provider WinTrust, ma i file di dati per i giochi sono spesso di dimensioni di molti gigabyte. L'approccio assunto dal caricatore per la verifica dei dati del gioco deve essere quello in cui un piccolo campione del set di dati viene testato nel tempo di esecuzione del gioco. Questo approccio consente di distribuire il costo dei test di verifica per tutta la durata dell'esperienza di gioco e di offrire un'esperienza utente senza tempi di attesa lunghi. A tale scopo, potrebbe essere necessaria un'organizzazione attenta dei dati. Alcuni MMOG adottano un approccio di database per gestire, gestire e verificare la correttezza degli asset di gioco nel tempo.

Dal punto di vista della sicurezza, il codice client deve essere progettato per non considerare attendibili i file di dati anche se si usa un tipo di convalida dei dati di base con il caricatore attendibile. Devono essere utilizzati controlli di intestazione, hash e altri controlli di integrità tradizionali. Il lavoro per la protezione avanzata del codice di I/O del client deve essere eseguito anche usando tecniche come il test fuzz, nonché sfruttando gli strumenti di analisi statica automatica del codice, ad esempio l'opzione **/analyze** in Visual Studio 2005 e Visual Studio 2008 (disponibile in Visual Studio Team System e il compilatore gratuito fornito con Windows SDK).

Per altre informazioni sulla sicurezza del software, vedere [Procedure di sicurezza consigliate per lo sviluppo di giochi](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 