---
title: Gestione delle eccezioni in WOW64
description: WOW64 usa le eccezioni native x64, ia64 o ARM64 come trasporto per le eccezioni x86. Pertanto, in un'applicazione a 32 bit in esecuzione in WOW64, le eccezioni non rilevate si comportano come eccezioni native a 64 bit.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047224"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="f3583-104">Gestione delle eccezioni in WOW64</span><span class="sxs-lookup"><span data-stu-id="f3583-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="f3583-105">WOW64 usa le eccezioni native x64, ia64 o ARM64 come trasporto per le eccezioni x86.</span><span class="sxs-lookup"><span data-stu-id="f3583-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="f3583-106">Pertanto, in un'applicazione a 32 bit in esecuzione in WOW64, le eccezioni non rilevate si comportano come eccezioni native a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f3583-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="f3583-107">In un'applicazione in esecuzione su una versione di Windows a 32 bit, le eccezioni non rilevate vengono passate ai gestori di eccezioni di livello superiore dell'applicazione, se disponibili.</span><span class="sxs-lookup"><span data-stu-id="f3583-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="f3583-108">Nella stessa applicazione a 32 bit in esecuzione in WOW64, è possibile che il sistema elimini le eccezioni non rilevate.</span><span class="sxs-lookup"><span data-stu-id="f3583-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="f3583-109">**Windows Vista, Windows Server 2003 e Windows XP:** Nella stessa applicazione a 32 bit in esecuzione in WOW64, il sistema chiama i filtri delle eccezioni, ma può impedire le eccezioni non rilevate senza richiamare i gestori associati.</span><span class="sxs-lookup"><span data-stu-id="f3583-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="f3583-110">Questo comportamento è stato modificato a partire da Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f3583-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="f3583-111">Per ulteriori informazioni sulle eccezioni non rilevate nelle routine della finestra, vedere la funzione [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f3583-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 