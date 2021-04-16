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
# <a name="updated-platform-support"></a><span data-ttu-id="401e2-103">Supporto aggiornato della piattaforma</span><span class="sxs-lookup"><span data-stu-id="401e2-103">Updated Platform Support</span></span>

<span data-ttu-id="401e2-104">Se necessario, la libreria DbgHelp è stata ampliata per supportare sia Windows a 32 che a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="401e2-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="401e2-105">Le definizioni della funzione e della struttura originali sono ancora in DbgHelp. h, ma sono presenti anche versioni aggiornate di queste definizioni compatibili con Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="401e2-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="401e2-106">Se si usano le funzioni aggiornate nel codice, è possibile compilarlo sia per Windows a 32 che a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="401e2-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="401e2-107">Il codice sarà anche più efficiente, poiché le funzioni originali chiamano semplicemente le funzioni aggiornate per eseguire il lavoro.</span><span class="sxs-lookup"><span data-stu-id="401e2-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="401e2-108">Ad esempio, DbgHelp. h contiene le definizioni per **SymUnloadModule** (funzione originale) e **SymUnloadModule64** (funzione aggiornata).</span><span class="sxs-lookup"><span data-stu-id="401e2-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="401e2-109">Queste definizioni sono quasi identiche, ma usano tipi diversi per il parametro *BaseOfDll* .</span><span class="sxs-lookup"><span data-stu-id="401e2-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="401e2-110">(**SymUnloadModule** usa il tipo **DWORD** , mentre **SymUnloadModule64** usa il tipo **DWORD64** ). Se si scrive il codice per l'uso di **SymUnloadModule64**, è possibile compilarlo per le finestre 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="401e2-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="401e2-111">Il codice è anche più efficiente rispetto a quando si chiama **SymUnloadModule**.</span><span class="sxs-lookup"><span data-stu-id="401e2-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="401e2-112">Di seguito è riportato un elenco delle funzioni aggiornate:</span><span class="sxs-lookup"><span data-stu-id="401e2-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="401e2-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="401e2-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="401e2-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="401e2-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="401e2-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="401e2-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="401e2-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="401e2-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="401e2-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="401e2-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="401e2-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="401e2-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="401e2-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="401e2-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="401e2-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="401e2-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="401e2-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="401e2-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="401e2-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="401e2-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="401e2-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="401e2-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="401e2-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="401e2-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="401e2-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="401e2-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="401e2-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="401e2-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="401e2-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="401e2-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="401e2-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="401e2-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="401e2-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="401e2-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="401e2-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="401e2-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="401e2-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="401e2-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="401e2-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="401e2-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="401e2-133">Di seguito è riportato un elenco delle strutture aggiornate:</span><span class="sxs-lookup"><span data-stu-id="401e2-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="401e2-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="401e2-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="401e2-135">**IMAGEHLP \_ simbolo posticipato \_ \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="401e2-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="401e2-136">**\_SYMBOL64 duplicato Imagehlp \_**</span><span class="sxs-lookup"><span data-stu-id="401e2-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="401e2-137">**\_LINE64 Imagehlp**</span><span class="sxs-lookup"><span data-stu-id="401e2-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="401e2-138">**\_MODULE64 Imagehlp**</span><span class="sxs-lookup"><span data-stu-id="401e2-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="401e2-139">**\_SYMBOL64 Imagehlp**</span><span class="sxs-lookup"><span data-stu-id="401e2-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="401e2-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="401e2-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="401e2-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="401e2-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



