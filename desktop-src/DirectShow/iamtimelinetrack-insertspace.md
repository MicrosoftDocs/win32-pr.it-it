---
description: Il metodo InsertSpace suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Metodo IAMTimelineTrack:: InsertSpace (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325631"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="192cb-103">Metodo IAMTimelineTrack:: InsertSpace</span><span class="sxs-lookup"><span data-stu-id="192cb-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="192cb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="192cb-104">\[Deprecated.</span></span> <span data-ttu-id="192cb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="192cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="192cb-106">Il `InsertSpace` metodo suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.</span><span class="sxs-lookup"><span data-stu-id="192cb-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="192cb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="192cb-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="192cb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="192cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="192cb-109">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="192cb-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="192cb-110">Ora in cui creare la divisione e il punto iniziale dello spazio inserito, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="192cb-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="192cb-111">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="192cb-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="192cb-112">Punto finale dello spazio inserito, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="192cb-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="192cb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="192cb-113">Return value</span></span>

<span data-ttu-id="192cb-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="192cb-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="192cb-115">Tra i possibili valori restituiti sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="192cb-115">Possible return values include the following:</span></span>



| <span data-ttu-id="192cb-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="192cb-116">Return code</span></span>                                                                                   | <span data-ttu-id="192cb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="192cb-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="192cb-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="192cb-119">Nessun oggetto all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="192cb-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="192cb-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="192cb-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="192cb-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="192cb-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="192cb-123">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="192cb-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="192cb-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="192cb-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="192cb-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="192cb-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="192cb-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="192cb-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="192cb-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="192cb-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="192cb-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="192cb-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="192cb-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="192cb-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="192cb-130">Requirements</span></span>



| <span data-ttu-id="192cb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="192cb-131">Requirement</span></span> | <span data-ttu-id="192cb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="192cb-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="192cb-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="192cb-133">Header</span></span><br/>  | <dl> <span data-ttu-id="192cb-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="192cb-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="192cb-135">Library</span></span><br/> | <dl> <span data-ttu-id="192cb-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="192cb-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="192cb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="192cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="192cb-138">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="192cb-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="192cb-139">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="192cb-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




