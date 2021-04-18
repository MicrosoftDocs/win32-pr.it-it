---
description: Il metodo SpliceWithNext unisce l'oggetto di origine a un altro oggetto di origine.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Metodo IAMTimelineSrc:: SpliceWithNext (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325179"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="750a5-103">Metodo IAMTimelineSrc:: SpliceWithNext</span><span class="sxs-lookup"><span data-stu-id="750a5-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="750a5-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="750a5-104">\[Deprecated.</span></span> <span data-ttu-id="750a5-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="750a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="750a5-106">Il `SpliceWithNext` metodo unisce l'oggetto di origine a un altro oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="750a5-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="750a5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="750a5-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="750a5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="750a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750a5-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="750a5-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="750a5-110">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine da aggiungere all'origine corrente.</span><span class="sxs-lookup"><span data-stu-id="750a5-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750a5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="750a5-111">Return value</span></span>

<span data-ttu-id="750a5-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="750a5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="750a5-113">Tra i possibili valori restituiti sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="750a5-113">Possible return values include the following:</span></span>



| <span data-ttu-id="750a5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="750a5-114">Return code</span></span>                                                                                   | <span data-ttu-id="750a5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="750a5-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="750a5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="750a5-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="750a5-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="750a5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="750a5-119">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="750a5-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="750a5-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="750a5-121">L'oggetto specificato dal parametro *pNext* non è un oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="750a5-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="750a5-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="750a5-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="750a5-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="750a5-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="750a5-124">Remarks</span></span>

<span data-ttu-id="750a5-125">Come attualmente implementato, questo metodo elimina tutti gli effetti su *pNext*.</span><span class="sxs-lookup"><span data-stu-id="750a5-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="750a5-126">Affinché questo metodo abbia esito positivo, *pNext* deve essere un frame di corrispondenza dell'oggetto di origine corrente, definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="750a5-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="750a5-127">Deve condividere lo stesso file di origine.</span><span class="sxs-lookup"><span data-stu-id="750a5-127">It must share the same source file.</span></span>
-   <span data-ttu-id="750a5-128">L'ora di inizio del supporto deve essere uguale all'ora di arresto del supporto dell'origine corrente.</span><span class="sxs-lookup"><span data-stu-id="750a5-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="750a5-129">La velocità di riproduzione deve essere la stessa.</span><span class="sxs-lookup"><span data-stu-id="750a5-129">The playback rate must be the same.</span></span> <span data-ttu-id="750a5-130">La velocità di riproduzione è durata media divisa per la durata della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="750a5-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="750a5-131">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="750a5-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="750a5-132">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="750a5-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="750a5-133">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="750a5-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="750a5-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="750a5-134">Requirements</span></span>



| <span data-ttu-id="750a5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="750a5-135">Requirement</span></span> | <span data-ttu-id="750a5-136">Valore</span><span class="sxs-lookup"><span data-stu-id="750a5-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="750a5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="750a5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="750a5-138"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="750a5-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="750a5-139">Library</span></span><br/> | <dl> <span data-ttu-id="750a5-140"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="750a5-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750a5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="750a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750a5-142">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="750a5-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="750a5-143">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="750a5-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




