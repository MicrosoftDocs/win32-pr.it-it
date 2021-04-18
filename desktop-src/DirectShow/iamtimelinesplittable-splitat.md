---
description: Il metodo SplitAt suddivide l'oggetto all'ora specificata.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Metodo IAMTimelineSplittable:: SplitAt (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329479"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="d726a-103">Metodo IAMTimelineSplittable:: SplitAt</span><span class="sxs-lookup"><span data-stu-id="d726a-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="d726a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d726a-104">\[Deprecated.</span></span> <span data-ttu-id="d726a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d726a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d726a-106">Il `SplitAt` metodo suddivide l'oggetto all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="d726a-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d726a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d726a-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="d726a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d726a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d726a-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="d726a-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="d726a-110">Ora in cui dividere l'oggetto, relativo all'inizio della sequenza temporale, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="d726a-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d726a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d726a-111">Return value</span></span>

<span data-ttu-id="d726a-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d726a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d726a-113">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d726a-113">Possible values include the following:</span></span>



| <span data-ttu-id="d726a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d726a-114">Return code</span></span>                                                                                   | <span data-ttu-id="d726a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d726a-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d726a-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="d726a-117">Niente da dividere.</span><span class="sxs-lookup"><span data-stu-id="d726a-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="d726a-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d726a-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d726a-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="d726a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d726a-121">L'oggetto non esiste in questo momento.</span><span class="sxs-lookup"><span data-stu-id="d726a-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="d726a-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d726a-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d726a-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d726a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d726a-124">Remarks</span></span>

<span data-ttu-id="d726a-125">Se si suddivide un'origine, un effetto o una transizione, questo metodo crea un secondo oggetto dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="d726a-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="d726a-126">L'oggetto originale viene troncato in corrispondenza dell'ora di suddivisione specificata e il nuovo oggetto sostituisce la parte troncata.</span><span class="sxs-lookup"><span data-stu-id="d726a-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="d726a-127">Il nuovo oggetto eredita tutte le stesse proprietà.</span><span class="sxs-lookup"><span data-stu-id="d726a-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="d726a-128">In un oggetto di origine, il metodo suddivide anche tutti gli effetti che ricadeno sull'ora di divisione.</span><span class="sxs-lookup"><span data-stu-id="d726a-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="d726a-129">La chiamata di questo metodo su un track divide tutte le origini, gli effetti e le transizioni contenuti nella traccia in corrispondenza della fase di suddivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="d726a-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="d726a-130">Non crea una seconda traccia. Una traccia inizia al momento zero e si estende fino all'infinito.</span><span class="sxs-lookup"><span data-stu-id="d726a-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="d726a-131">Per una traccia, se il tempo di suddivisione è successivo a tutti gli elementi della traccia, il metodo restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="d726a-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="d726a-132">Per qualsiasi altro oggetto, se l'ora di divisione non rientra in un punto qualsiasi all'interno dell'oggetto, il metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d726a-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="d726a-133">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d726a-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d726a-134">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d726a-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d726a-135">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d726a-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d726a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d726a-136">Requirements</span></span>



| <span data-ttu-id="d726a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d726a-137">Requirement</span></span> | <span data-ttu-id="d726a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="d726a-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d726a-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d726a-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d726a-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d726a-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="d726a-141">Library</span></span><br/> | <dl> <span data-ttu-id="d726a-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d726a-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d726a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d726a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d726a-144">**Interfaccia IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="d726a-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="d726a-145">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d726a-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




