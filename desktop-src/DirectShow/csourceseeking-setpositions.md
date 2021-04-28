---
description: 'Metodo CSourceSeeking.SetPositions: il metodo SetPositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking::SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Metodo CSourceSeeking.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085169"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="39ac1-104">Metodo CSourceSeeking.SetPositions</span><span class="sxs-lookup"><span data-stu-id="39ac1-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="39ac1-105">Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="39ac1-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="39ac1-106">Questo metodo implementa il [**metodo IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)</span><span class="sxs-lookup"><span data-stu-id="39ac1-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ac1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39ac1-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="39ac1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39ac1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ac1-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="39ac1-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="39ac1-110">Puntatore a una variabile che specifica la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="39ac1-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="39ac1-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="39ac1-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="39ac1-112">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="39ac1-112">Bitwise combination of flags.</span></span> <span data-ttu-id="39ac1-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="39ac1-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="39ac1-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="39ac1-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="39ac1-115">Puntatore a una variabile che specifica l'ora di arresto, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="39ac1-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="39ac1-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="39ac1-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="39ac1-117">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="39ac1-117">Bitwise combination of flags.</span></span> <span data-ttu-id="39ac1-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="39ac1-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ac1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39ac1-119">Return value</span></span>

<span data-ttu-id="39ac1-120">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="39ac1-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="39ac1-121">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="39ac1-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="39ac1-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="39ac1-122">Return code</span></span>                                                                                  | <span data-ttu-id="39ac1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39ac1-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="39ac1-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39ac1-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="39ac1-125">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="39ac1-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="39ac1-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="39ac1-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="39ac1-127">Flag non validi</span><span class="sxs-lookup"><span data-stu-id="39ac1-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="39ac1-128"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39ac1-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="39ac1-129">**Argomento puntatore NULL**</span><span class="sxs-lookup"><span data-stu-id="39ac1-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39ac1-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="39ac1-130">Remarks</span></span>

<span data-ttu-id="39ac1-131">Sono supportati i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="39ac1-131">The following flags are supported:</span></span>

-   <span data-ttu-id="39ac1-132">AM \_ SEEKING \_ NoPositioning</span><span class="sxs-lookup"><span data-stu-id="39ac1-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="39ac1-133">AM \_ SEEKING \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="39ac1-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="39ac1-134">AM \_ SEEKING \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="39ac1-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="39ac1-135">AM \_ SEEKING \_ IncrementalPositioning *(solo pStop)*</span><span class="sxs-lookup"><span data-stu-id="39ac1-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="39ac1-136">Per altre informazioni, vedere [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="39ac1-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="39ac1-137">Questo metodo aggiorna i valori delle variabili membro [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) e quindi chiama i metodi virtuali puri [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) e [**CSourceSeeking::ChangeSeeking::ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="39ac1-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39ac1-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39ac1-138">Requirements</span></span>



| <span data-ttu-id="39ac1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ac1-139">Requirement</span></span> | <span data-ttu-id="39ac1-140">Valore</span><span class="sxs-lookup"><span data-stu-id="39ac1-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ac1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39ac1-141">Header</span></span><br/>  | <dl> <span data-ttu-id="39ac1-142"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="39ac1-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39ac1-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="39ac1-143">Library</span></span><br/> | <dl> <span data-ttu-id="39ac1-144"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39ac1-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ac1-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39ac1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ac1-146">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="39ac1-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




