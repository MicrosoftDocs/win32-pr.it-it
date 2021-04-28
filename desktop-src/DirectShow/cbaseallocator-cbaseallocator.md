---
description: 'Costruttore CBaseAllocator.CBaseAllocator : metodo costruttore.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Costruttore CBaseAllocator.CBaseAllocator (Amfilter.h)
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
ms.openlocfilehash: dfda2b03d1ddb3f4a8ad5f4446dbee997da4e790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096360"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="23e63-103">Costruttore CBaseAllocator.CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="23e63-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="23e63-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="23e63-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23e63-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="23e63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e63-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="23e63-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="23e63-108">Puntatore a una stringa contenente il nome di debug dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="23e63-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="23e63-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="23e63-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="23e63-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="23e63-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="23e63-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="23e63-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="23e63-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="23e63-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="23e63-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="23e63-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23e63-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="23e63-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="23e63-115">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="23e63-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="23e63-116">Impostare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23e63-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="23e63-117">Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="23e63-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="23e63-118">*bEvent*</span><span class="sxs-lookup"><span data-stu-id="23e63-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="23e63-119">Valore booleano che indica se creare un semaforo.</span><span class="sxs-lookup"><span data-stu-id="23e63-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="23e63-120">Se **TRUE,** l'allocatore crea un semaforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)), che viene segnalato ogni volta che un campione diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="23e63-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="23e63-121">Impostare il valore **su FALSE** se si implementa una classe derivata che non richiede un semaforo.</span><span class="sxs-lookup"><span data-stu-id="23e63-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="23e63-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="23e63-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="23e63-123">Valore booleano che indica se il meccanismo di callback di rilascio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="23e63-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="23e63-124">Impostare il valore su **TRUE** se si vuole fornire un'interfaccia di callback, che viene chiamata quando vengono rilasciati i buffer.</span><span class="sxs-lookup"><span data-stu-id="23e63-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="23e63-125">Specificare il callback chiamando il [**metodo CBaseAllocator::SetNotify.**](cbaseallocator-setnotify.md)</span><span class="sxs-lookup"><span data-stu-id="23e63-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23e63-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23e63-126">Requirements</span></span>



| <span data-ttu-id="23e63-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e63-127">Requirement</span></span> | <span data-ttu-id="23e63-128">Valore</span><span class="sxs-lookup"><span data-stu-id="23e63-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e63-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23e63-129">Header</span></span><br/>  | <dl> <span data-ttu-id="23e63-130"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="23e63-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23e63-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="23e63-131">Library</span></span><br/> | <dl> <span data-ttu-id="23e63-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23e63-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e63-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23e63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e63-134">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="23e63-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




