---
description: Uso di SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: Uso di SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae79d9fd045ab3ce946c14468e56419d3074858c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225650"
---
# <a name="using-symsrv"></a>Uso di SymSrv

SymSrv recapita i file di simboli da archivi di simboli centralizzati. Questi archivi possono contenere un numero qualsiasi di file di simboli, corrispondenti a un numero qualsiasi di programmi o sistemi operativi. Gli archivi possono anche contenere file binari, che risultano particolarmente utili durante il debug dei file di minidump.

Gli archivi possono contenere il simbolo e i file binari effettivi o semplicemente i puntatori ai file di simboli. Se l'archivio contiene puntatori, SymSrv recupererà i file effettivi direttamente dalle origini.

SymSrv può anche separare un archivio simboli di grandi dimensioni in un subset più piccolo appropriato per un'attività di debug specializzata.

Infine, SymSrv può ottenere i file di simboli da un'origine HTTP o HTTPS usando le informazioni di accesso fornite dal sistema operativo. SymSrv supporta i siti HTTPS protetti da Smart Card, certificati e account di accesso e password regolari.

## <a name="setting-the-symbol-path"></a>Impostazione del percorso dei simboli

Come descritto in [percorsi di simboli](symbol-paths.md), il percorso dei simboli ( \_ variabile di ambiente del percorso dei simboli NT \_ \_ ) può essere costituito da diversi elementi di percorso separati da punti e virgola. Se uno o più di questi elementi Path iniziano con il testo "SRV \* ", l'elemento è un server di simboli e utilizzerà symsrv per individuare i file di simboli.

> [!Note]  
> Se il testo "SRV \* " non è specificato ma l'elemento Path effettivo è un archivio del server dei simboli, il gestore di simboli fungerà da se è \* stato specificato "SRV". Il gestore di simboli esegue questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.

 

Così come i percorsi dei simboli sono costituiti da elementi del percorso dei simboli separati da punti e virgola, i server di simboli sono costituiti da elementi di archivio simboli separati da asterischi. Dopo il prefisso "SRV" possono essere presenti fino a 10 archivi simboli \* . Gli archivi elencati a sinistra dell'elenco sono denominati archivi *downstream* e i punti vendita a destra sono detti archivi *upstream* .

<dl> SRV \* *SymbolStore*  
SRV \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

Se nel percorso è incluso un solo elemento di archivio simboli, SymSrv tenterà di usare il file richiesto direttamente da tale archivio.

Se sono presenti due archivi simboli nel percorso, SymSrv Cerca il file di simboli nell'archivio dei simboli più a sinistra. Se il file è presente, viene utilizzato. Se non è presente, SymSrv Cerca nell'archivio dei simboli immediatamente a destra. Se il file è presente, viene copiato nell'archivio di sinistra e aperto da questa posizione.

Se sono presenti più di due archivi, questo comportamento continua a destra fino a quando il file non viene trovato o nell'elenco non sono presenti altri archivi.

Il file non viene mai aperto da alcun archivio, ma dall'archivio più a sinistra. Se il file viene trovato altrove nella catena, viene copiato in ogni archivio a sinistra. Questo processo di copia è denominato "propagazione" e offre alcuni vantaggi che si clarfied più avanti in questo documento.

## <a name="types-of-symbol-stores"></a>Tipi di archivi simboli

Nella tabella seguente sono riportati esempi dei tipi di archivio simboli supportati.

|                            |                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\\\condivisione server          | Percorso UNC completo di una condivisione in un server remoto.                                                                                                                                                                                                                                                                                                 |
| c: \\ localCache             | Percorso di una directory nel computer client.                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | URL di un sito Web che ospita i simboli. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio presente nell'elenco.                                                                                                                                                                                                                          |
| https://SecureInternetSite | URL di un sito Web protetto che ospita i simboli. Questo può supportare password, credenziali di accesso di Windows, certificati e smart card. Deve essere l'archivio più a destra nell'elenco e non deve essere l'unico archivio presente nell'elenco.                                                                                                                              |
| <blank>              | Se non è presente testo tra due asterischi, questo indica l' *Archivio downstream predefinito*. Il percorso viene impostato chiamando [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory). Il valore predefinito è una directory denominata "sym" immediatamente sotto la directory di programma dell'applicazione chiamante. Questa operazione viene a volte definita *cache locale predefinita*. |



 

