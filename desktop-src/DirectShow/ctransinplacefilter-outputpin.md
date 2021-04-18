---
description: Il metodo OutputPin recupera un puntatore al pin di output del filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Metodo CTransInPlaceFilter. OutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328168"
---
# <a name="ctransinplacefilteroutputpin-method"></a><span data-ttu-id="b7dac-103">CTransInPlaceFilter. OutputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="b7dac-103">CTransInPlaceFilter.OutputPin method</span></span>

<span data-ttu-id="b7dac-104">Il `OutputPin` metodo recupera un puntatore al pin di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="b7dac-104">The `OutputPin` method retrieves a pointer to the filter's output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7dac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7dac-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a><span data-ttu-id="b7dac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7dac-106">Parameters</span></span>

<span data-ttu-id="b7dac-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b7dac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7dac-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7dac-108">Return value</span></span>

<span data-ttu-id="b7dac-109">Restituisce la variabile membro [**CTransformFilter:: m \_ pOutput**](ctransformfilter-m-poutput.md) .</span><span class="sxs-lookup"><span data-stu-id="b7dac-109">Returns the [**CTransformFilter::m\_pOutput**](ctransformfilter-m-poutput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7dac-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7dac-110">Requirements</span></span>



| <span data-ttu-id="b7dac-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7dac-111">Requirement</span></span> | <span data-ttu-id="b7dac-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b7dac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dac-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7dac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b7dac-114"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dac-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7dac-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7dac-115">Library</span></span><br/> | <dl> <span data-ttu-id="b7dac-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7dac-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7dac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dac-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="b7dac-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




