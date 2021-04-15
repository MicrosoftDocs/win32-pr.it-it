---
description: Funzioni di debug della sezione critica
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Funzioni di debug della sezione critica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520993"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="2200e-103">Funzioni di debug della sezione critica</span><span class="sxs-lookup"><span data-stu-id="2200e-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="2200e-104">Queste funzioni consentono di eseguire il debug di sezioni critiche nel codice, semplificando la ricerca della cause di un deadlock.</span><span class="sxs-lookup"><span data-stu-id="2200e-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="2200e-105">Queste funzioni usano la classe helper [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="2200e-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="2200e-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="2200e-106">Function</span></span>                             | <span data-ttu-id="2200e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2200e-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="2200e-108">**CritCheckIn**</span><span class="sxs-lookup"><span data-stu-id="2200e-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="2200e-109">Restituisce **true** se il thread corrente è proprietario della sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="2200e-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="2200e-110">**CritCheckOut**</span><span class="sxs-lookup"><span data-stu-id="2200e-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="2200e-111">Restituisce **false** se il thread corrente è proprietario della sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="2200e-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="2200e-112">**DbgLockTrace**</span><span class="sxs-lookup"><span data-stu-id="2200e-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="2200e-113">Abilita o Disabilita la registrazione di debug per una sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="2200e-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="2200e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2200e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2200e-115">Utilità di debug</span><span class="sxs-lookup"><span data-stu-id="2200e-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



