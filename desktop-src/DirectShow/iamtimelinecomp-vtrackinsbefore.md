---
description: Il metodo VTrackInsBefore inserisce una traccia virtuale nella composizione con la priorità specificata.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Metodo IAMTimelineComp:: VTrackInsBefore (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332034"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="57832-103">Metodo IAMTimelineComp:: VTrackInsBefore</span><span class="sxs-lookup"><span data-stu-id="57832-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="57832-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="57832-104">\[Deprecated.</span></span> <span data-ttu-id="57832-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57832-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="57832-106">Il `VTrackInsBefore` metodo inserisce una traccia virtuale nella composizione con la priorità specificata.</span><span class="sxs-lookup"><span data-stu-id="57832-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="57832-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57832-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="57832-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57832-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="57832-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="57832-110">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale.</span><span class="sxs-lookup"><span data-stu-id="57832-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="57832-111">*Priorità*</span><span class="sxs-lookup"><span data-stu-id="57832-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="57832-112">Priorità con cui inserire la traccia virtuale oppure-1 per inserire la traccia virtuale alla fine dell'elenco di priorità.</span><span class="sxs-lookup"><span data-stu-id="57832-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="57832-113">L'elenco di priorità determina quali clip sono visibili.</span><span class="sxs-lookup"><span data-stu-id="57832-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="57832-114">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="57832-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57832-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57832-115">Return value</span></span>

<span data-ttu-id="57832-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="57832-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="57832-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="57832-117">Return code</span></span>                                                                                   | <span data-ttu-id="57832-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57832-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="57832-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57832-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="57832-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="57832-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="57832-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="57832-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="57832-122">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="57832-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="57832-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="57832-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="57832-124">L'oggetto non è una traccia virtuale.</span><span class="sxs-lookup"><span data-stu-id="57832-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57832-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="57832-125">Remarks</span></span>

<span data-ttu-id="57832-126">Ogni traccia virtuale nella composizione ha un livello di priorità univoco.</span><span class="sxs-lookup"><span data-stu-id="57832-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="57832-127">I livelli di priorità sono compresi tra 0 e *n* -1, dove *n* è il numero di tracce virtuali nella composizione.</span><span class="sxs-lookup"><span data-stu-id="57832-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="57832-128">Per i gruppi video, un track virtuale nasconde qualsiasi traccia virtuale con un livello di priorità inferiore, tranne nei punti in cui la traccia è vuota o contiene una transizione.</span><span class="sxs-lookup"><span data-stu-id="57832-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="57832-129">È possibile considerare le tracce virtuali come livelli nella composizione finale.</span><span class="sxs-lookup"><span data-stu-id="57832-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="57832-130">Track 1 viene sovrapposto all'inizio della traccia 0, Track 2 è sovrapposto a Track 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="57832-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="57832-131">Se si specifica-1 per il parametro *Priority* , la traccia virtuale viene inserita alla fine dell'elenco, con un valore di priorità più alto rispetto alle tracce esistenti.</span><span class="sxs-lookup"><span data-stu-id="57832-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="57832-132">Se si specifica un valore di priorità già esistente nella composizione, ogni traccia con una priorità uguale o maggiore viene spostata verso l'alto di un livello di priorità.</span><span class="sxs-lookup"><span data-stu-id="57832-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="57832-133">**Esempio**: Track A ha priorità 0 e Track B ha priorità 1.</span><span class="sxs-lookup"><span data-stu-id="57832-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="57832-134">Se la traccia C viene inserita con priorità 0, tenere traccia di uno spostamento alla priorità 1, mentre Track B passa alla priorità 2.</span><span class="sxs-lookup"><span data-stu-id="57832-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="57832-135">Se la priorità specificata è maggiore del numero corrente di tracce nella composizione, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="57832-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="57832-136">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="57832-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="57832-137">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="57832-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="57832-138">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="57832-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57832-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57832-139">Requirements</span></span>



| <span data-ttu-id="57832-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="57832-140">Requirement</span></span> | <span data-ttu-id="57832-141">Valore</span><span class="sxs-lookup"><span data-stu-id="57832-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57832-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57832-142">Header</span></span><br/>  | <dl> <span data-ttu-id="57832-143"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57832-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="57832-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="57832-144">Library</span></span><br/> | <dl> <span data-ttu-id="57832-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57832-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57832-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57832-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57832-147">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="57832-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="57832-148">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="57832-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




