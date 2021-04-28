---
description: 'Metodo CTransformInputPin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Metodo CTransformInputPin.CheckMediaType (Transfrm.h)
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
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084999"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="6ac67-103">Metodo CTransformInputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="6ac67-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="6ac67-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="6ac67-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ac67-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="6ac67-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ac67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac67-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="6ac67-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="6ac67-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="6ac67-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac67-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ac67-109">Return value</span></span>

<span data-ttu-id="6ac67-110">Restituisce S \_ OK o un altro valore **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6ac67-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac67-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ac67-111">Remarks</span></span>

<span data-ttu-id="6ac67-112">Questo metodo implementa il metodo [**CBasePin::CheckMediaType virtuale**](cbasepin-checkmediatype.md) puro.</span><span class="sxs-lookup"><span data-stu-id="6ac67-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="6ac67-113">Chiama il metodo [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro, che è anche virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="6ac67-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="6ac67-114">La classe derivata del filtro deve implementare **CheckInputType** per determinare se un determinato tipo di input è accettabile.</span><span class="sxs-lookup"><span data-stu-id="6ac67-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="6ac67-115">Se il pin di output del filtro è connesso, questo metodo chiama anche il metodo [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) del filtro per determinare se il tipo di input è compatibile con il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="6ac67-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="6ac67-116">Anche **il metodo CheckTransform** è virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="6ac67-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac67-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ac67-117">Requirements</span></span>



| <span data-ttu-id="6ac67-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac67-118">Requirement</span></span> | <span data-ttu-id="6ac67-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6ac67-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac67-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ac67-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac67-121"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ac67-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ac67-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ac67-122">Library</span></span><br/> | <dl> <span data-ttu-id="6ac67-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ac67-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




