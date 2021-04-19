---
description: "Il metodo SetMediaType imposta il tipo di supporto per la connessione. Questo metodo esegue l'override del Metodo CBasePin:: SetMediaType."
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Metodo CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333174"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="c707d-104">CRendererInputPin. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="c707d-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="c707d-105">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="c707d-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="c707d-106">Questo metodo esegue l'override del metodo [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="c707d-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c707d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c707d-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="c707d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c707d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c707d-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="c707d-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c707d-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c707d-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c707d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c707d-111">Return value</span></span>

<span data-ttu-id="c707d-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c707d-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c707d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c707d-113">Requirements</span></span>



| <span data-ttu-id="c707d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c707d-114">Requirement</span></span> | <span data-ttu-id="c707d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c707d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c707d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c707d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c707d-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c707d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c707d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c707d-118">Library</span></span><br/> | <dl> <span data-ttu-id="c707d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c707d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c707d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c707d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c707d-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="c707d-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




