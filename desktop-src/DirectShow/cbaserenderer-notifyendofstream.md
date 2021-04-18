---
description: Il metodo NotifyEndOfStream Invia un \_ evento EC complete al gestore del grafico dei filtri.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: Metodo CBaseRenderer. NotifyEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330529"
---
# <a name="cbaserenderernotifyendofstream-method"></a><span data-ttu-id="c8b4a-103">CBaseRenderer. NotifyEndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="c8b4a-103">CBaseRenderer.NotifyEndOfStream method</span></span>

<span data-ttu-id="c8b4a-104">Il `NotifyEndOfStream` metodo invia un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c8b4a-104">The `NotifyEndOfStream` method posts an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b4a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8b4a-105">Syntax</span></span>


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="c8b4a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8b4a-106">Parameters</span></span>

<span data-ttu-id="c8b4a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c8b4a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8b4a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8b4a-108">Return value</span></span>

<span data-ttu-id="c8b4a-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c8b4a-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b4a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8b4a-110">Requirements</span></span>



| <span data-ttu-id="c8b4a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b4a-111">Requirement</span></span> | <span data-ttu-id="c8b4a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c8b4a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b4a-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8b4a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c8b4a-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b4a-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8b4a-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8b4a-115">Library</span></span><br/> | <dl> <span data-ttu-id="c8b4a-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b4a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b4a-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8b4a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b4a-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c8b4a-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="c8b4a-119">**CBaseRenderer:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c8b4a-119">**CBaseRenderer::EndOfStream**</span></span>](cbaserenderer-endofstream.md)
</dt> <dt>

[<span data-ttu-id="c8b4a-120">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c8b4a-120">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




