---
description: Il metodo DecideBufferSize imposta i requisiti del buffer.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Metodo CTransformOutputPin. DecideBufferSize (Transfrm. h)
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330845"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="eff7d-103">CTransformOutputPin. DecideBufferSize, metodo</span><span class="sxs-lookup"><span data-stu-id="eff7d-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="eff7d-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="eff7d-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eff7d-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="eff7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eff7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eff7d-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="eff7d-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="eff7d-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="eff7d-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="eff7d-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="eff7d-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="eff7d-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="eff7d-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eff7d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eff7d-111">Return value</span></span>

<span data-ttu-id="eff7d-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eff7d-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eff7d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="eff7d-113">Remarks</span></span>

<span data-ttu-id="eff7d-114">Questo metodo esegue l'override del metodo [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="eff7d-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="eff7d-115">Viene chiamato il metodo virtuale pure [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) del filtro, che deve essere implementato dalla classe derivata del filtro.</span><span class="sxs-lookup"><span data-stu-id="eff7d-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff7d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eff7d-116">Requirements</span></span>



| <span data-ttu-id="eff7d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eff7d-117">Requirement</span></span> | <span data-ttu-id="eff7d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eff7d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff7d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eff7d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="eff7d-120"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eff7d-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eff7d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="eff7d-121">Library</span></span><br/> | <dl> <span data-ttu-id="eff7d-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eff7d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




