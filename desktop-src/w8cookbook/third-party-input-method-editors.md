---
title: Editor dei metodi di input di terze parti
description: Editor dei metodi di input di terze parti
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104566937"
---
# <a name="third-party-input-method-editors"></a>Editor dei metodi di input di terze parti

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** -Windows Server 2012  


## <a name="description"></a>Descrizione

Gli IME (Input Method Editor) sono componenti software che consentono a un utente di digitare il testo in una lingua con più caratteri rispetto a quelli che possono essere rappresentati su una tastiera. Si tratta di un problema comune, ma non limitato alle lingue asiatiche orientali. Anziché ogni singolo carattere visualizzato in una singola chiave, gli utenti digitano combinazioni di chiavi che vengono quindi interpretate dall'IME. L'IME genera il carattere corrispondente al set di tratti chiave, che talvolta presenta all'utente un elenco di caratteri possibili da selezionare e quindi inserisce il carattere nella finestra di controllo di modifica dell'app dell'utente.

In passato, Windows ha consentito l'esecuzione di IME di terze parti nel sistema Windows e questa funzionalità continua per Windows 8. Gli utenti possono installare un IME di terze parti e usarlo. Viene inoltre avanzata la protezione avanzata del sistema e dei processi per prevenire gli IME dannosi, migliorare la sicurezza e migliorare l'esperienza utente.

In Windows 8 sono disponibili le seguenti informazioni:

-   Supporto IME di terze parti per tastiere hardware e tastiere touch
-   I fornitori IME di terze parti devono seguire le linee guida Microsoft per sviluppare gli IME per Windows 8
-   Gli IME di terze parti devono essere firmati digitalmente
-   Gli IME di terze parti devono essere compatibili con il Framework di servizi di testo (TSF) e i flag IME appropriati devono essere impostati per essere eseguiti correttamente in Windows 8
-   Gli IME di terze parti legacy potranno essere eseguiti in app desktop, ma verranno bloccati nelle app di Windows Store
-   Gli IME di terze parti possono utilizzare il layout di tastiera touch fornito da Windows per collegare l'IME, in modo che gli utenti possano utilizzare il proprio IME con tastiere touch. Tuttavia, alcune funzioni degli IME predefiniti per le tastiere touch non saranno disponibili per gli IME di terze parti
-   Windows Defender rimuoverà gli IME dannosi dal sistema Windows

## <a name="manifestation"></a>Manifestazione

**Modifiche al metodo di input e alla lingua di input**

Anziché visualizzare tutte le icone della modalità IME con l'icona di personalizzazione IME, viene visualizzata solo un'icona della modalità IME con l'icona di personalizzazione IME. Le due figure seguenti mostrano il riquadro a comparsa di input di Windows 8 e il riquadro a comparsa IME, con IME giapponese come metodo di input corrente. Se si fa clic sull'icona di personalizzazione IME, è possibile cambiare i metodi di input.

![metodi di input switch](images/inputindicator2.png)

Se si fa clic sull'icona modalità IME, è possibile passare a un'altra modalità IME.

![cambia modalità IME](images/inputindicator1.png)

Se un IME si basa sulla barra della lingua per mostrare le icone in modalità in Windows 7, è necessario modificare l'IME per visualizzare l'icona di personalizzazione e l'icona della modalità nell'indicatore di input in Windows 8.

> [!Note]  
> Nota: i dettagli su come un IME può mostrare l'icona di personalizzazione e l'icona della modalità nel SysTray sulla barra delle applicazioni del desktop verranno documentati e pubblicati pubblicamente nelle linee guida per gli IME per Windows 8.

 

**Nuovo ambiente Windows**

L'ambiente in Windows 8 modifica il panorama per gli IME. I concetti relativi alle app di Windows Store, ai contenitori di app del contesto locale e alle restrizioni API negli IME non erano presenti in Windows 7. Alcuni IME di Windows 7 esistenti smettono di rispondere quando vengono eseguiti all'interno di un'app di Windows Store e pertanto non consentono l'esecuzione di IME legacy nelle app di Windows Store. Inoltre, assicurarsi che le nuove versioni degli IME vengano convalidate per assicurarsi che siano compatibili con il nuovo ambiente dell'interfaccia utente prima che vengano eseguite all'interno di app di Windows Store.

## <a name="mitigation"></a>Strategia di riduzione del rischio

