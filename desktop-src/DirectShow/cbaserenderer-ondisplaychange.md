---
description: Il metodo OnDisplayChange Invia un \_ \_ evento di modifica della visualizzazione EC al gestore del grafico dei filtri.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Metodo CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333354"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="07df5-103">CBaseRenderer. OnDisplayChange, metodo</span><span class="sxs-lookup"><span data-stu-id="07df5-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="07df5-104">Il `OnDisplayChange` metodo invia un evento di [**\_ \_ modifica della visualizzazione EC**](ec-display-changed.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="07df5-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="07df5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07df5-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="07df5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07df5-106">Parameters</span></span>

<span data-ttu-id="07df5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07df5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07df5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07df5-108">Return value</span></span>

<span data-ttu-id="07df5-109">Restituisce **true** se l'evento è stato pubblicato; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="07df5-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07df5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="07df5-110">Remarks</span></span>

<span data-ttu-id="07df5-111">I renderer video devono chiamare questo metodo in risposta ai \_ messaggi WM DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="07df5-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="07df5-112">Se il pin di input è connesso, il metodo invia un \_ \_ evento di modifica della visualizzazione EC al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="07df5-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="07df5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07df5-113">Requirements</span></span>



| <span data-ttu-id="07df5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="07df5-114">Requirement</span></span> | <span data-ttu-id="07df5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="07df5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07df5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07df5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="07df5-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07df5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07df5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="07df5-118">Library</span></span><br/> | <dl> <span data-ttu-id="07df5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07df5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07df5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07df5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07df5-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="07df5-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




