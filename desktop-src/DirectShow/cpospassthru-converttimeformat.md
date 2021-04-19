---
description: 'Il metodo ConvertTimeFormat converte da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Metodo CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329517"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="34e3b-104">CPosPassThru. ConvertTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="34e3b-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="34e3b-105">Il `ConvertTimeFormat` metodo converte da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="34e3b-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="34e3b-106">Questo metodo implementa il metodo [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="34e3b-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34e3b-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="34e3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="34e3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e3b-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="34e3b-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="34e3b-110">Puntatore a una variabile che riceve l'ora convertita.</span><span class="sxs-lookup"><span data-stu-id="34e3b-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="34e3b-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="34e3b-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="34e3b-112">Puntatore al GUID del formato dell'ora del formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="34e3b-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="34e3b-113">Se è **null**, viene utilizzato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="34e3b-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="34e3b-114">*Origine*</span><span class="sxs-lookup"><span data-stu-id="34e3b-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="34e3b-115">Valore dell'ora da convertire.</span><span class="sxs-lookup"><span data-stu-id="34e3b-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="34e3b-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="34e3b-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="34e3b-117">Puntatore al GUID del formato dell'ora del formato da convertire.</span><span class="sxs-lookup"><span data-stu-id="34e3b-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="34e3b-118">Se è **null**, viene utilizzato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="34e3b-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e3b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34e3b-119">Return value</span></span>

<span data-ttu-id="34e3b-120">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="34e3b-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e3b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34e3b-121">Requirements</span></span>



| <span data-ttu-id="34e3b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e3b-122">Requirement</span></span> | <span data-ttu-id="34e3b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="34e3b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e3b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34e3b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="34e3b-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34e3b-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34e3b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="34e3b-126">Library</span></span><br/> | <dl> <span data-ttu-id="34e3b-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34e3b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e3b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34e3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e3b-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="34e3b-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="34e3b-130">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="34e3b-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




