---
title: Debug con simboli
description: Questo articolo offre una panoramica generale di come usare al meglio i simboli nel processo di debug.
ms.assetid: 7ce0c9c7-485c-8d72-0353-27fd2e369a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdabd1a99f203adb2422cc4bbc71c3fb2f6108a0a3869077e97683bdcf830100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070561"
---
# <a name="debugging-with-symbols"></a>Debug con simboli

Questo articolo offre una panoramica generale di come usare al meglio i simboli nel processo di debug. Spiega come usare il server di simboli Microsoft e come configurare e usare il proprio server di simboli privato. Queste procedure consigliate consentono di aumentare l'efficacia e la possibilità di eseguire il debug dei problemi, anche nei casi in cui tutti i simboli e i file eseguibili correlati a un problema non si trovano nel computer.

-   [Symbols](#debugging-with-symbols)
-   [Uso dei simboli per il debug](#using-symbols-for-debugging)
-   [Ottenere i simboli necessari](#getting-the-symbols-you-need)
    -   [Controllare se una DETERMINATA DLL o .exe file e PDB nella stessa cartella corrispondono](#check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match)
    -   [Controllare se tutte le DLL e i file eseguibili in un set di cartelle hanno file PDB corrispondenti](#check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs)
    -   [Funzionamento di symchk](#how-symchk-works)
-   [Server di simboli](#symbol-servers)
-   [Uso del server di simboli Microsoft](#using-the-microsoft-symbol-server)
-   [Recupero manuale dei simboli](#getting-symbols-manually)
-   [Configurazione di un server di simboli](#setting-up-a-symbol-server)
-   [Aggiunta di simboli a un server di simboli](#adding-symbols-to-a-symbol-server)
-   [Procedure consigliate](#best-practices)

## <a name="symbols"></a>Simboli

Per il debug sono disponibili diversi tipi di simboli. Includono simboli CodeView, COFF, DBG, SYM, PDB e anche simboli di esportazione generati da una tabella di esportazione di file binari. Questo white paper illustra solo i VS.NET e i simboli di formato PDB, perché sono il formato preferito più recente. Vengono generati per impostazione predefinita per i progetti compilati usando Visual Studio.

La generazione di file PDB per i file eseguibili di versione non influisce sulle ottimizzazioni o modifica significativamente le dimensioni dei file generati. In genere, l'unica differenza è il percorso e il nome file del file PDB è incorporato nel file eseguibile. Per questo motivo, è consigliabile produrre sempre file PDB, anche se non si vuole spedirli con l'eseguibile.

I file PDB vengono generati se un progetto viene compilato usando l'opzione del compilatore **/Zi** o **/ZI** (Produce PDB Information), insieme all'opzione del linker **/DEBUG** (Genera informazioni di debug). I file PDB generati dal compilatore vengono combinati e scritti in un singolo file PDB che si trova nella stessa directory del file eseguibile.

Per impostazione predefinita, i file PDB contengono le informazioni seguenti:

-   Simboli pubblici (in genere tutte le funzioni, variabili statiche e globali)
-   Elenco di file oggetto responsabili di sezioni di codice nel file eseguibile
-   Informazioni sull'ottimizzazione del puntatore ai frame (FPO)
-   Informazioni sul nome e sul tipo per le variabili locali e le strutture di dati
-   Informazioni sul file di origine e sul numero di riga

Se si è interessati a utenti che usano le informazioni sul file PDB per eseguire il reverse engineer dell'eseguibile, è anche possibile generare file PDB con striping usando l'opzione del linker **/PDBSTRIPPED:filename.** Se si dispone di file PDB esistenti da cui si desidera rimuovere informazioni private, è possibile usare uno strumento denominato pdbcopy, che fa parte degli strumenti di debug per Windows.

Per impostazione predefinita, i file PDB con striped contengono le informazioni seguenti:

-   Simboli pubblici (in genere solo funzioni non statiche e variabili globali)
-   Elenco di file oggetto responsabili di sezioni di codice nel file eseguibile
-   Informazioni sull'ottimizzazione del puntatore ai frame (FPO)

Si tratta delle informazioni minime necessarie per consentire il debug affidabile. Le informazioni minime rendono anche difficile ottenere informazioni aggiuntive sul codice sorgente originale. Poiché vengono generati sia un file PDB con striped che un normale file PDB, è possibile fornire la versione stripped agli utenti che potrebbero richiedere capacità di debug limitate, ma mantenere riservati i file PDB completi. Si noti **che /PDBSTRIPPED** genera un secondo file PDB più piccolo, quindi assicurarsi di usare il file PDB corretto quando si generano compilazioni per la distribuzione a livello generale. Per un progetto tipico, un PDB normale può avere dimensioni di pochi megabyte, ma una versione del PDB spogliata può essere di poche centinaia di kilobyte.

## <a name="using-symbols-for-debugging"></a>Uso dei simboli per il debug

Quando si esegue il debug di un'applicazione che si è verificata in modo anomalo, il debugger tenta di visualizzare le funzioni nello stack che hanno causato l'arresto anomalo del sistema. Senza un file PDB, il debugger non può risolvere i nomi delle funzioni, i relativi parametri o le variabili locali archiviate nello stack. Se si esegue il debug di file eseguibili a 32 bit, in alcune situazioni non è possibile ottenere tracce dello stack affidabili senza simboli. In alcuni casi è possibile esaminare i valori non elaborati nello stack e determinare quali valori possono essere indirizzi restituiti, ma questi possono essere facilmente confusi con i riferimenti alle funzioni o i dati.

Se le funzioni nello stack corrente sono state compilate usando l'ottimizzazione Omit Frame Pointers (**/Oy**) e se i simboli non sono presenti, il debugger non può determinare in modo affidabile quale funzione ha chiamato la funzione corrente. Ciò è dovuto al fatto che senza le informazioni FPO (Frame Pointer Optimization) contenute nei PDB, il debugger non può basarsi sul registro dei puntatori ai frame (EBP) per puntare al puntatore ai frame precedente salvato e all'indirizzo restituito della funzione padre. In alternativa, si può indovinare. A volte si ottiene il giusto. Tuttavia, spesso si sbaglia, il che può essere fuorviante. Se viene visualizzato un avviso relativo ai simboli mancanti o nessun simbolo caricato, come nell'esempio seguente, non considerare attendibile lo stack da quel punto in basso.

``` syntax
SWPerfTest.exe!TextFunction(... ...)    Line 59    C++
d3dx9d.dll!008829b5()
[Frames below may be incorrect and/or missing, no symbols loaded for d3dx9d.dll]
SWPerfTest.exe!main(int argc=, const char * * argv=)  Line 328 + 0x12 bytes     C++
SWPerfTest.exe!__mainCRTStartup() Line 716 + 0x17 bytes    C
kernel32.dll!@BaseThreadInitThunk@12() + 0x12 bytes
ntdll.dll!__RtlUserThreadStart@8() + 0x27 bytes
```

In molti casi, è possibile continuare il debug senza simboli, perché il problema si trova in una posizione con simboli accurati e non è necessario esaminare le funzioni più avanti nello stack di chiamate. Anche se in una libreria che si trova nello stack di chiamate non sono disponibili PDB, purché siano stati compilati con puntatori a frame, il debugger dovrebbe essere in grado di indovinare correttamente le funzioni padre. A partire da Windows XP Service Pack 2, tutti Windows FILE DLL e file eseguibili vengono compilati con FPO disabilitato, perché rende il debug più accurato. La disabilitazione di FPO consente inoltre ai profiler di campionamento di eseguire lo stack durante la fase di esecuzione, con un impatto minimo sulle prestazioni. Nelle versioni di Windows precedenti Windows XP SP2, tutti i file binari del sistema operativo richiedono file di simboli corrispondenti che contengono informazioni FPO, per consentire un debug e una profilatura accurati.

Se si esegue il debug di file eseguibili nativi a 64 bit, non sono necessari file di simboli per produrre tracce dello stack valide, perché i sistemi operativi e i compilatori x64 sono progettati per non richiederli. Tuttavia, sono comunque necessari file di simboli per recuperare i nomi delle funzioni, i parametri di chiamata e le variabili locali.

Tuttavia, in alcuni casi è particolarmente difficile eseguire il debug senza simboli. Ad esempio, se si esegue il debug di un programma per cui è stato compilato un file PDB e si arresta in modo anomalo in un callback da una funzione in una DLL per cui non sono presenti simboli, non sarà possibile vedere quale funzione ha causato il callback, perché non sarà possibile decodificare lo stack. Questo problema si verifica spesso nelle librerie di terze parti, se non vengono forniti PDB o nei componenti del sistema operativo precedenti, se i PDB non sono disponibili. I callback si verificano spesso durante il passaggio del messaggio, l'enumerazione, l'allocazione di memoria o la gestione delle eccezioni. Il debug di queste funzioni senza uno stack accurato può essere frustrante.

Per eseguire in modo affidabile il debug di mini dump generati in un computer diverso o che si sono arrestati in modo anomalo nel codice di cui non si è proprietari, è importante poter accedere a tutti i simboli e i file binari per i file eseguibili a cui viene fatto riferimento nel minidump. Se i simboli e i file binari sono disponibili da un server di simboli, vengono ottenuti automaticamente dal debugger. Per altre informazioni sui minidump, vedere l'white paper. [](/windows/desktop/DxTechArts/crash-dump-analysis)

## <a name="getting-the-symbols-you-need"></a>Ottenere i simboli necessari

Visual Studio e altri debugger Microsoft, ad esempio WinDbg, sono in genere impostati per funzionare solo se si compila un'applicazione e si esegue il debug nel proprio computer. Se è necessario fornire l'eseguibile a un altro utente, se si dispone di più versioni di una DLL o di un file .exe nel computer o se si vuole eseguire il debug accurato di un'applicazione che usa Windows o altre librerie, ad esempio DirectX, è necessario comprendere come i debugger trovano e caricano i simboli. Il debugger usa il percorso di ricerca dei simboli specificato dall'utente, disponibile in Simboli di debug delle opzioni in Visual Studio, o la variabile di ambiente \\ \\ NT SYMBOL \_ \_ \_ PATH. In genere, il debugger cerca i PDB corrispondenti nei percorsi seguenti:

-   Percorso specificato nella DLL o nel file eseguibile.

    Se nel computer è stata compilata una DLL o un file eseguibile, per impostazione predefinita il linker inserisce il percorso completo e il nome del file PDB associato all'interno della DLL o del file eseguibile. Quando si esegue il debug, il debugger verifica innanzitutto se il file di simboli esiste nel percorso specificato all'interno della DLL o del file eseguibile. Ciò è utile perché sono sempre disponibili simboli per il codice compilato nel computer.

-   PDB che possono essere presenti nella stessa cartella della DLL o del file eseguibile.
-   Qualsiasi cartella della cache di simboli locale.
-   Qualsiasi server di simboli di condivisione file di rete locale.
-   Qualsiasi server di simboli Internet, ad esempio il server di simboli Microsoft.

Per assicurarsi di avere tutti i PDB necessari per un debug accurato, installare gli strumenti di debug per Windows. Le versioni a 32 e 64 bit sono disponibili in Strumenti di [debug per Windows](/windows-hardware/drivers/debugger/).

Un utile strumento installato con questo pacchetto è symchk.exe. Può essere utile per identificare simboli mancanti o non corretti. Questo strumento ha un numero elevato di potenziali opzioni della riga di comando. Ecco due delle più utili e usate di frequente.

### <a name="check-if-a-given-dll-or-exe-file-and-pdb-in-the-same-folder-match"></a>Controllare se una DETERMINATA DLL o .exe file e PDB nella stessa cartella corrispondono

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" testing.dll /s .

SYMCHK: FAILED files = 0
SYMCHK: PASSED + IGNORED files = 1
```

/s **.** **l'opzione indica a symchk** di cercare i simboli solo nella cartella corrente e di non cercare in alcun server di simboli.

### <a name="check-if-all-the-dlls-and-executable-files-in-a-set-of-folders-have-matching-pdbs"></a>Controllare se tutte le DLL e i file eseguibili in un set di cartelle hanno file PDB corrispondenti

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" *.* /r
```

**L'opzione /r** imposta **symchk** per attraversare in modo ricorsivo le cartelle, per verificare che tutti i file eseguibili hanno PDB corrispondenti. Senza **l'opzione /s,** **symchk** usa il percorso NT SYMBOL corrente per cercare simboli in qualsiasi server privato o locale o nei \_ server di simboli \_ \_ Microsoft. Lo **strumento symchk** cerca solo i simboli per i file eseguibili (.exe, .dll e simili). Non è possibile usare caratteri jolly per cercare simboli per file non eseguibili.

### <a name="how-symchk-works"></a>Funzionamento di symchk

Quando il linker genera .dll file eseguibili e PDB, archivia GUID identici in ogni file. Il GUID viene usato dagli strumenti per determinare se un determinato file PDB corrisponde a una DLL o a un file eseguibile. Se si modifica una DLL o un file eseguibile, usando un editor di risorse o la codifica di protezione della copia o modificando le informazioni sulla versione, il GUID viene aggiornato e il debugger non può caricare il file PDB. Per questo motivo, è molto importante evitare di modificare la DLL o il file eseguibile dopo che è stato creato dal linker.

È anche possibile usare l'utilità DUMPBIN fornita con VS.NET per visualizzare i percorsi dei simboli cercati e per verificare se vengono trovati file di simboli che corrispondono a una determinata DLL o file eseguibile. Esempio:

``` syntax
DUMPBIN /PDBPATH:VERBOSE filename.exe
```

## <a name="symbol-servers"></a>Server di simboli

Un server di simboli è un repository per più versioni di file eseguibili e di simboli. Contiene i file di simboli stessi o i puntatori ai file di simboli associati. I debugger comprendono come usare i server di simboli e possono usarli per cercare simboli mancanti o sconosciuti.

I file DLL e eseguibili sono disponibili anche dal server di simboli Microsoft. Ciò consente di eseguire il debug di arresti anomali ed esaminare il codice per i file del sistema operativo che potrebbero non esistere nel computer. Se un debugger rileva un file eseguibile o una DLL che non esiste nel sistema in uso per il debug, richiede automaticamente sia i simboli che una copia del file binario dai server di simboli Microsoft. Ciò è utile se si esegue il debug di un componente con molte versioni, ad esempio msvcrt.dll, ed è necessario esaminare il codice per una versione che non esiste nel computer. Ciò consente anche di eseguire il debug di minidump generati in un sistema operativo diverso dal sistema in uso per il debug.

Microsoft pubblica tutti i file PDB per tutti i sistemi operativi e altri componenti ridistribuiti, ad esempio DirectX SDK, nel server di simboli accessibile esternamente. Ciò semplifica il debug di un'applicazione che usa questi file DLL o eseguibili. È possibile usare il server di simboli Microsoft per risolvere i simboli, insieme ai simboli locali per i componenti compilati nel computer.

È possibile configurare il computer per l'uso del server di simboli Microsoft, che consente di accedere a tutti i file di simboli Microsoft. È anche possibile configurare un server di simboli privato per la società, il team o la rete, che può essere usato per archiviare più versioni precedenti di un progetto in uso o per fornire una cache locale per i simboli usati dal server di simboli Microsoft.

Per usare un server di simboli, specificare il percorso di ricerca in una variabile di ambiente denominata \_ NT \_ SYMBOL \_ PATH. I debugger e gli strumenti moderni, ad esempio WinDbg, NTSD o Visual Studio, usano automaticamente questo percorso per cercare i simboli.

Quando un debugger cerca i simboli, esegue prima la ricerca in locale. Viene quindi cercata nei server di simboli. Quando trova un simbolo corrispondente, trasferisce il file di simboli nella cache locale. I simboli per una DLL tipica o un file eseguibile hanno dimensioni da 1 a 100 MB. Pertanto, se si esegue il debug di un processo che include molte DLL, può essere necessario del tempo per risolvere tutti i simboli e trasferirli in una cache locale.

## <a name="using-the-microsoft-symbol-server"></a>Uso del server di simboli Microsoft

Il server di simboli Microsoft consente di ottenere tutti i simboli più recenti, inclusi i simboli per i file con patch o aggiornati. Il server di simboli Microsoft è disponibile all'indirizzo <https://msdl.microsoft.com/download/symbols> .

È possibile accedere al server di simboli in uno dei modi seguenti:

-   Immettere direttamente l'indirizzo del server. Nel Visual Studio scegliere Opzioni dal **menu** Strumenti **,** quindi **Debug** e infine **Simboli**.
-   Usare la variabile di ambiente \_ NT \_ SYMBOL \_ PATH. È consigliabile adottare questa soluzione.

    Viene usato da tutti gli strumenti di debug. Viene usato anche da Visual Studio e viene letto e decodificato quando Visual Studio si apre. Pertanto, se si modifica, è necessario riavviare Visual Studio.

    Questa variabile di ambiente consente di specificare più server di simboli, ad esempio un server di simboli privato interno. Consente inoltre di specificare una directory della cache locale per archiviare i PDB per tutti i simboli cercati dai server di simboli, sia internamente che tramite Internet.

La sintassi per la \_ variabile NT SYMBOL PATH \_ \_ è:

``` syntax
srv*[local cache]*[private symbol server]*https://msdl.microsoft.com/download/symbols
```

Sostituire la cache locale con il nome di una directory nel computer in cui si vuole archiviare una cache di tutti i simboli usati, ad esempio \[ \] %SYSTEMROOT% \\ Symbols o \\ c:.

Il \[ server di simboli privato è \] facoltativo. Può puntare a un server di simboli che si trova nella rete oppure a un server di simboli condiviso dal team, dal gruppo di prodotti o dalla società.

Per usare solo il server di simboli Microsoft insieme a una cache locale di simboli, per velocizzare l'accesso tramite Internet, usare l'impostazione seguente per \_ NT \_ SYMBOL \_ PATH:

``` syntax
srv*c:\symbols*https://msdl.microsoft.com/download/symbols
```

Altre opzioni per NT SYMBOL PATH sono disponibili nel file della Guida installato con gli strumenti di debug \_ \_ Microsoft Windows \_ pacchetto.

I file eseguibili senza simboli possono aumentare il tempo necessario per avviare un debugger se si usa un server di simboli. Questo perché il debugger esegue una query sul server di simboli ogni volta che tenta di caricare l'eseguibile. Per questo motivo, è meglio richiedere sempre simboli per tutti i componenti.

Potrebbe non essere possibile richiedere simboli per ogni componente, ad esempio i driver video potrebbero avere DLL nello spazio del processo e i file PDB necessari sono disponibili nel server di simboli Microsoft. In questo caso, si verifica un piccolo ritardo quando si avvia una sessione di debug.

Per evitare questo piccolo ritardo, è possibile eseguire il debugger una sola volta per memorizzare nella cache tutti i simboli in locale dal server di simboli Microsoft. Modificare quindi NT \_ SYMBOL PATH per rimuovere il server di simboli \_ \_ Microsoft. A meno che i file eseguibili non cambino, i controlli per i file eseguibili che non dispongono di simboli non richiederanno una query su Internet, perché si dispone di copie locali memorizzate nella cache di tutti i simboli necessari dal server di simboli Microsoft.

## <a name="getting-symbols-manually"></a>Recupero manuale dei simboli

Se il debugger è stato configurato correttamente, carica automaticamente tutti i simboli necessari dalla cache locale o da un server di simboli. Se si desidera ottenere i simboli solo per un singolo eseguibile o per una cartella di file eseguibili, è possibile usare **symchk**. Ad esempio, se si vogliono scaricare i simboli per il file30.dll d3dx9 nella cartella Windows System nella directory corrente, è possibile usare il \_ comando seguente:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symchk" c:\Windows\System32\d3dx9_30.dll /oc \.
```

Lo **strumento symchk** ha molti altri usi. Per informazioni dettagliate, **vedere symchk /?** o cercare nella documentazione microsoft debugging tools for Windows .

## <a name="setting-up-a-symbol-server"></a>Configurazione di un server di simboli

La configurazione di un server di simboli è molto semplice. È utile per i motivi seguenti:

-   Per risparmiare larghezza di banda o per velocizzare la risoluzione dei simboli per l'azienda, il team o il prodotto. Un server di simboli interno in una condivisione file locale nella rete memorizza nella cache tutti i riferimenti a server di simboli esterni, ad esempio il server di simboli Microsoft. Un server di simboli locale o interno è accessibile rapidamente da più persone contemporaneamente. Di conseguenza, consente di risparmiare larghezza di banda e la latenza che possono essere create da richieste di simboli duplicate.
-   Per archiviare i simboli per le build, le versioni o le versioni esterne precedenti dell'applicazione. Archiviando i simboli per queste compilazioni in un server di simboli a cui è possibile accedere facilmente, è possibile eseguire il debug di arresti anomali e problemi in queste compilazioni in qualsiasi computer che dispone di un debugger e di una connessione al server di simboli locale. Ciò è particolarmente utile se si esegue il debug di minidump generati da file eseguibili non compilati manualmente, ovvero compilazioni generate da un altro programmatore o da un computer di compilazione. Se i simboli per queste compilazioni sono archiviati nel server di simboli, si avrà un debug affidabile e accurato.
-   Per mantenere aggiornati i simboli. Quando i componenti vengono aggiornati, ad esempio i componenti del sistema operativo modificati da Windows Update o da DirectX SDK, è comunque possibile eseguire il debug usando tutti i simboli più recenti.

La configurazione di un server di simboli nella propria rete locale è semplice come creare una condivisione file in un server e concedere agli utenti le autorizzazioni complete per accedere alla condivisione, per creare file e cartelle. Questa condivisione deve essere creata in un sistema operativo server, ad esempio Windows Server 2003, in modo che il numero di utenti che possono accedere alla condivisione contemporaneamente non sia limitato.

Ad esempio, se si configura una condivisione file nei simboli mainserver, i membri del team impostano \\ \\ NT SYMBOL PATH su \\ \_ quanto \_ \_ segue:

``` syntax
Srv*c:\symbols*\\mainserver\symbols*https://msdl.microsoft.com/download/symbols
```

Quando vengono recuperati i simboli, i file e le cartelle vengono visualizzati nella directory condivisa dei simboli \\ \\ mainserver, nonché nelle \\ singole cache, nella directory c: \\ symbols.

Questo è in genere tutto ciò che riguarda la configurazione e l'uso del proprio server di simboli o del server di simboli Microsoft.

## <a name="adding-symbols-to-a-symbol-server"></a>Aggiunta di simboli a un server di simboli

Per aggiungere, eliminare o modificare file in una condivisione del server di simboli, usare lo strumento symstore.exe simboli. Questo strumento fa parte degli strumenti di debug Microsoft per Windows pacchetto. La documentazione completa sui server di simboli, lo strumento symstore e i simboli di indicizzazione è inclusa nel pacchetto Debugging Tools for Windows.

È possibile aggiungere simboli direttamente al proprio server di simboli, come parte di un processo di compilazione, o rendere disponibili simboli all'intero team per librerie o strumenti di terze parti. Il processo di aggiunta di un simbolo a una condivisione file del server di simboli è detto simboli di indicizzazione. Esistono due modi comuni per indicizzare i simboli. Un file di simboli può essere copiato nel server di simboli. In caso contrario, è possibile copiare un puntatore al percorso del simbolo nel server di simboli. Se si dispone di una cartella di archivio che contiene le compilazioni precedente, è possibile indicizzare i puntatori ai file PDB già presenti nella condivisione, anziché duplicare i simboli. Poiché i simboli possono talvolta avere dimensioni di decine di megabyte, è buona idea pianificare in anticipo la quantità di spazio necessario per archiviare tutte le compilazioni del progetto durante lo sviluppo. Se si indicizzano solo i puntatori ai simboli, potrebbero verificarsi problemi se si rimuovono compilazioni meno comuni o si modifica il nome di una condivisione file.

Ad esempio, per indicizzare in modo ricorsivo tutti i simboli in c: dxsym Extras Symbols ottenuti da DirectX SDK di ottobre \\ \\ 2006 in una condivisione file del server di simboli denominata \\ \\ \\ simboli mainserver, è possibile usare il \\ comando seguente:

``` syntax
"c:\Program Files\Debugging Tools for Windows\symstore" add /f "C:\dxsym\Extras\Symbols\*.pdb"
/s \\mainserver\symbols /t "October 2006 DirectX SDK " /r
```

Il **parametro /t "comment"** viene usato per aggiungere una descrizione alla transazione che ha aggiunto i simboli. Ciò può essere utile quando si eseguono attività amministrative sui simboli.

## <a name="best-practices"></a>Procedure consigliate

-   Configurare la condivisione file del server di simboli per il team, la società o il prodotto.
-   Configurare \_ NT \_ SYMBOL PATH in modo che punti a una cache \_ locale, a un server di simboli privato e al server di simboli Microsoft.
-   Se un debugger non è in grado di caricare i simboli per un componente di cui si esegue il debug, contattare il proprietario del componente per richiedere i simboli, almeno un PDB privato.
-   Configurare un sistema di compilazione automatizzato per indicizzare i simboli nel server di simboli privato per ogni compilazione prodotta. Assicurarsi che le compilazioni distribuite siano le compilazioni generate da questo processo. In questo modo si garantisce che i simboli siano sempre disponibili per il debug dei problemi.
-   Configurare un server di simboli per consentire ai debugger di accedere al codice sorgente per un modulo specifico direttamente da un sistema di controllo del codice sorgente basato su Visual Source Cassaforte o Perforce. Se le informazioni sul file di origine e i simboli per una versione rilasciata di un gioco sono indicizzati, gli sviluppatori che hanno accesso al server dei simboli possono eseguire il debug completo a livello di origine dei problemi segnalati, senza mantenere gli ambienti di compilazione o le versioni precedenti dei file di origine nei computer di sviluppo. Per configurare il server di simboli per consentire l'indicizzazione delle informazioni sul file di origine, vedere la documentazione del server di origine.

 

 
