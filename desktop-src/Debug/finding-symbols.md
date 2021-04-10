---
description: Dopo che un file di simboli è stato caricato nel gestore dei simboli, un'applicazione può utilizzare le funzioni di localizzazione dei simboli per restituire informazioni sui simboli per un indirizzo specificato.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Ricerca di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f65830032cf363771b14f779726c59d976e8d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125700"
---
# <a name="finding-symbols"></a>Ricerca di simboli

Dopo che un file di simboli è stato caricato nel gestore dei simboli, un'applicazione può utilizzare le funzioni di localizzazione dei simboli per restituire informazioni sui simboli per un indirizzo specificato. Queste funzioni possono anche trovare un nome file di codice sorgente e il percorso di un numero di riga per un indirizzo.

## <a name="enumerating-symbol-files"></a>Enumerazione dei file di simboli

Per recuperare un elenco di tutti i file di simboli caricati dal nome del modulo, chiamare la funzione [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) . Per un esempio, vedere [enumerazione dei moduli di simboli](enumerating-symbol-modules.md). Per recuperare un elenco di simboli per un determinato modulo, chiamare la funzione [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) . Per un esempio, vedere [enumerazione dei simboli](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Recupero dei simboli per indirizzo

Per recuperare informazioni sui simboli per un indirizzo specifico, usare la funzione [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Questa funzione recupera le informazioni e le archivia in una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Poiché i nomi dei simboli sono di lunghezza variabile, è necessario fornire ulteriore spazio del buffer dopo la dichiarazione di struttura delle **\_ informazioni sui simboli** . Per un esempio, vedere [recupero delle informazioni sui simboli in base all'indirizzo](retrieving-symbol-information-by-address.md).

Si noti che non è necessario che l'indirizzo si trovi in un limite di simboli. Se l'indirizzo si trova dopo l'inizio di un simbolo ma prima della fine del simbolo (l'inizio del simbolo più le dimensioni del simbolo), la funzione individuerà il simbolo.

## <a name="retrieving-symbols-by-symbol-name"></a>Recupero di simboli in base al nome del simbolo

Per recuperare le informazioni sui simboli in una struttura di [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) per un modulo e un nome di simbolo specifici, usare la funzione [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Se è impostato il caricamento posticipato dei simboli, **SymFromName** tenterà di caricare il file di simboli per un modulo, se non è già stato caricato. Per specificare il nome di un modulo insieme a un nome di simbolo, usare il *modulo* Syntax. *SymName*. Il carattere "!" delimita il nome del modulo dal nome del simbolo. Per un esempio, vedere [recupero delle informazioni sui simboli in base al nome](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Recupero dei numeri di riga per indirizzo

Per recuperare il percorso del codice sorgente per un indirizzo specifico, usare la funzione [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) . Questa funzione compila una struttura [**\_ LINE64 di imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) che include il nome del file di origine e il percorso del numero di riga a cui fa riferimento l'indirizzo specificato. Per un esempio, vedere [recupero delle informazioni sui simboli in base all'indirizzo](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Recupero di numeri di riga in base al nome del simbolo

Per recuperare il percorso del codice sorgente per un nome di simbolo specifico, usare la funzione [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) . Questa funzione è simile a [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), ma recupera una [**struttura \_ LINE64 di imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) . Per usare [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) o **SymGetLineFromName64**, è necessario impostare l'opzione Load Lines ( \_ linee di carico SYMOPT \_ ) usando la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Per un esempio, vedere [recupero delle informazioni sui simboli in base al nome](retrieving-symbol-information-by-name.md).

 

 



