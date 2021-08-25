---
description: Di seguito sono riportate le funzioni DbgHelp.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Funzioni DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8afacd44409004034ed727920c98487a0e2e34ad03e7af4ef5a2e5e13ab5303c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912771"
---
# <a name="dbghelp-functions"></a>Funzioni DbgHelp

Di seguito sono riportate le funzioni DbgHelp.

## <a name="general"></a>Generale

Di seguito sono riportate le funzioni helper generali:

<dl>

[**EnumDirTree**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[**ImagehlpApiVersion**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[**ImagehlpApiVersionEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[**MakeSureDirectoryPathExists**](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[**SearchTreeForFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a>Debugger

Le funzioni del servizio di debug sono le funzioni più adatte per l'uso da parte di un debugger o del codice di debug in un'applicazione. Queste funzioni possono essere usate insieme alle funzioni di gestione dei simboli per semplificarne l'uso.

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**EnumerateLoadedModulesEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[**FindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[**FindDebugInfoFileEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[**FindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[**FindExecutableImageEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymSetParentWindow**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a>Accesso alle immagini

Le funzioni di accesso alle immagini accedono ai dati in un'immagine eseguibile. Le funzioni forniscono un accesso di alto livello alla base delle immagini e un accesso molto specifico alle parti più comuni dei dati di un'immagine.

<dl>

[**GetTimestampForLoadedLibrary**](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[**ImageDirectoryEntryToData**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[**ImageDirectoryEntryToDataEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[**ImageNtHeader**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[**ImageRvaToSection**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[**ImageRvaToVa**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a>Gestore simboli

Le [funzioni di gestione](symbol-handling.md) dei simboli offrono alle applicazioni un accesso semplice e portabile alle informazioni di debug simboliche di un'immagine. Queste funzioni devono essere usate esclusivamente per garantire l'accesso alle informazioni simboliche. Questa operazione è necessaria perché queste funzioni isolano l'applicazione dal formato del simbolo.

<dl>

[**SymAddSourceStream**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[**SymAddSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[**SymDeleteSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumLines**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[**SymEnumProcesses**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[**SymEnumSourceLines**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[**SymEnumSymbolsForAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[**SymEnumTypes**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[**SymEnumTypesByName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[**SymFindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[**SymFindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[**SymFindFileInPath**](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[**SymFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[**SymFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetFileLineOffsets64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[**SymGetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetOmaps**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[**SymGetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[**SymGetScope**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[**SymGetSymbolFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[**SymGetTypeFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[**SymGetTypeInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[**SymGetTypeInfoEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[**SymMatchFileName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[**SymMatchString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[**SymNext**](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[**SymPrev**](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymSearch**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[**SymSetScopeFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[**SymSetScopeFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a>Server di simboli

Il [server di](symbol-servers-and-symbol-stores.md) simboli consente ai debugger di recuperare automaticamente i file di simboli corretti senza nomi di prodotto, versioni o numeri di build. Le funzioni seguenti vengono usate con il server di simboli.

<dl>

[**SymSrvDeltaName**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[**SymSrvGetFileIndexes**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[**SymSrvGetFileIndexInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[**SymSrvGetFileIndexString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[**SymSrvGetSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[**SymSrvIsStore**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[**SymSrvStoreFile**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[**SymSrvStoreSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a>File minidump in modalità utente

Le funzioni di minidump consentono alle applicazioni di produrre file crashdump contenenti un subset utile dell'intero contesto del processo. questo file è noto come [file di minidump](minidump-files.md). Le funzioni seguenti vengono usate con i file di minidump.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a>Server di origine

[Il server](source-server-and-source-indexing.md) di origine consente a un client di recuperare la versione esatta dei file di origine usati per compilare un'applicazione. Le funzioni seguenti vengono usate con il server di origine.

-   [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [**SymEnumSourceFileTokens**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [**SymEnumSourceFileTokensProc**](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [**SymGetSourceFileFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [**SymGetSourceFileToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [**SymGetSourceVarFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a>Funzioni obsolete

<dl>

[**MapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**UnMapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



