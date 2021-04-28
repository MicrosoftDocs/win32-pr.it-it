---
description: 'Metodo CBaseOutputPin.Active: il metodo Active notifica al pin che il filtro è ora attivo.'
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Metodo CBaseOutputPin.Active (Amfilter.h)
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
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096209"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="1bb43-103">Metodo CBaseOutputPin.Active</span><span class="sxs-lookup"><span data-stu-id="1bb43-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="1bb43-104">Il `Active` metodo notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="1bb43-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb43-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bb43-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="1bb43-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bb43-106">Parameters</span></span>

<span data-ttu-id="1bb43-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1bb43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bb43-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bb43-108">Return value</span></span>

<span data-ttu-id="1bb43-109">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1bb43-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1bb43-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1bb43-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="1bb43-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1bb43-111">Return code</span></span>                                                                                          | <span data-ttu-id="1bb43-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bb43-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1bb43-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1bb43-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="1bb43-114">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="1bb43-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="1bb43-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="1bb43-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="1bb43-116">Nessun allocatore disponibile.</span><span class="sxs-lookup"><span data-stu-id="1bb43-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1bb43-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bb43-117">Remarks</span></span>

<span data-ttu-id="1bb43-118">Questo metodo esegue l'override [**del metodo CBasePin::Active.**](cbasepin-active.md)</span><span class="sxs-lookup"><span data-stu-id="1bb43-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="1bb43-119">Chiama il [**metodo IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) nell'allocatore per allocare memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="1bb43-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="1bb43-120">Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.</span><span class="sxs-lookup"><span data-stu-id="1bb43-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb43-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bb43-121">Requirements</span></span>



| <span data-ttu-id="1bb43-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb43-122">Requirement</span></span> | <span data-ttu-id="1bb43-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb43-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb43-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bb43-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1bb43-125"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bb43-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1bb43-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="1bb43-126">Library</span></span><br/> | <dl> <span data-ttu-id="1bb43-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1bb43-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bb43-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bb43-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb43-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="1bb43-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




