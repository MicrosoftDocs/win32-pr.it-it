---
description: Il metodo SetRecompFormatFromSource imposta il formato di ricompressione video usando il formato di compressione da un file di origine.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Metodo IAMTimelineGroup:: SetRecompFormatFromSource (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331623"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="04377-103">Metodo IAMTimelineGroup:: SetRecompFormatFromSource</span><span class="sxs-lookup"><span data-stu-id="04377-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="04377-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="04377-104">\[Deprecated.</span></span> <span data-ttu-id="04377-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04377-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04377-106">Il `SetRecompFormatFromSource` metodo imposta il formato di ricompressione video usando il formato di compressione da un file di origine.</span><span class="sxs-lookup"><span data-stu-id="04377-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="04377-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04377-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="04377-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04377-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04377-109">*pSource*</span><span class="sxs-lookup"><span data-stu-id="04377-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="04377-110">Puntatore all'interfaccia [**IAMTimelineSrc**](iamtimelinesrc.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="04377-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04377-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04377-111">Return value</span></span>

<span data-ttu-id="04377-112">Restituisce valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04377-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="04377-113">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="04377-113">Possible values include the following.</span></span>



| <span data-ttu-id="04377-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="04377-114">Return code</span></span>                                                                                             | <span data-ttu-id="04377-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04377-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04377-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04377-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="04377-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="04377-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="04377-118"><dt>**E \_ Nessuna \_ sequenza temporale**</dt></span><span class="sxs-lookup"><span data-stu-id="04377-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="04377-119">Il gruppo non si trova all'interno di una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="04377-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="04377-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="04377-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="04377-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="04377-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="04377-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="04377-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="04377-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="04377-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="04377-124"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="04377-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="04377-125">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="04377-125">Invalid media type.</span></span> <span data-ttu-id="04377-126">Il gruppo non è un gruppo video oppure il file di origine non contiene alcun flusso video.</span><span class="sxs-lookup"><span data-stu-id="04377-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04377-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="04377-127">Remarks</span></span>

<span data-ttu-id="04377-128">Questo metodo trova il file di origine associato a *pSource*, recupera il tipo di supporto del primo flusso video nel file e imposta il formato di compressione del gruppo che utilizza tale tipo.</span><span class="sxs-lookup"><span data-stu-id="04377-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="04377-129">Per ulteriori informazioni sui formati di compressione, vedere [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="04377-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="04377-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="04377-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04377-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04377-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04377-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="04377-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04377-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04377-133">Requirements</span></span>



| <span data-ttu-id="04377-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="04377-134">Requirement</span></span> | <span data-ttu-id="04377-135">Valore</span><span class="sxs-lookup"><span data-stu-id="04377-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04377-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04377-136">Header</span></span><br/>  | <dl> <span data-ttu-id="04377-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="04377-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04377-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="04377-138">Library</span></span><br/> | <dl> <span data-ttu-id="04377-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04377-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04377-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04377-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04377-141">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="04377-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="04377-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="04377-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




