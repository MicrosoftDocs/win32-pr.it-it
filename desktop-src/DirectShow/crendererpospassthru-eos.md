---
description: Il metodo EOS aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Metodo CRendererPosPassThru. EOS (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333173"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="a97ed-103">Metodo CRendererPosPassThru. EOS</span><span class="sxs-lookup"><span data-stu-id="a97ed-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="a97ed-104">Il `EOS` metodo aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="a97ed-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a97ed-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="a97ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a97ed-106">Parameters</span></span>

<span data-ttu-id="a97ed-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a97ed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a97ed-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a97ed-108">Return value</span></span>

<span data-ttu-id="a97ed-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a97ed-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a97ed-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a97ed-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a97ed-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a97ed-111">Return code</span></span>                                                                            | <span data-ttu-id="a97ed-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a97ed-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="a97ed-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a97ed-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a97ed-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a97ed-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="a97ed-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="a97ed-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a97ed-116">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a97ed-116">Failure.</span></span> <span data-ttu-id="a97ed-117">Probabilmente il filtro non è in streaming.</span><span class="sxs-lookup"><span data-stu-id="a97ed-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a97ed-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a97ed-118">Remarks</span></span>

<span data-ttu-id="a97ed-119">Il filtro deve chiamare questo metodo quando riceve una notifica di fine flusso ([**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span><span class="sxs-lookup"><span data-stu-id="a97ed-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="a97ed-120">Il metodo imposta entrambi i timestamp memorizzati nella cache uguale alla posizione di arresto, assicurando che il metodo [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisca i valori corretti alla fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="a97ed-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97ed-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a97ed-121">Requirements</span></span>



| <span data-ttu-id="a97ed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97ed-122">Requirement</span></span> | <span data-ttu-id="a97ed-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a97ed-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a97ed-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a97ed-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a97ed-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a97ed-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a97ed-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a97ed-126">Library</span></span><br/> | <dl> <span data-ttu-id="a97ed-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a97ed-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




