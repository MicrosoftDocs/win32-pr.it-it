---
description: Il metodo AddTailI aggiunge un elemento alla fine dell'elenco.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Metodo CBaseList. AddTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330702"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="a0764-103">CBaseList. AddTailI, metodo</span><span class="sxs-lookup"><span data-stu-id="a0764-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="a0764-104">Il `AddTailI` metodo aggiunge un elemento alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a0764-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0764-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0764-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="a0764-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0764-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0764-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="a0764-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="a0764-108">Puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="a0764-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0764-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0764-109">Return value</span></span>

<span data-ttu-id="a0764-110">Restituisce un valore di posizione per la nuova posizione della coda.</span><span class="sxs-lookup"><span data-stu-id="a0764-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0764-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0764-111">Remarks</span></span>

<span data-ttu-id="a0764-112">Se il metodo ha esito negativo, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="a0764-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0764-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0764-113">Requirements</span></span>



| <span data-ttu-id="a0764-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0764-114">Requirement</span></span> | <span data-ttu-id="a0764-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a0764-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0764-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0764-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a0764-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0764-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a0764-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0764-118">Library</span></span><br/> | <dl> <span data-ttu-id="a0764-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0764-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0764-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0764-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0764-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="a0764-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




