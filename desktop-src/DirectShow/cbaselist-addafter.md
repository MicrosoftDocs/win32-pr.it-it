---
description: Il metodo AddAfter inserisce un elenco dopo la posizione specificata.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Metodo CBaseList. AddAfter (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328686"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="2335c-103">CBaseList. AddAfter, metodo</span><span class="sxs-lookup"><span data-stu-id="2335c-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="2335c-104">Il `AddAfter` metodo inserisce un elenco dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="2335c-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="2335c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2335c-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="2335c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2335c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2335c-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="2335c-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="2335c-108">Posizione dopo la quale inserire l'elenco.</span><span class="sxs-lookup"><span data-stu-id="2335c-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="2335c-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="2335c-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="2335c-110">Puntatore all'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="2335c-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2335c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2335c-111">Return value</span></span>

<span data-ttu-id="2335c-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2335c-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2335c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2335c-113">Remarks</span></span>

<span data-ttu-id="2335c-114">Gli indicatori di posizione esistenti, incluso quello specificato nel parametro *pos* , rimangono validi.</span><span class="sxs-lookup"><span data-stu-id="2335c-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="2335c-115">Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="2335c-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="2335c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2335c-116">Requirements</span></span>



| <span data-ttu-id="2335c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2335c-117">Requirement</span></span> | <span data-ttu-id="2335c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2335c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2335c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2335c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2335c-120"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2335c-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2335c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="2335c-121">Library</span></span><br/> | <dl> <span data-ttu-id="2335c-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2335c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2335c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2335c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2335c-124">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="2335c-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




