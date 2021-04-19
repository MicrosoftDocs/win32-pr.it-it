---
description: Il metodo free viene chiamato durante un'operazione di decommit.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Metodo CMemAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333207"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="efaa4-103">CMemAllocator. free, metodo</span><span class="sxs-lookup"><span data-stu-id="efaa4-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="efaa4-104">Il `Free` metodo viene chiamato durante un'operazione di decommit.</span><span class="sxs-lookup"><span data-stu-id="efaa4-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="efaa4-105">Questo metodo implementa il metodo [**CBaseAllocator:: Free**](cbaseallocator-free.md) virtuale pure, ma non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="efaa4-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="efaa4-106">La memoria del buffer non viene effettivamente rilasciata finché l'oggetto **CMemAllocator** non viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="efaa4-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="efaa4-107">Il metodo del distruttore chiama [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md) per rilasciare la memoria.</span><span class="sxs-lookup"><span data-stu-id="efaa4-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="efaa4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efaa4-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="efaa4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="efaa4-109">Parameters</span></span>

<span data-ttu-id="efaa4-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="efaa4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="efaa4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efaa4-111">Return value</span></span>

<span data-ttu-id="efaa4-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="efaa4-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="efaa4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efaa4-113">Requirements</span></span>



| <span data-ttu-id="efaa4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="efaa4-114">Requirement</span></span> | <span data-ttu-id="efaa4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="efaa4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efaa4-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efaa4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="efaa4-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efaa4-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="efaa4-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="efaa4-118">Library</span></span><br/> | <dl> <span data-ttu-id="efaa4-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efaa4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efaa4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efaa4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efaa4-121">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="efaa4-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




