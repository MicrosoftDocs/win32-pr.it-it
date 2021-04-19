---
description: Il metodo DeliverBeginFlush richiede al pin di input connesso di iniziare un'operazione di svuotamento.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Metodo CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332258"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="23fbd-103">CBaseOutputPin. DeliverBeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="23fbd-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="23fbd-104">Il `DeliverBeginFlush` metodo richiede al pin di input connesso di iniziare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="23fbd-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23fbd-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="23fbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23fbd-106">Parameters</span></span>

<span data-ttu-id="23fbd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="23fbd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23fbd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23fbd-108">Return value</span></span>

<span data-ttu-id="23fbd-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23fbd-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="23fbd-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="23fbd-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="23fbd-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="23fbd-111">Return code</span></span>                                                                                           | <span data-ttu-id="23fbd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23fbd-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="23fbd-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="23fbd-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="23fbd-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="23fbd-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="23fbd-115"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="23fbd-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="23fbd-116">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="23fbd-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23fbd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="23fbd-117">Remarks</span></span>

<span data-ttu-id="23fbd-118">Questo metodo chiama il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="23fbd-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fbd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23fbd-119">Requirements</span></span>



| <span data-ttu-id="23fbd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fbd-120">Requirement</span></span> | <span data-ttu-id="23fbd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="23fbd-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fbd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23fbd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23fbd-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23fbd-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23fbd-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="23fbd-124">Library</span></span><br/> | <dl> <span data-ttu-id="23fbd-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23fbd-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23fbd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23fbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fbd-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="23fbd-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




