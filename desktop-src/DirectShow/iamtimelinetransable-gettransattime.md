---
description: Il metodo GetTransAtTime recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Metodo IAMTimelineTransable:: GetTransAtTime (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332969"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="e5ee7-103">Metodo IAMTimelineTransable:: GetTransAtTime</span><span class="sxs-lookup"><span data-stu-id="e5ee7-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="e5ee7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-104">\[Deprecated.</span></span> <span data-ttu-id="e5ee7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5ee7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5ee7-106">Il `GetTransAtTime` metodo recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ee7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5ee7-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="e5ee7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5ee7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ee7-109">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e5ee7-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ee7-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e5ee7-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="e5ee7-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ee7-112">Tempo da cui iniziare la ricerca, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e5ee7-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="e5ee7-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ee7-114">Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ee7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5ee7-115">Return value</span></span>

<span data-ttu-id="e5ee7-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e5ee7-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e5ee7-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e5ee7-117">Return code</span></span>                                                                                  | <span data-ttu-id="e5ee7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5ee7-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e5ee7-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="e5ee7-120">Non è stata trovata alcuna transizione.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="e5ee7-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e5ee7-122">È stata trovata una transizione.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="e5ee7-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e5ee7-124">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="e5ee7-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e5ee7-126">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="e5ee7-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5ee7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5ee7-127">Remarks</span></span>

<span data-ttu-id="e5ee7-128">Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e5ee7-129">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e5ee7-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e5ee7-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5ee7-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e5ee7-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e5ee7-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5ee7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5ee7-133">Requirements</span></span>



| <span data-ttu-id="e5ee7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ee7-134">Requirement</span></span> | <span data-ttu-id="e5ee7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e5ee7-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ee7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5ee7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e5ee7-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e5ee7-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5ee7-138">Library</span></span><br/> | <dl> <span data-ttu-id="e5ee7-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee7-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ee7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5ee7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ee7-141">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="e5ee7-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="e5ee7-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e5ee7-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




