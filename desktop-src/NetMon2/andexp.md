---
description: La struttura ANDEXP contiene una matrice di corrispondenze del criterio usate per valutare i dati del frame.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Struttura ANDEXP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346836"
---
# <a name="andexp-structure"></a><span data-ttu-id="1b350-103">Struttura ANDEXP</span><span class="sxs-lookup"><span data-stu-id="1b350-103">ANDEXP structure</span></span>

<span data-ttu-id="1b350-104">La struttura **ANDEXP** contiene una matrice di corrispondenze del criterio usate per valutare i dati del frame.</span><span class="sxs-lookup"><span data-stu-id="1b350-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b350-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b350-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="1b350-106">Members</span><span class="sxs-lookup"><span data-stu-id="1b350-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b350-107">**nPatternMatches**</span><span class="sxs-lookup"><span data-stu-id="1b350-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="1b350-108">Numero di corrispondenze del criterio.</span><span class="sxs-lookup"><span data-stu-id="1b350-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="1b350-109">**PatternMatch**</span><span class="sxs-lookup"><span data-stu-id="1b350-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="1b350-110">Matrice di elementi delle corrispondenze dei criteri.</span><span class="sxs-lookup"><span data-stu-id="1b350-110">Array of pattern match elements.</span></span> <span data-ttu-id="1b350-111">Si noti che ogni struttura **ANDEXP** può contenere un massimo di quattro elementi di corrispondenza del criterio.</span><span class="sxs-lookup"><span data-stu-id="1b350-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="1b350-112">Per ulteriori informazioni su questo membro, vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="1b350-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b350-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b350-113">Remarks</span></span>

<span data-ttu-id="1b350-114">I modelli nella matrice **PatternMatch** \[ Max \_ patterns \] vengono uniti come peer nelle istruzioni OR logiche nel formato</span><span class="sxs-lookup"><span data-stu-id="1b350-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="1b350-115">(Modello 1 \| \| Schema 2 \| \| modello 3).</span><span class="sxs-lookup"><span data-stu-id="1b350-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="1b350-116">Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="1b350-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="1b350-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b350-117">Requirements</span></span>



| <span data-ttu-id="1b350-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b350-118">Requirement</span></span> | <span data-ttu-id="1b350-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1b350-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b350-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b350-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b350-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1b350-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1b350-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b350-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b350-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1b350-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b350-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b350-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b350-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b350-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b350-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b350-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b350-127">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="1b350-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




