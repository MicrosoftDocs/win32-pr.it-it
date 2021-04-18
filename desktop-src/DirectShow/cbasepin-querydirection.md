---
description: 'Il metodo QueryDirection recupera la direzione del PIN (input o output). Questo metodo implementa il metodo IPin:: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Metodo CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328264"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="b0145-104">CBasePin. QueryDirection, metodo</span><span class="sxs-lookup"><span data-stu-id="b0145-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="b0145-105">Il `QueryDirection` metodo recupera la direzione del PIN (input o output).</span><span class="sxs-lookup"><span data-stu-id="b0145-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="b0145-106">Questo metodo implementa il metodo [**Ipin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .</span><span class="sxs-lookup"><span data-stu-id="b0145-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0145-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0145-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="b0145-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0145-109">*pPinDir*</span><span class="sxs-lookup"><span data-stu-id="b0145-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="b0145-110">Puntatore a una variabile che riceve un membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) .</span><span class="sxs-lookup"><span data-stu-id="b0145-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0145-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0145-111">Return value</span></span>

<span data-ttu-id="b0145-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="b0145-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0145-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0145-113">Requirements</span></span>



| <span data-ttu-id="b0145-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0145-114">Requirement</span></span> | <span data-ttu-id="b0145-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b0145-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0145-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0145-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b0145-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0145-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b0145-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0145-118">Library</span></span><br/> | <dl> <span data-ttu-id="b0145-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0145-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0145-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0145-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0145-121">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b0145-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




