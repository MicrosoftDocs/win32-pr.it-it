---
description: Il metodo ScheduleSample esegue l'override della classe di base che esegue il lavoro principale per gestire un conteggio degli esempi disegnati e rimossi (che vengono usati dall'implementazione di IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Metodo CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325350"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="c7a1d-103">CBaseVideoRenderer. ScheduleSample, metodo</span><span class="sxs-lookup"><span data-stu-id="c7a1d-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="c7a1d-104">Il `ScheduleSample` metodo esegue l'override della classe di base che esegue il lavoro principale per gestire un conteggio degli esempi disegnati e rimossi (che vengono usati dall'implementazione di [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).</span><span class="sxs-lookup"><span data-stu-id="c7a1d-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7a1d-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c7a1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7a1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a1d-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c7a1d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c7a1d-108">Puntatore all'esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="c7a1d-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7a1d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7a1d-109">Return value</span></span>

<span data-ttu-id="c7a1d-110">Restituisce **true** se l'esempio è pianificato; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c7a1d-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a1d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7a1d-111">Requirements</span></span>



| <span data-ttu-id="c7a1d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7a1d-112">Requirement</span></span> | <span data-ttu-id="c7a1d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c7a1d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a1d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7a1d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c7a1d-115"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7a1d-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7a1d-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7a1d-116">Library</span></span><br/> | <dl> <span data-ttu-id="c7a1d-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c7a1d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a1d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7a1d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a1d-119">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c7a1d-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




