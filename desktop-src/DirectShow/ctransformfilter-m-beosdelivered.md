---
description: Flag che indica se il filtro ha inviato una notifica di fine del flusso.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331146"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="7041b-103">Membro bEOSDelivered di CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="7041b-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="7041b-104">Flag che indica se il filtro ha inviato una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="7041b-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="7041b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7041b-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="7041b-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7041b-106">Remarks</span></span>

<span data-ttu-id="7041b-107">Se il filtro si interrompe quando non dispone di una connessione di input, invia una notifica di fine flusso a valle e imposta il flag su **true**.</span><span class="sxs-lookup"><span data-stu-id="7041b-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="7041b-108">La notifica di fine flusso garantisce che il filtro downstream non attenda gli esempi.</span><span class="sxs-lookup"><span data-stu-id="7041b-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="7041b-109">Si noti che il metodo [**EndOfStream**](ctransformfilter-endofstream.md) del filtro non imposta questo flag.</span><span class="sxs-lookup"><span data-stu-id="7041b-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="7041b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7041b-110">Requirements</span></span>



| <span data-ttu-id="7041b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7041b-111">Requirement</span></span> | <span data-ttu-id="7041b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7041b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7041b-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7041b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7041b-114"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7041b-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7041b-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="7041b-115">Library</span></span><br/> | <dl> <span data-ttu-id="7041b-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7041b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7041b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7041b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7041b-118">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="7041b-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




