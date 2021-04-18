---
description: "Il metodo IsDiscontinuity determina se l'esempio rappresenta un'operazione break nel flusso di dati. Questo metodo implementa il metodo IMediaSample:: IsDiscontinuity."
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Metodo CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324957"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="2d5f7-104">CMediaSample. IsDiscontinuity, metodo</span><span class="sxs-lookup"><span data-stu-id="2d5f7-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="2d5f7-105">Il `IsDiscontinuity` metodo determina se l'esempio rappresenta un'interruzioni nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="2d5f7-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="2d5f7-106">Questo metodo implementa il metodo [**IMediaSample:: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="2d5f7-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d5f7-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="2d5f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d5f7-108">Parameters</span></span>

<span data-ttu-id="2d5f7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2d5f7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d5f7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d5f7-110">Return value</span></span>

<span data-ttu-id="2d5f7-111">Restituisce \_ OK se l'esempio è un'interruzioni nel flusso di dati e in \_ caso contrario è false.</span><span class="sxs-lookup"><span data-stu-id="2d5f7-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d5f7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d5f7-112">Remarks</span></span>

<span data-ttu-id="2d5f7-113">La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d5f7-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5f7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d5f7-114">Requirements</span></span>



| <span data-ttu-id="2d5f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d5f7-115">Requirement</span></span> | <span data-ttu-id="2d5f7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2d5f7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5f7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d5f7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2d5f7-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5f7-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2d5f7-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d5f7-119">Library</span></span><br/> | <dl> <span data-ttu-id="2d5f7-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5f7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d5f7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d5f7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5f7-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="2d5f7-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




