---
description: Il metodo GetSmartRecompressFormat Recupera il formato di compressione corrente per la ricompressione intelligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Metodo IAMTimelineGroup:: GetSmartRecompressFormat (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328618"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="7cf63-103">Metodo IAMTimelineGroup:: GetSmartRecompressFormat</span><span class="sxs-lookup"><span data-stu-id="7cf63-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="7cf63-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7cf63-104">\[Deprecated.</span></span> <span data-ttu-id="7cf63-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7cf63-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7cf63-106">Il `GetSmartRecompressFormat` metodo recupera il formato di compressione corrente per la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="7cf63-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf63-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cf63-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7cf63-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cf63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf63-109">*ppFormat*</span><span class="sxs-lookup"><span data-stu-id="7cf63-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7cf63-110">Riceve un puntatore a una struttura [**SCompFmt0**](scompfmt0.md) , di cui viene eseguito il cast come puntatore a un oggetto Long.</span><span class="sxs-lookup"><span data-stu-id="7cf63-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="7cf63-111">Se il metodo ha esito negativo, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="7cf63-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf63-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cf63-112">Return value</span></span>

<span data-ttu-id="7cf63-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7cf63-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cf63-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cf63-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf63-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cf63-115">Remarks</span></span>

<span data-ttu-id="7cf63-116">Se l'applicazione non ha impostato un formato di compressione intelligente (chiamando [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), il formato restituito da questo metodo non sarà valido.</span><span class="sxs-lookup"><span data-stu-id="7cf63-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="7cf63-117">Chiamare il metodo [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) per determinare se è stato impostato un formato di compressione.</span><span class="sxs-lookup"><span data-stu-id="7cf63-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="7cf63-118">Se il metodo ha esito positivo, il chiamante deve liberare il tipo di supporto restituito ed eliminare la struttura [**SCompFmt0**](scompfmt0.md) :</span><span class="sxs-lookup"><span data-stu-id="7cf63-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="7cf63-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="7cf63-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7cf63-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7cf63-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7cf63-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7cf63-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7cf63-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cf63-122">Requirements</span></span>



| <span data-ttu-id="7cf63-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cf63-123">Requirement</span></span> | <span data-ttu-id="7cf63-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7cf63-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf63-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cf63-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7cf63-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf63-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7cf63-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cf63-127">Library</span></span><br/> | <dl> <span data-ttu-id="7cf63-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cf63-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf63-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cf63-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf63-130">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="7cf63-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="7cf63-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="7cf63-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




