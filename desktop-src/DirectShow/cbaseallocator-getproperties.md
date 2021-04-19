---
description: "Il metodo GetProperties Recupera il numero di buffer che l'allocatore creerà e le proprietà del buffer. Questo metodo implementa il metodo IMemAllocator:: GetProperties."
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: Metodo CBaseAllocator. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328174"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="a46af-104">Metodo CBaseAllocator. GetProperties</span><span class="sxs-lookup"><span data-stu-id="a46af-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="a46af-105">Il `GetProperties` metodo recupera il numero di buffer che l'allocatore creerà e le proprietà del buffer.</span><span class="sxs-lookup"><span data-stu-id="a46af-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="a46af-106">Questo metodo implementa il metodo [**IMemAllocator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="a46af-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46af-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a46af-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="a46af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a46af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a46af-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="a46af-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="a46af-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che riceve le proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="a46af-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a46af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a46af-111">Return value</span></span>

<span data-ttu-id="a46af-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a46af-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="a46af-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a46af-113">Requirements</span></span>



| <span data-ttu-id="a46af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a46af-114">Requirement</span></span> | <span data-ttu-id="a46af-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a46af-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46af-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a46af-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a46af-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a46af-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a46af-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="a46af-118">Library</span></span><br/> | <dl> <span data-ttu-id="a46af-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a46af-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a46af-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a46af-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46af-121">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="a46af-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




