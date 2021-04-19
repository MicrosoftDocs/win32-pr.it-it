---
description: Il metodo ResetEndOfStream Reimposta i flag di fine del flusso.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Metodo CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333331"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="e3a55-103">CBaseRenderer. ResetEndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="e3a55-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="e3a55-104">Il `ResetEndOfStream` metodo reimposta i flag di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="e3a55-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a55-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="e3a55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3a55-106">Parameters</span></span>

<span data-ttu-id="e3a55-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e3a55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3a55-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3a55-108">Return value</span></span>

<span data-ttu-id="e3a55-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3a55-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a55-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a55-110">Remarks</span></span>

<span data-ttu-id="e3a55-111">Questo metodo cancella la condizione di fine del flusso precedente.</span><span class="sxs-lookup"><span data-stu-id="e3a55-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="e3a55-112">A questo punto, il filtro può ricevere nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="e3a55-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="e3a55-113">I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e3a55-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a55-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a55-114">Requirements</span></span>



| <span data-ttu-id="e3a55-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a55-115">Requirement</span></span> | <span data-ttu-id="e3a55-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a55-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a55-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3a55-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a55-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a55-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3a55-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3a55-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3a55-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a55-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a55-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a55-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a55-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e3a55-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




