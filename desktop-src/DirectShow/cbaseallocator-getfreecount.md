---
description: Il metodo GetFreeCount Recupera il numero di campioni multimediali che non sono in uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Metodo CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331662"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="93498-103">CBaseAllocator. GetFreeCount, metodo</span><span class="sxs-lookup"><span data-stu-id="93498-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="93498-104">Il `GetFreeCount` metodo recupera il numero di campioni multimediali che non sono in uso.</span><span class="sxs-lookup"><span data-stu-id="93498-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="93498-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93498-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="93498-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93498-107">*plBuffersFree*</span><span class="sxs-lookup"><span data-stu-id="93498-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="93498-108">Indirizzo di una variabile che riceve il numero di campioni che non sono in uso.</span><span class="sxs-lookup"><span data-stu-id="93498-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93498-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93498-109">Return value</span></span>

<span data-ttu-id="93498-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93498-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="93498-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="93498-111">Remarks</span></span>

<span data-ttu-id="93498-112">Questo metodo implementa il metodo [**IMemAllocatorCallbackTemp:: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) .</span><span class="sxs-lookup"><span data-stu-id="93498-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="93498-113">L'allocatore non espone l'interfaccia IMemAllocatorCallbackTemp, a meno che il flag *fEnableReleaseCallback* non sia impostato su **true** nel costruttore CBaseAllocator.</span><span class="sxs-lookup"><span data-stu-id="93498-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="93498-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93498-114">Requirements</span></span>



| <span data-ttu-id="93498-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="93498-115">Requirement</span></span> | <span data-ttu-id="93498-116">Valore</span><span class="sxs-lookup"><span data-stu-id="93498-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93498-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93498-117">Header</span></span><br/>  | <dl> <span data-ttu-id="93498-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93498-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93498-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="93498-119">Library</span></span><br/> | <dl> <span data-ttu-id="93498-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="93498-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93498-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93498-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93498-122">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="93498-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




