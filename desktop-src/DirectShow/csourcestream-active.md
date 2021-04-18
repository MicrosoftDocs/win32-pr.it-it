---
description: "Il metodo attivo notifica al pin che il filtro è ora attivo. Questo metodo esegue l'override del Metodo CBasePin:: Active. Se il PIN è connesso, questo metodo avvia il thread di streaming."
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Metodo CSourceStream. Active (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329036"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="f9ee7-105">Metodo CSourceStream. Active</span><span class="sxs-lookup"><span data-stu-id="f9ee7-105">CSourceStream.Active method</span></span>

<span data-ttu-id="f9ee7-106">Il `Active` metodo notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="f9ee7-107">Questo metodo esegue l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="f9ee7-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="f9ee7-108">Se il PIN è connesso, questo metodo avvia il thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ee7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9ee7-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="f9ee7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9ee7-110">Parameters</span></span>

<span data-ttu-id="f9ee7-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9ee7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9ee7-112">Return value</span></span>

<span data-ttu-id="f9ee7-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9ee7-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f9ee7-114">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f9ee7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9ee7-115">Return code</span></span>                                                                             | <span data-ttu-id="f9ee7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9ee7-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="f9ee7-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ee7-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f9ee7-118">Il PIN è già attivo.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="f9ee7-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ee7-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f9ee7-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="f9ee7-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ee7-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="f9ee7-122">Non è stato possibile avviare il thread.</span><span class="sxs-lookup"><span data-stu-id="f9ee7-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9ee7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9ee7-123">Requirements</span></span>



| <span data-ttu-id="f9ee7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9ee7-124">Requirement</span></span> | <span data-ttu-id="f9ee7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ee7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ee7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9ee7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f9ee7-127"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ee7-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f9ee7-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9ee7-128">Library</span></span><br/> | <dl> <span data-ttu-id="f9ee7-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ee7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ee7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9ee7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ee7-131">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="f9ee7-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




