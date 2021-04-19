---
description: 'Il metodo GetTransAtTime2 recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a IAMTimelineTransable:: GetTransAtTime, ma accetta un parametro REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Metodo IAMTimelineTransable:: GetTransAtTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332967"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="e277a-104">Metodo IAMTimelineTransable:: GetTransAtTime2</span><span class="sxs-lookup"><span data-stu-id="e277a-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="e277a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e277a-105">\[Deprecated.</span></span> <span data-ttu-id="e277a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e277a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e277a-107">Il `GetTransAtTime2` metodo recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate.</span><span class="sxs-lookup"><span data-stu-id="e277a-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="e277a-108">Questo metodo è equivalente a [**IAMTimelineTransable:: GetTransAtTime**](iamtimelinetransable-gettransattime.md), ma accetta un parametro [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e277a-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e277a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e277a-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="e277a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e277a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e277a-111">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e277a-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e277a-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione.</span><span class="sxs-lookup"><span data-stu-id="e277a-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e277a-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="e277a-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="e277a-114">Tempo da cui iniziare la ricerca, in secondi.</span><span class="sxs-lookup"><span data-stu-id="e277a-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="e277a-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="e277a-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="e277a-116">Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e277a-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e277a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e277a-117">Return value</span></span>

<span data-ttu-id="e277a-118">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e277a-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e277a-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e277a-119">Return code</span></span>                                                                                  | <span data-ttu-id="e277a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e277a-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e277a-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="e277a-122">Non è stata trovata alcuna transizione.</span><span class="sxs-lookup"><span data-stu-id="e277a-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="e277a-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e277a-124">È stata trovata una transizione.</span><span class="sxs-lookup"><span data-stu-id="e277a-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="e277a-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e277a-126">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="e277a-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="e277a-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e277a-128">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="e277a-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e277a-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e277a-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e277a-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e277a-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e277a-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e277a-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e277a-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e277a-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e277a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e277a-133">Requirements</span></span>



| <span data-ttu-id="e277a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e277a-134">Requirement</span></span> | <span data-ttu-id="e277a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e277a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e277a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e277a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e277a-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e277a-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="e277a-138">Library</span></span><br/> | <dl> <span data-ttu-id="e277a-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e277a-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e277a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e277a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e277a-141">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="e277a-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="e277a-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e277a-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




