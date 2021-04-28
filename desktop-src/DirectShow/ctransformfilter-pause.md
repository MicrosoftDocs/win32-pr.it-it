---
description: 'Metodo CTransformFilter.Pause: il metodo Pause sospende il filtro. Questo metodo implementa il metodo IMediaFilter::P ause.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: Metodo CTransformFilter.Pause (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095099"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="8d425-104">Metodo CTransformFilter.Pause</span><span class="sxs-lookup"><span data-stu-id="8d425-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="8d425-105">Il `Pause` metodo sospende il filtro.</span><span class="sxs-lookup"><span data-stu-id="8d425-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="8d425-106">Questo metodo implementa il [**metodo IMediaFilter::P ause.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause)</span><span class="sxs-lookup"><span data-stu-id="8d425-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d425-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d425-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="8d425-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d425-108">Parameters</span></span>

<span data-ttu-id="8d425-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8d425-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d425-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d425-110">Return value</span></span>

<span data-ttu-id="8d425-111">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8d425-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d425-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d425-112">Remarks</span></span>

<span data-ttu-id="8d425-113">Questo metodo chiama il [**metodo StartStreaming.**](ctransformfilter-startstreaming.md)</span><span class="sxs-lookup"><span data-stu-id="8d425-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="8d425-114">Il **metodo StartStreaming** non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="8d425-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d425-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d425-115">Requirements</span></span>



| <span data-ttu-id="8d425-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d425-116">Requirement</span></span> | <span data-ttu-id="8d425-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8d425-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d425-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d425-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8d425-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d425-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8d425-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d425-120">Library</span></span><br/> | <dl> <span data-ttu-id="8d425-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d425-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d425-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d425-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d425-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8d425-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




