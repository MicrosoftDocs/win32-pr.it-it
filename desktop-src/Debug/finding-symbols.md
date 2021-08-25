---
description: Dopo che un file di simboli è stato caricato nel gestore dei simboli, un'applicazione può usare le funzioni del localizzatore di simboli per restituire informazioni sui simboli per un indirizzo specificato.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Ricerca di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90aae9d2894ca8abc7470b2068b508655a50bcb76e1a122f2307f81273abec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912700"
---
# <a name="finding-symbols"></a>Ricerca di simboli

Dopo che un file di simboli è stato caricato nel gestore dei simboli, un'applicazione può usare le funzioni del localizzatore di simboli per restituire informazioni sui simboli per un indirizzo specificato. Queste funzioni possono anche trovare un nome file di codice sorgente e la posizione del numero di riga per un indirizzo.

## <a name="enumerating-symbol-files"></a>Enumerazione dei file di simboli

Per recuperare un elenco di tutti i file di simboli caricati in base al nome del modulo, chiamare la [**funzione SymEnumerateModules64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) Per un esempio, vedere [Enumerazione dei moduli dei simboli.](enumerating-symbol-modules.md) Per recuperare un elenco di simboli per un determinato modulo, chiamare la [**funzione SymEnumSymbols.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) Per un esempio, vedere [Enumerazione dei simboli.](enumerating-symbols.md)

## <a name="retrieving-symbols-by-address"></a>Recupero di simboli in base all'indirizzo

Per recuperare informazioni simboliche per un indirizzo specifico, usare la [**funzione SymFromAddr.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) Questa funzione recupera le informazioni e le archivia in una [**struttura SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Poiché i nomi dei simboli sono di lunghezza variabile, è necessario fornire spazio nel buffer aggiuntivo dopo la **dichiarazione della struttura SYMBOL \_ INFO.** Per un esempio, vedere [Recupero di informazioni sui simboli in base all'indirizzo](retrieving-symbol-information-by-address.md).

Si noti che l'indirizzo non deve essere in un confine di simbolo. Se l'indirizzo è successivo all'inizio di un simbolo ma prima della fine del simbolo (l'inizio del simbolo più la dimensione del simbolo), la funzione individua il simbolo.

## <a name="retrieving-symbols-by-symbol-name"></a>Recupero di simboli in base al nome del simbolo

Per recuperare informazioni simboliche in [**una struttura SYMBOL \_ INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) per un modulo e un nome di simbolo specifici, usare la [**funzione SymFromName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) Se è impostato il caricamento posticipato dei simboli, **SymFromName** tenterà di caricare il file di simboli per un modulo, se non è già stato caricato. Per specificare un nome di modulo insieme a un nome di simbolo, usare la *sintassi Module*! *SymName*. Il carattere "!" delimita il nome del modulo dal nome del simbolo. Per un esempio, vedere [Recupero di informazioni sui simboli in base al nome](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Recupero di numeri di riga in base all'indirizzo

Per recuperare il percorso del codice sorgente per un indirizzo specifico, usare la [**funzione SymGetLineFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) Questa funzione riempie una [**struttura IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) che include il nome del file di origine e la posizione del numero di riga a cui fa riferimento l'indirizzo specificato. Per un esempio, vedere [Recupero di informazioni sui simboli in base all'indirizzo](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Recupero di numeri di riga in base al nome del simbolo

Per recuperare il percorso del codice sorgente per un nome di simbolo specifico, usare la [**funzione SymGetLineFromName64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) Questa funzione è simile a [**SymGetSymFromName64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)ma recupera una [**struttura IMAGEHLP \_ LINE64.**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) Per usare [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) o **SymGetLineFromName64,** è necessario impostare l'opzione load lines (SYMOPT LOAD LINES) usando la funzione \_ \_ [**SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) Per un esempio, vedere [Recupero di informazioni sui simboli in base al nome](retrieving-symbol-information-by-name.md).

 

 



