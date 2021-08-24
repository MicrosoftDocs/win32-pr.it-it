---
description: Uso di SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Uso di SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a627e50c6be3a3e8636378890025a6dde091948954e2709935c7dc84fa30c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655031"
---
# <a name="using-symsrv"></a>Uso di SymSrv

SymSrv fornisce i file di simboli da archivi di simboli centralizzati. Questi archivi possono contenere un numero qualsiasi di file di simboli, corrispondenti a un numero qualsiasi di programmi o sistemi operativi. Gli archivi possono anche contenere file binari, particolarmente utili durante il debug di file minidump.

Gli archivi possono contenere i file di simboli e binari effettivi o semplicemente puntatori ai file di simboli. Se l'archivio contiene puntatori, SymSrv recupererà i file effettivi direttamente dalle relative origini.

SymSrv può anche separare un archivio di simboli di grandi dimensioni in un subset più piccolo appropriato per un'attività di debug specializzata.

Infine, SymSrv può ottenere i file di simboli da un'origine HTTP o HTTPS usando le informazioni di accesso fornite dal sistema operativo. SymSrv supporta siti HTTPS protetti da smart card, certificati e normali account di accesso e password.

## <a name="setting-the-symbol-path"></a>Impostazione del percorso dei simboli

Come descritto in [Percorsi dei](symbol-paths.md)simboli, il percorso dei simboli (variabile di ambiente NT SYMBOL PATH) può essere costituito da diversi elementi del percorso separati da punti \_ e \_ \_ virgola. Se uno o più di questi elementi di percorso iniziano con il testo "srv", l'elemento è un server di simboli e userà SymSrv per individuare i file \* di simboli.

> [!Note]  
> Se il testo "srv " non è specificato ma l'elemento path effettivo è un archivio del server di simboli, il gestore dei simboli agirà come se fosse specificato \* "srv". \* Il gestore dei simboli determina questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.

 

Così come i percorsi dei simboli sono composti da elementi del percorso dei simboli separati da punti e virgola, i server dei simboli sono composti da elementi dell'archivio simboli separati da asterischi. Possono essere presenti fino a 10 archivi di simboli dopo il prefisso \* "srv". Gli archivi elencati a sinistra dell'elenco sono denominati *archivi downstream* e gli archivi a destra sono denominati *archivi upstream.*

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Se nel percorso è incluso un solo elemento dell'archivio simboli, SymSrv tenterà di usare il file richiesto direttamente da tale archivio.

Se nel percorso sono presenti due archivi di simboli, SymSrv cerca il file di simboli nell'archivio dei simboli più a sinistra. Se il file è presente, viene usato . Se non è presente, SymSrv cerca immediatamente a destra nell'archivio dei simboli. Se il file è presente, viene copiato nell'archivio di sinistra e aperto da questa cartella.

Se sono presenti più di due archivi, questo comportamento continua a destra fino a quando il file non viene trovato o non sono presenti altri archivi nell'elenco.

Il file non viene mai aperto da qualsiasi archivio, ma dall'archivio più a sinistra. Se il file si trova in un altro punto della catena, viene copiato in ogni archivio a sinistra. Questo processo di copia è detto "propagazione" e offre alcuni vantaggi che verranno forniti più avanti in questo documento.

## <a name="types-of-symbol-stores"></a>Tipi di archivi di simboli

Nella tabella seguente vengono visualizzati esempi dei tipi di archivio dei simboli supportati.

|  Tipo di archivio simboli       |  Descrizione |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\condivisione \\ server          | Percorso UNC completo di una condivisione in un server remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ LocalCache             | Percorso di una directory nel computer client.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | URL di un sito Web che ospita i simboli. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio nell'elenco.                                                                                                                                                                                                                          |
| https://SecureInternetSite | URL di un sito Web sicuro che ospita i simboli. Può supportare password, Windows credenziali di accesso, certificati e smart card. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio nell'elenco.                                                                                                                              |
| <blank>              | Se non è presente alcun testo tra due asterischi, indica *l'archivio downstream predefinito.* Il percorso viene impostato chiamando [**SymSetHomeDirectory.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) Il valore predefinito è una directory denominata "sym" immediatamente sotto la directory del programma dell'applicazione chiamante. Questa operazione viene talvolta definita cache *locale predefinita.* |



 