È possibile utilizzare un IME compatibile con desktop nel sistema. Questo potrebbe essere l'opzione migliore se si usano principalmente le applicazioni desktop e si vuole continuare a usare un IME legacy preferito per l'input. Si consiglia di utilizzare un IME per Windows 8 e di interrompere l'utilizzo di IME legacy/non certificati. Le notifiche vengono fornite sia dal linguaggio CPL che dall'opzione di input per avvertire gli effetti dell'utilizzo di un IME compatibile con il desktop.

Se un IME compatibile con il desktop non funziona nel sistema, viene visualizzato uno dei comportamenti seguenti:

-   Il linguaggio CPL UI labels compatibile con i desktop IME e visualizza un messaggio che indica che gli IME non compatibili funzionano solo nelle app desktop.
-   Il riquadro a comparsa di input grigio-compatibile con i desktop IME quando l'utente si trova all'interno di applicazioni Windows Store. Ciò indica che l'IME non funziona in questa app. Nel desktop gli IME compatibili con il desktop non sono disattivati. Se si passa a app di Windows Store con un IME non compatibile e si rende conto che l'IME è disattivato, usare l'indicatore di input per passare a un IME compatibile con le app di Windows Store.

Gli IME legacy o compatibili con il desktop sono limitati a queste condizioni:

-   Aggiornamento da Windows 7 a Windows 8 con IME di terze parti nel sistema
-   Il fornitore non ha rilasciato una versione compatibile con Windows 8 e l'utente prova a usare una versione esistente di Windows 7 nel frattempo

## <a name="solution"></a>Soluzione

**Generale**

Usare l'infrastruttura del Framework di servizi di testo (TSF) esistente per implementare la logica IME e i controlli comuni delle app di Windows Store per le interfacce utente. Creare finestre di proprietà per ospitare l'interfaccia utente.

Sono state aggiunte nuove API di ricerca per migliorare la stima della ricerca e fornire un'esperienza di ricerca più pulita nell'interfaccia utente.

Vengono inoltre aggiunte le API per notificare gli IME di terze parti quando viene richiamata una tastiera touch per proteggere l'interfaccia utente dalla tastiera touch. Per gli IME di terze parti viene automaticamente caricato un layout di tastiera tocco classico predefinito. Non è necessario alcun lavoro aggiuntivo per l'integrazione con il layout di tastiera tocco classico. Tuttavia, gli IME di terze parti saranno in grado di richiedere un layout tocco alternativo.

Acquisire familiarità con le linee guida IME per Windows 8 in modo da poter promuovere i principi chiave dell'esperienza utente dell'app di Windows Store nell'IME. Gli IME che rispettano le linee guida devono impostare un flag per indicare che l'IME è compatibile con la progettazione Microsoft. Windows 8 blocca tutti gli IME compatibili con il desktop dall'esecuzione nelle app di Windows Store.

La firma digitale, oltre alla revoca da parte di Windows Defender, impedisce l'installazione di IME dannosi nel sistema Windows 8. Al momento della verifica dell'identità, il file con estensione dll di un IME di terze parti è firmato digitalmente. Solo gli IME con questa firma digitale possono essere installati nel sistema senza che venga visualizzato un messaggio di avviso critico per l'utente. Gli utenti possono segnalare gli IME dannosi. Dopo che un IME è stato determinato come dannoso, Windows Defender lo rimuove dal sistema Windows.

**Text Services Framework**

Per poter essere eseguito in Windows 8, l'IME deve essere compatibile con TSF. Windows 8 blocca l'esecuzione di IME non compatibili con TSF nelle app di Windows Store. Quando viene avviata un'app, TSF carica il file IME. dll per l'IME selezionato dall'utente nel processo dell'app.

> [!Note]  
> Per fornire funzionalità o interfacce utente separate tra app di Windows Store e app desktop, il file con estensione dll caricato da TSF può verificare il tipo di app in cui viene caricato. L'IME chiama il metodo [ITfThreadMgrEx:: GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) e controlla il \_ flag TF MDF \_ IMMERSIVEMODE e può attivare la logica dell'app diversa a seconda del risultato.

 

Quando un IME viene caricato in un'app di Windows Store, è soggetto alle stesse restrizioni del contenitore di app dell'app stessa. Questo comportamento assicura che gli IME non siano in grado di violare i contratti di protezione delle app di Windows Store, sebbene dispongano dell'accesso a Desktop SDK (poiché non sono distribuiti o certificati da Windows Store). Alcune funzioni attualmente eseguite dagli IME sono interessate all'interno di un contenitore di app. Tali funzioni includono:

