---
title: Debug con simboli
description: Questo articolo fornisce una panoramica di alto livello su come usare al meglio i simboli nel processo di debug.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff63e2404a07a2f0ab5adcb156d83dc989b42fd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516941"
---
# <a name="debugging-with-symbols"></a>Debug con simboli

Questo articolo fornisce una panoramica di alto livello su come usare al meglio i simboli nel processo di debug. Viene illustrato come usare il server dei simboli Microsoft e come configurare e usare il proprio server di simboli privato. Queste procedure consigliate possono contribuire ad aumentare l'efficacia e la capacità di eseguire il debug dei problemi, anche nei casi in cui tutti i simboli e i file eseguibili correlati a un problema non si trovino nel computer.

-   [Symbols](#debugging-with-symbols)
-   [Uso di simboli per il debug](#using-symbols-for-debugging)
-   [Ottenere i simboli necessari](#getting-the-symbols-you-need)
    -   [Controllare se una determinata DLL o un file con estensione exe e un PDB nella stessa cartella corrispondono](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Controllare se tutte le dll e i file eseguibili in un set di cartelle hanno PDB corrispondenti](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Funzionamento di Symchk](#how-symchk-works)
-   [Server di simboli](#symbol-servers)
-   [Uso del server dei simboli Microsoft](#using-the-microsoft-symbol-server)
-   [Recupero manuale dei simboli](#getting-symbols-manually)
-   [Configurazione di un server di simboli](#setting-up-a-symbol-server)
-   [Aggiunta di simboli a un server di simboli](#adding-symbols-to-a-symbol-server)
-   [Procedure consigliate](#best-practices)

## <a name="symbols"></a>Simboli

Per il debug sono disponibili vari tipi di simboli. Includono i simboli CodeView, COFF, DBG, SYM, PDB e persino i simboli di esportazione generati da una tabella di esportazione di file binari. In questo white paper vengono descritti solo i simboli di formato VS.NET e PDB, perché si tratta del formato preferito più recente. Vengono generati per impostazione predefinita per i progetti compilati con Visual Studio.

La generazione di file PDB per gli eseguibili della versione non influisce sulle ottimizzazioni o modifica in modo significativo le dimensioni dei file generati. In genere, l'unica differenza è il percorso e il nome file del file PDB è incorporato nell'eseguibile. Per questo motivo, è necessario produrre sempre i file PDB, anche se non si vuole inviarli con l'eseguibile.

I file PDB vengono generati se un progetto viene compilato usando l'opzione del compilatore **/Zi** o **/Zi** (Produci informazioni PDB), insieme all'opzione del linker **/debug** (genera informazioni di debug). I file PDB generati dal compilatore vengono combinati e scritti in un unico file PDB che si trova nella stessa directory del file eseguibile.

Per impostazione predefinita, i file PDB contengono le informazioni seguenti:

-   Simboli pubblici (in genere tutte le funzioni, variabili statiche e globali)
-   Elenco di file oggetto responsabili di sezioni di codice nell'eseguibile
-   Informazioni sull'ottimizzazione del puntatore ai frame (Polinesia)
-   Informazioni sul nome e sul tipo per le variabili locali e le strutture di dati
-   Informazioni sul file di origine e sul numero di riga

Se si è interessati alle persone che usano le informazioni sul file PDB per aiutare a decodificare l'eseguibile, è anche possibile generare file PDB rimossi usando l'opzione del linker **/PDBSTRIPPED: filename** . Se si dispone di file PDB esistenti per cui si desidera rimuovere informazioni private, è possibile utilizzare uno strumento denominato pdbcopy, che fa parte degli strumenti di debug per Windows.

Per impostazione predefinita, i file PDB rimossi contengono le informazioni seguenti:

-   Simboli pubblici (in genere solo funzioni non statiche e variabili globali)
-   Elenco di file oggetto responsabili di sezioni di codice nell'eseguibile
-   Informazioni sull'ottimizzazione del puntatore ai frame (Polinesia)

Si tratta delle informazioni minime necessarie per consentire il debug affidabile. Le informazioni minime rendono anche difficile ottenere informazioni aggiuntive sul codice sorgente originale. Poiché vengono generati sia un file PDB rimosso che un normale file PDB, è possibile fornire la versione rimossa agli utenti che potrebbero richiedere funzionalità di debug limitate, mantenendo al tempo stesso la riservatezza completa PDB. Si noti che **/PDBSTRIPPED** genera un secondo file PDB più piccolo, quindi assicurarsi di usare il file PDB corretto quando si generano compilazioni per la distribuzione estesa. Per un progetto tipico, un PDB normale può avere una dimensione di pochi megabyte, ma una versione con rimozione del PDB può essere solo di poche centinaia di kilobyte.

## <a name="using-symbols-for-debugging"></a>Uso di simboli per il debug

Quando si esegue il debug di un'applicazione che si è arrestata in modo anomalo, il debugger tenta di visualizzare le funzioni nello stack che hanno causato l'arresto anomalo. Senza un file PDB, il debugger non è in grado di risolvere i nomi delle funzioni, i relativi parametri o le variabili locali archiviate nello stack. Se si esegue il debug di eseguibili a 32 bit, in alcune situazioni non è possibile ottenere tracce dello stack affidabili senza simboli. Talvolta è possibile esaminare i valori non elaborati nello stack e individuare i valori che possono essere indirizzi restituiti, ma possono essere facilmente confusi con i riferimenti alle funzioni o i dati.

Se le funzioni nello stack corrente sono state compilate usando l'ottimizzazione di omissione dei puntatori ai frame (**/Oy**) e se i simboli non sono presenti, il debugger non è in grado di determinare in modo affidabile la funzione che ha chiamato la funzione corrente. Questo perché senza le informazioni di ottimizzazione del puntatore ai frame (Polinesia) contenute in PDB, il debugger non può basarsi sul registro del puntatore del frame (EBP) per puntare al puntatore del frame precedente salvato e all'indirizzo restituito della funzione padre. Ma indovina. A volte si ottiene il diritto. Tuttavia, spesso risulta errato, che può essere fuorviante. Se viene visualizzato un avviso relativo ai simboli mancanti o non è stato caricato alcun simbolo, come nell'esempio seguente, non considerare attendibile lo stack da tale punto verso il basso.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

In molti casi, è possibile continuare il debug senza simboli, perché il problema si trova in una posizione con simboli accurati e non è necessario esaminare le funzioni più in basso nello stack di chiamate. Anche se una libreria presente nello stack di chiamate non dispone di PDB, purché siano stati compilati con puntatori ai frame, il debugger dovrebbe essere in grado di indovinare correttamente le funzioni padre. A partire da Windows XP Service Pack 2, tutti i file DLL e file eseguibili di Windows vengono compilati con la Polinesia disabilitata, perché il debug risulta più accurato. La disabilitazione di Polinesia consente inoltre ai profiler di campionamento di scorrere lo stack in fase di esecuzione, con un effetto minimo sulle prestazioni. Nelle versioni di Windows precedenti a Windows XP SP2, per tutti i file binari del sistema operativo sono necessari file di simboli corrispondenti contenenti informazioni sulla Polinesia, per consentire il debug e la profilatura accurati.

Se si esegue il debug di file eseguibili nativi a 64 bit, non sono necessari file di simboli per produrre analisi dello stack valide, perché i sistemi operativi e i compilatori x64 sono progettati per non richiederli. Tuttavia, sono ancora necessari i file di simboli per recuperare i nomi delle funzioni, i parametri di chiamata e le variabili locali.

Tuttavia, in alcuni casi è particolarmente difficile eseguire il debug senza simboli. Se, ad esempio, si esegue il debug di un programma per il quale è stato compilato un file PDB e si verifica un arresto anomalo di un callback da una funzione in una DLL per cui non sono disponibili simboli, non sarà possibile visualizzare la funzione che ha causato il callback, perché non sarà possibile decodificare lo stack. Questa situazione si verifica spesso nelle librerie di terze parti, se non vengono forniti PDB o nei componenti del sistema operativo precedenti, se PDB non sono disponibili. I callback spesso si verificano durante il passaggio dei messaggi, l'enumerazione, l'allocazione di memoria o la gestione delle eccezioni. Il debug di queste funzioni senza uno stack accurato può essere frustrante.

Per eseguire il debug in modo affidabile di piccoli dump generati in un computer diverso o che si sono arrestati in modo anomalo nel codice di cui non si è proprietari, è importante poter accedere a tutti i simboli e i file binari per gli eseguibili a cui viene fatto riferimento nel mini-dump. Se i simboli e i file binari sono disponibili da un server di simboli, vengono ottenuti automaticamente dal debugger. Per altre informazioni sui minidump, vedere l'white paper analisi dei [dump di arresto anomalo](/windows/desktop/DxTechArts/crash-dump-analysis) del sistema.

## <a name="getting-the-symbols-you-need"></a>Ottenere i simboli necessari

Visual Studio e altri debugger Microsoft, ad esempio WinDbg, vengono in genere configurati in modo da funzionare solo se si compila un'applicazione e ne viene eseguito il debug nel computer. Se è necessario assegnare il file eseguibile a un altro utente, se si dispone di più versioni di una DLL o di un file con estensione exe nel computer o se si desidera eseguire il debug accurato di un'applicazione che utilizza Windows o altre librerie, ad esempio DirectX, è necessario comprendere in che modo i debugger trovano e caricano i simboli. Il debugger usa il percorso di ricerca dei simboli specificato dall'utente, disponibile in opzioni di \\ debug \\ dei simboli in Visual Studio, o nella variabile di \_ \_ ambiente del percorso dei simboli NT \_ . In genere, il debugger cerca la corrispondenza di pdb nei percorsi seguenti:

-   Percorso specificato nella DLL o nel file eseguibile.

    Se è stata compilata una DLL o un file eseguibile nel computer, per impostazione predefinita il linker inserisce il percorso completo e il nome file del file PDB associato all'interno della DLL o del file eseguibile. Quando si esegue il debug, il debugger verifica prima di tutto se il file di simboli esiste nel percorso specificato all'interno della DLL o del file eseguibile. Questa operazione è utile perché i simboli sono sempre disponibili per il codice compilato nel computer.

-   PDB che può essere presente nella stessa cartella della DLL o del file eseguibile.
-   Qualsiasi cartella della cache di simboli locale.
-   Tutti i server di simboli di condivisione file di rete locale.
-   Tutti i server di simboli Internet, ad esempio il server di simboli Microsoft.

Per assicurarsi di avere tutti i PDB necessari per un debug accurato, installare gli strumenti di debug per Windows. Le versioni 32 e 64 bit sono disponibili in [strumenti di debug per Windows](/windows-hardware/drivers/debugger/).

Uno strumento utile installato con questo pacchetto è symchk.exe. Può aiutare a identificare i simboli mancanti o non corretti. Questo strumento ha un numero elevato di possibili opzioni della riga di comando. Ecco due dei più utili e usati di frequente.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Controllare se una determinata DLL o un file con estensione exe e un PDB nella stessa cartella corrispondono

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

L'opzione **/s** indica a **Symchk** di cercare i simboli solo nella cartella corrente e di non cercare i server dei simboli.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Controllare se tutte le dll e i file eseguibili in un set di cartelle hanno PDB corrispondenti

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

L'opzione **/r** imposta **Symchk** in modo da attraversare le cartelle in modo ricorsivo per verificare che tutti i file eseguibili abbiano PDB corrispondenti. Senza l'opzione **/s** , **Symchk** usa il \_ percorso del simbolo NT corrente \_ \_ per cercare i simboli in qualsiasi server privato o locale oppure nei server dei simboli Microsoft. Lo strumento **Symchk** Cerca solo i simboli per i file eseguibili (. exe,. dll e simili). Non è possibile usare la ricerca con caratteri jolly per i simboli per i file non eseguibili.

### <a name="how-symchk-works"></a>Funzionamento di Symchk

Quando il linker genera file con estensione dll, eseguibili e PDB, archivia i GUID identici in ogni file. Il GUID viene utilizzato dagli strumenti per determinare se un determinato file PDB corrisponde a una DLL o a un file eseguibile. Se si modifica una DLL o un file eseguibile, usando un editor di risorse o la codifica di protezione della copia, oppure modificando le informazioni sulla versione, il GUID viene aggiornato e il debugger non è in grado di caricare il file PDB. Per questo motivo, è molto importante evitare di modificare la DLL o il file eseguibile dopo che è stato creato dal linker.

È inoltre possibile utilizzare l'utilità DUMPBIN fornita con VS.NET per visualizzare i percorsi dei simboli in cui viene eseguita la ricerca e per verificare se i file di simboli vengono trovati corrispondenti a una DLL o a un file eseguibile specifico. Ad esempio:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Server di simboli

Un server di simboli è un repository per più versioni di file eseguibili e di simboli. Contiene i file di simboli stessi o i puntatori ai file di simboli associati. I debugger comprendono come usare i server di simboli e possono usarli per la ricerca di simboli mancanti o sconosciuti.

I file eseguibili e DLL sono anche disponibili nel server dei simboli Microsoft. In questo modo è possibile eseguire il debug degli arresti anomali ed esaminare il codice per i file del sistema operativo che potrebbero non esistere nel computer. Se un debugger rileva un file eseguibile o una DLL che non esiste nel sistema usato per il debug, richiede automaticamente sia i simboli che una copia del file binario dai server dei simboli Microsoft. Questa operazione è utile se si esegue il debug di un componente con numerose versioni, ad esempio msvcrt.dll, ed è necessario esaminare il codice per una versione che non esiste nel computer. Questo consente anche di eseguire il debug di mini dump generati in un sistema operativo diverso dal sistema usato per il debug.

Microsoft pubblica tutti i file PDB per tutti i sistemi operativi e altri componenti ridistribuiti, ad esempio DirectX SDK, nel server di simboli accessibile esternamente. In questo modo è più semplice eseguire il debug di un'applicazione che usa questi file DLL o eseguibili. È possibile usare il server dei simboli Microsoft per risolvere i simboli, insieme a tutti i simboli locali per i componenti compilati nel computer.

È possibile configurare il computer per l'utilizzo del server dei simboli Microsoft, che consente di accedere a tutti i file di simboli Microsoft. È anche possibile configurare un server di simboli privato per la società, il team o la rete, che può essere usato per archiviare più versioni precedenti di un progetto su cui si sta lavorando o per fornire una cache locale per i simboli usati dal server dei simboli Microsoft.

Per usare un server di simboli, specificare il percorso di ricerca in una variabile di ambiente \_ denominata \_ percorso del simbolo NT \_ . I debugger e gli strumenti moderni, ad esempio WinDbg, NTSD o Visual Studio, usano automaticamente questo percorso per la ricerca di simboli.

Quando un debugger cerca i simboli, cerca innanzitutto in locale. Quindi Cerca i server di simboli. Quando trova un simbolo corrispondente, trasferisce il file di simboli nella cache locale. I simboli per una DLL o un file eseguibile tipico sono compresi tra 1 e 100 MB. Di conseguenza, se si esegue il debug di un processo che include molte dll, potrebbe essere necessario del tempo per risolvere tutti i simboli e trasferirli a una cache locale.

## <a name="using-the-microsoft-symbol-server"></a>Uso del server dei simboli Microsoft

Il server dei simboli Microsoft consente di ottenere tutti i simboli più recenti, inclusi i simboli per i file modificati o con patch. Il server dei simboli Microsoft è disponibile all'indirizzo <https://msdl.microsoft.com/download/symbols> .

È possibile accedere al server di simboli in uno dei modi seguenti:

-   Immettere direttamente l'indirizzo del server. In Visual Studio scegliere **Opzioni** dal menu **strumenti** , quindi fare clic su **debug**, quindi scegliere **simboli**.
-   Usare il percorso dei simboli NT della variabile di ambiente \_ \_ \_ . È consigliabile adottare questa soluzione.

    Viene usato da tutti gli strumenti di debug. Viene anche usato da Visual Studio e viene letto e decodificato all'apertura di Visual Studio. Di conseguenza, se si modifica, è necessario riavviare Visual Studio.

    Questa variabile di ambiente consente di specificare più server di simboli, ad esempio un server di simboli privato interno. Consente inoltre di specificare una directory della cache locale per archiviare PDB per tutti i simboli cercati dai server di simboli, sia internamente che tramite Internet.

La sintassi per la \_ variabile del percorso dei simboli NT è la seguente \_ \_ :

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Sostituire \[ cache locale \] con il nome di una directory nel computer in cui si vuole archiviare una cache di tutti i simboli usati, ad esempio% SystemRoot% \\ symbols o c: \\ symbols.

Il \[ Server dei simboli privati \] è facoltativo. Può puntare a un server di simboli che si trova nella rete oppure può puntare a un server di simboli condiviso dal team, dal gruppo di prodotti o dalla società.

Per usare solo il server di simboli Microsoft insieme a una cache locale di simboli, per velocizzare l'accesso tramite Internet, usare l'impostazione seguente per il \_ \_ percorso dei simboli NT \_ :

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

È possibile trovare altre opzioni per il \_ \_ percorso dei simboli NT \_ nel file della Guida installato con il pacchetto Microsoft Debugging Tools for Windows.

Gli eseguibili senza simboli possono aumentare il tempo necessario per avviare un debugger se si usa un server di simboli. Questo perché il debugger esegue una query sul server di simboli ogni volta che tenta di caricare il file eseguibile. Per questo motivo, è consigliabile richiedere sempre i simboli per tutti i componenti.

Potrebbe non essere possibile richiedere simboli per ogni componente. ad esempio, i driver video possono avere dll nello spazio di processo e i file PDB necessari sono disponibili nel server dei simboli Microsoft. In questo caso si verifica un piccolo ritardo quando si avvia una sessione di debug.

Per evitare anche questo piccolo ritardo, è possibile eseguire il debugger una volta per memorizzare nella cache tutti i simboli localmente dal server dei simboli Microsoft. Modificare quindi il \_ \_ \_ percorso del simbolo NT per rimuovere il server dei simboli Microsoft. A meno che non vengano modificati i file eseguibili, i controlli per i file eseguibili privi di simboli non richiederanno una query su Internet, perché sono presenti copie memorizzate nella cache locale di tutti i simboli necessari dal server dei simboli Microsoft.

## <a name="getting-symbols-manually"></a>Recupero manuale dei simboli

Se il debugger è stato configurato correttamente, vengono caricati automaticamente i simboli richiesti dalla cache locale o da un server di simboli. Per ottenere i simboli solo per un singolo eseguibile o per una cartella di file eseguibili, è possibile usare **Symchk**. Se ad esempio si desidera scaricare i simboli per il \_ file d3dx930.dll nella cartella di sistema di Windows nella directory corrente, è possibile utilizzare il comando seguente:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

Lo strumento **Symchk** ha molti altri usi. Per informazioni dettagliate, vedere **Symchk/?** o consultare la documentazione di Microsoft debug Tools per Windows.

## <a name="setting-up-a-symbol-server"></a>Configurazione di un server di simboli

La configurazione di un server di simboli è molto semplice. È utile per i motivi seguenti:

-   Per risparmiare larghezza di banda o per velocizzare la risoluzione dei simboli per la società, il team o il prodotto. Un server di simboli interno in una condivisione file locale nella rete memorizza nella cache tutti i riferimenti a server dei simboli esterni, ad esempio il server di simboli Microsoft. È possibile accedere rapidamente a un server di simboli locale o interno da molte persone nello stesso momento. Quindi, consente di risparmiare larghezza di banda e la latenza che le richieste di simboli duplicate possono creare.
-   Per archiviare i simboli per le compilazioni precedenti, le versioni o le versioni esterne dell'applicazione. Archiviando i simboli per le compilazioni in un server di simboli a cui è possibile accedere facilmente, è possibile eseguire il debug di arresti anomali e problemi in queste compilazioni in qualsiasi computer con un debugger e una connessione al server di simboli locale. Questa operazione è particolarmente utile se si esegue il debug di minidump generati da file eseguibili non compilati, ovvero compilazioni generate da un altro programmatore o da un computer di compilazione. Se i simboli per tali compilazioni sono archiviati nel server di simboli, si otterrà un debug affidabile e accurato.
-   Per rendere aggiornati i simboli. Quando i componenti vengono aggiornati, ad esempio i componenti del sistema operativo che vengono modificati da Windows Update o da DirectX SDK, è comunque possibile eseguire il debug usando tutti i simboli più recenti.

La configurazione di un server di simboli nella propria rete locale è semplice come creare una condivisione file in un server e concedere agli utenti autorizzazioni complete per accedere alla condivisione, per creare file e cartelle. Questa condivisione deve essere creata in un sistema operativo server, ad esempio Windows Server 2003, in modo che il numero di utenti che possono accedere simultaneamente alla condivisione non sia limitato.

Ad esempio, se si configura una condivisione file nei \\ \\ simboli mainserver \\ , i membri del team impostano il \_ percorso del \_ simbolo NT \_ su quanto segue:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

Quando vengono recuperati i simboli, i file e le cartelle vengono visualizzati nella \\ \\ \\ directory condivisa dei simboli mainserver, oltre che nelle singole cache, nella \\ directory c: symbols.

Si tratta in genere di tutto ciò che è necessario per la configurazione e l'uso del proprio server di simboli o del server dei simboli Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Aggiunta di simboli a un server di simboli

Per aggiungere, eliminare o modificare i file in una condivisione server di simboli, usare lo strumento symstore.exe. Questo strumento fa parte del pacchetto Microsoft Debugging Tools for Windows. La documentazione completa sui server di simboli, lo strumento SymStore e i simboli di indicizzazione è inclusa nel pacchetto strumenti di debug per Windows.

Potrebbe essere necessario aggiungere simboli direttamente al proprio server di simboli, come parte di un processo di compilazione, oppure rendere disponibili i simboli per l'intero team per librerie o strumenti di terze parti. Il processo di aggiunta di un simbolo a una condivisione file del server di simboli è denominato simboli di indicizzazione. Esistono due modi comuni per indicizzare i simboli. Un file di simboli può essere copiato nel server di simboli. In alternativa, è possibile copiare un puntatore alla posizione del simbolo nel server di simboli. Se si dispone di una cartella di archiviazione che contiene le compilazioni precedenti, potrebbe essere necessario indicizzare i puntatori ai file PDB già presenti nella condivisione, anziché duplicare i simboli. Poiché i simboli possono talvolta avere dimensioni pari a decine di megabyte, è consigliabile pianificare in anticipo la quantità di spazio necessaria per archiviare tutte le compilazioni del progetto durante lo sviluppo. Se si indicizzano solo i puntatori a simboli, è possibile che si verifichino problemi se si rimuovono le compilazioni precedenti o si modifica il nome di una condivisione file.

Ad esempio, per indicizzare in modo ricorsivo tutti i simboli in c: \\ dxsym \\ extra \\ symbols ottenuti da ottobre 2006 DirectX SDK in una condivisione file del server di simboli denominata \\ \\ mainserver \\ symbols, è possibile usare il comando seguente:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

Il parametro **/t "comment"** viene usato per aggiungere una descrizione alla transazione che ha aggiunto i simboli. Questa operazione può essere utile quando si eseguono attività amministrative sui simboli.

## <a name="best-practices"></a>Procedure consigliate

-   Configurare la condivisione file del server di simboli per il team, la società o il prodotto.
-   Configurare \_ \_ \_ il percorso dei simboli NT in modo che punti a una cache locale, a un server di simboli privato e al server di simboli Microsoft.
-   Se un debugger non è in grado di caricare i simboli per un componente di cui si esegue il debug, contattare il proprietario del componente per richiedere i simboli, almeno un PDB rimosso.
-   Configurare un sistema di compilazione automatizzato per indicizzare i simboli nel server di simboli privato per ogni compilazione prodotta. Assicurarsi che le compilazioni distribuite siano le compilazioni generate da questo processo. Ciò garantisce che i simboli siano sempre disponibili per il debug dei problemi.
-   Configurare un server di simboli per consentire ai debugger di accedere al codice sorgente per un modulo specifico direttamente da un sistema di controllo del codice sorgente protetto da un'origine visiva o necessariamente basato su forza. Se le informazioni sul file di origine e i simboli per una versione rilasciata di un gioco sono indicizzati, gli sviluppatori che hanno accesso al server di simboli possono eseguire il debug completo del livello di origine dei problemi segnalati, senza mantenere gli ambienti di compilazione o le versioni precedenti dei file di origine nei propri computer di sviluppo. Per configurare il server di simboli per consentire l'indicizzazione delle informazioni sui file di origine, vedere la documentazione del server di origine.

 

 