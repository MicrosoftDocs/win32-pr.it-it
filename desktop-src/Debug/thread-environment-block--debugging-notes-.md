---
description: Blocco ambiente thread (note di debug)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Blocco ambiente thread (note di debug)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877786"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="23493-103">Blocco ambiente thread (note di debug)</span><span class="sxs-lookup"><span data-stu-id="23493-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="23493-104">Il blocco dell'ambiente del thread ([**struttura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) include informazioni di contesto per un thread.</span><span class="sxs-lookup"><span data-stu-id="23493-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="23493-105">Nelle versioni seguenti di Windows, l'offset dell'indirizzo TEB a 32 bit entro il TEB a 64 bit è 0.</span><span class="sxs-lookup"><span data-stu-id="23493-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="23493-106">Può essere usato per accedere direttamente al TEB a 32 bit di un thread WOW64.</span><span class="sxs-lookup"><span data-stu-id="23493-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="23493-107">Questo potrebbe cambiare nelle versioni successive di Windows</span><span class="sxs-lookup"><span data-stu-id="23493-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="23493-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23493-108">Windows Vista</span></span> | <span data-ttu-id="23493-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23493-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="23493-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23493-110">Windows 7</span></span>     | <span data-ttu-id="23493-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23493-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="23493-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="23493-112">Windows 8</span></span>     | <span data-ttu-id="23493-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23493-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="23493-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="23493-114">Windows 8.1</span></span>   | <span data-ttu-id="23493-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="23493-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="23493-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23493-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23493-117">Strutture di debug</span><span class="sxs-lookup"><span data-stu-id="23493-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="23493-118">**\_Contesto WOW64**</span><span class="sxs-lookup"><span data-stu-id="23493-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
