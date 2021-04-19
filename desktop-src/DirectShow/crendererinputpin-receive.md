---
description: "Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo esegue l'override del metodo CBaseInputPin:: Receive."
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Metodo CRendererInputPin. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333176"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="7fa1c-104">Metodo CRendererInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="7fa1c-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="7fa1c-105">Il `Receive` metodo riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="7fa1c-106">Questo metodo esegue l'override del metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa1c-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa1c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fa1c-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7fa1c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fa1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa1c-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7fa1c-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7fa1c-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa1c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fa1c-111">Return value</span></span>

<span data-ttu-id="7fa1c-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fa1c-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa1c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fa1c-113">Remarks</span></span>

<span data-ttu-id="7fa1c-114">Questo metodo chiama il metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) del filtro, che gestisce il rendering.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="7fa1c-115">Se il metodo ha esito negativo, il pin Invia un \_ evento ERRORABORT EC.</span><span class="sxs-lookup"><span data-stu-id="7fa1c-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa1c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fa1c-116">Requirements</span></span>



| <span data-ttu-id="7fa1c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa1c-117">Requirement</span></span> | <span data-ttu-id="7fa1c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7fa1c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa1c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fa1c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7fa1c-120"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fa1c-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7fa1c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fa1c-121">Library</span></span><br/> | <dl> <span data-ttu-id="7fa1c-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7fa1c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa1c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fa1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa1c-124">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="7fa1c-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




