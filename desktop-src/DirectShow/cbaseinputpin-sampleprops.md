---
description: Il metodo SampleProps recupera le proprietà dell'esempio più recente, in una struttura di \_ \_ Proprietà SAMPLE2.
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Metodo CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333211"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="3a8d0-103">CBaseInputPin. SampleProps, metodo</span><span class="sxs-lookup"><span data-stu-id="3a8d0-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="3a8d0-104">Il `SampleProps` metodo recupera le proprietà dell'esempio più recente, in una struttura [**di \_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="3a8d0-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a8d0-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="3a8d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a8d0-106">Parameters</span></span>

<span data-ttu-id="3a8d0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3a8d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a8d0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a8d0-108">Return value</span></span>

<span data-ttu-id="3a8d0-109">Restituisce l'indirizzo della variabile membro [**CBaseInputPin:: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3a8d0-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8d0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a8d0-110">Requirements</span></span>



| <span data-ttu-id="3a8d0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a8d0-111">Requirement</span></span> | <span data-ttu-id="3a8d0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3a8d0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8d0-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a8d0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3a8d0-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a8d0-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3a8d0-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a8d0-115">Library</span></span><br/> | <dl> <span data-ttu-id="3a8d0-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a8d0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a8d0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a8d0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8d0-118">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="3a8d0-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




