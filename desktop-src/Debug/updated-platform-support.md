---
description: Se necessario, la libreria DbgHelp è stata ampliata per supportare sia Windows a 32 che a 64 bit.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Supporto aggiornato della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523666"
---
# <a name="updated-platform-support"></a>Supporto aggiornato della piattaforma

Se necessario, la libreria DbgHelp è stata ampliata per supportare sia Windows a 32 che a 64 bit. Le definizioni della funzione e della struttura originali sono ancora in DbgHelp. h, ma sono presenti anche versioni aggiornate di queste definizioni compatibili con Windows a 64 bit. Se si usano le funzioni aggiornate nel codice, è possibile compilarlo sia per Windows a 32 che a 64 bit. Il codice sarà anche più efficiente, poiché le funzioni originali chiamano semplicemente le funzioni aggiornate per eseguire il lavoro.

Ad esempio, DbgHelp. h contiene le definizioni per **SymUnloadModule** (funzione originale) e **SymUnloadModule64** (funzione aggiornata). Queste definizioni sono quasi identiche, ma usano tipi diversi per il parametro *BaseOfDll* . (**SymUnloadModule** usa il tipo **DWORD** , mentre **SymUnloadModule64** usa il tipo **DWORD64** ). Se si scrive il codice per l'uso di **SymUnloadModule64**, è possibile compilarlo per le finestre 32 e 64 bit. Il codice è anche più efficiente rispetto a quando si chiama **SymUnloadModule**.

Di seguito è riportato un elenco delle funzioni aggiornate:

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

Di seguito è riportato un elenco delle strutture aggiornate:

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**IMAGEHLP \_ simbolo posticipato \_ \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**\_SYMBOL64 duplicato Imagehlp \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**\_LINE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**\_MODULE64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**\_SYMBOL64 Imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



