---
description: Il metodo DoRenderSample esegue il rendering di un campione.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Metodo CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329387"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="60601-103">CBaseRenderer. DoRenderSample, metodo</span><span class="sxs-lookup"><span data-stu-id="60601-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="60601-104">Il `DoRenderSample` metodo esegue il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="60601-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="60601-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60601-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="60601-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60601-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="60601-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="60601-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="60601-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60601-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60601-109">Return value</span></span>

<span data-ttu-id="60601-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60601-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60601-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="60601-111">Remarks</span></span>

<span data-ttu-id="60601-112">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="60601-112">The derived class must implement this method.</span></span> <span data-ttu-id="60601-113">Il comportamento dipende interamente dal tipo di filtro implementato.</span><span class="sxs-lookup"><span data-stu-id="60601-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="60601-114">Un renderer video, ad esempio, potrebbe creare l'immagine video contenuta nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="60601-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="60601-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60601-115">Requirements</span></span>



| <span data-ttu-id="60601-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="60601-116">Requirement</span></span> | <span data-ttu-id="60601-117">Valore</span><span class="sxs-lookup"><span data-stu-id="60601-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60601-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60601-118">Header</span></span><br/>  | <dl> <span data-ttu-id="60601-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60601-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60601-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="60601-120">Library</span></span><br/> | <dl> <span data-ttu-id="60601-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60601-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60601-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60601-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60601-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="60601-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




