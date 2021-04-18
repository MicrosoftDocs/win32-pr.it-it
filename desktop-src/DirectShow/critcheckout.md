---
description: Restituisce FALSE se il thread corrente è il proprietario della sezione critica specificata.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Funzione CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327189"
---
# <a name="critcheckout-function"></a><span data-ttu-id="1643b-103">CritCheckOut (funzione)</span><span class="sxs-lookup"><span data-stu-id="1643b-103">CritCheckOut function</span></span>

<span data-ttu-id="1643b-104">Restituisce **false** se il thread corrente è il proprietario della sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="1643b-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="1643b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1643b-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="1643b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1643b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1643b-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="1643b-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="1643b-108">Puntatore a una sezione critica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="1643b-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1643b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1643b-109">Return value</span></span>

<span data-ttu-id="1643b-110">Nelle build di debug, restituisce **false** se il thread corrente è il proprietario di questa sezione critica o **true** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1643b-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="1643b-111">Nelle compilazioni finali restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="1643b-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1643b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1643b-112">Remarks</span></span>

<span data-ttu-id="1643b-113">Questa funzione è l'inverso della funzione [**CritCheckIn**](critcheckin.md) .</span><span class="sxs-lookup"><span data-stu-id="1643b-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="1643b-114">Se **CritCheckIn** restituisce **true**, **CritCheckOut** restituisce **false** e viceversa.</span><span class="sxs-lookup"><span data-stu-id="1643b-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="1643b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1643b-115">Requirements</span></span>



| <span data-ttu-id="1643b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1643b-116">Requirement</span></span> | <span data-ttu-id="1643b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1643b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1643b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1643b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1643b-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1643b-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1643b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="1643b-120">Library</span></span><br/> | <dl> <span data-ttu-id="1643b-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1643b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1643b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1643b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1643b-123">Funzioni di debug della sezione critica</span><span class="sxs-lookup"><span data-stu-id="1643b-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




