---
description: Il metodo SetSampleSize specifica una dimensione del campione fissa o specifica che i campioni hanno una dimensione variabile.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Metodo CMediaType. SetSampleSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328505"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="c993b-103">CMediaType. SetSampleSize, metodo</span><span class="sxs-lookup"><span data-stu-id="c993b-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="c993b-104">Il `SetSampleSize` metodo specifica una dimensione del campione fissa o specifica che i campioni hanno una dimensione variabile.</span><span class="sxs-lookup"><span data-stu-id="c993b-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="c993b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c993b-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="c993b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c993b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c993b-107">*SZ*</span><span class="sxs-lookup"><span data-stu-id="c993b-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="c993b-108">Dimensioni campione, in byte o zero.</span><span class="sxs-lookup"><span data-stu-id="c993b-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c993b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c993b-109">Return value</span></span>

<span data-ttu-id="c993b-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c993b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c993b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c993b-111">Remarks</span></span>

<span data-ttu-id="c993b-112">Se il valore di *SZ* è zero, il tipo di supporto utilizza dimensioni campione variabili.</span><span class="sxs-lookup"><span data-stu-id="c993b-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="c993b-113">In caso contrario, le dimensioni del campione vengono fissate a *SZ* bytes.</span><span class="sxs-lookup"><span data-stu-id="c993b-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c993b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c993b-114">Requirements</span></span>



| <span data-ttu-id="c993b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c993b-115">Requirement</span></span> | <span data-ttu-id="c993b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c993b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c993b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c993b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c993b-118"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c993b-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c993b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c993b-119">Library</span></span><br/> | <dl> <span data-ttu-id="c993b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c993b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c993b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c993b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c993b-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c993b-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




