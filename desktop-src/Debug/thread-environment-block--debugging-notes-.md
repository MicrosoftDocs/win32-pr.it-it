---
description: Blocco dell'ambiente thread (note sul debug)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Blocco dell'ambiente thread (note sul debug)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550586"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="1216f-103">Blocco dell'ambiente thread (note sul debug)</span><span class="sxs-lookup"><span data-stu-id="1216f-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="1216f-104">Il blocco di ambiente thread ([**struttura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contiene informazioni di contesto per un thread.</span><span class="sxs-lookup"><span data-stu-id="1216f-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="1216f-105">Nelle versioni seguenti di Windows l'offset dell'indirizzo TEB a 32 bit all'interno del TEB a 64 bit è 0.</span><span class="sxs-lookup"><span data-stu-id="1216f-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="1216f-106">Può essere usato per accedere direttamente al TEB a 32 bit di un thread WOW64.</span><span class="sxs-lookup"><span data-stu-id="1216f-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="1216f-107">Questa modifica potrebbe cambiare nelle versioni successive di Windows</span><span class="sxs-lookup"><span data-stu-id="1216f-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="1216f-108">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="1216f-108">Platform</span></span>     | <span data-ttu-id="1216f-109">Versione</span><span class="sxs-lookup"><span data-stu-id="1216f-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="1216f-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1216f-110">Windows Vista</span></span> | <span data-ttu-id="1216f-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1216f-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="1216f-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1216f-112">Windows 7</span></span>     | <span data-ttu-id="1216f-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1216f-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="1216f-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1216f-114">Windows 8</span></span>     | <span data-ttu-id="1216f-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1216f-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="1216f-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1216f-116">Windows 8.1</span></span>   | <span data-ttu-id="1216f-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1216f-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1216f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1216f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1216f-119">Strutture di debug</span><span class="sxs-lookup"><span data-stu-id="1216f-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="1216f-120">**CONTESTO \_ WOW64**</span><span class="sxs-lookup"><span data-stu-id="1216f-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
