---
description: Il metodo RemoveI rimuove l'elemento in corrispondenza della posizione specificata.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Metodo CBaseList. RemoveI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330700"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="9997a-103">Metodo CBaseList. RemoveI</span><span class="sxs-lookup"><span data-stu-id="9997a-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="9997a-104">Il `RemoveI` metodo rimuove l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9997a-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="9997a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9997a-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="9997a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9997a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9997a-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="9997a-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="9997a-108">Valore di posizione che indica l'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9997a-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9997a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9997a-109">Return value</span></span>

<span data-ttu-id="9997a-110">Restituisce un puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="9997a-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="9997a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9997a-111">Remarks</span></span>

<span data-ttu-id="9997a-112">Questo metodo elimina il nodo dall'elenco, ma non elimina l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="9997a-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="9997a-113">Se *pos* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="9997a-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9997a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9997a-114">Requirements</span></span>



| <span data-ttu-id="9997a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9997a-115">Requirement</span></span> | <span data-ttu-id="9997a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9997a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9997a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9997a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9997a-118"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9997a-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9997a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="9997a-119">Library</span></span><br/> | <dl> <span data-ttu-id="9997a-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9997a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9997a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9997a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9997a-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="9997a-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




