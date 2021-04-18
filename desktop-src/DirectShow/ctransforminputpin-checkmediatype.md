---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Metodo CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328812"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="874c4-103">CTransformInputPin. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="874c4-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="874c4-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="874c4-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="874c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="874c4-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="874c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="874c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="874c4-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="874c4-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="874c4-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="874c4-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="874c4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="874c4-109">Return value</span></span>

<span data-ttu-id="874c4-110">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="874c4-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="874c4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="874c4-111">Remarks</span></span>

<span data-ttu-id="874c4-112">Questo metodo implementa il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="874c4-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="874c4-113">Chiama il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro, che è anche virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="874c4-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="874c4-114">La classe derivata del filtro deve implementare **CheckInputType** per determinare se un determinato tipo di input è accettabile.</span><span class="sxs-lookup"><span data-stu-id="874c4-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="874c4-115">Se il pin di output del filtro è connesso, questo metodo chiama anche il metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) del filtro per determinare se il tipo di input è compatibile con il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="874c4-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="874c4-116">Anche il metodo **CheckTransform** è virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="874c4-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="874c4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="874c4-117">Requirements</span></span>



| <span data-ttu-id="874c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="874c4-118">Requirement</span></span> | <span data-ttu-id="874c4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="874c4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="874c4-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="874c4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="874c4-121"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="874c4-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="874c4-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="874c4-122">Library</span></span><br/> | <dl> <span data-ttu-id="874c4-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="874c4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




