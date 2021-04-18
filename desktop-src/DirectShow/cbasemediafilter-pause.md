---
description: Sospende l'oggetto. Implementa il metodo IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Metodo CBaseMediaFilter. pause (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325077"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="55a45-104">CBaseMediaFilter. pause (metodo)</span><span class="sxs-lookup"><span data-stu-id="55a45-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="55a45-105">Sospende l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55a45-105">Pauses the object.</span></span> <span data-ttu-id="55a45-106">Implementa il metodo [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="55a45-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a45-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55a45-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="55a45-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="55a45-108">Parameters</span></span>

<span data-ttu-id="55a45-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="55a45-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55a45-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55a45-110">Return value</span></span>

<span data-ttu-id="55a45-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55a45-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a45-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="55a45-112">Remarks</span></span>

<span data-ttu-id="55a45-113">Nella classe di base, questo metodo imposta la variabile membro di [**\_ stato CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) su stato \_ sospeso ma non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="55a45-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a45-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55a45-114">Requirements</span></span>



| <span data-ttu-id="55a45-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a45-115">Requirement</span></span> | <span data-ttu-id="55a45-116">Valore</span><span class="sxs-lookup"><span data-stu-id="55a45-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a45-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55a45-117">Header</span></span><br/>  | <dl> <span data-ttu-id="55a45-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55a45-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55a45-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="55a45-119">Library</span></span><br/> | <dl> <span data-ttu-id="55a45-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="55a45-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a45-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55a45-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a45-122">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="55a45-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




