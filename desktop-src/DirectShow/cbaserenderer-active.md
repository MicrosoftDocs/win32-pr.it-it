---
description: Il metodo attivo viene chiamato quando lo stato viene impostato su in pausa o in esecuzione.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Metodo CBaseRenderer. Active (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329407"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="058c8-103">Metodo CBaseRenderer. Active</span><span class="sxs-lookup"><span data-stu-id="058c8-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="058c8-104">Il `Active` metodo viene chiamato quando lo stato viene impostato su in pausa o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="058c8-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="058c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="058c8-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="058c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="058c8-106">Parameters</span></span>

<span data-ttu-id="058c8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="058c8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="058c8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="058c8-108">Return value</span></span>

<span data-ttu-id="058c8-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="058c8-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="058c8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="058c8-110">Remarks</span></span>

<span data-ttu-id="058c8-111">Il pin di input chiama questo metodo dal proprio metodo [**CRendererInputPin:: Active**](crendererinputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="058c8-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="058c8-112">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="058c8-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="058c8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="058c8-113">Requirements</span></span>



| <span data-ttu-id="058c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="058c8-114">Requirement</span></span> | <span data-ttu-id="058c8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="058c8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058c8-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="058c8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="058c8-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="058c8-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="058c8-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="058c8-118">Library</span></span><br/> | <dl> <span data-ttu-id="058c8-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="058c8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="058c8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="058c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058c8-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="058c8-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




