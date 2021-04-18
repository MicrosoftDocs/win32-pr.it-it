---
description: Il metodo Disconnect interrompe la connessione al pin corrente. Questo metodo implementa il metodo IPin::D la connessione.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Metodo CBasePin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329544"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="884ad-104">Metodo CBasePin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="884ad-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="884ad-105">Il `Disconnect` metodo interrompe la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="884ad-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="884ad-106">Questo metodo implementa il metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="884ad-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="884ad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="884ad-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="884ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="884ad-108">Parameters</span></span>

<span data-ttu-id="884ad-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="884ad-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="884ad-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="884ad-110">Return value</span></span>

<span data-ttu-id="884ad-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="884ad-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="884ad-112">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="884ad-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="884ad-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="884ad-113">Return code</span></span>                                                                                         | <span data-ttu-id="884ad-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="884ad-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="884ad-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="884ad-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="884ad-116">Il PIN non era connesso.</span><span class="sxs-lookup"><span data-stu-id="884ad-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="884ad-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="884ad-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="884ad-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="884ad-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="884ad-119"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="884ad-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="884ad-120">Il filtro è attivo e il PIN non supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="884ad-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="884ad-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="884ad-121">Remarks</span></span>

<span data-ttu-id="884ad-122">La classe base delega la maggior parte del lavoro al metodo [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .</span><span class="sxs-lookup"><span data-stu-id="884ad-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="884ad-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="884ad-123">Requirements</span></span>



| <span data-ttu-id="884ad-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="884ad-124">Requirement</span></span> | <span data-ttu-id="884ad-125">Valore</span><span class="sxs-lookup"><span data-stu-id="884ad-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="884ad-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="884ad-126">Header</span></span><br/>  | <dl> <span data-ttu-id="884ad-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="884ad-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="884ad-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="884ad-128">Library</span></span><br/> | <dl> <span data-ttu-id="884ad-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="884ad-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884ad-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="884ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884ad-131">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="884ad-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




