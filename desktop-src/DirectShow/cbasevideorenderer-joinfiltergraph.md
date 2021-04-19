---
description: Il metodo JoinFilterGraph Invia \_ \_ una notifica di evento distrutta dalla finestra EC quando un filtro viene rimosso dal grafico dei filtri.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Metodo CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330232"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="e3a11-103">CBaseVideoRenderer. JoinFilterGraph, metodo</span><span class="sxs-lookup"><span data-stu-id="e3a11-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="e3a11-104">Il `JoinFilterGraph` metodo invia una notifica di evento [**\_ \_ distrutta dalla finestra EC**](ec-window-destroyed.md) quando un filtro viene rimosso dal grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e3a11-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a11-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="e3a11-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3a11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a11-107">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="e3a11-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a11-108">Puntatore al grafico di filtro da unire.</span><span class="sxs-lookup"><span data-stu-id="e3a11-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="e3a11-109">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3a11-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a11-110">Puntatore al nome del filtro da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e3a11-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a11-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3a11-111">Return value</span></span>

<span data-ttu-id="e3a11-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e3a11-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a11-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a11-113">Remarks</span></span>

<span data-ttu-id="e3a11-114">Questa funzione membro esegue l'override della funzione membro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="e3a11-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="e3a11-115">Se il filtro sta lasciando il grafico del filtro (*pGraph* è **null**), invia una notifica di evento [**\_ \_ distrutta dalla finestra EC**](ec-window-destroyed.md) , in modo che il gestore di risorse non mantenga il renderer come oggetto attivo.</span><span class="sxs-lookup"><span data-stu-id="e3a11-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a11-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a11-116">Requirements</span></span>



| <span data-ttu-id="e3a11-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a11-117">Requirement</span></span> | <span data-ttu-id="e3a11-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a11-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a11-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3a11-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a11-120"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a11-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3a11-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3a11-121">Library</span></span><br/> | <dl> <span data-ttu-id="e3a11-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a11-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a11-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a11-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a11-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e3a11-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