-   File dizionario
-   Aggiornamento Internet
-   Apprendimento immediato
-   Condivisione delle informazioni tra i processi

Per ulteriori informazioni, vedere le linee guida relative a IME per Windows 8.

Gli IME legacy non funzionano nelle app di Windows Store per evitare il rischio di esperienze utente non valide, inclusi gli arresti del sistema. Gli IME compatibili con le app di Windows Store devono essere autodichiarati impostando un flag che indica questa compatibilità. Questo flag viene fornito da TSF nella struttura TF \_ INPUTPROCESSORPROFILE. Per informazioni dettagliate su come usare questo flag per dichiarare un IME di terze parti come compatibile con le app di Windows Store, è possibile documentare e pubblicare pubblicamente le linee guida IME per Windows 8.

Gli IME compatibili con le app di Windows Store possono essere eseguiti in app desktop o app di Windows Store. Gli IME non compatibili possono essere eseguiti solo nei processi desktop.

**Interfaccia utente**

Sebbene gli IME di terze parti abbiano accesso alle API di windowing desktop, devono seguire le stesse restrizioni dell'API Windows dell'app in cui sono in esecuzione. Un IME, ad esempio, non può essere disegnato sopra un'app di Windows Store mentre è attivo in un'app desktop. Le restrizioni API sono destinate a impedire questi scenari:

-   App desktop che assumono lo stato attivo dalle app di Windows Store
-   Disegno di app desktop nell'app di Windows Store
-   App desktop che interferiscono con le app di Windows Store

**Supporto tastiera touch**

Sebbene il supporto per la tastiera touch (TKB) sia ancora disponibile per i fornitori di IME di terze parti, un'esperienza di tastiera touch completamente personalizzabile e integrata non viene fornita in Windows 8. Tuttavia, gli IME di terze parti possono mappare gli IME con il layout di tastiera ottimizzato per il tocco. Per impostazione predefinita, Windows Soft Input Panel (SIP) fornisce un layout di tastiera classico per gli IME di terze parti. Poiché la tastiera classica genera eventi chiave simili a quelli di una tastiera hardware, attualmente non è previsto alcun requisito di implementazione speciale per gli IME di terze parti per lavorare con una tastiera touch. La gestione dell'input per gli eventi chiave hardware gestirà anche gli eventi principali dei layout tocco classici.

> [!Note]  
> Nota: gli IME potrebbero dover iniziare a gestire gli eventi di input Unicode se è stato esteso il supporto TKB per includere anche i layout di tastiera ottimizzati.

 

Un IME di terze parti può scegliere di utilizzare il layout di tastiera ottimizzato per l'IME. Per altre informazioni, vedere le linee guida per IME di terze parti.

Assicurarsi che l'interfaccia utente del riquadro candidato (e altri elementi dell'interfaccia utente) non venga disegnata sotto la tastiera touch. Nella maggior parte dei casi, l'app deve ridimensionare la finestra per tenere conto della tastiera touch. Tuttavia, se un'app non esegue questa operazione, gli IME possono comunque usare l'API InputPaneFramework per apprendere la posizione della tastiera touch. Gli IME di terze parti possono usare questa API per ottenere lo spazio dello schermo utilizzato dalla tastiera a tocco prima di disegnare le interfacce utente candidate (o altre) e di rifluire la relativa interfaccia utente per evitare di disegnare sotto la tastiera touch.

**Ricerca**

In Windows 8, le app di Windows Store possono fornire con facilità agli utenti le funzionalità di ricerca implementando il [contratto di ricerca](/previous-versions/windows/apps/hh464906(v=win.10)) e integrando il riquadro di ricerca. Il riquadro di ricerca è una posizione centralizzata per consentire agli utenti di eseguire ricerche in tutte le app. Windows consente alle app che usano il riquadro di ricerca di ottenere gli utenti nel punto in cui desiderano procedere nel minor tempo possibile. In particolare, per gli utenti IME fornisce un'esperienza di ricerca univoca che consente agli IME compatibili di integrarsi con Windows 8 per una maggiore efficienza e usabilità.

Un IME è compatibile con l'esperienza di ricerca integrata se soddisfa questi criteri:

-   È compatibile con l'ambiente app di Windows Store
-   Implementa le API in modalità UILess di TFS
-   Implementa le API di integrazione della ricerca TFS:
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

