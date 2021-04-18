---
description: "Il metodo SetSyncPoint specifica se l'inizio di questo esempio è un punto di sincronizzazione. Questo metodo implementa il metodo IMediaSample:: SetSyncPoint."
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Metodo CMediaSample. SetSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324922"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="05bed-104">CMediaSample. SetSyncPoint, metodo</span><span class="sxs-lookup"><span data-stu-id="05bed-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="05bed-105">Il `SetSyncPoint` metodo specifica se l'inizio di questo esempio è un punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="05bed-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="05bed-106">Questo metodo implementa il metodo [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="05bed-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05bed-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="05bed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="05bed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05bed-109">*bIsSyncPoint*</span><span class="sxs-lookup"><span data-stu-id="05bed-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="05bed-110">Valore booleano che specifica se si tratta di un punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="05bed-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="05bed-111">Se **true**, si tratta di un punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="05bed-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05bed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05bed-112">Return value</span></span>

<span data-ttu-id="05bed-113">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05bed-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="05bed-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="05bed-114">Remarks</span></span>

<span data-ttu-id="05bed-115">Questo metodo aggiorna la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica la proprietà del punto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="05bed-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="05bed-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05bed-116">Requirements</span></span>



| <span data-ttu-id="05bed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05bed-117">Requirement</span></span> | <span data-ttu-id="05bed-118">Valore</span><span class="sxs-lookup"><span data-stu-id="05bed-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05bed-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05bed-119">Header</span></span><br/>  | <dl> <span data-ttu-id="05bed-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05bed-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05bed-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="05bed-121">Library</span></span><br/> | <dl> <span data-ttu-id="05bed-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05bed-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bed-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05bed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bed-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="05bed-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




