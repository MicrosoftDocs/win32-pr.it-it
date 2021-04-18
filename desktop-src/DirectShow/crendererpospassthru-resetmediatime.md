---
description: Il metodo ResetMediaTime Reimposta i timestamp memorizzati nella cache su zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Metodo CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327194"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="c3518-103">CRendererPosPassThru. ResetMediaTime, metodo</span><span class="sxs-lookup"><span data-stu-id="c3518-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="c3518-104">Il `ResetMediaTime` metodo reimposta i timestamp memorizzati nella cache su zero.</span><span class="sxs-lookup"><span data-stu-id="c3518-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3518-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3518-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="c3518-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3518-106">Parameters</span></span>

<span data-ttu-id="c3518-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c3518-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3518-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3518-108">Return value</span></span>

<span data-ttu-id="c3518-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3518-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3518-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3518-110">Remarks</span></span>

<span data-ttu-id="c3518-111">Il filtro deve chiamare questo metodo ogni volta che i timestamp memorizzati nella cache dal metodo [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) diventano non validi.</span><span class="sxs-lookup"><span data-stu-id="c3518-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="c3518-112">In particolare, deve chiamare questo metodo in risposta ai metodi [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) e [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="c3518-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="c3518-113">Dopo la chiamata a questo metodo, il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) restituisce zero per le ore di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="c3518-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3518-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3518-114">Requirements</span></span>



| <span data-ttu-id="c3518-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3518-115">Requirement</span></span> | <span data-ttu-id="c3518-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c3518-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3518-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3518-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3518-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3518-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3518-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c3518-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3518-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3518-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




