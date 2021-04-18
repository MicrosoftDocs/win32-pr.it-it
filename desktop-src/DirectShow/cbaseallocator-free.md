---
description: Il metodo Free rilascia tutta la memoria del buffer. Questo metodo viene chiamato quando il filtro proprietario esegue il commit dell'allocatore, dopo il rilascio dell'ultimo campione multimediale.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Metodo CBaseAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328268"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="0b318-104">CBaseAllocator. free, metodo</span><span class="sxs-lookup"><span data-stu-id="0b318-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="0b318-105">Il `Free` metodo rilascia tutta la memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="0b318-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="0b318-106">Questo metodo viene chiamato quando il filtro proprietario esegue il commit dell'allocatore, dopo il rilascio dell'ultimo campione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0b318-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b318-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b318-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0b318-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b318-108">Parameters</span></span>

<span data-ttu-id="0b318-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0b318-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b318-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b318-110">Return value</span></span>

<span data-ttu-id="0b318-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0b318-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b318-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b318-112">Remarks</span></span>

<span data-ttu-id="0b318-113">Dopo la chiamata del metodo [**decommit**](cbaseallocator-decommit.md) , l'allocatore chiama questo metodo quando rilascia l'ultimo esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="0b318-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="0b318-114">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0b318-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b318-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b318-115">Requirements</span></span>



| <span data-ttu-id="0b318-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b318-116">Requirement</span></span> | <span data-ttu-id="0b318-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0b318-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b318-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b318-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0b318-119"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b318-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b318-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b318-120">Library</span></span><br/> | <dl> <span data-ttu-id="0b318-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0b318-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b318-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b318-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b318-123">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="0b318-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




