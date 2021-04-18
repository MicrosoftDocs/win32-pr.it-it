---
description: Il metodo AddBeforeI inserisce un elemento prima della posizione specificata.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Metodo CBaseList. AddBeforeI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328678"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="b6770-103">CBaseList. AddBeforeI, metodo</span><span class="sxs-lookup"><span data-stu-id="b6770-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="b6770-104">Il `AddBeforeI` metodo inserisce un elemento prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b6770-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6770-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6770-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="b6770-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6770-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="b6770-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="b6770-108">Posizione prima della quale aggiungere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b6770-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="b6770-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="b6770-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="b6770-110">Puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="b6770-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6770-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6770-111">Return value</span></span>

<span data-ttu-id="b6770-112">Restituisce l'indicatore di posizione per l'elemento inserito.</span><span class="sxs-lookup"><span data-stu-id="b6770-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6770-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6770-113">Remarks</span></span>

<span data-ttu-id="b6770-114">Se *pos* è **null**, questo metodo aggiunge l'elemento alla parte finale dell'elenco (equivalente alla chiamata al metodo [**CBaseList:: AddTailI**](cbaselist-addtaili.md) ).</span><span class="sxs-lookup"><span data-stu-id="b6770-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6770-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6770-115">Requirements</span></span>



| <span data-ttu-id="b6770-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6770-116">Requirement</span></span> | <span data-ttu-id="b6770-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b6770-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6770-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6770-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b6770-119"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6770-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b6770-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6770-120">Library</span></span><br/> | <dl> <span data-ttu-id="b6770-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6770-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6770-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6770-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6770-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="b6770-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