Poiché non è possibile scrivere in un archivio simboli basato su HTTP, deve essere l'archivio più a destra nell'elenco. Se un archivio di simboli basato su HTTP si trova al centro o a sinistra dell'elenco di archivi, non è possibile copiare i file trovati in esso e la catena viene interrotta. Inoltre, poiché il gestore dei simboli non può aprire un file da un sito Web, un archivio basato su HTTP non deve essere l'archivio più a sinistra o solo nell'elenco. Se SymSrv viene visualizzato con questo percorso dei simboli, tenterà di eseguire il ripristino copiando il file nell'archivio downstream predefinito e aprirlo da tale posizione, indipendentemente dal fatto che l'archivio downstream predefinito sia indicato o meno nel percorso dei simboli.

## <a name="examples"></a>Esempio

Per usare SymSrv con un archivio simboli in \\ \\ mybuilds \\ mysymbols, impostare il percorso dei simboli seguente:

**set \_ NT \_ SYMBOL \_ PATH= srv \* \\ \\ mybuilds \\ mysymbols**

Per impostare il percorso dei simboli in modo che il debugger copierà i file di simboli da un archivio di simboli in \\ \\ mybuilds \\ mysymbols nella directory locale c: \\ localsymbols, usare:

**set \_ NT \_ SYMBOL \_ PATH=srv \* c: \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

Per impostare il percorso dei simboli in modo che il debugger copierà i file di simboli da un archivio di simboli in \\ \\ mybuilds mysymbols nell'archivio downstream predefinito (in genere \\ c: \\ \\ debuggers sym), usare:

**set \_ NT \_ SYMBOL \_ PATH=srv \* \* \\ \\ mybuilds \\ mysymbols**

Per usare un archivio a cascata, impostare il percorso dei simboli seguente:

**set \_ NT SYMBOL PATH = \_ \_ srv \* c: \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

In questo esempio SymSrv cerca prima di tutto il file in c: \\ localsymbols. Se viene trovato, restituirà un percorso al file. In caso contrario, SymSrv cerca il file \\ \\ nell'archivio \\ NearbyServer. Se viene trovato, SymSrv copia il file in c: localsymbols e restituisce un percorso al file. Se non viene trovato, SymSrv cerca il file in e, se viene trovato, SymSrv copia il file nell'archivio NearbyServer e quindi in \\ https://DistantServer \\ \\ \\ c: \\ localsymbols.

Nell'ultimo esempio viene illustrato come usare la progettazione di un percorso di simboli per ottimizzare il download dei simboli. Se si dispone di un sito di lavoro con un gruppo di debugger e tutti devono ottenere simboli da una posizione distante, è possibile configurare un server comune con un archivio simboli vicino a tutti i debugger. Configurare quindi ogni debugger con il percorso del simbolo precedente. Il primo debugger che richiede una determinata versione di foo.pdb lo scarica da nell'archivio NearbyServer e quindi nel proprio https://DistantServer \\ \\ computer in \\ c: \\ localsymbols. Il debugger successivo che richiede lo stesso file sarà in grado di scaricarlo dall'archivio NearbyServer perché è già stato scaricato in tale percorso \\ \\ dal debugger \\ precedente. Questa memorizzazione nella cache multi-livello consente di risparmiare tempo e larghezza di banda di rete significativi.

## <a name="microsoft-symbol-store"></a>Microsoft Symbol Store

Microsoft fornisce l'accesso a un server di simboli Internet che contiene i file di simboli per le numerose versioni Windows sistema operativo. Questo catalogo di simboli non è garantito per essere completo, ma è esteso. Sono rappresentati anche altri prodotti Microsoft.

Il server dei simboli Internet viene popolato con un'ampia gamma di simboli di Windows per i sistemi operativi Microsoft Windows, tra cui correzioni a caldo, Service Pack, pacchetti di rollup della sicurezza e versioni definitiva. I simboli sono disponibili anche nel server per le versioni beta correnti e i candidati alla versione finale per i prodotti Windows, oltre a un'ampia gamma di altri prodotti Microsoft, ad esempio Microsoft Internet Explorer.

Se si ha accesso a Internet durante il debug, è possibile configurare il debugger per scaricare i simboli in base alle esigenze durante una sessione di debug, anziché scaricare i file di simboli separatamente prima di una sessione di debug. I simboli vengono scaricati in un percorso di directory specificato dall'utente e quindi caricati dal debugger.

L'URL per l'archivio simboli Microsoft è https://msdl.microsoft.com/download/symbols . L'esempio seguente illustra come impostare il percorso dei simboli del debugger (sostituire il percorso dell'archivio downstream con *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>File compressi

