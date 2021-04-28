---
description: 'Metodo CBaseRenderer.GetPin: il metodo GetPin recupera un pin.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Metodo CBaseRenderer.GetPin (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119889"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="32361-103">Metodo CBaseRenderer.GetPin</span><span class="sxs-lookup"><span data-stu-id="32361-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="32361-104">Il `GetPin` metodo recupera un pin.</span><span class="sxs-lookup"><span data-stu-id="32361-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="32361-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32361-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="32361-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32361-107">*n*</span><span class="sxs-lookup"><span data-stu-id="32361-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="32361-108">Numero del pin specificato.</span><span class="sxs-lookup"><span data-stu-id="32361-108">Number of the specified pin.</span></span> <span data-ttu-id="32361-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="32361-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32361-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32361-110">Return value</span></span>

<span data-ttu-id="32361-111">Restituisce il [**puntatore CBaseRenderer::m \_ pInputPin.**](cbaserenderer-m-pinputpin.md)</span><span class="sxs-lookup"><span data-stu-id="32361-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="32361-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="32361-112">Remarks</span></span>

<span data-ttu-id="32361-113">Questo metodo implementa il [**metodo CBaseFilter::GetPin,**](cbasefilter-getpin.md) che è virtuale puro nella **classe CBaseFilter.**</span><span class="sxs-lookup"><span data-stu-id="32361-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="32361-114">Il filtro supporta esattamente un pin (il pin di input).</span><span class="sxs-lookup"><span data-stu-id="32361-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="32361-115">La prima volta che questo metodo viene chiamato, crea il segnaposto come nuovo [**oggetto CRendererInputPin.**](crendererinputpin.md)</span><span class="sxs-lookup"><span data-stu-id="32361-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="32361-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32361-116">Requirements</span></span>



| <span data-ttu-id="32361-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="32361-117">Requirement</span></span> | <span data-ttu-id="32361-118">Valore</span><span class="sxs-lookup"><span data-stu-id="32361-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32361-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32361-119">Header</span></span><br/>  | <dl> <span data-ttu-id="32361-120"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="32361-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32361-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="32361-121">Library</span></span><br/> | <dl> <span data-ttu-id="32361-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32361-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32361-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32361-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32361-124">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="32361-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




