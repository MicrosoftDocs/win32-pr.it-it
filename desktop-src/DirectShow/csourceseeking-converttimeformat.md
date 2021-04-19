---
description: 'Il metodo ConvertTimeFormat converte da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Metodo CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
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
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325660"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="9b583-104">CSourceSeeking. ConvertTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="9b583-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="9b583-105">Il `ConvertTimeFormat` metodo converte da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="9b583-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="9b583-106">Questo metodo implementa il metodo [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="9b583-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b583-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b583-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="9b583-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b583-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b583-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="9b583-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="9b583-110">Puntatore a una variabile che riceve l'ora convertita.</span><span class="sxs-lookup"><span data-stu-id="9b583-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="9b583-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="9b583-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9b583-112">Puntatore al GUID del formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b583-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="9b583-113">Se è **null**, viene utilizzato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="9b583-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="9b583-114">Vedere [**GUID del formato ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9b583-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b583-115">*Origine*</span><span class="sxs-lookup"><span data-stu-id="9b583-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="9b583-116">Valore dell'ora da convertire.</span><span class="sxs-lookup"><span data-stu-id="9b583-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="9b583-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="9b583-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9b583-118">Puntatore al GUID del formato dell'ora del formato da convertire.</span><span class="sxs-lookup"><span data-stu-id="9b583-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="9b583-119">Se è **null**, viene utilizzato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="9b583-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b583-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b583-120">Return value</span></span>

<span data-ttu-id="9b583-121">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9b583-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="9b583-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9b583-122">Return code</span></span>                                                                                  | <span data-ttu-id="9b583-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b583-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="9b583-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b583-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9b583-125">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="9b583-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="9b583-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9b583-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9b583-127">Argomento non valido</span><span class="sxs-lookup"><span data-stu-id="9b583-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="9b583-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9b583-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="9b583-129">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="9b583-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9b583-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b583-130">Remarks</span></span>

<span data-ttu-id="9b583-131">L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="9b583-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="9b583-132">Questo metodo restituisce E \_ INVALIDARG, eccetto nel caso più semplice in cui *PTargetFormat* e *pSourceFormat* specificano il tempo di supporto del \_ formato ora \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9b583-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b583-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b583-133">Requirements</span></span>



| <span data-ttu-id="9b583-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b583-134">Requirement</span></span> | <span data-ttu-id="9b583-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9b583-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b583-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b583-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9b583-137"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b583-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b583-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b583-138">Library</span></span><br/> | <dl> <span data-ttu-id="9b583-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9b583-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b583-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b583-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b583-141">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="9b583-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




