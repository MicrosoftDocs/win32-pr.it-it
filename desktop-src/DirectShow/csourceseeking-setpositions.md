---
description: 'Il metodo sepositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: sepositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Metodo CSourceSeeking. sepositions (Ctlutil. h)
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328486"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="b528a-104">Metodo CSourceSeeking. sepositions</span><span class="sxs-lookup"><span data-stu-id="b528a-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="b528a-105">Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="b528a-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="b528a-106">Questo metodo implementa il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="b528a-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b528a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b528a-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b528a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b528a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b528a-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="b528a-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="b528a-110">Puntatore a una variabile che specifica la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b528a-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="b528a-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="b528a-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b528a-112">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="b528a-112">Bitwise combination of flags.</span></span> <span data-ttu-id="b528a-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b528a-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b528a-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="b528a-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="b528a-115">Puntatore a una variabile che specifica l'ora di arresto, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="b528a-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="b528a-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="b528a-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b528a-117">Combinazione bit per bit di flag.</span><span class="sxs-lookup"><span data-stu-id="b528a-117">Bitwise combination of flags.</span></span> <span data-ttu-id="b528a-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b528a-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b528a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b528a-119">Return value</span></span>

<span data-ttu-id="b528a-120">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b528a-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b528a-121">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b528a-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b528a-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b528a-122">Return code</span></span>                                                                                  | <span data-ttu-id="b528a-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b528a-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b528a-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b528a-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b528a-125">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="b528a-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="b528a-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b528a-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b528a-127">Flag non validi</span><span class="sxs-lookup"><span data-stu-id="b528a-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="b528a-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b528a-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="b528a-129">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="b528a-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b528a-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b528a-130">Remarks</span></span>

<span data-ttu-id="b528a-131">Sono supportati i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="b528a-131">The following flags are supported:</span></span>

-   <span data-ttu-id="b528a-132">\_Ricerca di \_ nopositioning</span><span class="sxs-lookup"><span data-stu-id="b528a-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="b528a-133">\_Ricerca di \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="b528a-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="b528a-134">\_Ricerca di \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="b528a-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="b528a-135">\_Cerco \_ IncrementalPositioning (solo *pStop* )</span><span class="sxs-lookup"><span data-stu-id="b528a-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="b528a-136">Per altre informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="b528a-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="b528a-137">Questo metodo aggiorna i valori delle variabili [**membro CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) , quindi chiama i metodi virtuali puri [**CSourceSeeking:: iniziale**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="b528a-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b528a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b528a-138">Requirements</span></span>



| <span data-ttu-id="b528a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b528a-139">Requirement</span></span> | <span data-ttu-id="b528a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b528a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b528a-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b528a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b528a-142"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b528a-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b528a-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="b528a-143">Library</span></span><br/> | <dl> <span data-ttu-id="b528a-144"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b528a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b528a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b528a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b528a-146">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b528a-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




