---
description: Il metodo Run segnala al thread di streaming di essere eseguito.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Metodo CSourceStream. Run (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332321"
---
# <a name="csourcestreamrun-method"></a><span data-ttu-id="f64e2-103">Metodo CSourceStream. Run</span><span class="sxs-lookup"><span data-stu-id="f64e2-103">CSourceStream.Run method</span></span>

<span data-ttu-id="f64e2-104">Il `Run` metodo segnala al thread di streaming di essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="f64e2-104">The `Run` method signals the streaming thread to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f64e2-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="f64e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f64e2-106">Parameters</span></span>

<span data-ttu-id="f64e2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f64e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f64e2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f64e2-108">Return value</span></span>

<span data-ttu-id="f64e2-109">Restituisce S \_ OK o e \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f64e2-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="f64e2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f64e2-110">Remarks</span></span>

<span data-ttu-id="f64e2-111">Nella classe di base, questo metodo ha lo stesso effetto della richiesta [**CSourceStream::P ause**](csourcestream-pause.md) e non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f64e2-111">In the base class, this method has the same effect as the [**CSourceStream::Pause**](csourcestream-pause.md) request, and is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f64e2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f64e2-112">Requirements</span></span>



| <span data-ttu-id="f64e2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f64e2-113">Requirement</span></span> | <span data-ttu-id="f64e2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f64e2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64e2-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f64e2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f64e2-116"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f64e2-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f64e2-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="f64e2-117">Library</span></span><br/> | <dl> <span data-ttu-id="f64e2-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f64e2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64e2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f64e2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64e2-120">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="f64e2-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




