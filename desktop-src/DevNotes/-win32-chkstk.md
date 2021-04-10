---
description: Chiamata eseguita dal compilatore quando si dispone di più di una pagina di variabili locali nella funzione.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: Routine di _chkstk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965879"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="591d0-103">\_Routine chkstk</span><span class="sxs-lookup"><span data-stu-id="591d0-103">\_chkstk Routine</span></span>

<span data-ttu-id="591d0-104">Chiamata eseguita dal compilatore quando si dispone di più di una pagina di variabili locali nella funzione.</span><span class="sxs-lookup"><span data-stu-id="591d0-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="591d0-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="591d0-105">Remarks</span></span>

<span data-ttu-id="591d0-106">\_la routine chkstk è una routine di supporto per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="591d0-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="591d0-107">Per i compilatori x86, \_ la routine chkstk viene chiamata quando le variabili locali superano i 4K byte; per i compilatori x64 è di 8 KB.</span><span class="sxs-lookup"><span data-stu-id="591d0-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 



