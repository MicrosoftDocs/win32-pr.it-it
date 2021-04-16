---
description: Di seguito sono riportate le funzioni DbgHelp.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Funzioni DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db65e46fe407b26b1a6ec9ae3cb8d5d7301d5821
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524073"
---
# <a name="dbghelp-functions"></a><span data-ttu-id="066de-103">Funzioni DbgHelp</span><span class="sxs-lookup"><span data-stu-id="066de-103">DbgHelp Functions</span></span>

<span data-ttu-id="066de-104">Di seguito sono riportate le funzioni DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="066de-104">The following are the DbgHelp functions.</span></span>

## <a name="general"></a><span data-ttu-id="066de-105">Generale</span><span class="sxs-lookup"><span data-stu-id="066de-105">General</span></span>

<span data-ttu-id="066de-106">Di seguito sono riportate le funzioni di supporto generali:</span><span class="sxs-lookup"><span data-stu-id="066de-106">The following are general helper functions:</span></span>

<dl>

[<span data-ttu-id="066de-107">**EnumDirTree**</span><span class="sxs-lookup"><span data-stu-id="066de-107">**EnumDirTree**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[<span data-ttu-id="066de-108">**ImagehlpApiVersion**</span><span class="sxs-lookup"><span data-stu-id="066de-108">**ImagehlpApiVersion**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[<span data-ttu-id="066de-109">**ImagehlpApiVersionEx**</span><span class="sxs-lookup"><span data-stu-id="066de-109">**ImagehlpApiVersionEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[<span data-ttu-id="066de-110">**MakeSureDirectoryPathExists**</span><span class="sxs-lookup"><span data-stu-id="066de-110">**MakeSureDirectoryPathExists**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[<span data-ttu-id="066de-111">**SearchTreeForFile**</span><span class="sxs-lookup"><span data-stu-id="066de-111">**SearchTreeForFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a><span data-ttu-id="066de-112">Debugger</span><span class="sxs-lookup"><span data-stu-id="066de-112">Debugger</span></span>

<span data-ttu-id="066de-113">Le funzioni del servizio di debug sono le funzioni più adatte per l'uso da parte di un debugger o del codice di debug in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="066de-113">The debugging service functions are the functions most suited for use by a debugger or the debugging code in an application.</span></span> <span data-ttu-id="066de-114">Queste funzioni possono essere usate in concerto con le funzioni del gestore di simboli per un uso più semplice.</span><span class="sxs-lookup"><span data-stu-id="066de-114">These functions can be used in concert with the symbol handler functions for easier use.</span></span>

<dl>

[<span data-ttu-id="066de-115">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="066de-115">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="066de-116">**EnumerateLoadedModulesEx**</span><span class="sxs-lookup"><span data-stu-id="066de-116">**EnumerateLoadedModulesEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[<span data-ttu-id="066de-117">**FindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="066de-117">**FindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[<span data-ttu-id="066de-118">**FindDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="066de-118">**FindDebugInfoFileEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[<span data-ttu-id="066de-119">**FindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="066de-119">**FindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[<span data-ttu-id="066de-120">**FindExecutableImageEx**</span><span class="sxs-lookup"><span data-stu-id="066de-120">**FindExecutableImageEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[<span data-ttu-id="066de-121">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="066de-121">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="066de-122">**SymSetParentWindow**</span><span class="sxs-lookup"><span data-stu-id="066de-122">**SymSetParentWindow**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[<span data-ttu-id="066de-123">**UnDecorateSymbolName**</span><span class="sxs-lookup"><span data-stu-id="066de-123">**UnDecorateSymbolName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a><span data-ttu-id="066de-124">Accesso alle immagini</span><span class="sxs-lookup"><span data-stu-id="066de-124">Image Access</span></span>

<span data-ttu-id="066de-125">Le funzioni di accesso alle immagini accedono ai dati in un'immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="066de-125">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="066de-126">Le funzioni forniscono accesso di alto livello alla base di immagini e accesso molto specifico alle parti più comuni dei dati di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="066de-126">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="066de-127">**GetTimestampForLoadedLibrary**</span><span class="sxs-lookup"><span data-stu-id="066de-127">**GetTimestampForLoadedLibrary**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[<span data-ttu-id="066de-128">**ImageDirectoryEntryToData**</span><span class="sxs-lookup"><span data-stu-id="066de-128">**ImageDirectoryEntryToData**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[<span data-ttu-id="066de-129">**ImageDirectoryEntryToDataEx**</span><span class="sxs-lookup"><span data-stu-id="066de-129">**ImageDirectoryEntryToDataEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[<span data-ttu-id="066de-130">**ImageNtHeader**</span><span class="sxs-lookup"><span data-stu-id="066de-130">**ImageNtHeader**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[<span data-ttu-id="066de-131">**ImageRvaToSection**</span><span class="sxs-lookup"><span data-stu-id="066de-131">**ImageRvaToSection**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[<span data-ttu-id="066de-132">**ImageRvaToVa**</span><span class="sxs-lookup"><span data-stu-id="066de-132">**ImageRvaToVa**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a><span data-ttu-id="066de-133">Gestore simboli</span><span class="sxs-lookup"><span data-stu-id="066de-133">Symbol Handler</span></span>

<span data-ttu-id="066de-134">Le funzioni del [gestore di simboli](symbol-handling.md) consentono alle applicazioni di accedere in modo semplice e portatile alle informazioni sul debug simbolico di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="066de-134">The [symbol handler](symbol-handling.md) functions give applications easy and portable access to the symbolic debugging information of an image.</span></span> <span data-ttu-id="066de-135">Queste funzioni devono essere utilizzate esclusivamente per garantire l'accesso alle informazioni sui simboli.</span><span class="sxs-lookup"><span data-stu-id="066de-135">These functions should be used exclusively to ensure access to symbolic information.</span></span> <span data-ttu-id="066de-136">Questa operazione è necessaria perché queste funzioni isolano l'applicazione dal formato dei simboli.</span><span class="sxs-lookup"><span data-stu-id="066de-136">This is necessary because these functions isolate the application from the symbol format.</span></span>

<dl>

[<span data-ttu-id="066de-137">**SymAddSourceStream**</span><span class="sxs-lookup"><span data-stu-id="066de-137">**SymAddSourceStream**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[<span data-ttu-id="066de-138">**SymAddSymbol**</span><span class="sxs-lookup"><span data-stu-id="066de-138">**SymAddSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[<span data-ttu-id="066de-139">**SymCleanup**</span><span class="sxs-lookup"><span data-stu-id="066de-139">**SymCleanup**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[<span data-ttu-id="066de-140">**SymDeleteSymbol**</span><span class="sxs-lookup"><span data-stu-id="066de-140">**SymDeleteSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[<span data-ttu-id="066de-141">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="066de-141">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="066de-142">**SymEnumLines**</span><span class="sxs-lookup"><span data-stu-id="066de-142">**SymEnumLines**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[<span data-ttu-id="066de-143">**SymEnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="066de-143">**SymEnumProcesses**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[<span data-ttu-id="066de-144">**SymEnumSourceFiles**</span><span class="sxs-lookup"><span data-stu-id="066de-144">**SymEnumSourceFiles**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[<span data-ttu-id="066de-145">**SymEnumSourceLines**</span><span class="sxs-lookup"><span data-stu-id="066de-145">**SymEnumSourceLines**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[<span data-ttu-id="066de-146">**SymEnumSymbols**</span><span class="sxs-lookup"><span data-stu-id="066de-146">**SymEnumSymbols**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[<span data-ttu-id="066de-147">**SymEnumSymbolsForAddr**</span><span class="sxs-lookup"><span data-stu-id="066de-147">**SymEnumSymbolsForAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[<span data-ttu-id="066de-148">**SymEnumTypes**</span><span class="sxs-lookup"><span data-stu-id="066de-148">**SymEnumTypes**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[<span data-ttu-id="066de-149">**SymEnumTypesByName**</span><span class="sxs-lookup"><span data-stu-id="066de-149">**SymEnumTypesByName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[<span data-ttu-id="066de-150">**SymFindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="066de-150">**SymFindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[<span data-ttu-id="066de-151">**SymFindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="066de-151">**SymFindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[<span data-ttu-id="066de-152">**SymFindFileInPath**</span><span class="sxs-lookup"><span data-stu-id="066de-152">**SymFindFileInPath**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[<span data-ttu-id="066de-153">**SymFromAddr**</span><span class="sxs-lookup"><span data-stu-id="066de-153">**SymFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[<span data-ttu-id="066de-154">**SymFromIndex**</span><span class="sxs-lookup"><span data-stu-id="066de-154">**SymFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[<span data-ttu-id="066de-155">**SymFromName**</span><span class="sxs-lookup"><span data-stu-id="066de-155">**SymFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[<span data-ttu-id="066de-156">**SymFromToken**</span><span class="sxs-lookup"><span data-stu-id="066de-156">**SymFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[<span data-ttu-id="066de-157">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="066de-157">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="066de-158">**SymGetFileLineOffsets64**</span><span class="sxs-lookup"><span data-stu-id="066de-158">**SymGetFileLineOffsets64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[<span data-ttu-id="066de-159">**SymGetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="066de-159">**SymGetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[<span data-ttu-id="066de-160">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="066de-160">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="066de-161">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="066de-161">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="066de-162">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="066de-162">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="066de-163">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="066de-163">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="066de-164">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="066de-164">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="066de-165">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="066de-165">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="066de-166">**SymGetOmaps**</span><span class="sxs-lookup"><span data-stu-id="066de-166">**SymGetOmaps**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[<span data-ttu-id="066de-167">**SymGetOptions**</span><span class="sxs-lookup"><span data-stu-id="066de-167">**SymGetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[<span data-ttu-id="066de-168">**SymGetScope**</span><span class="sxs-lookup"><span data-stu-id="066de-168">**SymGetScope**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[<span data-ttu-id="066de-169">**SymGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="066de-169">**SymGetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[<span data-ttu-id="066de-170">**SymGetSymbolFile**</span><span class="sxs-lookup"><span data-stu-id="066de-170">**SymGetSymbolFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[<span data-ttu-id="066de-171">**SymGetTypeFromName**</span><span class="sxs-lookup"><span data-stu-id="066de-171">**SymGetTypeFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[<span data-ttu-id="066de-172">**SymGetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="066de-172">**SymGetTypeInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[<span data-ttu-id="066de-173">**SymGetTypeInfoEx**</span><span class="sxs-lookup"><span data-stu-id="066de-173">**SymGetTypeInfoEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[<span data-ttu-id="066de-174">**SymInitialize**</span><span class="sxs-lookup"><span data-stu-id="066de-174">**SymInitialize**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[<span data-ttu-id="066de-175">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="066de-175">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="066de-176">**SymLoadModuleEx**</span><span class="sxs-lookup"><span data-stu-id="066de-176">**SymLoadModuleEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[<span data-ttu-id="066de-177">**SymMatchFileName**</span><span class="sxs-lookup"><span data-stu-id="066de-177">**SymMatchFileName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[<span data-ttu-id="066de-178">**SymMatchString**</span><span class="sxs-lookup"><span data-stu-id="066de-178">**SymMatchString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[<span data-ttu-id="066de-179">**SymNext**</span><span class="sxs-lookup"><span data-stu-id="066de-179">**SymNext**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[<span data-ttu-id="066de-180">**SymPrev**</span><span class="sxs-lookup"><span data-stu-id="066de-180">**SymPrev**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[<span data-ttu-id="066de-181">**SymRefreshModuleList**</span><span class="sxs-lookup"><span data-stu-id="066de-181">**SymRefreshModuleList**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[<span data-ttu-id="066de-182">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="066de-182">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="066de-183">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="066de-183">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="066de-184">**SymSearch**</span><span class="sxs-lookup"><span data-stu-id="066de-184">**SymSearch**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[<span data-ttu-id="066de-185">**SymSetContext**</span><span class="sxs-lookup"><span data-stu-id="066de-185">**SymSetContext**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[<span data-ttu-id="066de-186">**SymSetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="066de-186">**SymSetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[<span data-ttu-id="066de-187">**SymSetOptions**</span><span class="sxs-lookup"><span data-stu-id="066de-187">**SymSetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[<span data-ttu-id="066de-188">**SymSetScopeFromAddr**</span><span class="sxs-lookup"><span data-stu-id="066de-188">**SymSetScopeFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[<span data-ttu-id="066de-189">**SymSetScopeFromIndex**</span><span class="sxs-lookup"><span data-stu-id="066de-189">**SymSetScopeFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[<span data-ttu-id="066de-190">**SymSetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="066de-190">**SymSetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[<span data-ttu-id="066de-191">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="066de-191">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="066de-192">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="066de-192">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a><span data-ttu-id="066de-193">Server di simboli</span><span class="sxs-lookup"><span data-stu-id="066de-193">Symbol Server</span></span>

<span data-ttu-id="066de-194">Il [server di simboli](symbol-servers-and-symbol-stores.md) consente ai debugger di recuperare automaticamente i file di simboli corretti senza nomi di prodotto, versioni o numeri di Build.</span><span class="sxs-lookup"><span data-stu-id="066de-194">The [symbol server](symbol-servers-and-symbol-stores.md) enables debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="066de-195">Con il server di simboli vengono utilizzate le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="066de-195">The following functions are used with the symbol server.</span></span>

<dl>

[<span data-ttu-id="066de-196">**SymSrvDeltaName**</span><span class="sxs-lookup"><span data-stu-id="066de-196">**SymSrvDeltaName**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[<span data-ttu-id="066de-197">**SymSrvGetFileIndexes**</span><span class="sxs-lookup"><span data-stu-id="066de-197">**SymSrvGetFileIndexes**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[<span data-ttu-id="066de-198">**SymSrvGetFileIndexInfo**</span><span class="sxs-lookup"><span data-stu-id="066de-198">**SymSrvGetFileIndexInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[<span data-ttu-id="066de-199">**SymSrvGetFileIndexString**</span><span class="sxs-lookup"><span data-stu-id="066de-199">**SymSrvGetFileIndexString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[<span data-ttu-id="066de-200">**SymSrvGetSupplement**</span><span class="sxs-lookup"><span data-stu-id="066de-200">**SymSrvGetSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[<span data-ttu-id="066de-201">**SymSrvIsStore**</span><span class="sxs-lookup"><span data-stu-id="066de-201">**SymSrvIsStore**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[<span data-ttu-id="066de-202">**SymSrvStoreFile**</span><span class="sxs-lookup"><span data-stu-id="066de-202">**SymSrvStoreFile**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[<span data-ttu-id="066de-203">**SymSrvStoreSupplement**</span><span class="sxs-lookup"><span data-stu-id="066de-203">**SymSrvStoreSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a><span data-ttu-id="066de-204">File di minidump in modalità utente</span><span class="sxs-lookup"><span data-stu-id="066de-204">User-mode Minidump Files</span></span>

<span data-ttu-id="066de-205">Le funzioni di minidump consentono alle applicazioni di produrre file CrashDumps che contengono un subset utile dell'intero contesto del processo. Questa operazione è nota come [file di minidump](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="066de-205">The minidump functions provide a way for applications to produce crashdump files that contain a useful subset of the entire process context; this is known as a [minidump file](minidump-files.md).</span></span> <span data-ttu-id="066de-206">Con i file di minidump vengono usate le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="066de-206">The following functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="066de-207">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="066de-207">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="066de-208">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="066de-208">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="066de-209">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="066de-209">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a><span data-ttu-id="066de-210">Server di origine</span><span class="sxs-lookup"><span data-stu-id="066de-210">Source Server</span></span>

<span data-ttu-id="066de-211">Il [server di origine](source-server-and-source-indexing.md) consente a un client di recuperare la versione esatta dei file di origine utilizzati per compilare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="066de-211">[Source server](source-server-and-source-indexing.md) enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="066de-212">Le funzioni seguenti vengono utilizzate con il server di origine.</span><span class="sxs-lookup"><span data-stu-id="066de-212">The following functions are used with source server.</span></span>

-   [<span data-ttu-id="066de-213">**SymGetSourceFile**</span><span class="sxs-lookup"><span data-stu-id="066de-213">**SymGetSourceFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [<span data-ttu-id="066de-214">**SymEnumSourceFileTokens**</span><span class="sxs-lookup"><span data-stu-id="066de-214">**SymEnumSourceFileTokens**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [<span data-ttu-id="066de-215">**SymEnumSourceFileTokensProc**</span><span class="sxs-lookup"><span data-stu-id="066de-215">**SymEnumSourceFileTokensProc**</span></span>](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [<span data-ttu-id="066de-216">**SymGetSourceFileFromToken**</span><span class="sxs-lookup"><span data-stu-id="066de-216">**SymGetSourceFileFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [<span data-ttu-id="066de-217">**SymGetSourceFileToken**</span><span class="sxs-lookup"><span data-stu-id="066de-217">**SymGetSourceFileToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [<span data-ttu-id="066de-218">**SymGetSourceVarFromToken**</span><span class="sxs-lookup"><span data-stu-id="066de-218">**SymGetSourceVarFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a><span data-ttu-id="066de-219">Funzioni obsolete</span><span class="sxs-lookup"><span data-stu-id="066de-219">Obsolete Functions</span></span>

<dl>

[<span data-ttu-id="066de-220">**MapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="066de-220">**MapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[<span data-ttu-id="066de-221">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="066de-221">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="066de-222">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="066de-222">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="066de-223">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="066de-223">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="066de-224">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="066de-224">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="066de-225">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="066de-225">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="066de-226">**UnMapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="066de-226">**UnMapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



