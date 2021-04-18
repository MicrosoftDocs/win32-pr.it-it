---
description: Metodo del costruttore. Il costruttore ottiene l'accesso al pin specificato.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Costruttore CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331818"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="0791d-104">Costruttore CAutoUsingOutputPin. CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="0791d-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="0791d-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0791d-105">Constructor method.</span></span> <span data-ttu-id="0791d-106">Il costruttore ottiene l'accesso al pin specificato.</span><span class="sxs-lookup"><span data-stu-id="0791d-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0791d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0791d-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0791d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0791d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0791d-109">*pOutputPin*</span><span class="sxs-lookup"><span data-stu-id="0791d-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0791d-110">Puntatore a un oggetto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="0791d-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0791d-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="0791d-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0791d-112">Puntatore a una variabile che contiene un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0791d-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="0791d-113">Il valore deve essere S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0791d-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0791d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0791d-114">Remarks</span></span>

<span data-ttu-id="0791d-115">Quando il metodo restituisce, il valore di *\* PHR* indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="0791d-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0791d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0791d-116">Requirements</span></span>



| <span data-ttu-id="0791d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0791d-117">Requirement</span></span> | <span data-ttu-id="0791d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0791d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0791d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0791d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0791d-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0791d-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0791d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="0791d-121">Library</span></span><br/> | <dl> <span data-ttu-id="0791d-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0791d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0791d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0791d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0791d-124">**Classe CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0791d-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




