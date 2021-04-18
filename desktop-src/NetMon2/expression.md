---
description: Contiene un gruppo di matrici ANDEXP valutate come peer.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Struttura di espressioni (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305940"
---
# <a name="expression-structure"></a><span data-ttu-id="bc257-103">Struttura dell'espressione</span><span class="sxs-lookup"><span data-stu-id="bc257-103">EXPRESSION structure</span></span>

<span data-ttu-id="bc257-104">La struttura dell' **espressione** contiene un gruppo di matrici **ANDEXP** valutate come peer nelle espressioni and logiche, che hanno il formato</span><span class="sxs-lookup"><span data-stu-id="bc257-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="bc257-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span><span class="sxs-lookup"><span data-stu-id="bc257-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc257-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc257-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="bc257-107">Members</span><span class="sxs-lookup"><span data-stu-id="bc257-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc257-108">**nAndExps**</span><span class="sxs-lookup"><span data-stu-id="bc257-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="bc257-109">Numero di modelli di **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="bc257-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="bc257-110">**AndExp**</span><span class="sxs-lookup"><span data-stu-id="bc257-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="bc257-111">Matrice di modelli di **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="bc257-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="bc257-112">Il filtro di acquisizione dispone tutte le righe di questa matrice come istruzioni AND logiche.</span><span class="sxs-lookup"><span data-stu-id="bc257-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="bc257-113">Tenere presente che ogni struttura dell'espressione può contenere un massimo di quattro modelli di **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="bc257-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc257-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc257-114">Remarks</span></span>

<span data-ttu-id="bc257-115">Per ulteriori informazioni sull'implementazione di questa struttura come parte di un filtro di acquisizione, vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bc257-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc257-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc257-116">Requirements</span></span>



| <span data-ttu-id="bc257-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc257-117">Requirement</span></span> | <span data-ttu-id="bc257-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bc257-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc257-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc257-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc257-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc257-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc257-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc257-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc257-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc257-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc257-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc257-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc257-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc257-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc257-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc257-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc257-126">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="bc257-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="bc257-127">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="bc257-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




