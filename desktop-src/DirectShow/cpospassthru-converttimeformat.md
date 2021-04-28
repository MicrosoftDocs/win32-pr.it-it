---
description: 'Metodo CPosPassThru.ConvertTimeFormat: il metodo ConvertTimeFormat esegue la conversione da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking::ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Metodo CPosPassThru.ConvertTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098959"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="a1a16-104">Metodo CPosPassThru.ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a1a16-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="a1a16-105">Il `ConvertTimeFormat` metodo esegue la conversione da un formato di ora a un altro.</span><span class="sxs-lookup"><span data-stu-id="a1a16-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="a1a16-106">Questo metodo implementa il [**metodo IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)</span><span class="sxs-lookup"><span data-stu-id="a1a16-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a16-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1a16-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a1a16-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1a16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a16-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="a1a16-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="a1a16-110">Puntatore a una variabile che riceve l'ora convertita.</span><span class="sxs-lookup"><span data-stu-id="a1a16-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="a1a16-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="a1a16-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a1a16-112">Puntatore al GUID del formato dell'ora del formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1a16-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="a1a16-113">Se **NULL,** viene usato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="a1a16-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="a1a16-114">*Origine*</span><span class="sxs-lookup"><span data-stu-id="a1a16-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="a1a16-115">Valore dell'ora da convertire.</span><span class="sxs-lookup"><span data-stu-id="a1a16-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="a1a16-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="a1a16-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a1a16-117">Puntatore al GUID del formato dell'ora del formato da convertire.</span><span class="sxs-lookup"><span data-stu-id="a1a16-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="a1a16-118">Se **NULL,** viene usato il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="a1a16-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a16-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1a16-119">Return value</span></span>

<span data-ttu-id="a1a16-120">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="a1a16-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a16-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1a16-121">Requirements</span></span>



| <span data-ttu-id="a1a16-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a16-122">Requirement</span></span> | <span data-ttu-id="a1a16-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a1a16-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a16-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1a16-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a16-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1a16-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a1a16-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1a16-126">Library</span></span><br/> | <dl> <span data-ttu-id="a1a16-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a1a16-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1a16-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1a16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a16-129">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="a1a16-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="a1a16-130">**GUID di formato ora**</span><span class="sxs-lookup"><span data-stu-id="a1a16-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




