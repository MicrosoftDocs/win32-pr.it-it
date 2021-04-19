---
description: Il metodo InputPin recupera un puntatore al pin di input del filtro.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Metodo CTransInPlaceFilter. InputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326392"
---
# <a name="ctransinplacefilterinputpin-method"></a><span data-ttu-id="2bf2c-103">CTransInPlaceFilter. InputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="2bf2c-103">CTransInPlaceFilter.InputPin method</span></span>

<span data-ttu-id="2bf2c-104">Il `InputPin` metodo recupera un puntatore al pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-104">The `InputPin` method retrieves a pointer to the filter's input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf2c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bf2c-105">Syntax</span></span>


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a><span data-ttu-id="2bf2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2bf2c-106">Parameters</span></span>

<span data-ttu-id="2bf2c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2bf2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bf2c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bf2c-108">Return value</span></span>

<span data-ttu-id="2bf2c-109">Restituisce la variabile membro [**CTransformFilter:: m \_ Pinput**](ctransformfilter-m-pinput.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf2c-109">Returns the [**CTransformFilter::m\_pInput**](ctransformfilter-m-pinput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf2c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bf2c-110">Requirements</span></span>



| <span data-ttu-id="2bf2c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf2c-111">Requirement</span></span> | <span data-ttu-id="2bf2c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2bf2c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf2c-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bf2c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2bf2c-114"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf2c-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2bf2c-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="2bf2c-115">Library</span></span><br/> | <dl> <span data-ttu-id="2bf2c-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf2c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf2c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bf2c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf2c-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="2bf2c-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




