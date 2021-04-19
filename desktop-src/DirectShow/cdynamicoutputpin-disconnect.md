---
description: Il metodo Disconnect interrompe la connessione al pin corrente. Questo metodo implementa il metodo IPin::D la connessione.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Metodo CDynamicOutputPin. Disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331790"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="bbcdf-104">Metodo CDynamicOutputPin. Disconnect</span><span class="sxs-lookup"><span data-stu-id="bbcdf-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="bbcdf-105">Il `Disconnect` metodo interrompe la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="bbcdf-106">Questo metodo implementa il metodo [**Ipin::D la connessione**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="bbcdf-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbcdf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbcdf-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="bbcdf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbcdf-108">Parameters</span></span>

<span data-ttu-id="bbcdf-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbcdf-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbcdf-110">Return value</span></span>

<span data-ttu-id="bbcdf-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bbcdf-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bbcdf-112">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bbcdf-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bbcdf-113">Return code</span></span>                                                                             | <span data-ttu-id="bbcdf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbcdf-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bbcdf-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="bbcdf-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="bbcdf-116">Il PIN non era connesso.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="bbcdf-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbcdf-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="bbcdf-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="bbcdf-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbcdf-119">Remarks</span></span>

<span data-ttu-id="bbcdf-120">Questo metodo esegue l'override del metodo [**CBasePin::D la connessione**](cbasepin-disconnect.md) per abilitare la disconnessione mentre il filtro è attivo.</span><span class="sxs-lookup"><span data-stu-id="bbcdf-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbcdf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbcdf-121">Requirements</span></span>



| <span data-ttu-id="bbcdf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbcdf-122">Requirement</span></span> | <span data-ttu-id="bbcdf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bbcdf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbcdf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbcdf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bbcdf-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbcdf-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bbcdf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bbcdf-126">Library</span></span><br/> | <dl> <span data-ttu-id="bbcdf-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bbcdf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbcdf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbcdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbcdf-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bbcdf-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




