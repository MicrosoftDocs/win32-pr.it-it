---
description: SymStore (symstore.exe) è uno strumento per la creazione di archivi simboli. È incluso nel pacchetto di strumenti di debug per Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Uso di SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126813"
---
# <a name="using-symstore"></a>Uso di SymStore

SymStore (symstore.exe) è uno strumento per la creazione di archivi simboli. È incluso nel pacchetto [di strumenti di debug per Windows](https://www.microsoft.com/?ref=go) .

SymStore archivia i simboli in un formato che consente al debugger di cercare i simboli in base al timestamp e alle dimensioni dell'immagine (per un file con estensione DBG o eseguibile) oppure la firma e l'età (per un file con estensione pdb). Il vantaggio dell'archivio dei simboli nel formato di archiviazione dei simboli tradizionale è che tutti i simboli possono essere archiviati o a cui viene fatto riferimento nello stesso server e recuperati dal debugger senza alcuna conoscenza precedente del prodotto che contiene il simbolo corrispondente.

Si noti che più versioni dei file di simboli PDB, ad esempio le versioni Public e private, non possono essere archiviate nello stesso server, perché ognuna contengono la stessa firma e l'età.

## <a name="symstore-transactions"></a>Transazioni SymStore

Ogni chiamata a SymStore viene registrata come transazione. Esistono due tipi di transazioni: Add ed Delete.

Quando viene creato l'archivio dei simboli, viene creata una directory denominata "000admin" nella radice del server. La directory 000admin contiene un file per ogni transazione, nonché i file di log Server.txt e History.txt. Il file di Server.txt contiene un elenco di tutte le transazioni attualmente presenti nel server. Il file di History.txt contiene una cronologia cronologica di tutte le transazioni.

Ogni volta che SymStore archivia o rimuove i file di simboli, viene creato un nuovo numero di transazione. Quindi, viene creato un file, il cui nome è il numero di transazione, in 000admin. Questo file contiene un elenco di tutti i file o puntatori che sono stati aggiunti all'archivio simboli durante la transazione. Se viene eliminata una transazione, SymStore leggerà il file di transazione per individuare i file e i puntatori da eliminare.

Le opzioni **Add** e **Canc** specificano se deve essere eseguita una transazione Add o DELETE. Se si include l'opzione **/p** con un'operazione Add, viene specificato che deve essere aggiunto un puntatore. Se si omette l'opzione **/p** , viene specificato che è necessario aggiungere il file di simboli effettivo.

È anche possibile creare l'archivio dei simboli in due fasi separate. Nella prima fase si usa SymStore con l'opzione **/x** per creare un file di indice. Nella seconda fase, si usa SymStore con l'opzione **/y** per creare l'archivio effettivo di file o puntatori dalle informazioni contenute nel file di indice.

Questa tecnica può essere utile per svariati motivi. Questo consente, ad esempio, di ricreare facilmente l'archivio simboli se l'archivio è in qualche modo perduto, purché il file di indice esista ancora. O forse il computer che contiene i file di simboli ha una connessione di rete lenta al computer in cui verrà creato l'archivio dei simboli. In questo caso, è possibile creare il file di indice nello stesso computer dei file di simboli, trasferire il file di indice nel secondo computer, quindi creare l'archivio nel secondo computer.

Per un elenco completo di tutti i parametri di SymStore, vedere [Opzioni di Command-Line SymStore](symstore-command-line-options.md).

> [!Note]  
> SymStore non supporta transazioni simultanee da più utenti. È consigliabile che un utente sia designato come "amministratore" dell'archivio simboli ed è responsabile di tutte le transazioni **Aggiungi** e **del** .

 

## <a name="transaction-examples"></a>Esempi di transazioni

Ecco due esempi di SymStore che aggiungono puntatori a simboli per la build 3790 di Windows Server 2003 a \\ \\ SampleDir \\ symsrv:

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

Nell'esempio seguente SymStore aggiunge i file di simboli effettivi per un progetto di applicazione in \\ \\ Largeapp \\ AppServer \\ bin a \\ \\ TestDir \\ symsrv:

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

Di seguito è riportato un esempio di utilizzo di un file di indice. In primo luogo, SymStore crea un file di indice in base alla raccolta di file di simboli nei \\ \\ \\ bin Largeapp AppServer \\ \\ . In questo caso, il file di indice si trova in un terzo computer, \\ \\ HUBSERVER \\ hubshare. Usare l'opzione **/g** per specificare che il prefisso del file " \\ \\ Largeapp \\ AppServer" potrebbe cambiare in futuro:

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

Si supponga ora di spostare tutti i file di simboli dal computer \\ \\ Largeapp \\ AppServer e inserirli in \\ \\ archivio \\ AppServer. È quindi possibile creare l'archivio dei simboli dal file di indice \\ \\ hubserver \\ hubshare \\myindex.txt come indicato di seguito:

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

Infine, di seguito è riportato un esempio di SymStore che elimina un file aggiunto da una transazione precedente. Per una spiegazione su come determinare l'ID della transazione, in questo caso 0000000096, vedere la sezione seguente.

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a>File compressi

SymStore può essere usato con i file compressi in due modi diversi.

1.  Usare SymStore con l'opzione **/p** per archiviare i puntatori nei file di simboli. Al termine della SymStore, comprimere i file a cui fanno riferimento i puntatori.
2.  Usare SymStore con l'opzione **/x** per creare un file di indice. Al termine della SymStore, comprimere i file elencati nel file di indice. Usare quindi SymStore con l'opzione **/y** e, se si vuole, l'opzione **/p** , per archiviare i file o i puntatori ai file nell'archivio dei simboli. Per eseguire questa operazione, SymStore non dovrà decomprimere i file.

Il server di simboli sarà responsabile della decompressione dei file quando sono necessari.

Se si utilizza SymSrv come server di simboli, è necessario eseguire la compressione utilizzando lo strumento compress.exe distribuito con Microsoft Windows Software Development Kit (SDK). I file compressi devono avere un carattere di sottolineatura come ultimo carattere nelle estensioni di file, ad esempio Module1. PD \_ o Module2. DB \_ . Per informazioni dettagliate, vedere [uso di symsrv](using-symsrv.md).

## <a name="the-servertxt-and-historytxt-files"></a>File server.txt e history.txt

Quando viene aggiunta una transazione, vengono aggiunti diversi elementi di informazioni a server.txt e history.txt per la funzionalità di ricerca futura. Di seguito è riportato un esempio di riga in server.txt e history.txt per una transazione di aggiunta:

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

Si tratta di una riga delimitata da virgole. I campi vengono definiti come indicato di seguito.



| Campo      | Descrizione                                                                         |
|------------|-------------------------------------------------------------------------------------|
| 0000000096 | Numero ID transazione, creato da SymStore.                                      |
| add        | Tipo di transazione. Questo campo può essere **Add** o **Canc**.                   |
| ptr        | Indica se i file o i puntatori sono stati aggiunti. Questo campo può essere **file** o **ptr**. |
| 10/09/99   | Data in cui si è verificata la transazione.                                                     |
| 00:08:32   | Ora di inizio della transazione.                                                      |
| Windows XP | Prodotto.                                                                            |
| da x86 a fre    | Version (facoltativo).                                                                 |
| Aggiunto da | Commento (facoltativo)                                                                  |
| Non utilizzato     | (Riservato per un uso successivo).                                                           |



 

Di seguito sono riportate alcune righe di esempio dal file di transazione 0000000096. Ogni riga registra la directory e il percorso del file o del puntatore aggiunto alla directory.

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

Se si usa una **transazione per** annullare le transazioni di **aggiunta** originali, queste righe verranno rimosse da server.txt e la riga seguente verrà aggiunta al history.txt:

``` syntax
0000000105,del,0000000096
```

I campi per la transazione DELETE vengono definiti nel modo seguente.



| Campo      | Descrizione                                                       |
|------------|-------------------------------------------------------------------|
| 0000000105 | Numero ID transazione, creato da SymStore.                    |
| del        | Tipo di transazione. Questo campo può essere **Add** o **Canc**. |
| 0000000096 | Transazione eliminata.                                     |



 

## <a name="symbol-storage-format"></a>Formato di archiviazione simboli

SymStore usa il file system stesso come database. Viene creato un elevato albero di directory con nomi di directory basati su elementi quali i timestamp del file di simboli, le firme, l'età e altri dati.

Ad esempio, dopo aver aggiunto al server diversi file ACPI. dbg diversi, le directory potrebbero avere un aspetto simile al seguente:

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

In questo esempio, il percorso di ricerca per il file di simboli ACPI. dbg potrebbe avere un aspetto simile al seguente: \\ \\ \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.

All'interno della directory di ricerca potrebbero esistere tre file:

1.  Se il file è stato archiviato, ACPI. dbg sarà presente.
2.  Se è stato archiviato un puntatore, sarà presente un file denominato file. ptr che conterrà il percorso del file di simboli effettivo.
3.  Un file denominato refs. PTR, che contiene un elenco di tutti i percorsi correnti per ACPI. dbg con questo timestamp e le dimensioni dell'immagine che sono attualmente aggiunti all'archivio simboli.

Visualizzazione dell'elenco di directory di \\ \\ Builds \\ symsrv \\ ACPI. dbg \\ 37cdb03962040 fornisce quanto segue:

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

Il file file. PTR contiene la stringa di testo " \\ \\ combuilds \\ symbols \\ x86 \\ 2128. chk \\ symbols \\ sys \\ ACPI. dbg". Poiché in questa directory non è presente alcun file denominato ACPI. dbg, il debugger tenterà di trovare il file nei \\ \\ simboli di compilazione \\ \\ x86 \\ 2128. chk \\ simboli \\ sys \\ ACPI. dbg.

Il contenuto di refs. ptr viene usato solo da SymStore, non dal debugger. Questo file contiene un record di tutte le transazioni eseguite in questa directory. Una riga di esempio da refs. PTR potrebbe essere:

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

Questo mostra che un puntatore a \\ \\ compiles \\ symbols \\ x86 \\ 2128. \\ chk symbols \\ sys \\ ACPI. dbg è stato aggiunto con la transazione "0000000026".

Alcuni file di simboli vengono mantenuti costanti tramite vari prodotti o compilazioni o un prodotto specifico. Un esempio è il file Msvcrt. pdb. Eseguendo una directory di \\ \\ Builds \\ symsrv \\ Msvcrt. pdb viene mostrato che al server dei simboli sono state aggiunte solo due versioni di MSVCRT. pdb:

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

Tuttavia, se si esegue una directory di \\ \\ \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 è indicato che refs. PTR contiene diversi puntatori.

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

Il contenuto di \\ \\ Builds \\ symsrv \\ Msvcrt. pdb \\ 37a8f40e2 \\ refs. ptr è il seguente:

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

Questo mostra che è stato usato lo stesso file Msvcrt. pdb per più compilazioni di simboli archiviati in \\ \\ symsrv di compilazione \\ .

Di seguito è riportato un esempio di una directory che contiene una combinazione di aggiunte di file e puntatori:

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

In questo caso refs. PTR presenta il contenuto seguente:

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Quindi, le transazioni 43, 44 e 45 aggiungono lo stesso file al server e le transazioni 46 e 47 aggiungono puntatori. Se vengono eliminate le transazioni 43, 44 e 45, il file Dbghelp. dbg verrà eliminato dalla directory. La directory avrà quindi il contenuto seguente:

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

Ora file. PTR contiene " \\ \\ sampledir2 \\ bin \\ symbols \\ retail \\ dll \\ dbghelp. dbg" e refs. PTR Contains

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

Ogni volta che la voce finale in refs. ptr è un puntatore, il file file. PTR sarà presente e conterrà il percorso del file associato. Ogni volta che la voce finale in refs. ptr è un file, non è presente alcun file. PTR presente in questa directory. Pertanto, qualsiasi operazione di eliminazione che rimuove la voce finale in refs. PTR può comportare la creazione, l'eliminazione o la modifica di file. ptr.

 

 



