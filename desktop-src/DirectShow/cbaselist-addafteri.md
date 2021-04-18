---
description: Il metodo AddAfterI inserisce un elemento dopo la posizione specificata.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Metodo CBaseList. AddAfterI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328684"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="7b499-103">CBaseList. AddAfterI, metodo</span><span class="sxs-lookup"><span data-stu-id="7b499-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="7b499-104">Il `AddAfterI` metodo inserisce un elemento dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7b499-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b499-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b499-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="7b499-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b499-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b499-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="7b499-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="7b499-108">Posizione dopo la quale aggiungere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7b499-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="7b499-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="7b499-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="7b499-110">Puntatore all'elemento da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7b499-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b499-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b499-111">Return value</span></span>

<span data-ttu-id="7b499-112">Restituisce l'indicatore di posizione dell'elemento inserito.</span><span class="sxs-lookup"><span data-stu-id="7b499-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b499-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b499-113">Remarks</span></span>

<span data-ttu-id="7b499-114">Se *pos* è **null**, questo metodo aggiunge l'elemento all'inizio dell'elenco (equivalente alla chiamata al metodo [**CBaseList:: AddHeadI**](cbaselist-addheadi.md) ).</span><span class="sxs-lookup"><span data-stu-id="7b499-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b499-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b499-115">Requirements</span></span>



| <span data-ttu-id="7b499-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b499-116">Requirement</span></span> | <span data-ttu-id="7b499-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b499-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b499-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b499-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7b499-119"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b499-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7b499-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b499-120">Library</span></span><br/> | <dl> <span data-ttu-id="7b499-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7b499-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b499-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b499-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b499-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="7b499-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




