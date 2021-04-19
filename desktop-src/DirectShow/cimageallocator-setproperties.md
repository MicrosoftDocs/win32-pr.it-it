---
description: "Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo esegue l'override del metodo CBaseAllocator:: SetValue."
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Metodo CImageAllocator. seproperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331789"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="fdd25-104">Metodo CImageAllocator. seproperties</span><span class="sxs-lookup"><span data-stu-id="fdd25-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="fdd25-105">Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="fdd25-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="fdd25-106">Questo metodo esegue l'override del metodo [**CBaseAllocator::**](cbaseallocator-setproperties.md) SetValue.</span><span class="sxs-lookup"><span data-stu-id="fdd25-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd25-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdd25-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="fdd25-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdd25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd25-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="fdd25-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd25-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="fdd25-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="fdd25-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="fdd25-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd25-112">Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.</span><span class="sxs-lookup"><span data-stu-id="fdd25-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd25-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdd25-113">Return value</span></span>

<span data-ttu-id="fdd25-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fdd25-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd25-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdd25-115">Remarks</span></span>

<span data-ttu-id="fdd25-116">Questo metodo chiama [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) per convalidare le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="fdd25-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="fdd25-117">Viene anche chiamata la versione della classe di base di `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="fdd25-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd25-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdd25-118">Requirements</span></span>



| <span data-ttu-id="fdd25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd25-119">Requirement</span></span> | <span data-ttu-id="fdd25-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fdd25-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd25-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdd25-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fdd25-122"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdd25-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fdd25-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="fdd25-123">Library</span></span><br/> | <dl> <span data-ttu-id="fdd25-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fdd25-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd25-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdd25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd25-126">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="fdd25-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




