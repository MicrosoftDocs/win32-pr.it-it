---
title: Routine di _aulldiv
description: Divide due interi ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104472203"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="af8dc-103">\_Routine aulldiv</span><span class="sxs-lookup"><span data-stu-id="af8dc-103">\_aulldiv Routine</span></span>

<span data-ttu-id="af8dc-104">Divide due interi **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="af8dc-105">Ad esempio, per dividere due valori UInt64, il compilatore potrebbe generare una chiamata alla routine **\_ aulldiv** .</span><span class="sxs-lookup"><span data-stu-id="af8dc-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="af8dc-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="af8dc-106">Remarks</span></span>

<span data-ttu-id="af8dc-107">La routine **\_ aulldiv** è una routine di supporto per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="af8dc-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="af8dc-108">Il fatto che il compilatore usi **\_ aulldiv** dipenda completamente dal set di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="af8dc-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="af8dc-109">Questa funzione viene utilizzata solo su piattaforme x86.</span><span class="sxs-lookup"><span data-stu-id="af8dc-109">This function is used only on x86 platforms.</span></span>
