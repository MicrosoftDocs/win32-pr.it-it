---
description: Determina se il pin può accettare esempi.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Metodo CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324274"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="55439-103">CBaseInputPin. CheckStreaming, metodo</span><span class="sxs-lookup"><span data-stu-id="55439-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="55439-104">Determina se il pin può accettare esempi.</span><span class="sxs-lookup"><span data-stu-id="55439-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="55439-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55439-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="55439-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55439-106">Parameters</span></span>

<span data-ttu-id="55439-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="55439-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55439-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55439-108">Return value</span></span>

<span data-ttu-id="55439-109">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="55439-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="55439-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="55439-110">Return code</span></span>                                                                                           | <span data-ttu-id="55439-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55439-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="55439-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55439-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="55439-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="55439-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="55439-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="55439-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="55439-115">È in corso lo scaricamento del PIN.</span><span class="sxs-lookup"><span data-stu-id="55439-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="55439-116"><dt>**errore di runtime di VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55439-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="55439-117">Si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55439-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="55439-118"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55439-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="55439-119">Il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="55439-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="55439-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="55439-120">Remarks</span></span>

<span data-ttu-id="55439-121">La classe derivata può eseguire l'override di questo metodo per eseguire ulteriori controlli.</span><span class="sxs-lookup"><span data-stu-id="55439-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="55439-122">Nel metodo che esegue l'override, chiamare anche l'implementazione della classe di base.</span><span class="sxs-lookup"><span data-stu-id="55439-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="55439-123">Il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="55439-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="55439-124">È necessario eseguire l'override del metodo [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) per chiamare anche questo metodo.</span><span class="sxs-lookup"><span data-stu-id="55439-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="55439-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55439-125">Requirements</span></span>



| <span data-ttu-id="55439-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55439-126">Requirement</span></span> | <span data-ttu-id="55439-127">Valore</span><span class="sxs-lookup"><span data-stu-id="55439-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55439-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55439-128">Header</span></span><br/>  | <dl> <span data-ttu-id="55439-129"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55439-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55439-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="55439-130">Library</span></span><br/> | <dl> <span data-ttu-id="55439-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="55439-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55439-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55439-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55439-133">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="55439-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




