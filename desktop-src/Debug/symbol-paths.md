---
description: La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione pdb e dbg). Il percorso di ricerca può essere costituito da uno o più elementi del percorso separati da punti e virgola.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Percorsi dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddf01dfbb5aedfcdd2d96cdfd5d4fdd10e6d3f71b5c69024917ddac534d3824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405901"
---
# <a name="symbol-paths"></a>Percorsi dei simboli

La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione pdb e dbg). Il percorso di ricerca può essere costituito da uno o più elementi del percorso separati da punti e virgola.

## <a name="specifying-search-paths"></a>Specifica dei percorsi di ricerca

Per specificare dove il gestore dei simboli cerca i file di simboli nelle directory dei dischi, chiamare la [**funzione SymSetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) In alternativa, è possibile specificare un percorso di ricerca dei simboli nel *parametro UserSearchPath* della [**funzione SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)

Il *parametro UserSearchPath* in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e il parametro *SearchPath* in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) accettano un puntatore a una stringa con terminazione Null che specifica un percorso o una serie di percorsi separati da un punto e virgola. Il gestore dei simboli usa questi percorsi per cercare i file di simboli. Se questo parametro è **NULL,** il gestore dei simboli cerca la directory che contiene il modulo in cui vengono cercati i simboli. In caso contrario, se questo parametro viene specificato come valore non **NULL,** il gestore dei simboli cerca prima i percorsi impostati dall'applicazione prima di cercare la directory del modulo. Se si imposta la variabile di ambiente NT SYMBOL PATH o NT ALT SYMBOL PATH, il gestore dei simboli cerca i file di \_ \_ simboli \_ \_ \_ \_ \_ nell'ordine seguente:

1. Variabile \_ di ambiente NT SYMBOL \_ \_ PATH.
2. Variabile \_ di ambiente NT ALT SYMBOL \_ \_ \_ PATH.
3. Directory che contiene il modulo corrispondente.

Per recuperare i percorsi di ricerca, chiamare la [**funzione SymGetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)

Il percorso di ricerca per i file di database di programma (con estensione pdb) è diverso dal percorso per i file di debug (con estensione dbg). L'algoritmo è determinato dalla funzionalità della libreria di simboli. Per impostazione predefinita, Microsoft Visual C/C++ crea simboli di formato Microsoft, li rimuove dall'immagine e li inserisce in un file con estensione pdb separato. In genere, il file con estensione pdb si trova nella directory che contiene l'immagine eseguibile. Visual C/C++ incorpora il percorso assoluto del file con estensione pdb nell'immagine eseguibile. Se il gestore dei simboli non riesce a trovare il file con estensione pdb in tale percorso o se il file con estensione pdb è stato spostato in un'altra directory, il gestore dei simboli individua il file con estensione pdb usando il percorso di ricerca descritto per i file con estensione dbg.

## <a name="path-element-types"></a>Tipi di elemento Path

Esistono tre tipi di elementi path.

### <a name="standard-path-element"></a>Elemento Path standard

Per cercare un elemento di percorso standard, cercare nella radice della directory specificata dall'elemento path. Il gestore di simboli cerca anche in una sottodirectory di "simboli" che corrisponde all'estensione di file del modulo che i simboli vengono cercati. Si tratta in genere di "dll", "exe" o "sys". Infine, cerca in una sottodirectory denominata "symbols" con una directory con lo stesso nome dell'estensione. Ad esempio, se l'elemento del percorso del simbolo è "c: mySymbols" e il file in cui vengono cercati i simboli è "boo.dll", verrà cercata la directory \\ seguente.

- c: \\ mySymbols  
- c: \\ dll mySymbols \\  
- c: \\ mySymbols \\ symbols \\ dll  

Il gestore di simboli usa questa logica per cercare qualsiasi elemento di percorso che non soddisfa i criteri per essere un *server* di simboli o *una cache* (descritto di seguito).

### <a name="symbol-server-path-element"></a>Elemento Percorso server di simboli

Un *elemento del percorso del server* di simboli usa una tecnologia speciale che consente di individuare un simbolo che corrisponde esattamente al modulo in questione. Per [altre informazioni, vedere Uso di SymSrv.](using-symsrv.md)

Il gestore dei simboli considera un elemento path come server di simboli se inizia con il testo \* "srv".

> [!Note]  
> Se il testo "srv" non è specificato ma l'elemento path effettivo è un archivio del server di simboli, il gestore dei simboli agirà come se fosse specificato \* "srv". \* Il gestore di simboli esegue questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.

 

### <a name="cache-path-element"></a>Elemento Percorso cache

Un *elemento del* percorso della cache è una variazione in un elemento del percorso del server di simboli.

Questa directory viene cercata come qualsiasi altro server di simboli. Tuttavia, se il simbolo non viene trovato qui e si trova in un elemento path più in basso nella catena del percorso del simbolo, il simbolo verrà copiato e archiviato nel server di simboli specificato in questo elemento.

Il gestore dei simboli considera un elemento path come elemento della cache se inizia con il testo \* "cache". Per specificare una cache in "c: myCache", usare un elemento del percorso \\ del simbolo "cache \* c: \\ myCache".

## <a name="example-search-path"></a>Percorso di ricerca di esempio

Per verificare il funzionamento, impostare questo percorso di ricerca.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Di seguito è riportato un elenco dell'output dettagliato del gestore di simboli durante la ricerca di ntdll.pdb, usando il percorso di ricerca elencato sopra.

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

Le prime tre righe di output mostrano il gestore di simboli che elabora il primo elemento path di `.` . Si tratta di un elemento di percorso standard.

La quarta riga mostra il gestore dei simboli che usa il server di simboli per cercare il file nel secondo elemento path di `cache*c:\myCache` cui è un elemento del percorso della cache.

La quinta riga mostra che il file si trova nel terzo elemento path di `srv*\\symbols\symbols` , che è un elemento del percorso del server di simboli.

La sesta riga indica che il file viene copiato nella cache.

Ultime due righe in cui il file viene aperto dalla cache.
