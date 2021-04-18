---
description: 'Il metodo InsertSpace2 suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi. Questo metodo è equivalente a IAMTimelineTrack:: InsertSpace, ma accetta valori REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Metodo IAMTimelineTrack:: InsertSpace2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325627"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="c7228-104">Metodo IAMTimelineTrack:: InsertSpace2</span><span class="sxs-lookup"><span data-stu-id="c7228-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="c7228-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c7228-105">\[Deprecated.</span></span> <span data-ttu-id="c7228-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7228-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7228-107">Il `InsertSpace2` metodo suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.</span><span class="sxs-lookup"><span data-stu-id="c7228-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="c7228-108">Questo metodo è equivalente a [**IAMTimelineTrack:: InsertSpace**](iamtimelinetrack-insertspace.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="c7228-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7228-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7228-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="c7228-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7228-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7228-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="c7228-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c7228-112">Ora in cui creare la divisione e il punto iniziale dello spazio inserito, in secondi.</span><span class="sxs-lookup"><span data-stu-id="c7228-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c7228-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="c7228-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c7228-114">Punto finale dello spazio inserito, in secondi.</span><span class="sxs-lookup"><span data-stu-id="c7228-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7228-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7228-115">Return value</span></span>

<span data-ttu-id="c7228-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7228-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c7228-117">Tra i possibili valori restituiti sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c7228-117">Possible return values include the following:</span></span>



| <span data-ttu-id="c7228-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c7228-118">Return code</span></span>                                                                                   | <span data-ttu-id="c7228-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7228-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="c7228-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="c7228-121">Nessun oggetto all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="c7228-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="c7228-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c7228-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c7228-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c7228-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c7228-125">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="c7228-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="c7228-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c7228-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c7228-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="c7228-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7228-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7228-129">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c7228-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7228-130">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7228-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7228-131">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c7228-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7228-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7228-132">Requirements</span></span>



| <span data-ttu-id="c7228-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7228-133">Requirement</span></span> | <span data-ttu-id="c7228-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c7228-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7228-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7228-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c7228-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7228-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7228-137">Library</span></span><br/> | <dl> <span data-ttu-id="c7228-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7228-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7228-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7228-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7228-140">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="c7228-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="c7228-141">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c7228-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




