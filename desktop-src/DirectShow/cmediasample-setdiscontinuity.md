---
description: "Il metodo SetDiscontinuity specifica se l'esempio rappresenta un'operazione break nel flusso di dati. Questo metodo implementa il metodo IMediaSample:: SetDiscontinuity."
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Metodo CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325315"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="a83e1-104">CMediaSample. SetDiscontinuity, metodo</span><span class="sxs-lookup"><span data-stu-id="a83e1-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="a83e1-105">Il `SetDiscontinuity` metodo specifica se l'esempio rappresenta un'interruzioni nel flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="a83e1-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="a83e1-106">Questo metodo implementa il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="a83e1-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a83e1-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="a83e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a83e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a83e1-109">*bDiscont*</span><span class="sxs-lookup"><span data-stu-id="a83e1-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="a83e1-110">Valore booleano che specifica se questo esempio è una discontinuità.</span><span class="sxs-lookup"><span data-stu-id="a83e1-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="a83e1-111">Se **true**, l'esempio di supporto è discontinuo con l'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="a83e1-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a83e1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a83e1-112">Return value</span></span>

<span data-ttu-id="a83e1-113">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a83e1-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a83e1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a83e1-114">Remarks</span></span>

<span data-ttu-id="a83e1-115">Questo metodo aggiorna la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica la proprietà discontinuity.</span><span class="sxs-lookup"><span data-stu-id="a83e1-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83e1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a83e1-116">Requirements</span></span>



| <span data-ttu-id="a83e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a83e1-117">Requirement</span></span> | <span data-ttu-id="a83e1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a83e1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a83e1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a83e1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a83e1-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a83e1-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a83e1-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="a83e1-121">Library</span></span><br/> | <dl> <span data-ttu-id="a83e1-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a83e1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a83e1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a83e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83e1-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="a83e1-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




