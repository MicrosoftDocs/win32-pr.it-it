---
description: 'Il metodo QueryAccept determina se il pin accetta un tipo di supporto specificato. Questo metodo implementa il metodo IPin:: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Metodo CBasePin. QueryAccept (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333796"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="06e04-104">CBasePin. QueryAccept, metodo</span><span class="sxs-lookup"><span data-stu-id="06e04-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="06e04-105">Il `QueryAccept` metodo determina se il pin accetta un tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="06e04-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="06e04-106">Questo metodo implementa il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .</span><span class="sxs-lookup"><span data-stu-id="06e04-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e04-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06e04-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="06e04-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06e04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e04-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="06e04-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="06e04-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="06e04-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e04-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06e04-111">Return value</span></span>

<span data-ttu-id="06e04-112">Restituisce \_ OK se il tipo di supporto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="06e04-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="06e04-113">In caso contrario, restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="06e04-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e04-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="06e04-114">Remarks</span></span>

<span data-ttu-id="06e04-115">Nella classe di base, questo metodo delega al metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="06e04-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="06e04-116">Se **CheckMediaType** ha esito negativo, `QueryAccept` restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="06e04-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="06e04-117">Questo metodo non è contenuta nella sezione critica del PIN ([**CBasePin:: m \_ pLock**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="06e04-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="06e04-118">Se la classe derivata modifica dinamicamente il set di tipi di supporti accettabili, è necessario eseguire l'override di questo metodo per mantenere la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="06e04-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e04-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06e04-119">Requirements</span></span>



| <span data-ttu-id="06e04-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e04-120">Requirement</span></span> | <span data-ttu-id="06e04-121">Valore</span><span class="sxs-lookup"><span data-stu-id="06e04-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e04-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06e04-122">Header</span></span><br/>  | <dl> <span data-ttu-id="06e04-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06e04-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06e04-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="06e04-124">Library</span></span><br/> | <dl> <span data-ttu-id="06e04-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06e04-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e04-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06e04-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e04-127">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="06e04-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




