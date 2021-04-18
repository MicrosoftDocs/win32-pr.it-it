---
description: Il metodo SendRepaint Invia un evento Repaint al gestore del grafico dei filtri.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Metodo CBaseRenderer. SendRepaint (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329534"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="0984f-103">CBaseRenderer. SendRepaint, metodo</span><span class="sxs-lookup"><span data-stu-id="0984f-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="0984f-104">Il `SendRepaint` metodo invia un evento Repaint al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="0984f-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="0984f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0984f-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="0984f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0984f-106">Parameters</span></span>

<span data-ttu-id="0984f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0984f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0984f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0984f-108">Return value</span></span>

<span data-ttu-id="0984f-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0984f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0984f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0984f-110">Remarks</span></span>

<span data-ttu-id="0984f-111">Questo metodo invia un evento di [**\_ ridisegno EC**](ec-repaint.md) al gestore del grafico del filtro se le condizioni seguenti sono vere:</span><span class="sxs-lookup"><span data-stu-id="0984f-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="0984f-112">Il pin di input è connesso.</span><span class="sxs-lookup"><span data-stu-id="0984f-112">The input pin is connected.</span></span>
-   <span data-ttu-id="0984f-113">Il filtro non Scarica i dati.</span><span class="sxs-lookup"><span data-stu-id="0984f-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="0984f-114">Non è stata raggiunta la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="0984f-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="0984f-115">Il flag [**\_ BAbort di CBaseRenderer:: m**](cbaserenderer-m-babort.md) è **false**.</span><span class="sxs-lookup"><span data-stu-id="0984f-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="0984f-116">Il flag [**\_ BRepaintStatus di CBaseRenderer:: m**](cbaserenderer-m-brepaintstatus.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="0984f-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="0984f-117">A seconda dello stato del grafico, l' \_ evento di ridisegno EC può causare il reinvio di un campione da parte del filtro upstream, il grafico del filtro per cercare la posizione corrente oppure il gestore del grafico del filtro per sospendere momentaneamente.</span><span class="sxs-lookup"><span data-stu-id="0984f-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="0984f-118">(Vedere la pagina relativa al [**\_ ridisegno EC**](ec-repaint.md)). Questo evento è potenzialmente inefficiente, quindi deve essere usato in modo sporadico.</span><span class="sxs-lookup"><span data-stu-id="0984f-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="0984f-119">Tuttavia, i renderer video a volte devono aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0984f-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="0984f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0984f-120">Requirements</span></span>



| <span data-ttu-id="0984f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0984f-121">Requirement</span></span> | <span data-ttu-id="0984f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0984f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0984f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0984f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0984f-124"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0984f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0984f-125">Library</span></span><br/> | <dl> <span data-ttu-id="0984f-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0984f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0984f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0984f-128">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="0984f-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




