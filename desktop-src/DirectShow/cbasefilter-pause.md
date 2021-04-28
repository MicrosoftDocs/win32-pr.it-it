---
description: 'Metodo CBaseFilter.Pause: il metodo Pause sospende il filtro. Questo metodo implementa il metodo IMediaFilter::P ause.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Metodo CBaseFilter.Pause (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120089"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="f6321-104">Metodo CBaseFilter.Pause</span><span class="sxs-lookup"><span data-stu-id="f6321-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="f6321-105">Il `Pause` metodo sospende il filtro.</span><span class="sxs-lookup"><span data-stu-id="f6321-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="f6321-106">Questo metodo implementa il [**metodo IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="f6321-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6321-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6321-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="f6321-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6321-108">Parameters</span></span>

<span data-ttu-id="f6321-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f6321-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6321-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6321-110">Return value</span></span>

<span data-ttu-id="f6321-111">Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.</span><span class="sxs-lookup"><span data-stu-id="f6321-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6321-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6321-112">Remarks</span></span>

<span data-ttu-id="f6321-113">Questo metodo chiama [**il metodo CBasePin::Active**](cbasepin-active.md) su ogni segnaposto connesso del filtro.</span><span class="sxs-lookup"><span data-stu-id="f6321-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6321-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6321-114">Requirements</span></span>



| <span data-ttu-id="f6321-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6321-115">Requirement</span></span> | <span data-ttu-id="f6321-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f6321-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6321-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6321-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f6321-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6321-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f6321-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6321-119">Library</span></span><br/> | <dl> <span data-ttu-id="f6321-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f6321-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6321-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6321-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6321-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f6321-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




