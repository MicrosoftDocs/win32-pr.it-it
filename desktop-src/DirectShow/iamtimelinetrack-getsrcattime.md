---
description: Il metodo GetSrcAtTime recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Metodo IAMTimelineTrack:: GetSrcAtTime (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325633"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="afc4e-103">Metodo IAMTimelineTrack:: GetSrcAtTime</span><span class="sxs-lookup"><span data-stu-id="afc4e-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="afc4e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="afc4e-104">\[Deprecated.</span></span> <span data-ttu-id="afc4e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="afc4e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="afc4e-106">Il `GetSrcAtTime` metodo recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.</span><span class="sxs-lookup"><span data-stu-id="afc4e-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc4e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afc4e-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="afc4e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="afc4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc4e-109">*ppSrc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="afc4e-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc4e-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="afc4e-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="afc4e-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="afc4e-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="afc4e-112">Ora di inizio della ricerca, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="afc4e-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="afc4e-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="afc4e-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="afc4e-114">Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="afc4e-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc4e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afc4e-115">Return value</span></span>

<span data-ttu-id="afc4e-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="afc4e-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="afc4e-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="afc4e-117">Return code</span></span>                                                                                  | <span data-ttu-id="afc4e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afc4e-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="afc4e-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="afc4e-120">Impossibile trovare un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="afc4e-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="afc4e-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="afc4e-122">Si trova un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="afc4e-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="afc4e-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="afc4e-124">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="afc4e-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="afc4e-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="afc4e-126">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="afc4e-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="afc4e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="afc4e-127">Remarks</span></span>

<span data-ttu-id="afc4e-128">Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="afc4e-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="afc4e-129">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="afc4e-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="afc4e-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="afc4e-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="afc4e-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="afc4e-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="afc4e-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="afc4e-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="afc4e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afc4e-133">Requirements</span></span>



| <span data-ttu-id="afc4e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc4e-134">Requirement</span></span> | <span data-ttu-id="afc4e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="afc4e-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc4e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afc4e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="afc4e-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="afc4e-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="afc4e-138">Library</span></span><br/> | <dl> <span data-ttu-id="afc4e-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afc4e-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc4e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afc4e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc4e-141">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="afc4e-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="afc4e-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="afc4e-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




