---
description: Il gestore di simboli è progettato per tenere traccia di diversi set di file di simboli.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inizializzazione del gestore di simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126051"
---
# <a name="symbol-handler-initialization"></a><span data-ttu-id="f881d-103">Inizializzazione del gestore di simboli</span><span class="sxs-lookup"><span data-stu-id="f881d-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="f881d-104">Il gestore di simboli è progettato per tenere traccia di diversi set di file di simboli.</span><span class="sxs-lookup"><span data-stu-id="f881d-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="f881d-105">Per inizializzare il gestore di simboli, chiamare la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="f881d-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="f881d-106">Il parametro *hProcess* può essere un numero arbitrario univoco, un valore restituito dalla funzione [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o l'identificatore di qualsiasi processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f881d-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="f881d-107">Il parametro *fInvadeProcess* indica se il gestore di simboli deve enumerare i moduli caricati dal processo e caricare i simboli per ogni modulo.</span><span class="sxs-lookup"><span data-stu-id="f881d-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="f881d-108">Se *fInvadeProcess* è **true**, il parametro *hProcess* deve essere il valore restituito da **GetCurrentProcess** o l'identificatore di un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="f881d-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="f881d-109">Per aggiornare l'elenco, usare la funzione [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .</span><span class="sxs-lookup"><span data-stu-id="f881d-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="f881d-110">L'uso di *fInvadeProcess* è un modo semplice per caricare tutti i file di simboli per un processo.</span><span class="sxs-lookup"><span data-stu-id="f881d-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="f881d-111">Tuttavia, il gestore di simboli non tenterà di caricare i simboli per i moduli caricati successivamente dalla funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="f881d-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="f881d-112">In questo caso, è necessario utilizzare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .</span><span class="sxs-lookup"><span data-stu-id="f881d-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
