---
description: Il metodo CompleteStateChange determina se una transizione allo stato di sospensione è stata completata.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Metodo CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329390"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="bddd6-103">CBaseRenderer. CompleteStateChange, metodo</span><span class="sxs-lookup"><span data-stu-id="bddd6-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="bddd6-104">Il `CompleteStateChange` metodo determina se una transizione allo stato di sospensione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bddd6-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddd6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bddd6-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="bddd6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bddd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bddd6-107">*Stato precedente*</span><span class="sxs-lookup"><span data-stu-id="bddd6-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="bddd6-108">Stato precedente alla transizione.</span><span class="sxs-lookup"><span data-stu-id="bddd6-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bddd6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bddd6-109">Return value</span></span>

<span data-ttu-id="bddd6-110">Restituisce \_ OK se la transizione è completa.</span><span class="sxs-lookup"><span data-stu-id="bddd6-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="bddd6-111">In caso contrario, restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="bddd6-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="bddd6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bddd6-112">Remarks</span></span>

<span data-ttu-id="bddd6-113">Il metodo [**CBaseRenderer::P ause**](cbaserenderer-pause.md) chiama questo metodo per aggiornare lo stato della transizione di stato.</span><span class="sxs-lookup"><span data-stu-id="bddd6-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="bddd6-114">In generale, la transizione a Paused non viene completata fino a quando il filtro non riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="bddd6-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="bddd6-115">In alcune situazioni, tuttavia, la transizione viene completata immediatamente: ad esempio, se il filtro è scollegato o se è stata raggiunta la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="bddd6-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="bddd6-116">Questo metodo controlla i vari criteri e quindi chiama il metodo [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) o il metodo [**CBaseRenderer:: nobattistraday**](cbaserenderer-notready.md) per aggiornare lo stato della transizione.</span><span class="sxs-lookup"><span data-stu-id="bddd6-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddd6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bddd6-117">Requirements</span></span>



| <span data-ttu-id="bddd6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bddd6-118">Requirement</span></span> | <span data-ttu-id="bddd6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bddd6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddd6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bddd6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bddd6-121"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bddd6-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bddd6-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="bddd6-122">Library</span></span><br/> | <dl> <span data-ttu-id="bddd6-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bddd6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddd6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bddd6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddd6-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="bddd6-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




