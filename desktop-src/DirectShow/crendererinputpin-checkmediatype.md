---
description: "Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico. Questo metodo esegue l'override del Metodo CBasePin:: CheckMediaType."
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Metodo CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328629"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="3adab-104">CRendererInputPin. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="3adab-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="3adab-105">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="3adab-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="3adab-106">Questo metodo esegue l'override del metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3adab-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3adab-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="3adab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3adab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adab-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="3adab-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3adab-110">Puntatore a un oggetto del tipo di supporto che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="3adab-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3adab-111">Return value</span></span>

<span data-ttu-id="3adab-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3adab-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3adab-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3adab-113">Requirements</span></span>



| <span data-ttu-id="3adab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3adab-114">Requirement</span></span> | <span data-ttu-id="3adab-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3adab-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adab-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3adab-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3adab-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3adab-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3adab-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3adab-118">Library</span></span><br/> | <dl> <span data-ttu-id="3adab-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3adab-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adab-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3adab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adab-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="3adab-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




