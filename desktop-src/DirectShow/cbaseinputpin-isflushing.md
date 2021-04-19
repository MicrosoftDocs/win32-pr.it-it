---
description: Il metodo di svuotamento esegue una query per determinare se il filtro sta attualmente scaricando.
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: Metodo CBaseInputPin. IsValid (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5af91e78d10f480596b8e0820ee6de4c4df2998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326061"
---
# <a name="cbaseinputpinisflushing-method"></a><span data-ttu-id="04520-103">Metodo CBaseInputPin. di scaricamento</span><span class="sxs-lookup"><span data-stu-id="04520-103">CBaseInputPin.IsFlushing method</span></span>

<span data-ttu-id="04520-104">Il `IsFlushing` metodo esegue una query per determinare se il filtro sta attualmente scaricando.</span><span class="sxs-lookup"><span data-stu-id="04520-104">The `IsFlushing` method queries whether the filter is currently flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="04520-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04520-105">Syntax</span></span>


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a><span data-ttu-id="04520-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04520-106">Parameters</span></span>

<span data-ttu-id="04520-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="04520-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04520-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04520-108">Return value</span></span>

<span data-ttu-id="04520-109">Restituisce la variabile membro [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md) .</span><span class="sxs-lookup"><span data-stu-id="04520-109">Returns the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="04520-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04520-110">Requirements</span></span>



| <span data-ttu-id="04520-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="04520-111">Requirement</span></span> | <span data-ttu-id="04520-112">Valore</span><span class="sxs-lookup"><span data-stu-id="04520-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04520-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04520-113">Header</span></span><br/>  | <dl> <span data-ttu-id="04520-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04520-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04520-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="04520-115">Library</span></span><br/> | <dl> <span data-ttu-id="04520-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="04520-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04520-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04520-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04520-118">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="04520-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




