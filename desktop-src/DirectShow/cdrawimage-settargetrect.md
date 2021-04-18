---
description: Il metodo SetTargetRect imposta il rettangolo di destinazione.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Metodo CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327206"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="243d3-103">CDrawImage. SetTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="243d3-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="243d3-104">Il `SetTargetRect` metodo imposta il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="243d3-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="243d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="243d3-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="243d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="243d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243d3-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="243d3-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="243d3-108">Puntatore a una struttura **Rect** che definisce il nuovo rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="243d3-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243d3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="243d3-109">Return value</span></span>

<span data-ttu-id="243d3-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="243d3-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="243d3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="243d3-111">Remarks</span></span>

<span data-ttu-id="243d3-112">Il filtro proprietario deve chiamare questo metodo se il rettangolo di origine viene modificato; ad esempio, in risposta a una chiamata [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .</span><span class="sxs-lookup"><span data-stu-id="243d3-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="243d3-113">Prima di chiamare questo metodo, convalidare il rettangolo specificato in *pTargetRect*, relativo alla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="243d3-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="243d3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="243d3-114">Requirements</span></span>



| <span data-ttu-id="243d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="243d3-115">Requirement</span></span> | <span data-ttu-id="243d3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="243d3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243d3-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="243d3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="243d3-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="243d3-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="243d3-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="243d3-119">Library</span></span><br/> | <dl> <span data-ttu-id="243d3-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="243d3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243d3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="243d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243d3-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="243d3-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




