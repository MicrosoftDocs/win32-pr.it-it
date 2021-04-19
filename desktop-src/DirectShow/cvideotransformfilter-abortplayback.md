---
description: Il metodo AbortPlayback viene usato per segnalare un errore di streaming. Invia un \_ evento ERRORABORT EC al gestore del grafico dei filtri e invia una notifica di fine flusso a valle.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Metodo CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324180"
---
# <a name="cvideotransformfilterabortplayback-method"></a><span data-ttu-id="f2e23-104">CVideoTransformFilter. AbortPlayback, metodo</span><span class="sxs-lookup"><span data-stu-id="f2e23-104">CVideoTransformFilter.AbortPlayback method</span></span>

<span data-ttu-id="f2e23-105">Il `AbortPlayback` metodo viene usato per segnalare un errore di streaming.</span><span class="sxs-lookup"><span data-stu-id="f2e23-105">The `AbortPlayback` method is used to signal a streaming error.</span></span> <span data-ttu-id="f2e23-106">Invia un evento [**\_ ERRORABORT EC**](ec-errorabort.md) al gestore del grafico dei filtri e invia una notifica di fine flusso a valle.</span><span class="sxs-lookup"><span data-stu-id="f2e23-106">It sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the Filter Graph Manager, and sends an end-of-stream notification downstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e23-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2e23-107">Syntax</span></span>


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="f2e23-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2e23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e23-109">*h*</span><span class="sxs-lookup"><span data-stu-id="f2e23-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="f2e23-110">Valore **HRESULT** dell'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f2e23-110">**HRESULT** value of the operation that failed.</span></span> <span data-ttu-id="f2e23-111">Questo valore viene utilizzato come primo parametro di evento per l' \_ evento ERRORABORT EC.</span><span class="sxs-lookup"><span data-stu-id="f2e23-111">This value is used as the first event parameter for the EC\_ERRORABORT event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e23-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2e23-112">Return value</span></span>

<span data-ttu-id="f2e23-113">Restituisce il valore del parametro *HR* .</span><span class="sxs-lookup"><span data-stu-id="f2e23-113">Returns the value of the *hr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e23-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2e23-114">Requirements</span></span>



| <span data-ttu-id="f2e23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e23-115">Requirement</span></span> | <span data-ttu-id="f2e23-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f2e23-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e23-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2e23-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f2e23-118"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e23-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f2e23-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2e23-119">Library</span></span><br/> | <dl> <span data-ttu-id="f2e23-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2e23-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e23-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2e23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e23-122">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f2e23-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




