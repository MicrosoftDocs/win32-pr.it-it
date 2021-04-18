---
description: Il metodo GetFilterGraph recupera un puntatore al gestore del grafico dei filtri.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Metodo CBaseFilter. GetFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328948"
---
# <a name="cbasefiltergetfiltergraph-method"></a><span data-ttu-id="e5c13-103">CBaseFilter. GetFilterGraph, metodo</span><span class="sxs-lookup"><span data-stu-id="e5c13-103">CBaseFilter.GetFilterGraph method</span></span>

<span data-ttu-id="e5c13-104">Il `GetFilterGraph` metodo recupera un puntatore al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="e5c13-104">The `GetFilterGraph` method retrieves a pointer to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5c13-105">Syntax</span></span>


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a><span data-ttu-id="e5c13-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5c13-106">Parameters</span></span>

<span data-ttu-id="e5c13-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e5c13-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5c13-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5c13-108">Return value</span></span>

<span data-ttu-id="e5c13-109">Restituisce il valore di [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md).</span><span class="sxs-lookup"><span data-stu-id="e5c13-109">Returns the value of [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c13-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c13-110">Requirements</span></span>



| <span data-ttu-id="e5c13-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c13-111">Requirement</span></span> | <span data-ttu-id="e5c13-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c13-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c13-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c13-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c13-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c13-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e5c13-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5c13-115">Library</span></span><br/> | <dl> <span data-ttu-id="e5c13-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c13-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c13-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c13-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c13-118">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e5c13-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




