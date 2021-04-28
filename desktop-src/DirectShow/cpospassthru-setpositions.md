---
description: 'Metodo CPosPassThru.SetPositions: il metodo SetPositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking::SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Metodo CPosPassThru.SetPositions (Ctlutil.h)
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
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085479"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="153c5-104">Metodo CPosPassThru.SetPositions</span><span class="sxs-lookup"><span data-stu-id="153c5-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="153c5-105">Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="153c5-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="153c5-106">Questo metodo implementa il [**metodo IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="153c5-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="153c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="153c5-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="153c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="153c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153c5-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="153c5-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="153c5-110">Puntatore a una variabile che specifica la posizione corrente, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="153c5-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="153c5-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="153c5-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="153c5-112">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="153c5-112">Bitwise combination of flags.</span></span> <span data-ttu-id="153c5-113">Per [**altre informazioni, vedere IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="153c5-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="153c5-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="153c5-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="153c5-115">Puntatore a una variabile che specifica l'ora di arresto, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="153c5-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="153c5-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="153c5-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="153c5-117">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="153c5-117">Bitwise combination of flags.</span></span> <span data-ttu-id="153c5-118">Per [**altre informazioni, vedere IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="153c5-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153c5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="153c5-119">Return value</span></span>

<span data-ttu-id="153c5-120">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="153c5-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="153c5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="153c5-121">Requirements</span></span>



| <span data-ttu-id="153c5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="153c5-122">Requirement</span></span> | <span data-ttu-id="153c5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="153c5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153c5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="153c5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="153c5-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="153c5-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="153c5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="153c5-126">Library</span></span><br/> | <dl> <span data-ttu-id="153c5-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="153c5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153c5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="153c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153c5-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="153c5-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




