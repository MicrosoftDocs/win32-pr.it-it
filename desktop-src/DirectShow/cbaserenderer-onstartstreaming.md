---
description: Il metodo OnStartStreaming viene chiamato quando il filtro inizia il flusso.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Metodo CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327954"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="f716d-103">CBaseRenderer. OnStartStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="f716d-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="f716d-104">Il `OnStartStreaming` metodo viene chiamato quando il filtro inizia il flusso.</span><span class="sxs-lookup"><span data-stu-id="f716d-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="f716d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f716d-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="f716d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f716d-106">Parameters</span></span>

<span data-ttu-id="f716d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f716d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f716d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f716d-108">Return value</span></span>

<span data-ttu-id="f716d-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f716d-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f716d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f716d-110">Remarks</span></span>

<span data-ttu-id="f716d-111">Il metodo [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f716d-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="f716d-112">Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="f716d-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f716d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f716d-113">Requirements</span></span>



| <span data-ttu-id="f716d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f716d-114">Requirement</span></span> | <span data-ttu-id="f716d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f716d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f716d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f716d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f716d-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f716d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f716d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="f716d-118">Library</span></span><br/> | <dl> <span data-ttu-id="f716d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f716d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f716d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f716d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f716d-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f716d-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




