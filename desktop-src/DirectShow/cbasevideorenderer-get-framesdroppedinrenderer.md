---
description: Il \_ metodo Get FramesDroppedInRenderer Recupera il numero di frame eliminati dal renderer.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Metodo CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326417"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="1851a-103">Metodo CBaseVideoRenderer. Get \_ FramesDroppedInRenderer</span><span class="sxs-lookup"><span data-stu-id="1851a-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="1851a-104">Il `get_FramesDroppedInRenderer` metodo recupera il numero di frame eliminati dal renderer.</span><span class="sxs-lookup"><span data-stu-id="1851a-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1851a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1851a-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="1851a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1851a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1851a-107">*pcFramesDropped*</span><span class="sxs-lookup"><span data-stu-id="1851a-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="1851a-108">Puntatore al numero di frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="1851a-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1851a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1851a-109">Return value</span></span>

<span data-ttu-id="1851a-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1851a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1851a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1851a-111">Remarks</span></span>

<span data-ttu-id="1851a-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) .</span><span class="sxs-lookup"><span data-stu-id="1851a-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="1851a-113">Questo è il modo in cui la pagina delle proprietà recupera i dati dall'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1851a-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="1851a-114">I frame possono anche essere eliminati a Monte senza che vengano visualizzati anche dal renderer.</span><span class="sxs-lookup"><span data-stu-id="1851a-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="1851a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1851a-115">Requirements</span></span>



| <span data-ttu-id="1851a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1851a-116">Requirement</span></span> | <span data-ttu-id="1851a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1851a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1851a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1851a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1851a-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1851a-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1851a-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="1851a-120">Library</span></span><br/> | <dl> <span data-ttu-id="1851a-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1851a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1851a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1851a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1851a-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="1851a-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




