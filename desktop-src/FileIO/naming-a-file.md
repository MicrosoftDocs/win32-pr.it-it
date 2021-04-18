---
description: Tutti i file system supportati da Windows usano il concetto di file e directory per accedere ai dati archiviati in un disco o in un dispositivo.
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: Denominazione di file, percorsi e spazi dei nomi
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 59f626c931a61255cef8be9ede594cb97924cfb0
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/04/2021
ms.locfileid: "106303664"
---
# <a name="naming-files-paths-and-namespaces"></a>Denominazione di file, percorsi e spazi dei nomi

Tutti i file system supportati da Windows usano il concetto di file e directory per accedere ai dati archiviati in un disco o in un dispositivo. Gli sviluppatori Windows che utilizzano le API di Windows per l'I/O di file e dispositivi devono comprendere le diverse regole, convenzioni e limitazioni dei nomi di file e directory.

È possibile accedere ai dati da dischi, dispositivi e condivisioni di rete usando le API di I/O di file. I file e le directory, insieme agli spazi dei nomi, fanno parte del concetto di percorso, ovvero una rappresentazione di stringa di dove ottenere i dati indipendentemente dal fatto che si trovino da un disco o da un dispositivo o da una connessione di rete per un'operazione specifica.

Alcuni file System, ad esempio NTFS, supportano file e directory collegati, che seguono anche le convenzioni di denominazione dei file e le regole come un normale file o una directory. Per altre informazioni, vedere [collegamenti reali e giunzioni](hard-links-and-junctions.md) e [reparse point e operazioni su file](reparse-points-and-file-operations.md).

Per ulteriori informazioni, vedere le sottosezioni seguenti:

