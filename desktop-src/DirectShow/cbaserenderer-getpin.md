---
description: Il metodo GetPin recupera un PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Metodo CBaseRenderer. GetPin (Renbase. h)
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
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325519"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="34df9-103">CBaseRenderer. GetPin, metodo</span><span class="sxs-lookup"><span data-stu-id="34df9-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="34df9-104">Il `GetPin` metodo recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="34df9-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="34df9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34df9-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="34df9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34df9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34df9-107">*n*</span><span class="sxs-lookup"><span data-stu-id="34df9-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="34df9-108">Numero del PIN specificato.</span><span class="sxs-lookup"><span data-stu-id="34df9-108">Number of the specified pin.</span></span> <span data-ttu-id="34df9-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="34df9-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34df9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34df9-110">Return value</span></span>

<span data-ttu-id="34df9-111">Restituisce il puntatore [**\_ pInputPin CBaseRenderer:: m**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="34df9-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="34df9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="34df9-112">Remarks</span></span>

<span data-ttu-id="34df9-113">Questo metodo implementa il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , che è virtuale puro nella classe **CBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="34df9-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="34df9-114">Il filtro supporta esattamente un pin (il pin di input).</span><span class="sxs-lookup"><span data-stu-id="34df9-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="34df9-115">La prima volta che questo metodo viene chiamato, crea il PIN come nuovo oggetto [**CRendererInputPin**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="34df9-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="34df9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34df9-116">Requirements</span></span>



| <span data-ttu-id="34df9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34df9-117">Requirement</span></span> | <span data-ttu-id="34df9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="34df9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34df9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34df9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="34df9-120"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34df9-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34df9-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="34df9-121">Library</span></span><br/> | <dl> <span data-ttu-id="34df9-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34df9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34df9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34df9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34df9-124">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="34df9-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




