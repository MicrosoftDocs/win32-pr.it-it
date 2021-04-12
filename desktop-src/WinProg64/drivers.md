---
title: Driver (Guida per programmatori per Windows a 64 bit)
description: La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare un'unica base di codice sorgente per le applicazioni a 32 bit e 64 bit. In larga misura, questo vale anche per i driver Windows a 32 bit e a 64 bit.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- driver programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340212"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="654e2-105">Driver (Guida per programmatori per Windows a 64 bit)</span><span class="sxs-lookup"><span data-stu-id="654e2-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="654e2-106">La versione a 64 bit di Windows è progettata per consentire agli sviluppatori di usare un'unica base di codice sorgente per le applicazioni a 32 bit e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="654e2-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="654e2-107">In larga misura, questo vale anche per i driver Windows a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="654e2-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="654e2-108">Tuttavia, i driver a 32 bit non possono essere eseguiti su Windows a 64 bit e devono essere trasportati.</span><span class="sxs-lookup"><span data-stu-id="654e2-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="654e2-109">Per le applicazioni in modalità utente, Windows a 64 bit include WOW64, che consente l'esecuzione di applicazioni Windows a 32 bit (con alcune perdite di prestazioni) sui sistemi che eseguono Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="654e2-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="654e2-110">Non esiste alcun livello di conversione equivalente per i driver.</span><span class="sxs-lookup"><span data-stu-id="654e2-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="654e2-111">Per informazioni sul porting dei driver in Windows a 64 bit, vedere [problemi relativi a 64 bit](https://msdn.microsoft.com/library/aa489627.aspx) in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="654e2-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




