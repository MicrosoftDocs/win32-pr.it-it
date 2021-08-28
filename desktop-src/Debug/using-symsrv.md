---
description: Uso di SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Uso di SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f0abcbd76b710e6a9429baa1ceff6d3a53a0df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886495"
---
# <a name="using-symsrv"></a>Uso di SymSrv

SymSrv recapita i file di simboli da archivi di simboli centralizzati. Questi archivi possono contenere un numero qualsiasi di file di simboli, corrispondenti a un numero qualsiasi di programmi o sistemi operativi. Gli archivi possono anche contenere file binari, particolarmente utili quando si esegue il debug di file minidump.

Gli archivi possono contenere il simbolo effettivo e i file binari o semplicemente puntatori a file di simboli. Se l'archivio contiene puntatori, SymSrv recupererà i file effettivi direttamente dalle relative origini.

SymSrv può anche separare un archivio di simboli di grandi dimensioni in un subset più piccolo appropriato per un'attività di debug specializzata.

Infine, SymSrv può ottenere i file di simboli da un'origine HTTP o HTTPS usando le informazioni di accesso fornite dal sistema operativo. SymSrv supporta siti HTTPS protetti da smart card, certificati e account di accesso e password regolari.

## <a name="setting-the-symbol-path"></a>Impostazione del percorso dei simboli

Come descritto in [Percorsi dei](symbol-paths.md)simboli, il percorso dei simboli (variabile di ambiente NT SYMBOL PATH) può essere costituito da diversi elementi di percorso separati da punti \_ e \_ \_ virgola. Se uno o più di questi elementi path iniziano con il testo "srv", l'elemento è un server di simboli e userà SymSrv per individuare i file \* di simboli.

> [!Note]  
> Se il testo "srv" non è specificato ma l'elemento path effettivo è un archivio del server di simboli, il gestore dei simboli agirà come se fosse specificato \* "srv". \* Il gestore di simboli esegue questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.

 

Proprio come i percorsi dei simboli sono composti da elementi del percorso dei simboli separati da punti e virgola, i server dei simboli sono composti da elementi dell'archivio simboli separati da asterischi. Dopo il prefisso "srv" possono essere presenti fino a 10 archivi \* di simboli. Gli archivi elencati a sinistra dell'elenco sono denominati *archivi downstream* e gli archivi a destra sono denominati *archivi upstream.*

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Se nel percorso è incluso un solo elemento dell'archivio simboli, SymSrv tenterà di usare il file richiesto direttamente da tale archivio.

Se nel percorso sono presenti due archivi simboli, SymSrv cerca il file di simboli nell'archivio simboli più a sinistra. Se il file è presente, viene usato. Se non è presente, SymSrv cerca immediatamente a destra nell'archivio simboli. Se il file è presente, viene copiato nell'archivio sinistro e aperto da qui.

Se sono presenti più di due archivi, questo comportamento continua a destra fino a quando non viene trovato il file o non sono presenti altri archivi nell'elenco.

Il file non viene mai aperto da alcun archivio, ma dall'archivio più a sinistra. Se il file si trova in un altro punto della catena, viene copiato in ogni archivio a sinistra. Questo processo di copia è detto "propagazione" e offre alcuni vantaggi che verranno forniti più avanti in questo documento.

## <a name="types-of-symbol-stores"></a>Tipi di archivi di simboli

Nella tabella seguente vengono visualizzati esempi dei tipi di archivio simboli supportati.

|  Tipo di archivio simboli       |  Descrizione |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\condivisione \\ server          | Percorso UNC completo di una condivisione in un server remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Percorso di una directory nel computer client.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | URL di un sito Web che ospita i simboli. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio nell'elenco.                                                                                                                                                                                                                          |
| https://SecureInternetSite | URL di un sito Web sicuro che ospita i simboli. Può supportare password, Windows credenziali di accesso, certificati e smart card. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio nell'elenco.                                                                                                                              |
| &lt;blank&gt;              | Se non è presente testo tra due asterischi, indica *l'archivio downstream predefinito.* Il percorso viene impostato chiamando [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). Il valore predefinito è una directory denominata "sym" immediatamente sotto la directory di programma dell'applicazione chiamante. Questa operazione viene talvolta definita cache *locale predefinita.* |



 

