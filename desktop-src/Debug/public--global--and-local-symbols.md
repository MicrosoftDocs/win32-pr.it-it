---
description: Le funzionalità di gestione dei simboli dell'API DbgHelp si sono evolute nel corso degli anni.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Simboli pubblici, globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406101"
---
# <a name="public-global-and-local-symbols"></a>Simboli pubblici, globali e locali

Le funzionalità di gestione dei simboli dell'API DbgHelp si sono evolute nel corso degli anni. Per garantire che il codice funzioni in diversi scenari e fornisce dettagli completi sui simboli, usare le funzioni più recenti quando possibile. Ad esempio, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) [**sostituisce SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) sostituisce [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)e [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) sostituisce [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Simboli pubblici

Le versioni iniziali di DbgHelp.dll supportate esaminando solo i simboli pubblici. Questi simboli vengono generati per qualsiasi elemento nel codice che deve essere esposto tra file di origine diversi. Includono anche tutti gli elementi esportati fuori dal modulo.

I simboli vengono incorporati nell'immagine o archiviati separatamente in un file con estensione dbg o pdb. Le uniche informazioni archiviate sono il nome e l'indirizzo del simbolo. I nomi sono disponibili come nomi decorati. Per visualizzare i nomi non dichiarati, chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT UNDNAME o usare la \_ [**funzione UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)

Si noti che l'API DbgHelp non è stata inizialmente progettata per supportare più istanze dello stesso simbolo all'interno di un modulo. Questo perché i simboli pubblici sono limitati ai nomi univoci all'interno di un modulo. Pertanto, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) restituisce solo il primo simbolo corrispondente. Per recuperare tutti i simboli corrispondenti, chiamare [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Simboli globali e locali

Le versioni più recenti di DbgHelp.dll i simboli globali e locali quando si usano file con estensione pdb. Queste nuove versioni includono funzioni statiche, funzioni con ambito all'interno di un file di origine, parametri di funzione e variabili locali. Quando DbgHelp cerca un simbolo, controlla le tabelle dei simboli globali e locali prima di controllare la tabella dei simboli pubblici. Ciò è dovuto al fatto che per questi tipi di simboli sono disponibili più informazioni di quelle disponibili per i simboli pubblici.

I simboli globali e locali vengono archiviati con nomi non dichiarati. Pertanto, il flag \_ SYMOPT UNDNAME non ha alcun effetto. Per ottenere nomi di simboli decorati, è necessario usare il flag SYMOPT \_ PUBLICS \_ ONLY. In questo modo DbgHelp cerca solo i simboli pubblici.

Per visualizzare simboli locali o parametri di funzione, chiamare la funzione [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) con il membro **InstructionOffset** della struttura [**IMAGEHLP \_ STACK \_ FRAME**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) impostato sull'indirizzo di qualsiasi simbolo di funzione. Le chiamate successive [**a SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) e [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) possono operare all'interno del contesto di questo indirizzo. A tale scopo, impostare il *parametro BaseOfDll* su **NULL** e omettere l'identificatore di modulo dal *parametro Name* *o Mask.* In questo modo DbgHelp cerca i simboli corrispondenti all'interno dell'ambito indicato da **SymSetContext.**

Per determinare se un simbolo è un parametro, controllare il **membro Flags** della struttura [**SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Se il simbolo è un parametro, il membro contiene SYMFLAG \_ PARAMETER. Se è un simbolo locale, il membro contiene SYMFLAG \_ LOCAL.

 

 



