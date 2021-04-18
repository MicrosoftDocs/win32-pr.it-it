---
description: "Il metodo GetSrcAtTime2 recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a IAMTimelineTrack:: GetSrcAtTime, ma accetta un valore REFTIME."
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Metodo IAMTimelineTrack:: GetSrcAtTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325632"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="e2d39-104">Metodo IAMTimelineTrack:: GetSrcAtTime2</span><span class="sxs-lookup"><span data-stu-id="e2d39-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="e2d39-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e2d39-105">\[Deprecated.</span></span> <span data-ttu-id="e2d39-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2d39-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e2d39-107">Il `GetSrcAtTime2` metodo recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.</span><span class="sxs-lookup"><span data-stu-id="e2d39-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="e2d39-108">Questo metodo è equivalente a [**IAMTimelineTrack:: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e2d39-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d39-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2d39-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="e2d39-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2d39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d39-111">*ppSrc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e2d39-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d39-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="e2d39-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="e2d39-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="e2d39-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d39-114">Ora di inizio della ricerca, in secondi.</span><span class="sxs-lookup"><span data-stu-id="e2d39-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="e2d39-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="e2d39-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="e2d39-116">Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e2d39-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d39-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2d39-117">Return value</span></span>

<span data-ttu-id="e2d39-118">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e2d39-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e2d39-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e2d39-119">Return code</span></span>                                                                                  | <span data-ttu-id="e2d39-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2d39-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="e2d39-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="e2d39-122">Impossibile trovare un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="e2d39-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="e2d39-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e2d39-124">Si trova un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="e2d39-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="e2d39-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e2d39-126">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="e2d39-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="e2d39-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e2d39-128">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="e2d39-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e2d39-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2d39-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2d39-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e2d39-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2d39-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2d39-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2d39-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e2d39-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2d39-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2d39-133">Requirements</span></span>



| <span data-ttu-id="e2d39-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d39-134">Requirement</span></span> | <span data-ttu-id="e2d39-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e2d39-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d39-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2d39-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e2d39-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e2d39-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2d39-138">Library</span></span><br/> | <dl> <span data-ttu-id="e2d39-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2d39-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d39-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2d39-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d39-141">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="e2d39-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="e2d39-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e2d39-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




