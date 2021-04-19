---
description: Il metodo SetRepaintStatus Abilita o Disabilita gli eventi di ridisegno.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Metodo CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333002"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="34282-103">CBaseRenderer. SetRepaintStatus, metodo</span><span class="sxs-lookup"><span data-stu-id="34282-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="34282-104">Il `SetRepaintStatus` metodo consente di abilitare o disabilitare gli eventi di ridisegno.</span><span class="sxs-lookup"><span data-stu-id="34282-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="34282-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34282-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="34282-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34282-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="34282-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="34282-108">Valore booleano che indica se gli eventi di Repaint sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="34282-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="34282-109">Se **true**, il filtro invierà gli eventi di [**\_ ridisegno EC**](ec-repaint.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="34282-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="34282-110">In caso contrario, non verrà inviato alcun \_ evento di ridisegno EC.</span><span class="sxs-lookup"><span data-stu-id="34282-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34282-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34282-111">Return value</span></span>

<span data-ttu-id="34282-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="34282-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34282-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="34282-113">Remarks</span></span>

<span data-ttu-id="34282-114">Questo metodo garantisce che il gestore del grafo del filtro non venga invaso da eventi di ridisegno EC ridondanti \_ .</span><span class="sxs-lookup"><span data-stu-id="34282-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="34282-115">Dopo che il filtro ha inviato un evento di [**\_ ridisegno EC**](ec-repaint.md) , chiama questo metodo con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="34282-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="34282-116">Il filtro non invia più eventi di \_ ridisegno EC fino a quando non riceve più dati.</span><span class="sxs-lookup"><span data-stu-id="34282-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="34282-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34282-117">Requirements</span></span>



| <span data-ttu-id="34282-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34282-118">Requirement</span></span> | <span data-ttu-id="34282-119">Valore</span><span class="sxs-lookup"><span data-stu-id="34282-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34282-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34282-120">Header</span></span><br/>  | <dl> <span data-ttu-id="34282-121"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34282-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34282-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="34282-122">Library</span></span><br/> | <dl> <span data-ttu-id="34282-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34282-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34282-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34282-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34282-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="34282-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




