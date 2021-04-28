---
description: 'Metodo CTransformOutputPin.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Metodo CTransformOutputPin.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084839"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="d6b8a-103">Metodo CTransformOutputPin.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="d6b8a-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="d6b8a-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="d6b8a-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6b8a-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="d6b8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6b8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b8a-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="d6b8a-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b8a-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="d6b8a-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d6b8a-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="d6b8a-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b8a-110">Puntatore a [**una struttura \_ ALLOCATOR PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del pin di input.</span><span class="sxs-lookup"><span data-stu-id="d6b8a-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b8a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6b8a-111">Return value</span></span>

<span data-ttu-id="d6b8a-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d6b8a-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b8a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6b8a-113">Remarks</span></span>

<span data-ttu-id="d6b8a-114">Questo metodo esegue l'override [**del metodo CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md)</span><span class="sxs-lookup"><span data-stu-id="d6b8a-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="d6b8a-115">Chiama il metodo [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) virtuale puro del filtro, che deve essere implementato dalla classe derivata del filtro.</span><span class="sxs-lookup"><span data-stu-id="d6b8a-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b8a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6b8a-116">Requirements</span></span>



| <span data-ttu-id="d6b8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6b8a-117">Requirement</span></span> | <span data-ttu-id="d6b8a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d6b8a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b8a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6b8a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d6b8a-120"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6b8a-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6b8a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6b8a-121">Library</span></span><br/> | <dl> <span data-ttu-id="d6b8a-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d6b8a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




