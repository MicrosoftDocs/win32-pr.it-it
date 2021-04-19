---
description: Il metodo GetAllocatorRequirements recupera le proprietà dell'allocatore richieste dal pin di input.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Metodo CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326064"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="3ac5c-103">CBaseInputPin. GetAllocatorRequirements, metodo</span><span class="sxs-lookup"><span data-stu-id="3ac5c-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="3ac5c-104">Il `GetAllocatorRequirements` metodo recupera le proprietà dell'allocatore richieste dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ac5c-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="3ac5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ac5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac5c-107">*pProps*</span><span class="sxs-lookup"><span data-stu-id="3ac5c-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="3ac5c-108">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , compilata con i requisiti.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac5c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ac5c-109">Return value</span></span>

<span data-ttu-id="3ac5c-110">Restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac5c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ac5c-111">Remarks</span></span>

<span data-ttu-id="3ac5c-112">Quando un pin di output Inizializza un allocatore di memoria, può chiamare questo metodo per determinare se il pin di input presenta requisiti di buffer.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="3ac5c-113">Per ulteriori informazioni, vedere [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3ac5c-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="3ac5c-114">L'implementazione di questo metodo è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-114">Implementing this method is optional.</span></span> <span data-ttu-id="3ac5c-115">Se il filtro ha requisiti di allineamento o prefisso specifici, eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3ac5c-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac5c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ac5c-116">Requirements</span></span>



| <span data-ttu-id="3ac5c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac5c-117">Requirement</span></span> | <span data-ttu-id="3ac5c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3ac5c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac5c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ac5c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3ac5c-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac5c-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3ac5c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ac5c-121">Library</span></span><br/> | <dl> <span data-ttu-id="3ac5c-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac5c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac5c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ac5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac5c-124">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="3ac5c-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




