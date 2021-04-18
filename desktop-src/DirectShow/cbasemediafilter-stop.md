---
description: "Il metodo Stop arresta l'oggetto. Questo metodo implementa il metodo IMediaFilter:: stop."
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Metodo CBaseMediaFilter. Stop (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325070"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="11023-104">Metodo CBaseMediaFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="11023-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="11023-105">Il `Stop` metodo interrompe l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="11023-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="11023-106">Questo metodo implementa il metodo [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="11023-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11023-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11023-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="11023-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11023-108">Parameters</span></span>

<span data-ttu-id="11023-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="11023-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11023-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11023-110">Return value</span></span>

<span data-ttu-id="11023-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11023-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="11023-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="11023-112">Remarks</span></span>

<span data-ttu-id="11023-113">Nella classe di base, questo metodo imposta la variabile membro di [**\_ stato CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) su stato \_ arrestato ma non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="11023-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="11023-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11023-114">Requirements</span></span>



| <span data-ttu-id="11023-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11023-115">Requirement</span></span> | <span data-ttu-id="11023-116">Valore</span><span class="sxs-lookup"><span data-stu-id="11023-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11023-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11023-117">Header</span></span><br/>  | <dl> <span data-ttu-id="11023-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11023-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="11023-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="11023-119">Library</span></span><br/> | <dl> <span data-ttu-id="11023-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="11023-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11023-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11023-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11023-122">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="11023-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




