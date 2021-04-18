---
description: 'Il metodo ZeroBetween2 rimuove tutti gli elementi dalla traccia tra le ore specificate. Questo metodo è equivalente a IAMTimelineTrack:: ZeroBetween, ma accetta valori REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Metodo IAMTimelineTrack:: ZeroBetween2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325615"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="270a5-104">Metodo IAMTimelineTrack:: ZeroBetween2</span><span class="sxs-lookup"><span data-stu-id="270a5-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="270a5-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="270a5-105">\[Deprecated.</span></span> <span data-ttu-id="270a5-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="270a5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="270a5-107">Il `ZeroBetween2` metodo rimuove tutti gli elementi dalla traccia tra le ore specificate.</span><span class="sxs-lookup"><span data-stu-id="270a5-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="270a5-108">Questo metodo è equivalente a [**IAMTimelineTrack:: ZeroBetween**](iamtimelinetrack-zerobetween.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="270a5-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="270a5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="270a5-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="270a5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="270a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="270a5-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="270a5-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="270a5-112">Inizio dell'intervallo da cancellare, in secondi.</span><span class="sxs-lookup"><span data-stu-id="270a5-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="270a5-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="270a5-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="270a5-114">Fine dell'intervallo da cancellare, in secondi.</span><span class="sxs-lookup"><span data-stu-id="270a5-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="270a5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="270a5-115">Return value</span></span>

<span data-ttu-id="270a5-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="270a5-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="270a5-117">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="270a5-117">Possible values include the following.</span></span>



| <span data-ttu-id="270a5-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="270a5-118">Return code</span></span>                                                                             | <span data-ttu-id="270a5-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="270a5-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="270a5-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="270a5-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="270a5-121">L'intervallo di tempo va oltre tutti gli elementi nella traccia.</span><span class="sxs-lookup"><span data-stu-id="270a5-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="270a5-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="270a5-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="270a5-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="270a5-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="270a5-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="270a5-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="270a5-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="270a5-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="270a5-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="270a5-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="270a5-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="270a5-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="270a5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="270a5-128">Requirements</span></span>



| <span data-ttu-id="270a5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="270a5-129">Requirement</span></span> | <span data-ttu-id="270a5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="270a5-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="270a5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="270a5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="270a5-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="270a5-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="270a5-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="270a5-133">Library</span></span><br/> | <dl> <span data-ttu-id="270a5-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="270a5-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="270a5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="270a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270a5-136">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="270a5-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="270a5-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="270a5-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