Poiché non è possibile scrivere in un archivio di simboli basato su HTTP, è necessario che sia l'archivio più a destra dell'elenco. Se un archivio di simboli basato su HTTP si trovava al centro o a sinistra dell'elenco dei negozi, non sarebbe possibile copiarvi i file trovati e la catena verrebbe interrotta. Inoltre, poiché il gestore di simboli non è in grado di aprire un file da un sito Web, un archivio basato su HTTP non deve essere l'archivio più a sinistra o solo nell'elenco. Se SymSrv viene visualizzato con questo percorso dei simboli, tenterà di eseguire il recupero copiando il file nell'archivio downstream predefinito e aprendolo da questa posizione, indipendentemente dal fatto che l'archivio downstream predefinito sia indicato o meno nel percorso dei simboli.

## <a name="examples"></a>Esempio

Per usare SymSrv con un archivio di simboli in \\ \\ compiles \\ , impostare il percorso dei simboli seguente:

**imposta \_ il \_ percorso del simbolo NT \_ = SRV \* \\ \\ Compila i \\ simboli**

Per impostare il percorso dei simboli in modo che il debugger copi i file di simboli da un archivio di simboli in \\ \\ ricompila i simboli nella \\ Directory locale c: \\ localsymbols, usare:

**set \_ NT \_ Symbol \_ path = SRV \* c: \\ localsymbols \* \\ \\ Compila i \\ simboli**

Per impostare il percorso dei simboli in modo che il debugger copi i file di simboli da un archivio di simboli in \\ \\ ricompila i simboli nell' \\ Archivio downstream predefinito (in genere c: \\ debugger \\ sym), usare:

**imposta \_ il \_ percorso del simbolo NT \_ = SRV \* \* \\ \\ Compila i \\ simboli**

Per usare un archivio a catena, impostare il percorso dei simboli seguente:

**set \_ NT \_ Symbol \_ path = SRV \* c: \\ localsymbols \* \\ \\ NearbyServer \\ Store\*https://DistantServer**

In questo esempio, SymSrv cerca innanzitutto il file in c: \\ localsymbols. Se viene trovato, verrà restituito un percorso al file. In caso contrario, SymSrv Cerca il file in \\ \\ NearbyServer \\ Store. Se viene trovato, SymSrv copia il file in c: \\ localsymbols e restituisce un percorso del file. se non viene trovato, symsrv Cerca il file in https://DistantServer e, se viene trovato, symsrv copia il file nell' \\ \\ \\ Archivio NearbyServer, quindi in c: \\ localsymbols.

Nell'ultimo esempio viene illustrato come è possibile utilizzare la progettazione oculata di un percorso di simboli per ottimizzare il download dei simboli. Se si dispone di un sito di lavoro con un gruppo di debugger ed è necessario ottenere i simboli da una posizione distante, è possibile configurare un server comune con un archivio di simboli vicino a tutti i debugger. Configurare quindi ogni debugger con il percorso dei simboli sopra riportato. Il primo debugger che richiede una determinata versione di foo. pdb lo scaricherà da https://DistantServer nell' \\ \\ \\ Archivio NearbyServer e quindi nel relativo computer in c: \\ localsymbols. Il debugger successivo che richiede lo stesso file sarà in grado di scaricarlo dall' \\ \\ \\ Archivio NearbyServer perché è già stato scaricato in tale percorso dal debugger precedente. Questa funzionalità di memorizzazione nella cache a più livelli consente di risparmiare tempo e larghezza di banda di rete notevoli.

## <a name="microsoft-symbol-store"></a>Archivio simboli Microsoft

Microsoft fornisce l'accesso a un server di simboli Internet che contiene i file di simboli per le numerose versioni del sistema operativo Windows. Il catalogo dei simboli non è necessariamente completo, ma è esteso. Sono rappresentati anche altri prodotti Microsoft.

Il server dei simboli Internet viene popolato con una varietà di simboli Windows per i sistemi operativi Microsoft Windows, tra cui hotfix, Service Pack, pacchetti di rollup della sicurezza e versioni finali. I simboli sono inoltre disponibili sul server per le versioni beta correnti e i candidati di rilascio per i prodotti Windows, oltre a un'ampia gamma di altri prodotti Microsoft, ad esempio Microsoft Internet Explorer.

Se si ha accesso a Internet durante il debug, è possibile configurare il debugger per scaricare i simboli in base alle esigenze durante una sessione di debug, anziché scaricare i file di simboli separatamente prima di una sessione di debug. I simboli vengono scaricati in un percorso di directory specificato e quindi vengono caricati dal debugger.

L'URL per l'archivio simboli Microsoft è https://msdl.microsoft.com/download/symbols . Nell'esempio seguente viene illustrato come impostare il percorso dei simboli del debugger (sostituire il percorso dell'archivio downstream per *c: \\ DownstreamStore*):

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>File compressi

