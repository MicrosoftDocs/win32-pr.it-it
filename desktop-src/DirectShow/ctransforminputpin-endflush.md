---
description: "Il metodo EndFlush termina un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: EndFlush."
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Metodo CTransformInputPin. EndFlush (Transfrm. h)
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
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328801"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="4d3d2-104">CTransformInputPin. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="4d3d2-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="4d3d2-105">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="4d3d2-106">Questo metodo implementa il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="4d3d2-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d3d2-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="4d3d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d3d2-108">Parameters</span></span>

<span data-ttu-id="4d3d2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d3d2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d3d2-110">Return value</span></span>

<span data-ttu-id="4d3d2-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d3d2-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4d3d2-112">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4d3d2-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4d3d2-113">Return code</span></span>                                                                                           | <span data-ttu-id="4d3d2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d3d2-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="4d3d2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d2-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="4d3d2-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="4d3d2-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d2-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4d3d2-118">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4d3d2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d3d2-119">Remarks</span></span>

<span data-ttu-id="4d3d2-120">Questo metodo chiama il metodo [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) del filtro per recapitare la chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="4d3d2-121">Chiama quindi il metodo [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) del PIN.</span><span class="sxs-lookup"><span data-stu-id="4d3d2-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d3d2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d3d2-122">Requirements</span></span>



| <span data-ttu-id="4d3d2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d3d2-123">Requirement</span></span> | <span data-ttu-id="4d3d2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4d3d2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3d2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d3d2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4d3d2-126"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d2-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d3d2-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d3d2-127">Library</span></span><br/> | <dl> <span data-ttu-id="4d3d2-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d3d2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




