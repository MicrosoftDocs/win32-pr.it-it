---
description: "Il metodo AlterQuality notifica al filtro che è richiesta una modifica di qualità. Questo metodo esegue l'override del metodo CTransformFilter:: AlterQuality."
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Metodo CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324177"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="cb222-104">CVideoTransformFilter. AlterQuality, metodo</span><span class="sxs-lookup"><span data-stu-id="cb222-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="cb222-105">Il `AlterQuality` metodo notifica al filtro che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="cb222-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="cb222-106">Questo metodo esegue l'override del metodo [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .</span><span class="sxs-lookup"><span data-stu-id="cb222-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb222-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb222-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="cb222-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb222-109">*d*</span><span class="sxs-lookup"><span data-stu-id="cb222-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="cb222-110">Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="cb222-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb222-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb222-111">Return value</span></span>

<span data-ttu-id="cb222-112">Restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cb222-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb222-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb222-113">Remarks</span></span>

<span data-ttu-id="cb222-114">Questo metodo viene chiamato quando il pin di output riceve un messaggio di qualità (tramite il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).</span><span class="sxs-lookup"><span data-stu-id="cb222-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="cb222-115">Il valore di ritardo da *q* viene archiviato nella variabile **membro \_ itrLate m** .</span><span class="sxs-lookup"><span data-stu-id="cb222-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="cb222-116">Il valore restituito di E \_ Fail indica che il renderer dovrebbe essere aggiornato eliminando i frame, sebbene anche la classe **CVideoTransformFilter** elimini i frame nelle condizioni corrette.</span><span class="sxs-lookup"><span data-stu-id="cb222-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb222-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb222-117">Requirements</span></span>



| <span data-ttu-id="cb222-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb222-118">Requirement</span></span> | <span data-ttu-id="cb222-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cb222-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb222-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb222-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cb222-121"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb222-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cb222-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb222-122">Library</span></span><br/> | <dl> <span data-ttu-id="cb222-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb222-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb222-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb222-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb222-125">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="cb222-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="cb222-126">**CVideoTransformFilter::ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="cb222-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