-   [Nomi di file e directory](#file-and-directory-names)
    -   [Convenzioni di denominazione](#naming-conventions)
    -   [Short e Long Name](#short-vs-long-names)
-   [Percorsi](#fully-qualified-vs-relative-paths)
    -   [Percorsi completi e relativi](#fully-qualified-vs-relative-paths)
    -   [Limite lunghezza massima percorso](#maximum-path-length-limitation)
-   [Namespaces](#win32-file-namespaces) (Spazi dei nomi)
    -   [Spazi dei nomi dei file Win32](#win32-file-namespaces)
    -   [Spazi dei nomi dei dispositivi Win32](#win32-device-namespaces)
    -   [Spazi dei nomi NT](#nt-namespaces)
-   [Argomenti correlati](#related-topics)


Per informazioni sulla configurazione di Windows 10 in modo da supportare percorsi di file lunghi, vedere [limite massimo](./maximum-file-path-limitation.md)per la lunghezza del percorso.


## <a name="file-and-directory-names"></a>Nomi di file e directory

Tutti i file System seguono le stesse convenzioni di denominazione generali per un singolo file: un nome di file di base e un'estensione facoltativa, separati da un punto. Tuttavia, ogni file system, ad esempio NTFS, CDFS, exFAT, UDF, FAT e FAT32, può avere regole specifiche e diverse sulla formazione dei singoli componenti nel percorso di una directory o di un file. Si noti che una *directory* è semplicemente un file con un attributo speciale che lo designa come una directory, ma in caso contrario deve seguire tutte le stesse regole di denominazione di un file normale. Poiché la *directory* dei termini si riferisce semplicemente a un tipo speciale di file per quanto concerne la file System, in alcuni materiali di riferimento verrà usato il termine *file* generale per includere sia i concetti di directory che i file di dati. Per questo motivo, se non diversamente specificato, eventuali regole di denominazione o di utilizzo o esempi per un file devono essere applicati anche a una directory. Il termine *percorso* fa riferimento a una o più directory, barre rovesciate e possibilmente un nome di volume. Per ulteriori informazioni, vedere la sezione [percorsi](#fully-qualified-vs-relative-paths) .

Le limitazioni del numero di caratteri possono anche essere diverse e possono variare a seconda del file system e del formato del prefisso del nome percorso utilizzato. Questa operazione è ulteriormente complicata dal supporto per i meccanismi di compatibilità con le versioni precedenti. Ad esempio, il file system FAT MS-DOS precedente supporta un massimo di 8 caratteri per il nome del file di base e 3 caratteri per l'estensione, per un totale di 12 caratteri, incluso il separatore del punto. Questa operazione è comunemente nota come *nome file 8,3*. I file system FAT e NTFS di Windows non sono limitati ai nomi di file di 8,3, perché hanno un supporto per il *nome di file lungo*, ma supportano ancora la versione 8,3 dei nomi file lunghi.

### <a name="naming-conventions"></a>Convenzioni di denominazione

Le seguenti regole fondamentali consentono alle applicazioni di creare ed elaborare nomi validi per file e directory, indipendentemente dal file system:

-   Utilizzare un punto per separare il nome del file di base dall'estensione nel nome di una directory o di un file.
-   Utilizzare una barra rovesciata ( \\ ) per separare i *componenti* di un *percorso*. La barra rovesciata divide il nome del file dal percorso e un nome di directory da un altro nome di directory in un percorso. Non è possibile usare una barra rovesciata nel nome del file o della directory effettiva perché è un carattere riservato che separa i nomi in componenti.
-   Usare una barra rovesciata come parte dei [nomi di volume](naming-a-volume.md), ad esempio "c: \\ " in "c: \\ path \\ file" o " \\ \\ server \\ share" in " \\ \\ server \\ share \\ path \\ file" per i nomi di Universal Naming Convention (UNC). Per ulteriori informazioni sui nomi UNC, vedere la sezione [limite massimo](#maximum-path-length-limitation) per la lunghezza del percorso.
-   Non presupporre la distinzione tra maiuscole e minuscole. Si considerino, ad esempio, che i nomi OSCAR, Oscar e Oscar siano identici, anche se alcuni file System, ad esempio un file system conforme a POSIX, possono considerarli diversi. Si noti che NTFS supporta la semantica POSIX per la distinzione tra maiuscole e minuscole, ma questo non è il comportamento predefinito. Per ulteriori informazioni, vedere [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
-   Gli indicatori di volume (lettere di unità) non fanno distinzione tra maiuscole e minuscole. Ad esempio, "D: \\ " e "d: \\ " fanno riferimento allo stesso volume.
-   Utilizzare qualsiasi carattere nella tabella codici corrente per un nome, inclusi i caratteri Unicode e i caratteri nel set di caratteri esteso (128-255), ad eccezione dei seguenti:

    -   I seguenti caratteri riservati:

        -   < (minore di)
        -   \> (maggiore di)
        -   : (due punti)
        -   " (virgolette doppie)
        -   / (barra)
        -   \\ barra rovesciata
        -   \| (barra verticale o pipe)
        -   ? (punto interrogativo)
        -   \* (asterisco)

    -   Valore intero zero, talvolta definito carattere ASCII *NUL* .
    -   Caratteri le cui rappresentazioni integer sono comprese nell'intervallo compreso tra 1 e 31, tranne per i flussi di dati alternativi in cui sono consentiti questi caratteri. Per ulteriori informazioni sui flussi di file, vedere [flussi di file](file-streams.md).
    -   Qualsiasi altro carattere non consentito dall'file system di destinazione.

-   Utilizzare un punto come *componente* di directory in un percorso per rappresentare la directory corrente, ad esempio ". \\temp.txt ". Per ulteriori informazioni, vedere [percorsi](#fully-qualified-vs-relative-paths).
-   Usare due punti consecutivi (..) come *componente* di directory in un percorso per rappresentare l'elemento padre della directory corrente, ad esempio ". \\temp.txt ". Per ulteriori informazioni, vedere [percorsi](#fully-qualified-vs-relative-paths).
-   Non usare i nomi riservati seguenti per il nome di un file:

    CON, PRN, AUX, NUL, COM1, COM2, COM3, COM4, COM5, COM6, COM7, COM8, COM9, LPT1, LPT2, LPT3, LPT4, LPT5, LPT6, LPT7, LPT8 e LPT9. Evitare inoltre questi nomi seguiti immediatamente da un'estensione; ad esempio, NUL.txt non è consigliabile. Per altre informazioni, vedere [Spazi dei nomi](#win32-file-namespaces).

-   Non terminare il nome di un file o di una directory con uno spazio o un punto. Sebbene il file system sottostante possa supportare tali nomi, la shell di Windows e l'interfaccia utente non lo sono. Tuttavia, è accettabile specificare un punto come primo carattere di un nome. Ad esempio, ". Temp".

### <a name="short-vs-long-names"></a>Short e Long Name

Un nome di file lungo è considerato un nome di file che supera la convenzione di denominazione dello stile MS-DOS breve (detta anche *8,3*). Quando si crea un nome di file lungo, Windows può anche creare un breve formato 8,3 del nome, denominato *alias 8,3* o nome breve, e archiviarlo anche sul disco. Questo alias 8,3 può essere disabilitato per motivi di prestazioni, a livello o per un volume specificato, a seconda del file system specifico.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** gli alias 8,3 non possono essere disabilitati per i volumi specificati fino a Windows 7 e windows Server 2008 R2.

In molti file System, un nome file conterrà una tilde (~) in ogni componente del nome troppo lungo per essere conforme alle regole di denominazione 8,3.

> [!Note]  
> Non tutti i file System seguono la convenzione di sostituzione tilde e i sistemi possono essere configurati per disabilitare la generazione di alias 8,3 anche se normalmente lo supportano. Pertanto, non presupporre che l'alias 8,3 esista già sul disco.

 

Per richiedere i nomi di file 8,3, i nomi di file lunghi o il percorso completo di un file dal sistema, prendere in considerazione le opzioni seguenti:

-   Per ottenere il formato 8,3 di un nome di file lungo, usare la funzione [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) .
-   Per ottenere la versione del nome file lungo di un nome breve, utilizzare la funzione [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) .
-   Per ottenere il percorso completo di un file, usare la funzione [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) .

Nei file System più recenti, ad esempio NTFS, exFAT, UDF e FAT32, Windows archivia i nomi di file lunghi su disco in Unicode, il che significa che il nome di file lungo originale viene sempre mantenuto. Questo vale anche se un nome di file lungo contiene caratteri estesi, indipendentemente dalla tabella codici attiva durante un'operazione di lettura o scrittura su disco.

I file che utilizzano nomi di file lunghi possono essere copiati tra partizioni file system NTFS e partizioni FAT file system Windows senza perdere le informazioni sul nome file. Questo potrebbe non essere vero per i file system FAT MS-DOS precedenti e per alcuni tipi di file System CDFS (CD-ROM), a seconda del nome file effettivo. In questo caso, se possibile, viene sostituito il nome file breve.

## <a name="paths"></a>Percorsi

Il *percorso* di un file specificato è costituito da uno o più *componenti*, separati da un carattere speciale (barra rovesciata), in cui ogni componente è in genere un nome di directory o un nome di file, ma con alcune eccezioni rilevanti descritte di seguito. Spesso è fondamentale per l'interpretazione del sistema di un percorso simile all'inizio, o *prefisso*, del percorso. Questo prefisso determina lo *spazio dei nomi* utilizzato dal percorso, oltre ai caratteri speciali utilizzati nella posizione all'interno del percorso, incluso l'ultimo carattere.

Se un componente di un percorso è un nome di file, deve essere l'ultimo componente.

Ogni componente di un percorso sarà vincolato anche dalla lunghezza massima specificata per un determinato file system. In generale, queste regole rientrano in due categorie: *short* e *Long*. Si noti che i nomi di directory vengono archiviati dal file system come tipo speciale di file, ma le regole di denominazione per i file si applicano anche ai nomi di directory. Per riepilogare, un percorso è semplicemente la rappresentazione di stringa della gerarchia tra tutte le directory esistenti per un nome di file o di directory specifico.

### <a name="fully-qualified-vs-relative-paths"></a>Percorsi completi e relativi

Per le funzioni API Windows che modificano i file, i nomi di file possono spesso essere relativi alla directory corrente, mentre alcune API richiedono un percorso completo. Un nome file è relativo alla directory corrente se non inizia con uno dei seguenti elementi:

-   Nome UNC di qualsiasi formato, che inizia sempre con due caratteri di barra rovesciata (" \\ \\ "). Per ulteriori informazioni, vedere la sezione successiva.
-   Indicatore di disco con una barra rovesciata, ad esempio "C: \\ " o "d: \\ ".
-   Una singola barra rovesciata, ad esempio " \\ directory" o " \\file.txt". Questa operazione viene definita anche *percorso assoluto*.

Se un nome di file inizia con un indicatore di disco ma non con la barra rovesciata dopo i due punti, viene interpretato come un percorso relativo della directory corrente sull'unità con la lettera specificata. Si noti che la directory corrente può essere o meno la directory radice a seconda di ciò che è stato impostato durante l'operazione "Change Directory" più recente su tale disco. Esempi di questo formato sono i seguenti:

-   "C:tmp.txt" fa riferimento a un file denominato "tmp.txt" nella directory corrente nell'unità C.
-   "C:TEMPDIR \\tmp.txt" si riferisce a un file in una sottodirectory della directory corrente nell'unità C.

Un percorso viene definito anche relativo se contiene "puntini". ovvero due punti insieme in un componente del percorso. Questo identificatore speciale viene usato per indicare la directory al di sopra della directory corrente, altrimenti nota come "directory padre". Esempi di questo formato sono i seguenti:

-   "..\\tmp.txt "specifica un file denominato tmp.txt posizionato nell'elemento padre della directory corrente.
-   "..\\..\\tmp.txt "specifica un file che corrisponde a due directory al di sopra della directory corrente.
-   "..\\ TEMPDIR \\tmp.txt "specifica un file denominato tmp.txt che si trova in una directory denominata TEMPDIR che è una directory peer della directory corrente.

I percorsi relativi possono combinare entrambi i tipi di esempio, ad esempio "C:.. \\tmp.txt ". Questa operazione è utile perché, anche se il sistema tiene traccia dell'unità corrente insieme alla directory corrente di tale unità, tiene traccia anche delle directory correnti in ognuna delle diverse lettere di unità (se il sistema ha più di una), indipendentemente dall'indicatore di unità impostato come unità corrente.

### <a name="maximum-path-length-limitation"></a>Limite lunghezza massima percorso


Nelle edizioni di Windows precedenti a Windows 10 versione 1607, la lunghezza massima per un percorso è il **\_ percorso** massimo, definito come 260 caratteri. Nelle versioni successive di Windows, per rimuovere il limite è necessario modificare una chiave del registro di sistema o utilizzare lo strumento Criteri di gruppo. Per i dettagli completi, vedere [limitazione della lunghezza massima del percorso](./maximum-file-path-limitation.md) .


## <a name="namespaces"></a>Spazi dei nomi

Nelle API Windows sono presenti due categorie principali di convenzioni dello spazio dei nomi, comunemente definite *spazi dei nomi NT* e gli *spazi dei nomi Win32*. Lo spazio dei nomi NT è stato progettato per essere lo spazio dei nomi di livello più basso in cui potrebbero esistere altri sottosistemi e spazi dei nomi, tra cui il sottosistema Win32 e, per estensione, gli spazi dei nomi Win32. POSIX è un altro esempio di un sottosistema di Windows basato sullo spazio dei nomi NT. Nelle prime versioni di Windows sono stati definiti anche diversi nomi predefiniti o riservati per determinati dispositivi speciali, ad esempio le porte di comunicazione (seriale e parallela) e la console di visualizzazione predefinita come parte di quello che ora è denominato spazio dei nomi del dispositivo NT e sono ancora supportati nelle versioni correnti di Windows per compatibilità con le versioni precedenti.

### <a name="win32-file-namespaces"></a>Spazi dei nomi dei file Win32

Il prefisso e le convenzioni dello spazio dei nomi Win32 sono riepilogati in questa sezione e nella sezione seguente, con le descrizioni del modo in cui vengono usati. Si noti che questi esempi sono destinati all'uso con le funzioni dell'API Windows e non funzionano necessariamente con le applicazioni shell di Windows, ad esempio Esplora risorse. Per questo motivo, esiste una gamma più ampia di percorsi possibili rispetto a quelli disponibili in genere nelle applicazioni della shell di Windows e le applicazioni Windows che sfruttano questa possibilità possono essere sviluppate utilizzando le convenzioni dello spazio dei nomi.

Per l'i/O di file, il \\ \\ prefisso "? \\ " per una stringa di percorso indica alle API Windows di disabilitare tutte le analisi delle stringhe e di inviare la stringa che lo segue direttamente al file System. Se, ad esempio, il file system supporta percorsi e nomi di file di grandi dimensioni, è possibile superare i limiti **massimi del \_ percorso** che altrimenti verranno applicati dalle API di Windows. Per ulteriori informazioni sulla limitazione del percorso massimo normale, vedere la sezione precedente [limitazione della lunghezza massima del percorso](#maximum-path-length-limitation).

Poiché disattiva l'espansione automatica della stringa di percorso, il prefisso " \\ \\ ? \\ " consente anche l'uso di ".." e "." nei nomi di percorso, che può essere utile se si sta tentando di eseguire operazioni su un file con questi identificatori di percorso relativi altrimenti riservati come parte del percorso completo.

Molte, ma non tutte le API di i/O dei file supportano " \\ \\ ? \\ "; è opportuno esaminare l'argomento di riferimento relativo a ogni API. 

Si noti che è necessario usare le API Unicode per assicurarsi che il \\ \\ prefisso "? \\ " consenta di superare il **\_ percorso massimo** 

### <a name="win32-device-namespaces"></a>Spazi dei nomi dei dispositivi Win32

Il \\ \\ prefisso ". \\ " accederà allo spazio dei nomi del dispositivo Win32 anziché allo spazio dei nomi del file Win32. Questo è il modo in cui l'accesso ai dischi fisici e ai volumi viene eseguito direttamente, senza passare attraverso la file system, se l'API supporta questo tipo di accesso. È possibile accedere a molti dispositivi diversi dai dischi in questo modo, ad esempio usando le funzioni [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) .

Se ad esempio si desidera aprire la porta di comunicazione seriale 1 del sistema, è possibile utilizzare "COM1" nella chiamata alla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Questa operazione funziona perché COM1-COM9 fa parte dei nomi riservati nello spazio dei nomi NT, sebbene l'uso del \\ \\ prefisso ". \\ " funzioni anche con questi nomi di dispositivo. Per confronto, se è installata una lavagna di espansione seriale della porta 100 e si vuole aprire COM56, non è possibile aprirla con "COM56" perché non è disponibile uno spazio dei nomi NT predefinito per COM56. Sarà necessario aprirlo utilizzando " \\ \\ . \\ COM56 "perché" \\ \\ . \\ "passa direttamente allo spazio dei nomi del dispositivo senza provare a individuare un alias predefinito.

Un altro esempio di utilizzo dello spazio dei nomi del dispositivo Win32 consiste nell'utilizzare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con " \\ \\ . \\ PhysicalDisk *x*"(dove *x* è un valore intero valido) o" \\ \\ . \\ CdRom *X*". Questo consente di accedere direttamente a tali dispositivi, ignorando la file system. Questa operazione funziona perché i nomi dei dispositivi vengono creati dal sistema durante l'enumerazione di questi dispositivi e alcuni driver creeranno anche altri alias nel sistema. Ad esempio, il driver di dispositivo che implementa il nome "C: \\ " ha il proprio spazio dei nomi che corrisponde anche al file System.

Le API che passano attraverso la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) generalmente funzionano con il \\ \\ prefisso ". \\ " perché **CreateFile** è la funzione usata per aprire sia i file che i dispositivi, a seconda dei parametri usati.

Se si lavora con le funzioni dell'API Windows, è consigliabile usare il \\ \\ prefisso ". \\ " per accedere solo ai dispositivi e non ai file.

La maggior parte delle API non supporterà \\ \\ il ". \\ ". solo quelli progettati per funzionare con lo spazio dei nomi del dispositivo lo riconoscono. Controllare sempre l'argomento di riferimento per ogni API.

### <a name="nt-namespaces"></a>Spazi dei nomi NT

Sono inoltre disponibili API che consentono di utilizzare la convenzione dello spazio dei nomi NT, ma la gestione oggetti di Windows rende superfluo nella maggior parte dei casi. Per illustrare, è utile esplorare gli spazi dei nomi di Windows nel Visualizzatore oggetti di sistema utilizzando lo strumento [WinObj](/sysinternals/downloads/winobj) di Windows Sysinternals. Quando si esegue questo strumento, viene visualizzato lo spazio dei nomi NT che inizia alla radice o " \\ ". Sottocartella denominata "Global??" è il percorso in cui risiede lo spazio dei nomi Win32. Gli oggetti dispositivo denominati si trovano nello spazio dei nomi NT all'interno della sottodirectory "Device". Qui è possibile trovare anche Serial0 e Serial1, gli oggetti dispositivo che rappresentano le prime due porte COM, se presenti nel sistema. Un oggetto dispositivo che rappresenta un volume è simile a "HarddiskVolume1", sebbene il suffisso numerico possa variare. Il nome "DR0" nella sottodirectory "Discorigido0" è un esempio dell'oggetto dispositivo che rappresenta un disco e così via.

Per rendere questi oggetti dispositivo accessibili dalle applicazioni Windows, i driver di dispositivo creano un collegamento simbolico (collegamento simbolico) nello spazio dei nomi Win32, "globale??", ai rispettivi oggetti dispositivo. Ad esempio, COM0 e COM1 sotto "Global??" le sottodirectory sono semplicemente collegamenti simbolici a Serial0 e Serial1, "C:" è un collegamento simbolico a HarddiskVolume1, "Physicaldrive0" è un collegamento simbolico a DR0 e così via. Senza un collegamento simbolico, il dispositivo "xxx" specificato non sarà disponibile per nessuna applicazione Windows che usa le convenzioni dello spazio dei nomi Win32, come descritto in precedenza. Tuttavia, è possibile aprire un handle a tale dispositivo usando le API che supportano il percorso assoluto dello spazio dei nomi NT nel formato " \\ dispositivo \\ xxx".

Con l'aggiunta del supporto per più utenti tramite Servizi terminal e macchine virtuali, è più necessario virtualizzare il dispositivo radice a livello di sistema nello spazio dei nomi Win32. Questa operazione è stata eseguita aggiungendo il collegamento simbolico denominato "GLOBALROOT" allo spazio dei nomi Win32, che è possibile visualizzare in "Global??" sottodirectory dello strumento WinObj browser precedentemente discusso e può accedere tramite il percorso " \\ \\ ? \\ GLOBALROOT". Questo prefisso garantisce che il percorso che segue cerca nel percorso radice reale di System Object Manager e non in un percorso dipendente dalla sessione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Confronto delle funzionalità del file System](filesystem-functionality-comparison.md)
</dt> </dl>

 

 