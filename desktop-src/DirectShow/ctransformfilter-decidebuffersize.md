---
description: Il metodo DecideBufferSize imposta i requisiti del buffer del PIN di output.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Metodo CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328914"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="c70ef-103">CTransformFilter. DecideBufferSize, metodo</span><span class="sxs-lookup"><span data-stu-id="c70ef-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="c70ef-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="c70ef-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c70ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c70ef-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c70ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c70ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c70ef-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="c70ef-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="c70ef-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) sull'allocatore del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="c70ef-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="c70ef-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="c70ef-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="c70ef-110">Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer dal pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="c70ef-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c70ef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c70ef-111">Return value</span></span>

<span data-ttu-id="c70ef-112">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c70ef-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c70ef-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c70ef-113">Remarks</span></span>

<span data-ttu-id="c70ef-114">Il metodo [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) del PIN di output chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c70ef-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="c70ef-115">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c70ef-115">The derived class must implement this method.</span></span> <span data-ttu-id="c70ef-116">Per ulteriori informazioni, vedere [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="c70ef-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c70ef-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c70ef-117">Requirements</span></span>



| <span data-ttu-id="c70ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c70ef-118">Requirement</span></span> | <span data-ttu-id="c70ef-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c70ef-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70ef-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c70ef-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c70ef-121"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c70ef-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c70ef-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="c70ef-122">Library</span></span><br/> | <dl> <span data-ttu-id="c70ef-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c70ef-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c70ef-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c70ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c70ef-125">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c70ef-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