Quando viene attivato nel riquadro di ricerca, l'IME compatibile viene inserito in modalità UILess e non è in grado di visualizzarne l'interfaccia utente. Invia invece i candidati alla conversione a Windows, che li visualizzerà nel controllo elenco candidati inline.

L'IME invia anche candidati Windows che devono essere usati per eseguire la ricerca corrente. questi candidati potrebbero essere gli stessi dei candidati alla conversione oppure possono essere personalizzati per la ricerca. I candidati di ricerca validi soddisfano questi criteri:

-   Nessun prefisso sovrapposto
-   Nessuna stima candidata (solo completamento)

Gli IME che non soddisfano i criteri e non sono compatibili con la ricerca vengono mostrati allo stesso modo di altri controlli delle app di Windows Store e non sono in grado di sfruttare i vantaggi dell'integrazione dell'interfaccia utente e dei candidati alla ricerca. Le app ricevono le query solo dopo che l'utente ha terminato la composizione.

Quando un'app che supporta il contratto di ricerca riceve una query, l'evento di query includerà una matrice "queryTextAlternatives" contenente tutte le alternative note, classificate dalla più pertinente (probabilmente) a meno pertinente (probabilmente improbabile). Ogni volta che vengono fornite alternative, l'app deve considerare ogni alternativa come una query e restituire tutti i risultati che corrispondono a una delle alternative (come se l'utente avesse eseguito più query contemporaneamente), eseguendo essenzialmente una query "or" al servizio fornendo i risultati. Per migliorare le prestazioni, le app limiteranno spesso la corrispondenza alle 10 alternative più rilevanti.

**Firma digitale IME**

Tutti gli IME di terze parti devono essere firmati digitalmente per poter essere installati nel sistema Windows 8 come IME. Utilizzando SmartScreen, gli utenti possono visualizzare un messaggio di avviso quando Scarica un IME non firmato dal Web. Per ottenere un certificato e firmare i file:

-   **USA firma Authenticode per la firma digitale di programmi**
    -   Ottenere un certificato di firma codice Authenticode valido da una delle numerose autorità di certificazione supportate da Windows
    -   Usare gli strumenti di sviluppo (ad esempio [signtool.exe](../seccrypto/signtool.md)) per firmare le app prima della distribuzione
    -   Per ulteriori informazioni e una descrizione dettagliata del processo di firma del codice, vedere il post di Blog [relativo alla firma del codice Authenticode](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing)
-   **Assicurarsi che i download non vengano rilevati come malware**
    -   I programmi scaricati che vengono rilevati e confermati come malware influiscono sulla reputazione del download e sulla reputazione del certificato digitale usato per firmare il file
-   **Richiedi certificazione Windows**
    -   Visitare la pagina relativa alla certificazione delle app Windows su MSDN

Per altre informazioni, vedere gli articoli relativi alle firme digitali e alla firma del codice:

-   [Panoramica di Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Verifica dell'integrità e dell'autenticità](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Che cosa sono i certificati digitali?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Se un IME **non è** firmato, l'utente riceve questo messaggio di avviso quando tenta di scaricare l'IME:

![messaggio di avviso IME non firmato](images/downloadwarning02-fhu-ivu.png)

Se un IME è firmato, gli utenti visualizzeranno invece questo messaggio:

![messaggio firmato IME](images/downloadwarning01-fhu-vcu.png)

In base a queste notifiche, gli utenti possono scegliere se eliminare il file o ignorare l'avviso ed eseguire il programma scaricato.

**Revoca IME**

Gli IME che sono dannosi o che non seguono le linee guida IME di Windows 8 possono essere rimossi dal sistema utilizzando Windows Defender. Per ulteriori informazioni sugli IME dannosi, vedere l'articolo sugli [IME di terze parti in Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).

## <a name="resources"></a>Risorse

-   [Metodo ITfThreadMgrEx:: Get Active Flags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Tutto ciò che occorre sapere sulla firma del codice Authenticode](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Contratti ed estensioni per app Windows](/previous-versions/windows/apps/hh464906(v=win.10))
-   [Requisiti di certificazione per le applicazioni desktop di Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Requisiti di certificazione per le app di Windows](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Uso del kit di certificazione app Windows](../win_cert/using-the-windows-app-certification-kit.md)
-   [Panoramica di Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Verifica dell'integrità e dell'autenticità](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Procedure consigliate per la firma del codice](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Che cosa sono i certificati digitali?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 