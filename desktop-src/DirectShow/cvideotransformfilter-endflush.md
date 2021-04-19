---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Questo metodo esegue l'override del metodo CTransformFilter:: EndFlush."
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Metodo CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330199"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="517a7-104">CVideoTransformFilter. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="517a7-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="517a7-105">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="517a7-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="517a7-106">Questo metodo esegue l'override del metodo [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="517a7-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="517a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="517a7-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="517a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="517a7-108">Parameters</span></span>

<span data-ttu-id="517a7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="517a7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="517a7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="517a7-110">Return value</span></span>

<span data-ttu-id="517a7-111">Restituisce \_ OK se ha esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="517a7-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="517a7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="517a7-112">Remarks</span></span>

<span data-ttu-id="517a7-113">Questo metodo reimposta tutte le misurazioni delle prestazioni interne del filtro.</span><span class="sxs-lookup"><span data-stu-id="517a7-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="517a7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="517a7-114">Requirements</span></span>



| <span data-ttu-id="517a7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="517a7-115">Requirement</span></span> | <span data-ttu-id="517a7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="517a7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517a7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="517a7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="517a7-118"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="517a7-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="517a7-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="517a7-119">Library</span></span><br/> | <dl> <span data-ttu-id="517a7-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="517a7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="517a7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="517a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517a7-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="517a7-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




