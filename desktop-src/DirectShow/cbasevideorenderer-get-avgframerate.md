---
description: Il \_ metodo Get AvgFrameRate calcola e recupera la frequenza dei fotogrammi media conseguita.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Metodo CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331522"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="5db3d-103">Metodo CBaseVideoRenderer. Get \_ AvgFrameRate</span><span class="sxs-lookup"><span data-stu-id="5db3d-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="5db3d-104">Il `get_AvgFrameRate` metodo calcola e recupera la frequenza dei fotogrammi media conseguita.</span><span class="sxs-lookup"><span data-stu-id="5db3d-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db3d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5db3d-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="5db3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5db3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db3d-107">*piAvgFrameRate*</span><span class="sxs-lookup"><span data-stu-id="5db3d-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="5db3d-108">Puntatore al numero di fotogrammi al secondo dall'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="5db3d-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db3d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5db3d-109">Return value</span></span>

<span data-ttu-id="5db3d-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5db3d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db3d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5db3d-111">Remarks</span></span>

<span data-ttu-id="5db3d-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .</span><span class="sxs-lookup"><span data-stu-id="5db3d-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db3d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5db3d-113">Requirements</span></span>



| <span data-ttu-id="5db3d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5db3d-114">Requirement</span></span> | <span data-ttu-id="5db3d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5db3d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db3d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5db3d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5db3d-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5db3d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5db3d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="5db3d-118">Library</span></span><br/> | <dl> <span data-ttu-id="5db3d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5db3d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db3d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5db3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db3d-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="5db3d-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




