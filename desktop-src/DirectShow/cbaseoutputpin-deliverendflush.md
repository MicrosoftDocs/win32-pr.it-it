---
description: Il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di svuotamento.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Metodo CBaseOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332068"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="27cfc-103">CBaseOutputPin. DeliverEndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="27cfc-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="27cfc-104">Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="27cfc-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="27cfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27cfc-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="27cfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27cfc-106">Parameters</span></span>

<span data-ttu-id="27cfc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="27cfc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27cfc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27cfc-108">Return value</span></span>

<span data-ttu-id="27cfc-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27cfc-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="27cfc-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="27cfc-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="27cfc-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="27cfc-111">Return code</span></span>                                                                                           | <span data-ttu-id="27cfc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27cfc-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="27cfc-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27cfc-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="27cfc-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="27cfc-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="27cfc-115"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="27cfc-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="27cfc-116">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="27cfc-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27cfc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="27cfc-117">Remarks</span></span>

<span data-ttu-id="27cfc-118">Questo metodo chiama il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="27cfc-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="27cfc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27cfc-119">Requirements</span></span>



| <span data-ttu-id="27cfc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="27cfc-120">Requirement</span></span> | <span data-ttu-id="27cfc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="27cfc-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27cfc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27cfc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="27cfc-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27cfc-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="27cfc-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="27cfc-124">Library</span></span><br/> | <dl> <span data-ttu-id="27cfc-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="27cfc-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27cfc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27cfc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cfc-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="27cfc-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




