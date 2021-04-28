---
description: "Metodo CTransformInputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Metodo CTransformInputPin.EndFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095059"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="037d8-104">Metodo CTransformInputPin.EndFlush</span><span class="sxs-lookup"><span data-stu-id="037d8-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="037d8-105">Il `EndFlush` metodo termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="037d8-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="037d8-106">Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="037d8-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="037d8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="037d8-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="037d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="037d8-108">Parameters</span></span>

<span data-ttu-id="037d8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="037d8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="037d8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="037d8-110">Return value</span></span>

<span data-ttu-id="037d8-111">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="037d8-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="037d8-112">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="037d8-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="037d8-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="037d8-113">Return code</span></span>                                                                                           | <span data-ttu-id="037d8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="037d8-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="037d8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="037d8-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="037d8-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="037d8-117"><dt>**VFW \_ E \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="037d8-118">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="037d8-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="037d8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="037d8-119">Remarks</span></span>

<span data-ttu-id="037d8-120">Questo metodo chiama il metodo [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) del filtro per recapitare la chiamata a valle.</span><span class="sxs-lookup"><span data-stu-id="037d8-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="037d8-121">Chiama quindi il metodo [**CBaseInputPin::EndFlush del**](cbaseinputpin-endflush.md) pin.</span><span class="sxs-lookup"><span data-stu-id="037d8-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="037d8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="037d8-122">Requirements</span></span>



| <span data-ttu-id="037d8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="037d8-123">Requirement</span></span> | <span data-ttu-id="037d8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="037d8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="037d8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="037d8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="037d8-126"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="037d8-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="037d8-127">Library</span></span><br/> | <dl> <span data-ttu-id="037d8-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




