---
description: Il metodo allocator recupera un puntatore all'allocatore di memoria.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Metodo CRendererInputPin. allocator (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328819"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="873b5-103">Metodo CRendererInputPin. allocator</span><span class="sxs-lookup"><span data-stu-id="873b5-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="873b5-104">Il `Allocator` metodo recupera un puntatore all'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="873b5-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="873b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="873b5-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="873b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="873b5-106">Parameters</span></span>

<span data-ttu-id="873b5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="873b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="873b5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="873b5-108">Return value</span></span>

<span data-ttu-id="873b5-109">Restituisce un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore o **null**.</span><span class="sxs-lookup"><span data-stu-id="873b5-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="873b5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="873b5-110">Remarks</span></span>

<span data-ttu-id="873b5-111">Questo metodo restituisce la variabile membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="873b5-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="873b5-112">Il metodo non incrementa il conteggio dei riferimenti nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="873b5-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="873b5-113">Questo metodo è esclusivamente un metodo di funzione di accesso.</span><span class="sxs-lookup"><span data-stu-id="873b5-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="873b5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="873b5-114">Requirements</span></span>



| <span data-ttu-id="873b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="873b5-115">Requirement</span></span> | <span data-ttu-id="873b5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="873b5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="873b5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="873b5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="873b5-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="873b5-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="873b5-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="873b5-119">Library</span></span><br/> | <dl> <span data-ttu-id="873b5-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="873b5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873b5-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="873b5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873b5-122">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="873b5-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




