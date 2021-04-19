---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: EndFlush."
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Metodo CRenderedInputPin. EndFlush (Amextra. h)
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
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329366"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="3c647-104">CRenderedInputPin. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="3c647-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="3c647-105">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="3c647-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="3c647-106">Questo metodo implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="3c647-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c647-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c647-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="3c647-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c647-108">Parameters</span></span>

<span data-ttu-id="3c647-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3c647-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c647-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c647-110">Return value</span></span>

<span data-ttu-id="3c647-111">Restituisce \_ OK se l'esito è positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="3c647-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c647-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c647-112">Remarks</span></span>

<span data-ttu-id="3c647-113">Questo metodo cancella tutti gli eventi di [**\_ completamento EC**](ec-complete.md) in sospeso.</span><span class="sxs-lookup"><span data-stu-id="3c647-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c647-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c647-114">Requirements</span></span>



| <span data-ttu-id="3c647-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c647-115">Requirement</span></span> | <span data-ttu-id="3c647-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3c647-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c647-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c647-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3c647-118"><dt>Amextra. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c647-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c647-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c647-119">Library</span></span><br/> | <dl> <span data-ttu-id="3c647-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c647-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c647-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c647-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c647-122">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="3c647-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