SymSrv è compatibile con gli archivi di simboli che contengono file compressi, purché questa compressione sia stata preformata dallo strumento compress.exe distribuito con il Resource Kit di Windows Server 2003. I file compressi devono avere un carattere di sottolineatura come ultimo carattere nelle estensioni di file, ad esempio Module1. PD \_ o Module2. DB \_ . Per informazioni dettagliate, vedere [uso di SymStore](using-symstore.md).

Quando si esegue la propagazione, i file non vengono decompressi, a meno che l'archivio di destinazione non sia l'archivio più a sinistra nel percorso. Se è presente un solo archivio nel percorso e contiene un file compresso, SymSrv copierà il file nell'archivio downstream predefinito e lo aprirà da qui, anche se l'archivio downstream predefinito non è indicato nel percorso dei simboli.

**DbgHelp 6,1 e versioni precedenti:** Se i file nell'archivio master sono compressi, è necessario utilizzare un archivio downstream. SymSrv decomprimerà tutti i file prima di copiarli nell'archivio downstream.

## <a name="deleting-the-cache"></a>Eliminazione della cache

Se si usa un archivio downstream come cache, è possibile eliminare questa directory in qualsiasi momento per risparmiare spazio su disco.

È possibile disporre di un archivio di simboli vast che include i file di simboli per molti programmi o versioni di Windows diverse. Se si aggiorna la versione di Windows utilizzata nel computer di destinazione, i file di simboli memorizzati nella cache corrisponderanno a quelli della versione precedente. Questi file memorizzati nella cache non saranno più usati e pertanto questo potrebbe essere il momento giusto per eliminare la cache.

Strumenti di debug per Windows è dotato di un'utilità denominata agestore.exe che consente di rimuovere selettivamente i file da un albero di directory, lasciando i file usati più di recente. Questo strumento è progettato per eliminare i file inutilizzati dagli archivi dei server di simboli. Consente di controllare molte opzioni, tra cui gli algoritmi di riduzione delle dimensioni di data e di directory.

## <a name="flat-cache-directory"></a>Directory della cache flat

È possibile dichiarare l'archivio downstream predefinito come una directory flat, anziché una struttura ad albero di simboli standard. A tale scopo, chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con **la \_ \_ directory SYMOPT Flat** , che imposta anche l'opzione di **\_ \_ \_ archiviazione predefinita SSRVOPT Flat** in SymSrv. Assicurarsi di chiamare [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) prima di procedere. in caso contrario, i file di simboli possono essere scritti nella directory del programma.

## <a name="pointer-files"></a>File puntatore

SymStore consente di creare e usare file che puntano a un file di destinazione invece che al file di destinazione. Se un archivio di simboli contiene un file di puntatore di questo tipo, l'impostazione predefinita consiste nel copiare il file dal percorso indicato nel file del puntatore nell'archivio. Per configurare un archivio in modo tale che il file del puntatore venga copiato al posto del file a cui fa riferimento, creare un file denominato wantsptr.txt nella radice dell'archivio di destinazione. Il contenuto di wantsptr.txt non è importante, ma solo la presenza del file.

## <a name="excluding-files-from-symbols-list"></a>Esclusione di file dall'elenco di simboli

Per escludere i file da una ricerca di simboli, è possibile specificarne i nomi in symsrv.ini o nel registro di sistema. Per specificare i file in symsrv.ini, creare una sezione esclusioni e elencare i file. I nomi file possono contenere caratteri jolly, come illustrato nell'esempio seguente:

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini deve trovarsi nella stessa directory in cui risiede symsrv.dll. Nella maggior parte delle installazioni, il file non esiste e sarà necessario crearne uno nuovo.

In alternativa, è possibile archiviare i file da escludere nel registro di sistema. Creare la seguente chiave del registro di sistema: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Symbol Server \\ esclusioni**. Archiviare ogni nome di file come valore stringa (REG \_ SZ) in questa chiave. Il nome del valore stringa specifica il nome del file da escludere. È possibile usare il contenuto del valore stringa per archiviare un commento che descrive il motivo per cui il file viene escluso.

## <a name="installation"></a>Installazione

Il server di simboli SymSrv (symsrv.dll) è incluso nel pacchetto degli strumenti di debug per Windows. Deve essere installato nella stessa directory della copia di dbghelp.dll che si sta caricando. Per ulteriori informazioni, vedere [chiamata della libreria DbgHelp](calling-the-dbghelp-library.md).

 

 



