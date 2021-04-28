---
description: 'Metodo CTransformFilter.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer del pin di output.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Metodo CTransformFilter.DecideBufferSize (Transfrm.h)
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
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095149"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="de2d5-103">Metodo CTransformFilter.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="de2d5-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="de2d5-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer del pin di output.</span><span class="sxs-lookup"><span data-stu-id="de2d5-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de2d5-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="de2d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de2d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de2d5-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="de2d5-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="de2d5-108">Puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) nell'allocatore del pin di output.</span><span class="sxs-lookup"><span data-stu-id="de2d5-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="de2d5-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="de2d5-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="de2d5-110">Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer dal pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="de2d5-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de2d5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de2d5-111">Return value</span></span>

<span data-ttu-id="de2d5-112">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="de2d5-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de2d5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="de2d5-113">Remarks</span></span>

<span data-ttu-id="de2d5-114">Il metodo [**CTransformOutputPin::D ecideBufferSize**](ctransformoutputpin-decidebuffersize.md) del pin di output chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="de2d5-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="de2d5-115">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="de2d5-115">The derived class must implement this method.</span></span> <span data-ttu-id="de2d5-116">Per altre informazioni, vedere [**CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="de2d5-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de2d5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2d5-117">Requirements</span></span>



| <span data-ttu-id="de2d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de2d5-118">Requirement</span></span> | <span data-ttu-id="de2d5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="de2d5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2d5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de2d5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="de2d5-121"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="de2d5-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de2d5-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="de2d5-122">Library</span></span><br/> | <dl> <span data-ttu-id="de2d5-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de2d5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de2d5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de2d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de2d5-125">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="de2d5-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




