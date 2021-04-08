---
title: Affinità processori in WOW64
description: Windows a 32 bit supporta un massimo di 32 processori. Pertanto, le funzioni come GetProcessAffinityMask simulano un computer con processori 32 quando vengono chiamate in WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- Programmazione di Windows con affinità processori a 64 bit
- Programmazione Windows WOW64 a 64 bit, affinità processori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728410"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="33756-106">Affinità processori in WOW64</span><span class="sxs-lookup"><span data-stu-id="33756-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="33756-107">Windows a 32 bit supporta un massimo di 32 processori.</span><span class="sxs-lookup"><span data-stu-id="33756-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="33756-108">Pertanto, le funzioni come [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulano un computer con processori 32 quando vengono chiamate in WOW64.</span><span class="sxs-lookup"><span data-stu-id="33756-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="33756-109">La maschera di affinità viene ottenuta eseguendo un'operazione OR bit per bit dei primi 32 bit della maschera con i 32 bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="33756-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="33756-110">Se pertanto un thread presenta affinità per i processori 0, 1 e 32, WOW64 segnala l'affinità come 0 e 1, perché il processore 32 viene mappato al processore 0.</span><span class="sxs-lookup"><span data-stu-id="33756-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="33756-111">Le funzioni che impostano l'affinità del processore, ad esempio [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), limitano i processori ai primi processori 32 in WOW64.</span><span class="sxs-lookup"><span data-stu-id="33756-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="33756-112">Per ulteriori informazioni sull'affinità processori, vedere la pagina relativa a [più processori](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="33756-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 