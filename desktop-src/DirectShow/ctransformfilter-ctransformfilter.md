---
description: Metodo del costruttore.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Costruttore CTransformFilter. CTransformFilter (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329148"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="0de95-103">Costruttore CTransformFilter. CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="0de95-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="0de95-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0de95-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de95-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0de95-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="0de95-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0de95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de95-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="0de95-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="0de95-108">Stringa contenente il nome di debug del filtro.</span><span class="sxs-lookup"><span data-stu-id="0de95-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="0de95-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0de95-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de95-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="0de95-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0de95-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0de95-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0de95-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="0de95-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0de95-113">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="0de95-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0de95-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="0de95-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="0de95-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="0de95-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0de95-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0de95-116">Remarks</span></span>

<span data-ttu-id="0de95-117">Il costruttore non crea i pin del filtro.</span><span class="sxs-lookup"><span data-stu-id="0de95-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="0de95-118">Questo errore si verifica durante la prima chiamata al metodo [**GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="0de95-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="0de95-119">Il costruttore inizializza le variabili membro [**\_ Pinput**](ctransformfilter-m-pinput.md) e [**m \_ pOutput**](ctransformfilter-m-poutput.md) su **null**.</span><span class="sxs-lookup"><span data-stu-id="0de95-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de95-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0de95-120">Requirements</span></span>



| <span data-ttu-id="0de95-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0de95-121">Requirement</span></span> | <span data-ttu-id="0de95-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0de95-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de95-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0de95-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0de95-124"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0de95-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0de95-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0de95-125">Library</span></span><br/> | <dl> <span data-ttu-id="0de95-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0de95-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0de95-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0de95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de95-128">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="0de95-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




