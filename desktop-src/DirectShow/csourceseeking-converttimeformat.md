---
description: 'Metodo CSourceSeeking.ConvertTimeFormat: il metodo ConvertTimeFormat esegue la conversione da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking::ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Metodo CSourceSeeking.ConvertTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085249"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="6581e-104">Metodo CSourceSeeking.ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6581e-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="6581e-105">Il `ConvertTimeFormat` metodo converte da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="6581e-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="6581e-106">Questo metodo implementa il [**metodo IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)</span><span class="sxs-lookup"><span data-stu-id="6581e-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6581e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6581e-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="6581e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6581e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6581e-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="6581e-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="6581e-110">Puntatore a una variabile che riceve l'ora convertita.</span><span class="sxs-lookup"><span data-stu-id="6581e-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="6581e-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="6581e-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6581e-112">Puntatore al GUID del formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6581e-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="6581e-113">Se **NULL,** viene usato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="6581e-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="6581e-114">Vedere [**GUID di formato dell'ora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="6581e-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="6581e-115">*Origine*</span><span class="sxs-lookup"><span data-stu-id="6581e-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="6581e-116">Valore dell'ora da convertire.</span><span class="sxs-lookup"><span data-stu-id="6581e-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="6581e-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="6581e-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6581e-118">Puntatore al GUID del formato dell'ora del formato da convertire.</span><span class="sxs-lookup"><span data-stu-id="6581e-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="6581e-119">Se **NULL,** viene usato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="6581e-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6581e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6581e-120">Return value</span></span>

<span data-ttu-id="6581e-121">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6581e-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="6581e-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6581e-122">Return code</span></span>                                                                                  | <span data-ttu-id="6581e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6581e-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="6581e-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6581e-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6581e-125">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="6581e-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="6581e-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6581e-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6581e-127">Argomento non valido</span><span class="sxs-lookup"><span data-stu-id="6581e-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="6581e-128"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="6581e-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="6581e-129">**Argomento puntatore NULL**</span><span class="sxs-lookup"><span data-stu-id="6581e-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6581e-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="6581e-130">Remarks</span></span>

<span data-ttu-id="6581e-131">L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità da 100 nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="6581e-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="6581e-132">Questo metodo restituisce E INVALIDARG, ad eccezione del caso semplice in cui \_ *pTargetFormat* e *pSourceFormat* specificano entrambi TIME \_ FORMAT MEDIA \_ \_ TIME.</span><span class="sxs-lookup"><span data-stu-id="6581e-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="6581e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6581e-133">Requirements</span></span>



| <span data-ttu-id="6581e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6581e-134">Requirement</span></span> | <span data-ttu-id="6581e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6581e-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6581e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6581e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6581e-137"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6581e-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6581e-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="6581e-138">Library</span></span><br/> | <dl> <span data-ttu-id="6581e-139"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6581e-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6581e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6581e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6581e-141">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="6581e-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




