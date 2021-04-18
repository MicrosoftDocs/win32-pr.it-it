---
description: Il metodo DisconnectInternal interrompe la connessione al pin corrente.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Metodo CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329543"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="ef976-103">CBasePin. DisconnectInternal, metodo</span><span class="sxs-lookup"><span data-stu-id="ef976-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="ef976-104">Il `DisconnectInternal` metodo interrompe la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="ef976-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef976-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef976-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="ef976-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef976-106">Parameters</span></span>

<span data-ttu-id="ef976-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ef976-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef976-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef976-108">Return value</span></span>

<span data-ttu-id="ef976-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef976-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ef976-110">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ef976-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="ef976-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ef976-111">Return code</span></span>                                                                                         | <span data-ttu-id="ef976-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef976-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef976-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ef976-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="ef976-114">Il PIN non era connesso.</span><span class="sxs-lookup"><span data-stu-id="ef976-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="ef976-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef976-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ef976-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ef976-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ef976-117"><dt>**VFW \_ E \_ non \_ arrestato**</dt></span><span class="sxs-lookup"><span data-stu-id="ef976-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="ef976-118">Il filtro è attivo e il PIN non supporta la riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="ef976-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef976-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef976-119">Remarks</span></span>

<span data-ttu-id="ef976-120">Il metodo [**CBasePin::D di disconnessione**](cbasepin-disconnect.md) delega il processo di disconnessione a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ef976-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="ef976-121">Questo metodo chiama il metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ef976-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="ef976-122">Rilascia anche il conteggio dei riferimenti sull'altro pin, che è contenuto dalla variabile membro [**\_ connesso CBasePin:: m**](cbasepin-m-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="ef976-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef976-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef976-123">Requirements</span></span>



| <span data-ttu-id="ef976-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef976-124">Requirement</span></span> | <span data-ttu-id="ef976-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ef976-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef976-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef976-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ef976-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef976-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef976-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef976-128">Library</span></span><br/> | <dl> <span data-ttu-id="ef976-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef976-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef976-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef976-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef976-131">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="ef976-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




