---
description: Il metodo inattivo notifica al pin che il filtro non è più attivo.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Metodo CBaseInputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326062"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="a0b63-103">Metodo CBaseInputPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="a0b63-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="a0b63-104">Il `Inactive` metodo notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="a0b63-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0b63-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="a0b63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0b63-106">Parameters</span></span>

<span data-ttu-id="a0b63-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a0b63-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0b63-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0b63-108">Return value</span></span>

<span data-ttu-id="a0b63-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0b63-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a0b63-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a0b63-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a0b63-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0b63-111">Return code</span></span>                                                                                          | <span data-ttu-id="a0b63-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0b63-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a0b63-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="a0b63-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a0b63-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="a0b63-115"><dt>**\_ \_ \_ allocatore E nessun allocatore**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="a0b63-116">Nessun allocatore di memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="a0b63-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0b63-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0b63-117">Remarks</span></span>

<span data-ttu-id="a0b63-118">Questo metodo esegue l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b63-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="a0b63-119">Chiama il metodo [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) per decommitre l'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="a0b63-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="a0b63-120">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo che esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="a0b63-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b63-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0b63-121">Requirements</span></span>



| <span data-ttu-id="a0b63-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b63-122">Requirement</span></span> | <span data-ttu-id="a0b63-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a0b63-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b63-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0b63-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a0b63-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a0b63-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0b63-126">Library</span></span><br/> | <dl> <span data-ttu-id="a0b63-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0b63-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0b63-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b63-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="a0b63-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




