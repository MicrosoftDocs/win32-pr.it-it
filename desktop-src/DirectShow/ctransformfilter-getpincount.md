---
description: Il metodo GetPinCount Recupera il numero di pin sul filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Metodo CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331151"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="0dd53-103">CTransformFilter. GetPinCount, metodo</span><span class="sxs-lookup"><span data-stu-id="0dd53-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="0dd53-104">Il `GetPinCount` metodo recupera il numero di pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="0dd53-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dd53-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="0dd53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dd53-106">Parameters</span></span>

<span data-ttu-id="0dd53-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0dd53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dd53-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dd53-108">Return value</span></span>

<span data-ttu-id="0dd53-109">Restituisce 2.</span><span class="sxs-lookup"><span data-stu-id="0dd53-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dd53-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dd53-110">Remarks</span></span>

<span data-ttu-id="0dd53-111">Questo metodo esegue l'override del metodo [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd53-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="0dd53-112">La classe **CTransformFilter** supporta esattamente un pin di input e un pin di output.</span><span class="sxs-lookup"><span data-stu-id="0dd53-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd53-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd53-113">Requirements</span></span>



| <span data-ttu-id="0dd53-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd53-114">Requirement</span></span> | <span data-ttu-id="0dd53-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd53-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd53-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dd53-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0dd53-117"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dd53-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0dd53-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="0dd53-118">Library</span></span><br/> | <dl> <span data-ttu-id="0dd53-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0dd53-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd53-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd53-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd53-121">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="0dd53-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




