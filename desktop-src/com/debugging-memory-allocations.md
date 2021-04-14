---
title: Debug delle allocazioni di memoria
description: Debug delle allocazioni di memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339327"
---
# <a name="debugging-memory-allocations"></a><span data-ttu-id="ed1a2-103">Debug delle allocazioni di memoria</span><span class="sxs-lookup"><span data-stu-id="ed1a2-103">Debugging Memory Allocations</span></span>

<span data-ttu-id="ed1a2-104">COM fornisce l'interfaccia [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) che gli sviluppatori possono utilizzare per eseguire il debug delle allocazioni di memoria.</span><span class="sxs-lookup"><span data-stu-id="ed1a2-104">COM provides the [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) interface for developers to use to debug their memory allocations.</span></span> <span data-ttu-id="ed1a2-105">Per ogni metodo in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)sono disponibili due metodi in **IMallocSpy**, un metodo "pre" e un metodo "post".</span><span class="sxs-lookup"><span data-stu-id="ed1a2-105">For each method in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc), there are two methods in **IMallocSpy**, a "pre" method and a "post" method.</span></span> <span data-ttu-id="ed1a2-106">Quando uno sviluppatore lo implementa e lo pubblica nel sistema, il sistema chiama il metodo **IMallocSpy** "pre" immediatamente prima del metodo **IMalloc** corrispondente, consentendo in modo efficace al codice di debug di "Spy" nell'operazione di allocazione e chiama il metodo "post" per rilasciare la spia.</span><span class="sxs-lookup"><span data-stu-id="ed1a2-106">After a developer implements it and publishes it to the system, the system calls the **IMallocSpy** "pre" method just before the corresponding **IMalloc** method, effectively allowing the debug code to "spy" on the allocation operation, and calls the "post" method to release the spy.</span></span>

<span data-ttu-id="ed1a2-107">Ad esempio, quando COM rileva che la chiamata successiva è una chiamata a [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), chiama [**IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), eseguendo tutte le operazioni di debug desiderate dallo sviluppatore durante l'esecuzione dell' **allocazione** e, quando la chiamata di **Alloc** restituisce, chiama [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) per rilasciare la spia e restituire il controllo al codice.</span><span class="sxs-lookup"><span data-stu-id="ed1a2-107">For example, when COM detects that the next call is a call to [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), it calls [**IMallocSpy::PreAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), executing whatever debug operations the developer wants during the **Alloc** execution, and then, when the **Alloc** call returns, calls [**IMallocSpy::PostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) to release the spy and return control to the code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed1a2-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed1a2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed1a2-109">Gestione dell'allocazione di memoria</span><span class="sxs-lookup"><span data-stu-id="ed1a2-109">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> </dl>

 

 