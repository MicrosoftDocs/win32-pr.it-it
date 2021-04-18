---
description: "Il metodo IsPreroll determina se l'esempio è un esempio di preroll. Non è necessario visualizzare un campione di preroll. Questo metodo implementa il metodo IMediaSample:: IsPreroll."
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Metodo CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324956"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="f4099-105">CMediaSample. IsPreroll, metodo</span><span class="sxs-lookup"><span data-stu-id="f4099-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="f4099-106">Il `IsPreroll` metodo determina se l'esempio è un esempio di preroll.</span><span class="sxs-lookup"><span data-stu-id="f4099-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="f4099-107">Non è necessario visualizzare un campione di preroll.</span><span class="sxs-lookup"><span data-stu-id="f4099-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="f4099-108">Questo metodo implementa il metodo [**IMediaSample:: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .</span><span class="sxs-lookup"><span data-stu-id="f4099-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4099-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4099-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="f4099-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4099-110">Parameters</span></span>

<span data-ttu-id="f4099-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f4099-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4099-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4099-112">Return value</span></span>

<span data-ttu-id="f4099-113">Restituisce \_ OK se l'esempio è un campione di preroll e \_ in caso contrario è false.</span><span class="sxs-lookup"><span data-stu-id="f4099-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4099-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4099-114">Remarks</span></span>

<span data-ttu-id="f4099-115">La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4099-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4099-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4099-116">Requirements</span></span>



| <span data-ttu-id="f4099-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4099-117">Requirement</span></span> | <span data-ttu-id="f4099-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f4099-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4099-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4099-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f4099-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4099-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4099-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4099-121">Library</span></span><br/> | <dl> <span data-ttu-id="f4099-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f4099-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4099-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4099-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4099-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="f4099-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