SymSrv è compatibile con gli archivi di simboli che contengono file compressi, purché questa compressione sia stata precompiata con lo strumento compress.exe distribuito con il Resource Kit di Windows Server 2003. I file compressi devono contenere un carattere di sottolineatura come ultimo carattere nelle estensioni di file (ad esempio, module1.pd \_ o module2.db). \_ Per informazioni dettagliate, [vedere Uso di SymStore.](using-symstore.md)

In caso di propagazione, i file non vengono decompressi a meno che l'archivio di destinazione non sia l'archivio più a sinistra nel percorso. Se nel percorso è presente un solo archivio contenente un file compresso, SymSrv copia il file nell'archivio downstream predefinito e lo apre da questa posizione, anche se l'archivio downstream predefinito non è indicato nel percorso dei simboli.

**DbgHelp 6.1 e versioni precedenti:** Se i file nell'archivio master sono compressi, è necessario utilizzare un archivio downstream. SymSrv decomprimerà tutti i file prima di copiarli nell'archivio downstream.

## <a name="deleting-the-cache"></a>Eliminazione della cache

Se si usa un archivio downstream come cache, è possibile eliminare questa directory in qualsiasi momento per risparmiare spazio su disco.

È possibile avere un archivio di simboli di grandi dimensioni che include file di simboli per molti programmi o versioni Windows diverse. Se si aggiorna la versione di Windows usata nel computer di destinazione, i file di simboli memorizzati nella cache corrisponderanno tutti alla versione precedente. Questi file memorizzati nella cache non saranno più in uso e quindi potrebbe essere il momento giusto per eliminare la cache.

Strumenti di debug per Windows viene fornita con un'utilità denominata agestore.exe che rimuoverà in modo selettivo i file da un albero di directory, lasciando i file usati più di recente. Questo strumento è progettato per eliminare i file inutilizzati dagli archivi del server di simboli. Consente di controllare molte opzioni, inclusi gli algoritmi di data limite e dimensioni della directory.

## <a name="flat-cache-directory"></a>Flat Cache Directory

È possibile dichiarare l'archivio downstream predefinito come directory flat, anziché come struttura ad albero dei simboli standard. A tale scopo, chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **SYMOPT \_ FLAT \_ DIRECTORY** (in questo modo viene impostata anche l'opzione **SSRVOPT \_ FLAT DEFAULT \_ \_ STORE** in SymSrv). Assicurarsi di chiamare [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) prima di eseguire questa operazione. In caso contrario, i file di simboli possono essere scritti nella directory del programma.

## <a name="pointer-files"></a>File puntatore

SymStore può creare e usare file che puntano a un file di destinazione anziché al file di destinazione stesso. Se un archivio simboli contiene un file di puntatore di questo tipo, l'impostazione predefinita è copiare il file dal percorso indicato nel file di puntatore all'archivio. Per configurare un archivio in modo che il file del puntatore sia copiato anziché il file a cui punta, creare un file denominato wantsptr.txt nella radice dell'archivio di destinazione. Il contenuto wantsptr.txt non è importante, ma solo la presenza del file.

## <a name="excluding-files-from-symbols-list"></a>Esclusione di file dall'elenco di simboli

Per escludere i file da una ricerca di simboli, è possibile specificarne i nomi symsrv.ini o nel Registro di sistema. Per specificare i file in symsrv.ini, creare una sezione denominata Esclusioni ed elencare i file. I nomi di file possono contenere caratteri jolly, come illustrato nell'esempio seguente:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini deve trovarsi nella stessa directory in cui symsrv.dll risiede. Nella maggior parte delle installazioni il file non esiste ed è necessario crearne uno nuovo.

In alternativa, è possibile archiviare i file da escludere nel Registro di sistema. Creare la chiave del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE Software Microsoft Symbol Server \_ \\ \\ \\ \\ Exclusions**. Archiviare ogni nome file come valore stringa (REG \_ SZ) all'interno di questa chiave. Il nome del valore stringa specifica il nome del file da escludere. È possibile usare il contenuto del valore stringa per archiviare un commento che descrive il motivo per cui il file viene escluso.

## <a name="installation"></a>Installazione

Il server di simboli SymSrv (symsrv.dll) è incluso nel pacchetto debugging tools for Windows. Deve essere installato nella stessa directory della copia dbghelp.dll che si sta caricando. Per altre informazioni, vedere [Chiamata della libreria DbgHelp](calling-the-dbghelp-library.md).

 

 



