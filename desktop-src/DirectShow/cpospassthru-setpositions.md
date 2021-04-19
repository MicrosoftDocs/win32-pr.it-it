---
description: 'Il metodo sepositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: sepositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Metodo CPosPassThru. sepositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333194"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="d16d2-104">Metodo CPosPassThru. sepositions</span><span class="sxs-lookup"><span data-stu-id="d16d2-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="d16d2-105">Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="d16d2-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="d16d2-106">Questo metodo implementa il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="d16d2-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d16d2-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d16d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d16d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16d2-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="d16d2-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="d16d2-110">Puntatore a una variabile che specifica la posizione corrente, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d16d2-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="d16d2-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="d16d2-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="d16d2-112">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="d16d2-112">Bitwise combination of flags.</span></span> <span data-ttu-id="d16d2-113">Per ulteriori informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="d16d2-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="d16d2-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="d16d2-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d16d2-115">Puntatore a una variabile che specifica l'ora di arresto, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d16d2-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="d16d2-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="d16d2-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="d16d2-117">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="d16d2-117">Bitwise combination of flags.</span></span> <span data-ttu-id="d16d2-118">Per ulteriori informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="d16d2-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16d2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d16d2-119">Return value</span></span>

<span data-ttu-id="d16d2-120">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="d16d2-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d16d2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d16d2-121">Requirements</span></span>



| <span data-ttu-id="d16d2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d16d2-122">Requirement</span></span> | <span data-ttu-id="d16d2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d16d2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d16d2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d16d2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d16d2-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d16d2-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d16d2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d16d2-126">Library</span></span><br/> | <dl> <span data-ttu-id="d16d2-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d16d2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d16d2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d16d2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16d2-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="d16d2-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




