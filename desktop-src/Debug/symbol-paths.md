---
description: La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione PDB e DBG). Il percorso di ricerca può essere costituito da uno o più elementi Path separati da punti e virgola.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Percorsi dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966046"
---
# <a name="symbol-paths"></a>Percorsi dei simboli

La libreria DbgHelp usa il percorso di ricerca dei simboli per individuare i simboli di debug (file con estensione PDB e DBG). Il percorso di ricerca può essere costituito da uno o più elementi Path separati da punti e virgola.

## <a name="specifying-search-paths"></a>Specifica dei percorsi di ricerca

Per specificare la posizione in cui il gestore di simboli eseguirà la ricerca di file di simboli nelle directory del disco, chiamare la funzione [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) . In alternativa, è possibile specificare un percorso di ricerca dei simboli nel parametro *UserSearchPath* della funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

Il parametro *UserSearchPath* in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e il parametro *SearchPath* in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) accettano un puntatore a una stringa con terminazione null che specifica un percorso o una serie di percorsi separati da un punto e virgola. Il gestore di simboli utilizza questi percorsi per la ricerca di file di simboli. Se questo parametro è **null**, il gestore di simboli Cerca nella directory che contiene il modulo per il quale vengono cercati i simboli. In caso contrario, se questo parametro viene specificato come valore non **null** , il gestore di simboli cerca innanzitutto nei percorsi impostati dall'applicazione prima di eseguire ricerche nella directory del modulo. Se si imposta il \_ \_ percorso del simbolo NT o la variabile di \_ \_ \_ ambiente NT ALT \_ Symbol \_ path, il gestore di simboli Cerca i file di simboli nell'ordine seguente:

1. \_Variabile di \_ ambiente del percorso dei simboli NT \_ .
2. \_Variabile di \_ ambiente del percorso dei simboli Alt NT \_ \_ .
3. Directory che contiene il modulo corrispondente.

Per recuperare i percorsi di ricerca, chiamare la funzione [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .

Il percorso di ricerca per i file di database di programma (con estensione pdb) è diverso dal percorso dei file di debug (con estensione dbg). L'algoritmo è determinato dalla funzionalità della libreria dei simboli. Per impostazione predefinita, Microsoft Visual C/C++ Crea simboli di formato Microsoft, li rimuove dall'immagine e li inserisce in un file con estensione PDB separato. Il file con estensione PDB, in genere, si trova nella directory che contiene l'immagine eseguibile. Visual C/C++ incorpora il percorso assoluto del file con estensione pdb nell'immagine eseguibile. Se il gestore di simboli non riesce a trovare il file con estensione PDB in tale percorso o se il file con estensione PDB è stato spostato in un'altra directory, il gestore dei simboli individuerà il file con estensione PDB utilizzando il percorso di ricerca descritto per i file con estensione dbg.

## <a name="path-element-types"></a>Tipi di elemento Path

Sono disponibili tre tipi di elementi Path.

### <a name="standard-path-element"></a>Elemento Path standard

Viene eseguita la ricerca di un elemento Path standard cercando nella radice della directory specificata dall'elemento Path. Il gestore di simboli Cerca anche in una sottodirectory di "symbols" che corrisponde all'estensione di file del modulo che vengono cercati i simboli. Si tratta in genere di "dll", "exe" o "sys". Infine, Cerca in una sottodirectory denominata "simboli" con una directory con lo stesso nome dell'estensione. Se, ad esempio, l'elemento del percorso dei simboli è "c: i simboli \\ " e il file in cui vengono cercati i simboli è "boo.dll", verrà eseguita una ricerca nelle directory seguenti.

- c: \\ simboli  
- c: \\ simbologia \\ dll  
- c: file \\ \\ \\ dll simboli  

Il gestore di simboli usa questa logica per cercare qualsiasi elemento del percorso che non soddisfi i criteri per essere un *server di simboli* o una *cache* (descritto di seguito).

### <a name="symbol-server-path-element"></a>Elemento Path del server di simboli

Un elemento Path del *Server dei simboli* usa una tecnologia speciale che può individuare un simbolo che corrisponde esattamente al modulo in questione. Per altri dettagli, vedere [uso di symsrv](using-symsrv.md) .

Il gestore di simboli considera un elemento Path come un server di simboli se inizia con il testo "SRV \* ".

> [!Note]  
> Se il testo "SRV \* " non è specificato ma l'elemento Path effettivo è un archivio del server dei simboli, il gestore di simboli fungerà da se è \* stato specificato "SRV". Il gestore di simboli esegue questa determinazione cercando l'esistenza di un file denominato "pingme.txt" nella directory radice del percorso specificato.

 

### <a name="cache-path-element"></a>Elemento Path della cache

Un elemento del percorso *della cache* è una variante di un elemento Path del server di simboli.

Questa directory viene cercata come qualsiasi altro server di simboli. Tuttavia, se il simbolo non viene trovato qui e si trova in un elemento path più in basso nella catena del percorso dei simboli, il simbolo verrà copiato e archiviato nel server di simboli specificato in questo elemento.

Il gestore di simboli considera un elemento Path come elemento della cache se inizia con il testo "cache \* ". Per specificare una cache in "c: cache \\ ", usare un elemento del percorso dei simboli "cache \* c: cache \\ ".

## <a name="example-search-path"></a>Percorso di ricerca di esempio

Per verificarne il funzionamento, impostare questo percorso di ricerca.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Di seguito è riportato un elenco dell'output dettagliato del gestore di simboli durante la ricerca di ntdll. pdb, usando il percorso di ricerca riportato sopra.

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

Le prime tre righe di output mostrano il gestore di simboli che elabora il primo elemento Path di `.` . Si tratta di un elemento Path standard.

La quarta riga indica il gestore di simboli che usa il server di simboli per cercare il file nel secondo elemento Path di `cache*c:\myCache` , che è un elemento Path della cache.

La Quinta riga indica che il file si trova nel terzo elemento Path di `srv*\\symbols\symbols` , che è un elemento Path del server dei simboli.

La sesta riga indica che il file viene copiato nella cache.

Le ultime due righe che il file viene aperto dalla cache.
