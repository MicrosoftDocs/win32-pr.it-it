---
description: Il metodo ForceRefresh è obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Metodo CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329515"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="514b7-103">CPosPassThru. ForceRefresh, metodo</span><span class="sxs-lookup"><span data-stu-id="514b7-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="514b7-104">Il `ForceRefresh` metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="514b7-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="514b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="514b7-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="514b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="514b7-106">Parameters</span></span>

<span data-ttu-id="514b7-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="514b7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="514b7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="514b7-108">Return value</span></span>

<span data-ttu-id="514b7-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="514b7-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="514b7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="514b7-110">Remarks</span></span>

<span data-ttu-id="514b7-111">Originariamente questa classe era progettata per memorizzare nella cache i puntatori alle interfacce [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del pin connesso.</span><span class="sxs-lookup"><span data-stu-id="514b7-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="514b7-112">Il `ForceRefresh` metodo ha rilasciato tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="514b7-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="514b7-113">Attualmente implementata, questa classe non memorizza nella cache tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="514b7-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="514b7-114">Per compatibilità, il `ForceRefresh` metodo è ancora incluso, ma restituisce S \_ OK senza eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="514b7-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="514b7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="514b7-115">Requirements</span></span>



| <span data-ttu-id="514b7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="514b7-116">Requirement</span></span> | <span data-ttu-id="514b7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="514b7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="514b7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="514b7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="514b7-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="514b7-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="514b7-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="514b7-120">Library</span></span><br/> | <dl> <span data-ttu-id="514b7-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="514b7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514b7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="514b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514b7-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="514b7-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




