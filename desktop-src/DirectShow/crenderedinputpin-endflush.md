---
description: "Metodo CRenderedInputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Metodo CRenderedInputPin.EndFlush (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098919"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="d1d3d-104">Metodo CRenderedInputPin.EndFlush</span><span class="sxs-lookup"><span data-stu-id="d1d3d-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="d1d3d-105">Il `EndFlush` metodo termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="d1d3d-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="d1d3d-106">Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="d1d3d-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d3d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1d3d-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="d1d3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1d3d-108">Parameters</span></span>

<span data-ttu-id="d1d3d-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d1d3d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1d3d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1d3d-110">Return value</span></span>

<span data-ttu-id="d1d3d-111">Restituisce S \_ OK in caso di esito positivo oppure un codice di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d1d3d-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d3d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1d3d-112">Remarks</span></span>

<span data-ttu-id="d1d3d-113">Questo metodo cancella tutti gli eventi [**EC \_ COMPLETE in**](ec-complete.md) sospeso.</span><span class="sxs-lookup"><span data-stu-id="d1d3d-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d3d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1d3d-114">Requirements</span></span>



| <span data-ttu-id="d1d3d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d3d-115">Requirement</span></span> | <span data-ttu-id="d1d3d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d1d3d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d3d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1d3d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d1d3d-118"><dt>Amextra.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d3d-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1d3d-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1d3d-119">Library</span></span><br/> | <dl> <span data-ttu-id="d1d3d-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d3d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d3d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1d3d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d3d-122">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="d1d3d-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




