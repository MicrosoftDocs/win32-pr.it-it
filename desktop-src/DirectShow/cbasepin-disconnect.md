---
description: 'Metodo CBasePin.Disconnect: il metodo Disconnect interrompe la connessione pin corrente. Questo metodo implementa il metodo IPin::D isconnect.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Metodo CBasePin.Disconnect (Amfilter.h)
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
ms.openlocfilehash: bda01d02db2a93a90c63f206b723a55df2373418
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096009"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="07602-104">Metodo CBasePin.Disconnect</span><span class="sxs-lookup"><span data-stu-id="07602-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="07602-105">Il `Disconnect` metodo interrompe la connessione pin corrente.</span><span class="sxs-lookup"><span data-stu-id="07602-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="07602-106">Questo metodo implementa il [**metodo IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="07602-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07602-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07602-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="07602-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07602-108">Parameters</span></span>

<span data-ttu-id="07602-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07602-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07602-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07602-110">Return value</span></span>

<span data-ttu-id="07602-111">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="07602-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="07602-112">I valori possibili sono quelli riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="07602-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="07602-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="07602-113">Return code</span></span>                                                                                         | <span data-ttu-id="07602-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07602-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07602-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="07602-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="07602-116">Il pin non è connesso.</span><span class="sxs-lookup"><span data-stu-id="07602-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="07602-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="07602-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="07602-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="07602-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="07602-119"><dt>**VFW \_ E \_ NON \_ ARRESTATO**</dt></span><span class="sxs-lookup"><span data-stu-id="07602-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="07602-120">Il filtro è attivo e il pin non supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="07602-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07602-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="07602-121">Remarks</span></span>

<span data-ttu-id="07602-122">La classe base delega la maggior parte del lavoro al [**metodo CBasePin::D isconnectInternal.**](cbasepin-disconnectinternal.md)</span><span class="sxs-lookup"><span data-stu-id="07602-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07602-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07602-123">Requirements</span></span>



| <span data-ttu-id="07602-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="07602-124">Requirement</span></span> | <span data-ttu-id="07602-125">Valore</span><span class="sxs-lookup"><span data-stu-id="07602-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07602-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07602-126">Header</span></span><br/>  | <dl> <span data-ttu-id="07602-127"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="07602-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="07602-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="07602-128">Library</span></span><br/> | <dl> <span data-ttu-id="07602-129"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07602-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07602-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07602-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07602-131">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="07602-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




