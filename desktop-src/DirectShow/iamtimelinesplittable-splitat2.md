---
description: "Il metodo SplitAt2 suddivide l'oggetto all'ora specificata. Questo metodo è equivalente a IAMTimelineSplittable:: SplitAt, ma accetta un valore REFTIME."
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Metodo IAMTimelineSplittable:: SplitAt2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325722"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="e43ca-104">Metodo IAMTimelineSplittable:: SplitAt2</span><span class="sxs-lookup"><span data-stu-id="e43ca-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="e43ca-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e43ca-105">\[Deprecated.</span></span> <span data-ttu-id="e43ca-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e43ca-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e43ca-107">Il `SplitAt2` metodo suddivide l'oggetto all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="e43ca-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="e43ca-108">Questo metodo è equivalente a [**IAMTimelineSplittable:: SplitAt**](iamtimelinesplittable-splitat.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e43ca-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43ca-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e43ca-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="e43ca-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e43ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43ca-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="e43ca-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="e43ca-112">Ora in cui dividere l'oggetto, relativo all'inizio della sequenza temporale, in secondi.</span><span class="sxs-lookup"><span data-stu-id="e43ca-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43ca-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e43ca-113">Return value</span></span>

<span data-ttu-id="e43ca-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e43ca-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e43ca-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e43ca-115">Possible values include the following:</span></span>



| <span data-ttu-id="e43ca-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e43ca-116">Return code</span></span>                                                                                   | <span data-ttu-id="e43ca-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e43ca-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="e43ca-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="e43ca-119">Niente da dividere.</span><span class="sxs-lookup"><span data-stu-id="e43ca-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="e43ca-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e43ca-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e43ca-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="e43ca-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e43ca-123">L'oggetto non esiste in questo momento.</span><span class="sxs-lookup"><span data-stu-id="e43ca-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="e43ca-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e43ca-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e43ca-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e43ca-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="e43ca-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e43ca-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e43ca-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e43ca-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e43ca-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e43ca-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e43ca-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e43ca-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e43ca-130">Requirements</span></span>



| <span data-ttu-id="e43ca-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e43ca-131">Requirement</span></span> | <span data-ttu-id="e43ca-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e43ca-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e43ca-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e43ca-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e43ca-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e43ca-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e43ca-135">Library</span></span><br/> | <dl> <span data-ttu-id="e43ca-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e43ca-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43ca-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e43ca-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43ca-138">**Interfaccia IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="e43ca-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="e43ca-139">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e43ca-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




