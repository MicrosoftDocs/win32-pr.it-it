---
description: Il metodo Prev recupera la posizione precedente nell'elenco.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Metodo CBaseList. prev (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328644"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="c4c82-103">CBaseList. prev, metodo</span><span class="sxs-lookup"><span data-stu-id="c4c82-103">CBaseList.Prev method</span></span>

<span data-ttu-id="c4c82-104">Il `Prev` metodo recupera la posizione precedente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c4c82-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4c82-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="c4c82-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c82-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="c4c82-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c82-108">Valore della posizione.</span><span class="sxs-lookup"><span data-stu-id="c4c82-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c82-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4c82-109">Return value</span></span>

<span data-ttu-id="c4c82-110">Restituisce l'indicatore di posizione precedente alla posizione specificata in *pos*.</span><span class="sxs-lookup"><span data-stu-id="c4c82-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c82-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4c82-111">Remarks</span></span>

<span data-ttu-id="c4c82-112">Se *pos* è la prima posizione nell'elenco, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="c4c82-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="c4c82-113">Se *pos* è **null**, il metodo restituisce l'ultima posizione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c4c82-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c82-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4c82-114">Requirements</span></span>



| <span data-ttu-id="c4c82-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c82-115">Requirement</span></span> | <span data-ttu-id="c4c82-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c82-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c82-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4c82-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c4c82-118"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c82-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c4c82-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4c82-119">Library</span></span><br/> | <dl> <span data-ttu-id="c4c82-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c82-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c82-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4c82-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c82-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="c4c82-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




