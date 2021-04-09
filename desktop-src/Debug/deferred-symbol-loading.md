---
description: Per ridurre il tempo e la memoria quando si utilizzano molti file di simboli, utilizzare la funzione SymSetOptions per impostare l'opzione di caricamento posticipato dei simboli ( \_ caricamenti posticipati SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Caricamento posticipato dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965888"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="b9c32-103">Caricamento posticipato dei simboli</span><span class="sxs-lookup"><span data-stu-id="b9c32-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="b9c32-104">Per conservare il tempo e la memoria quando si utilizzano molti file di simboli, utilizzare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per impostare l'opzione di caricamento posticipato dei simboli (SYMOPT \_ rinviati \_ ), quindi utilizzare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) per caricare i simboli rinviati per tutti i moduli.</span><span class="sxs-lookup"><span data-stu-id="b9c32-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="b9c32-105">Il gestore dei simboli elenca i simboli disponibili per i moduli, ma non esegue il mapping delle informazioni di debug in memoria fino a quando non viene richiesto.</span><span class="sxs-lookup"><span data-stu-id="b9c32-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="b9c32-106">Si tratta del metodo preferito per utilizzare in modo efficiente i simboli di debug.</span><span class="sxs-lookup"><span data-stu-id="b9c32-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="b9c32-107">Tutte le funzioni che utilizzano simboli sono interessate dal caricamento posticipato dei simboli.</span><span class="sxs-lookup"><span data-stu-id="b9c32-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 



