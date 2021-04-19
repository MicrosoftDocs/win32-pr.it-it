---
description: Il \_ metodo Get FramesDrawn recupera la \_ variabile membro cFramesDrawn di m, assegnando il numero di frame disegnati dopo l'avvio del flusso.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Metodo CBaseVideoRenderer.get_FramesDrawn (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326421"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="fe7ca-103">Metodo CBaseVideoRenderer. Get \_ FramesDrawn</span><span class="sxs-lookup"><span data-stu-id="fe7ca-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="fe7ca-104">Il `get_FramesDrawn` metodo recupera la variabile membro **\_ cFramesDrawn di m** , assegnando il numero di frame disegnati dopo l'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe7ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe7ca-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="fe7ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe7ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe7ca-107">*pcFramesDrawn*</span><span class="sxs-lookup"><span data-stu-id="fe7ca-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="fe7ca-108">Puntatore al numero di frame disegnati.</span><span class="sxs-lookup"><span data-stu-id="fe7ca-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe7ca-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe7ca-109">Return value</span></span>

<span data-ttu-id="fe7ca-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fe7ca-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe7ca-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe7ca-111">Remarks</span></span>

<span data-ttu-id="fe7ca-112">Questa funzione membro implementa il metodo [**IQualProp:: Get \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .</span><span class="sxs-lookup"><span data-stu-id="fe7ca-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe7ca-113">Requirements</span></span>



| <span data-ttu-id="fe7ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe7ca-114">Requirement</span></span> | <span data-ttu-id="fe7ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fe7ca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7ca-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe7ca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fe7ca-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ca-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe7ca-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe7ca-118">Library</span></span><br/> | <dl> <span data-ttu-id="fe7ca-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe7ca-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe7ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7ca-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="fe7ca-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




