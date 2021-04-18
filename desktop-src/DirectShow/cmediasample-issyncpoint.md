---
description: "Il metodo IsSyncPoint determina se l'inizio dell'esempio è un punto di sincronizzazione. Questo metodo implementa il metodo IMediaSample:: IsSyncPoint."
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Metodo CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324952"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="5eb0e-104">CMediaSample. IsSyncPoint, metodo</span><span class="sxs-lookup"><span data-stu-id="5eb0e-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="5eb0e-105">Il `IsSyncPoint` metodo determina se l'inizio dell'esempio è un punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5eb0e-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="5eb0e-106">Questo metodo implementa il metodo [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="5eb0e-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb0e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eb0e-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="5eb0e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5eb0e-108">Parameters</span></span>

<span data-ttu-id="5eb0e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5eb0e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5eb0e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5eb0e-110">Return value</span></span>

<span data-ttu-id="5eb0e-111">Restituisce \_ OK se l'esempio è un punto di sincronizzazione, oppure S \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5eb0e-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb0e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eb0e-112">Remarks</span></span>

<span data-ttu-id="5eb0e-113">La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5eb0e-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb0e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eb0e-114">Requirements</span></span>



| <span data-ttu-id="5eb0e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb0e-115">Requirement</span></span> | <span data-ttu-id="5eb0e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5eb0e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb0e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5eb0e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5eb0e-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5eb0e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5eb0e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="5eb0e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5eb0e-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5eb0e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb0e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eb0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb0e-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="5eb0e-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




