---
description: Il metodo SetStartStop imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Metodo IAMTimelineObj:: SetStartStop (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330809"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="04d8f-103">Metodo IAMTimelineObj:: SetStartStop</span><span class="sxs-lookup"><span data-stu-id="04d8f-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="04d8f-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04d8f-104">\[Deprecated.</span></span> <span data-ttu-id="04d8f-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04d8f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04d8f-106">Il `SetStartStop` metodo imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="04d8f-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d8f-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="04d8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04d8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d8f-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="04d8f-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="04d8f-110">Nuova ora di inizio, in unità 100-nanosecondi, oppure-1 per la conservazione dell'ora di inizio esistente.</span><span class="sxs-lookup"><span data-stu-id="04d8f-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="04d8f-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="04d8f-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="04d8f-112">Nuova ora di arresto, in unità 100-nanosecondi, oppure-1 per la conservazione dell'ora di arresto esistente.</span><span class="sxs-lookup"><span data-stu-id="04d8f-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d8f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04d8f-113">Return value</span></span>

<span data-ttu-id="04d8f-114">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="04d8f-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="04d8f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="04d8f-115">Return code</span></span>                                                                                  | <span data-ttu-id="04d8f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04d8f-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="04d8f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04d8f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="04d8f-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="04d8f-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="04d8f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="04d8f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="04d8f-120">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="04d8f-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="04d8f-121"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="04d8f-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="04d8f-122">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="04d8f-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="04d8f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="04d8f-123">Remarks</span></span>

<span data-ttu-id="04d8f-124">Tracce, composizioni e gruppi non implementano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="04d8f-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="04d8f-125">Per questi oggetti, l'ora di inizio è sempre zero e l'ora di arresto è l'ora di arresto massima degli oggetti in essi contenuti.</span><span class="sxs-lookup"><span data-stu-id="04d8f-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="04d8f-126">Non impostare orari sovrapposti negli oggetti di origine all'interno della stessa traccia. Questa operazione può causare comportamenti indefiniti.</span><span class="sxs-lookup"><span data-stu-id="04d8f-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="04d8f-127">Per gli oggetti di origine, le ore di inizio e di fine sono indipendenti dagli orari di inizio e di fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="04d8f-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="04d8f-128">La modifica di una coppia di valori non comporta la modifica dell'altro.</span><span class="sxs-lookup"><span data-stu-id="04d8f-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="04d8f-129">Per impostare l'ora di inizio e di fine del supporto, chiamare il metodo [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="04d8f-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="04d8f-130">Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="04d8f-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="04d8f-131">Per ottenere le transizioni e i tagli accurati dei frame, impostare i parametri *Start* e *Stop* sui limiti del frame.</span><span class="sxs-lookup"><span data-stu-id="04d8f-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="04d8f-132">È possibile usare il metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) per convertire un valore di ora nel limite di frame più vicino oppure usare la funzione seguente per eseguire la conversione da un numero di frame all'ora di riferimento:</span><span class="sxs-lookup"><span data-stu-id="04d8f-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="04d8f-133">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="04d8f-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04d8f-134">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04d8f-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04d8f-135">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="04d8f-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04d8f-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04d8f-136">Requirements</span></span>



| <span data-ttu-id="04d8f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d8f-137">Requirement</span></span> | <span data-ttu-id="04d8f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="04d8f-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d8f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04d8f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="04d8f-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d8f-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04d8f-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="04d8f-141">Library</span></span><br/> | <dl> <span data-ttu-id="04d8f-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04d8f-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d8f-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04d8f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d8f-144">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="04d8f-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="04d8f-145">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="04d8f-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




