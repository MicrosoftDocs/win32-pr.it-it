---
description: Il metodo PassNotify passa un messaggio di controllo di qualità all'oggetto appropriato.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Metodo CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326665"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="87d8a-103">CBaseInputPin. PassNotify, metodo</span><span class="sxs-lookup"><span data-stu-id="87d8a-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="87d8a-104">Il `PassNotify` metodo passa un messaggio di controllo di qualità all'oggetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="87d8a-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87d8a-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="87d8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87d8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d8a-107">*d*</span><span class="sxs-lookup"><span data-stu-id="87d8a-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="87d8a-108">Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo della qualità.</span><span class="sxs-lookup"><span data-stu-id="87d8a-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d8a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87d8a-109">Return value</span></span>

<span data-ttu-id="87d8a-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87d8a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87d8a-111">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="87d8a-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="87d8a-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87d8a-112">Return code</span></span>                                                                                       | <span data-ttu-id="87d8a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87d8a-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="87d8a-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87d8a-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="87d8a-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="87d8a-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="87d8a-116"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="87d8a-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="87d8a-117">Impossibile trovare un oggetto per accettare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="87d8a-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87d8a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="87d8a-118">Remarks</span></span>

<span data-ttu-id="87d8a-119">Chiamare questo metodo se il filtro non gestisce i messaggi di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="87d8a-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="87d8a-120">Questo metodo passa il messaggio a uno degli oggetti seguenti, in ordine di preferenza:</span><span class="sxs-lookup"><span data-stu-id="87d8a-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="87d8a-121">Gestore di controllo della qualità esterno, se è stato chiamato il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue.</span><span class="sxs-lookup"><span data-stu-id="87d8a-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="87d8a-122">Pin di output upstream.</span><span class="sxs-lookup"><span data-stu-id="87d8a-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d8a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87d8a-123">Requirements</span></span>



| <span data-ttu-id="87d8a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d8a-124">Requirement</span></span> | <span data-ttu-id="87d8a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="87d8a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d8a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87d8a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="87d8a-127"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87d8a-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87d8a-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="87d8a-128">Library</span></span><br/> | <dl> <span data-ttu-id="87d8a-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87d8a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d8a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87d8a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d8a-131">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="87d8a-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="87d8a-132">Gestione controllo qualità</span><span class="sxs-lookup"><span data-stu-id="87d8a-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




