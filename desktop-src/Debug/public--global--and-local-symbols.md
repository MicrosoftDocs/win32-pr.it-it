---
description: Le funzionalità di gestione dei simboli dell'API DbgHelp si sono evolute nel corso degli anni.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Simboli pubblici, globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bf93ec8f11d1cec9c5fec64e2479dd91ee5cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049148"
---
# <a name="public-global-and-local-symbols"></a>Simboli pubblici, globali e locali

Le funzionalità di gestione dei simboli dell'API DbgHelp si sono evolute nel corso degli anni. Per assicurarsi che il codice funzioni in un'ampia gamma di scenari e fornisca dettagli completi sui simboli, usare le funzioni più recenti laddove possibile. Ad esempio, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) sostituisce [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) sostituisce [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)e [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) sostituisce [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Simboli pubblici

Le versioni iniziali di DbgHelp.dll supportano l'analisi solo dei simboli pubblici. Questi simboli vengono generati per qualsiasi elemento nel codice che deve essere esposto tra diversi file di origine. Includono anche tutti gli elementi che vengono esportati dal modulo.

I simboli sono incorporati nell'immagine o archiviati separatamente in un file con estensione DBG o PDB. Le uniche informazioni archiviate sono il nome e l'indirizzo del simbolo. I nomi sono disponibili come nomi decorati. Per visualizzare i nomi non decorati, chiamare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ UNDNAME oppure usare la funzione [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .

Si noti che l'API DbgHelp non è stata progettata inizialmente per supportare più istanze dello stesso simbolo all'interno di un modulo. Ciò è dovuto al fatto che i simboli pubblici sono limitati a nomi univoci all'interno di un modulo. Pertanto, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) restituisce solo il primo simbolo che corrisponde a. Per recuperare tutti i simboli corrispondenti, chiamare [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Simboli globali e locali

Le versioni più recenti di DbgHelp.dll supportano i simboli globali e locali quando si utilizzano i file con estensione pdb. Queste nuove versioni includono funzioni statiche, funzioni con ambito all'interno di un file di origine, parametri di funzione e variabili locali. Quando DbgHelp Cerca un simbolo, verifica le tabelle dei simboli globali e locali prima di controllare la tabella dei simboli pubblici. Questo perché sono disponibili più informazioni per questi tipi di simboli rispetto a quelli disponibili per i simboli pubblici.

I simboli globali e locali vengono archiviati con nomi non decorati. Pertanto, il \_ flag UNDNAME di SYMOPT non ha alcun effetto. Per ottenere i nomi dei simboli decorati, è necessario usare il \_ flag SYMOPT publics \_ only. In questo modo, DbgHelp esegue la ricerca solo nei simboli pubblici.

Per visualizzare i simboli locali o i parametri della funzione, chiamare la funzione [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) con il membro **InstructionOffset** della struttura dello [**\_ Stack \_ frame Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) impostato sull'indirizzo di un simbolo di funzione. Le chiamate successive a [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) e [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) possono funzionare nel contesto di questo indirizzo. A tale scopo, impostare il parametro *BaseOfDll* su **null** e omettere l'identificatore del modulo dal *nome* o dal parametro *mask* . Questa operazione impone a DbgHelp di cercare i simboli corrispondenti nell'ambito indicato da **SymSetContext**.

Per determinare se un simbolo è un parametro, controllare il membro dei **flag** della struttura delle [**\_ informazioni sui simboli**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Se il simbolo è un parametro, il membro contiene il \_ parametro SYMFLAG. Se è un simbolo locale, il membro contiene SYMFLAG \_ local.

 

 