Poiché non è possibile scrivere in un archivio simboli basato su HTTP, deve essere l'archivio più a destra nell'elenco. Se un archivio simboli basato su HTTP si trova al centro o a sinistra dell'elenco degli archivi, non sarebbe possibile copiare i file trovati in esso e la catena verrebbe interrotta. Inoltre, poiché il gestore dei simboli non può aprire un file da un sito Web, un archivio basato su HTTP non deve essere l'archivio più a sinistra o solo nell'elenco. Se SymSrv viene visualizzato con questo percorso di simboli, tenterà di eseguire il ripristino copiando il file nell'archivio downstream predefinito e aprirlo da tale posizione, indipendentemente dal fatto che l'archivio downstream predefinito sia indicato o meno nel percorso del simbolo.

## <a name="examples"></a>Esempio

Per usare SymSrv con un archivio simboli \\ \\ in mybuilds \\ mysymbols, impostare il percorso del simbolo seguente:

**set \_ NT \_ SYMBOL \_ PATH= srv \* \\ \\ mybuilds \\ mysymbols**

Per impostare il percorso del simbolo in modo che il debugger copierà i file di simboli da un archivio simboli in \\ \\ mybuilds \\ mysymbols nella directory locale c: \\ localsymbols, usare:

**set \_ NT \_ SYMBOL \_ PATH=srv \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Per impostare il percorso del simbolo in modo che il debugger copierà i file di simboli da un archivio simboli in \\ \\ mybuilds mysymbols nell'archivio downstream predefinito (in genere \\ c: \\ debuggers \\ sym), usare:

**impostare \_ NT \_ SYMBOL \_ PATH=srv \* \* \\ \\ mybuilds \\ mysymbols**

Per usare un archivio a catena, impostare il percorso del simbolo seguente:

**set \_ NT SYMBOL PATH = \_ \_ srv \* c: \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

In questo esempio, SymSrv cerca innanzitutto il file in c: \\ localsymbols. Se viene trovato, restituirà un percorso al file. In caso contrario, SymSrv cerca il file \\ \\ nell'archivio \\ NearbyServer. Se viene trovato, SymSrv copia il file in c: localsymbols e restituisce un percorso al file. Se non viene trovato, SymSrv cerca il file in e, se viene trovato, SymSrv copia il file nell'archivio NearbyServer, quindi in \\ https://DistantServer \\ \\ \\ c: \\ localsymbols.

Nell'ultimo esempio viene illustrato come usare la progettazione di un percorso di simboli per ottimizzare il download dei simboli. Se si dispone di un sito di lavoro con un gruppo di debugger e tutti devono ottenere simboli da una posizione distante, è possibile configurare un server comune con un archivio simboli vicino a tutti i debugger. Configurare quindi ogni debugger con il percorso del simbolo precedente. Il primo debugger che richiede una determinata versione di foo.pdb lo scarica dall'archivio NearbyServer e quindi nel proprio https://DistantServer \\ \\ computer in \\ c: \\ localsymbols. Il debugger successivo che richiede lo stesso file sarà in grado di scaricarlo dall'archivio NearbyServer perché è già stato scaricato in tale percorso \\ \\ dal debugger \\ precedente. Questa memorizzazione nella cache a più livelli consente di risparmiare tempo e larghezza di banda di rete significativi.

## <a name="microsoft-symbol-store"></a>Microsoft Symbol Store

Microsoft fornisce l'accesso a un server di simboli Internet che contiene i file di simboli per le numerose versioni del Windows sistema operativo. Questo catalogo di simboli non è garantito per essere completo, ma è completo. Sono rappresentati anche altri prodotti Microsoft.

Il server di simboli Internet viene popolato con una varietà di simboli Windows per i sistemi operativi Microsoft Windows, tra cui correzioni rapida, Service Pack, pacchetti di rollup della sicurezza e versioni successive. I simboli sono disponibili anche nel server per le versioni beta correnti e i candidati alla versione finale per i prodotti Windows, oltre a un'ampia gamma di altri prodotti Microsoft, ad esempio Microsoft Internet Explorer.

Se si ha accesso a Internet durante il debug, è possibile configurare il debugger per scaricare i simboli in base alle esigenze durante una sessione di debug, anziché scaricare i file di simboli separatamente prima di una sessione di debug. I simboli vengono scaricati in un percorso di directory specificato e quindi vengono caricati dal debugger.

L'URL per l'archivio simboli Microsoft è https://msdl.microsoft.com/download/symbols . L'esempio seguente illustra come impostare il percorso del simbolo del debugger (sostituire il percorso dell'archivio downstream con *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>File compressi

