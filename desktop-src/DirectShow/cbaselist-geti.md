---
description: Il metodo GetI recupera l'elemento in corrispondenza della posizione specificata.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Metodo CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328661"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="1e855-103">CBaseList. GetI, metodo</span><span class="sxs-lookup"><span data-stu-id="1e855-103">CBaseList.GetI method</span></span>

<span data-ttu-id="1e855-104">Il `GetI` metodo recupera l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1e855-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e855-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e855-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="1e855-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e855-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="1e855-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="1e855-108">Indicatore di posizione per l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1e855-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e855-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e855-109">Return value</span></span>

<span data-ttu-id="1e855-110">Restituisce un puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="1e855-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e855-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e855-111">Remarks</span></span>

<span data-ttu-id="1e855-112">Se *pos* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="1e855-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e855-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e855-113">Requirements</span></span>



| <span data-ttu-id="1e855-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e855-114">Requirement</span></span> | <span data-ttu-id="1e855-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1e855-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e855-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e855-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1e855-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e855-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1e855-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="1e855-118">Library</span></span><br/> | <dl> <span data-ttu-id="1e855-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1e855-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e855-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e855-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e855-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="1e855-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




