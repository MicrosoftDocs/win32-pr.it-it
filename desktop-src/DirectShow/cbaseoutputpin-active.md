---
description: Il metodo attivo notifica al pin che il filtro è ora attivo.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Metodo CBaseOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329558"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="71aa2-103">Metodo CBaseOutputPin. Active</span><span class="sxs-lookup"><span data-stu-id="71aa2-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="71aa2-104">Il `Active` metodo notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="71aa2-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="71aa2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71aa2-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="71aa2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71aa2-106">Parameters</span></span>

<span data-ttu-id="71aa2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="71aa2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71aa2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71aa2-108">Return value</span></span>

<span data-ttu-id="71aa2-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71aa2-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71aa2-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="71aa2-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="71aa2-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71aa2-111">Return code</span></span>                                                                                          | <span data-ttu-id="71aa2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71aa2-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="71aa2-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71aa2-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="71aa2-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="71aa2-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="71aa2-115"><dt>**\_ \_ \_ allocatore E nessun allocatore**</dt></span><span class="sxs-lookup"><span data-stu-id="71aa2-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="71aa2-116">Nessun allocatore disponibile.</span><span class="sxs-lookup"><span data-stu-id="71aa2-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71aa2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="71aa2-117">Remarks</span></span>

<span data-ttu-id="71aa2-118">Questo metodo esegue l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="71aa2-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="71aa2-119">Chiama il metodo [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) sull'allocatore per allocare memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="71aa2-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="71aa2-120">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo che esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="71aa2-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71aa2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71aa2-121">Requirements</span></span>



| <span data-ttu-id="71aa2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71aa2-122">Requirement</span></span> | <span data-ttu-id="71aa2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="71aa2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71aa2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71aa2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="71aa2-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71aa2-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71aa2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="71aa2-126">Library</span></span><br/> | <dl> <span data-ttu-id="71aa2-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71aa2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71aa2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71aa2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aa2-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="71aa2-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




