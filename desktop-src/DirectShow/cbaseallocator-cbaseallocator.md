---
description: Metodo del costruttore.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Costruttore CBaseAllocator. CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324041"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="30e37-103">Costruttore CBaseAllocator. CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="30e37-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="30e37-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="30e37-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30e37-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="30e37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e37-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="30e37-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="30e37-108">Puntatore a una stringa contenente il nome di debug dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="30e37-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="30e37-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="30e37-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="30e37-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="30e37-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="30e37-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="30e37-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="30e37-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="30e37-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="30e37-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="30e37-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30e37-114">*PHR*</span><span class="sxs-lookup"><span data-stu-id="30e37-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="30e37-115">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30e37-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="30e37-116">Impostare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="30e37-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="30e37-117">Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="30e37-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="30e37-118">*con lo sfogo*</span><span class="sxs-lookup"><span data-stu-id="30e37-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="30e37-119">Valore booleano che indica se creare un semaforo.</span><span class="sxs-lookup"><span data-stu-id="30e37-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="30e37-120">Se **true**, l'allocatore crea un semaforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), che viene segnalato ogni volta che un campione diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="30e37-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="30e37-121">Impostare il valore su **false** se si implementa una classe derivata che non richiede un semaforo.</span><span class="sxs-lookup"><span data-stu-id="30e37-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="30e37-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="30e37-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="30e37-123">Valore booleano che indica se il meccanismo di richiamata della versione è abilitato.</span><span class="sxs-lookup"><span data-stu-id="30e37-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="30e37-124">Impostare il valore su **true** se si desidera fornire un'interfaccia di callback, che viene chiamata quando vengono rilasciati i buffer.</span><span class="sxs-lookup"><span data-stu-id="30e37-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="30e37-125">Specificare il callback chiamando il metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="30e37-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30e37-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30e37-126">Requirements</span></span>



| <span data-ttu-id="30e37-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e37-127">Requirement</span></span> | <span data-ttu-id="30e37-128">Valore</span><span class="sxs-lookup"><span data-stu-id="30e37-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e37-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30e37-129">Header</span></span><br/>  | <dl> <span data-ttu-id="30e37-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30e37-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="30e37-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="30e37-131">Library</span></span><br/> | <dl> <span data-ttu-id="30e37-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="30e37-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e37-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30e37-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e37-134">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="30e37-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




