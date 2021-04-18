---
description: "Il metodo SetStartStop2 imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto. Questo metodo è equivalente a IAMTimelineObj:: SetStartStop, ma accetta valori REFTIME."
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Metodo IAMTimelineObj:: SetStartStop2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330808"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="4f166-104">Metodo IAMTimelineObj:: SetStartStop2</span><span class="sxs-lookup"><span data-stu-id="4f166-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="4f166-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4f166-105">\[Deprecated.</span></span> <span data-ttu-id="4f166-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f166-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f166-107">Il `SetStartStop2` metodo imposta l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4f166-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="4f166-108">Questo metodo è equivalente a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4f166-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f166-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f166-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="4f166-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f166-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f166-111">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="4f166-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="4f166-112">Nuova ora di inizio, in secondi, o-1 per la conservazione dell'ora di inizio esistente.</span><span class="sxs-lookup"><span data-stu-id="4f166-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="4f166-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="4f166-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="4f166-114">Nuova ora di arresto, in secondi, oppure-1 per la conservazione dell'ora di arresto esistente.</span><span class="sxs-lookup"><span data-stu-id="4f166-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f166-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f166-115">Return value</span></span>

<span data-ttu-id="4f166-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="4f166-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4f166-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4f166-117">Return code</span></span>                                                                                  | <span data-ttu-id="4f166-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f166-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="4f166-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f166-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4f166-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f166-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="4f166-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4f166-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4f166-122">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="4f166-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="4f166-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4f166-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="4f166-124">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4f166-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="4f166-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f166-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f166-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4f166-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f166-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f166-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f166-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4f166-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f166-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f166-129">Requirements</span></span>



| <span data-ttu-id="4f166-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f166-130">Requirement</span></span> | <span data-ttu-id="4f166-131">Valore</span><span class="sxs-lookup"><span data-stu-id="4f166-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f166-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f166-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4f166-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f166-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f166-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f166-134">Library</span></span><br/> | <dl> <span data-ttu-id="4f166-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f166-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f166-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f166-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f166-137">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="4f166-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4f166-138">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4f166-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




