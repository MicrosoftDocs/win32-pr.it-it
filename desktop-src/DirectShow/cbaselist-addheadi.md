---
description: Il metodo AddHeadI aggiunge un elemento all'inizio dell'elenco.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Metodo CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328673"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="f6f6b-103">CBaseList. AddHeadI, metodo</span><span class="sxs-lookup"><span data-stu-id="f6f6b-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="f6f6b-104">Il `AddHeadI` metodo aggiunge un elemento all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6f6b-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="f6f6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6f6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f6b-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="f6f6b-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f6b-108">Puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f6b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6f6b-109">Return value</span></span>

<span data-ttu-id="f6f6b-110">Restituisce un valore di posizione che indica la nuova posizione Head.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6f6b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6f6b-111">Remarks</span></span>

<span data-ttu-id="f6f6b-112">Se il metodo ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f6b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6f6b-113">Requirements</span></span>



| <span data-ttu-id="f6f6b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6f6b-114">Requirement</span></span> | <span data-ttu-id="f6f6b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f6f6b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f6b-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6f6b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f6f6b-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f6b-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f6f6b-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6f6b-118">Library</span></span><br/> | <dl> <span data-ttu-id="f6f6b-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f6b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f6b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6f6b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f6b-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