SymSrv è compatibile con gli archivi di simboli che contengono file compressi, purché questa compressione sia stata preformatta con lo strumento compress.exe distribuito con Windows Server 2003 Resource Kit. I file compressi devono avere un carattere di sottolineatura come ultimo carattere nelle estensioni di file , ad esempio module1.pd \_ o module2.db \_ . Per informazioni dettagliate, vedere [Uso di SymStore.](using-symstore.md)

In caso di propagazione, i file non vengono compressi a meno che l'archivio di destinazione non sia l'archivio più a sinistra nel percorso. Se nel percorso è presente un solo archivio contenente un file compresso, SymSrv copierà il file nell'archivio downstream predefinito e lo aprirà da questa posizione, anche se l'archivio downstream predefinito non è indicato nel percorso del simbolo.

**DbgHelp 6.1 e versioni precedenti:** Se i file nell'archivio master sono compressi, è necessario usare un archivio downstream. SymSrv decomprimerà tutti i file prima di copiarli nell'archivio downstream.

## <a name="deleting-the-cache"></a>Eliminazione della cache

Se si usa un archivio downstream come cache, è possibile eliminare questa directory in qualsiasi momento per risparmiare spazio su disco.

È possibile avere un archivio di simboli di grandi dimensioni che include file di simboli per molti programmi o versioni Windows diverse. Se si aggiorna la versione di Windows nel computer di destinazione, i file di simboli memorizzati nella cache corrisponderanno tutti alla versione precedente. Questi file memorizzati nella cache non verranno ulteriormente utilizzati e pertanto potrebbe essere un buon momento per eliminare la cache.

Debugging Tools for Windows include un'utilità denominata agestore.exe che rimuoverà in modo selettivo i file da un albero di directory, lasciando i file usati più di recente. Questo strumento è progettato per eliminare i file inutilizzati dagli archivi del server di simboli. Consente di controllare molte opzioni, tra cui gli algoritmi di data e dimensione della directory tagliati.

## <a name="flat-cache-directory"></a>Flat Cache Directory

È possibile dichiarare l'archivio downstream predefinito come directory flat, anziché come struttura ad albero dei simboli standard. A tale scopo, chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ FLAT \_ DIRECTORY** (in questo modo viene impostata anche l'opzione **SSRVOPT \_ FLAT DEFAULT \_ \_ STORE** in SymSrv). Assicurarsi di chiamare [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) prima di eseguire questa operazione. In caso contrario, i file di simboli possono essere scritti nella directory del programma.

## <a name="pointer-files"></a>File puntatore

SymStore può creare e usare file che puntano a un file di destinazione anziché al file di destinazione stesso. Se un archivio di simboli contiene un file di puntatore di questo tipo, l'impostazione predefinita è copiare il file dal percorso indicato nel file di puntatore all'archivio. Per configurare un archivio in modo che il file del puntatore sia copiato anziché il file a cui punta, creare un file denominato wantsptr.txt nella radice dell'archivio di destinazione. Il contenuto wantsptr.txt non è importante, ma solo la presenza del file.

## <a name="excluding-files-from-symbols-list"></a>Esclusione di file dall'elenco dei simboli

Per escludere file da una ricerca di simboli, è possibile specificarne i nomi symsrv.ini o nel Registro di sistema. Per specificare i file in symsrv.ini, creare una sezione denominata Esclusioni ed elencare i file. I nomi dei file possono contenere caratteri jolly, come illustrato nell'esempio seguente:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini deve trovarsi nella stessa directory in cui symsrv.dll risiede. Nella maggior parte delle installazioni il file non esiste ed è necessario crearne uno nuovo.

In alternativa, è possibile archiviare i file da escludere nel Registro di sistema. Creare la chiave del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE Software Microsoft Symbol Server \_ \\ \\ \\ \\ Exclusions**. Archiviare ogni nome file come valore stringa (REG \_ SZ) all'interno di questa chiave. Il nome del valore stringa specifica il nome del file da escludere. È possibile usare il contenuto del valore stringa per archiviare un commento che descrive il motivo per cui il file viene escluso.

## <a name="installation"></a>Installazione

Il server di simboli SymSrv (symsrv.dll) è incluso nel pacchetto debugging tools for Windows. Deve essere installato nella stessa directory della copia del dbghelp.dll che si sta caricando. Per altri dettagli, vedere [Chiamata della libreria DbgHelp.](calling-the-dbghelp-library.md)

 

 



