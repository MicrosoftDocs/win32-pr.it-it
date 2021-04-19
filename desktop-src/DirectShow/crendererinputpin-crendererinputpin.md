---
description: Il metodo CRendererInputPin è un metodo del costruttore.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Costruttore CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333188"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="e2aa5-103">Costruttore CRendererInputPin. CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="e2aa5-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="e2aa5-104">Il `CRendererInputPin` metodo è un metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e2aa5-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2aa5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2aa5-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="e2aa5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2aa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2aa5-107">*pRenderer*</span><span class="sxs-lookup"><span data-stu-id="e2aa5-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="e2aa5-108">Puntatore all'oggetto [**CBaseRenderer**](cbaserenderer.md) che implementa il filtro.</span><span class="sxs-lookup"><span data-stu-id="e2aa5-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="e2aa5-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="e2aa5-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e2aa5-110">Puntatore a una variabile che riceve un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2aa5-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="e2aa5-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="e2aa5-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e2aa5-112">Puntatore a una stringa di caratteri wide contenente l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="e2aa5-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2aa5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2aa5-113">Requirements</span></span>



| <span data-ttu-id="e2aa5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2aa5-114">Requirement</span></span> | <span data-ttu-id="e2aa5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e2aa5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2aa5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2aa5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e2aa5-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2aa5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2aa5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2aa5-118">Library</span></span><br/> | <dl> <span data-ttu-id="e2aa5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e2aa5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2aa5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2aa5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2aa5-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="e2aa5-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




