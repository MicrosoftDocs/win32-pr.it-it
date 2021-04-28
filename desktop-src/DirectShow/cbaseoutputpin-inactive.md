---
description: 'Metodo CBaseOutputPin.Inactive: il metodo Inactive notifica al pin che il filtro non è più attivo.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Metodo CBaseOutputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc4901bba7f1e34d49ff5bafb7b291544157bd9c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096139"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="9b171-103">Metodo CBaseOutputPin.Inactive</span><span class="sxs-lookup"><span data-stu-id="9b171-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="9b171-104">Il `Inactive` metodo notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="9b171-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b171-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b171-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="9b171-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b171-106">Parameters</span></span>

<span data-ttu-id="9b171-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9b171-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b171-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b171-108">Return value</span></span>

<span data-ttu-id="9b171-109">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9b171-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9b171-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9b171-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9b171-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9b171-111">Return code</span></span>                                                                                          | <span data-ttu-id="9b171-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b171-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9b171-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="9b171-114">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="9b171-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="9b171-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="9b171-116">Nessun allocatore di memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="9b171-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b171-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b171-117">Remarks</span></span>

<span data-ttu-id="9b171-118">Questo metodo esegue l'override [**del metodo CBasePin::Inactive.**](cbasepin-inactive.md)</span><span class="sxs-lookup"><span data-stu-id="9b171-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="9b171-119">Chiama il metodo [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) per decommettere l'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="9b171-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="9b171-120">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.</span><span class="sxs-lookup"><span data-stu-id="9b171-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b171-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b171-121">Requirements</span></span>



| <span data-ttu-id="9b171-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b171-122">Requirement</span></span> | <span data-ttu-id="9b171-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9b171-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b171-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b171-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9b171-125"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9b171-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b171-126">Library</span></span><br/> | <dl> <span data-ttu-id="9b171-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b171-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b171-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b171-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="9b171-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




