---
description: Il metodo TrackGetPriority Recupera il livello di priorità dell'oggetto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Metodo IAMTimelineVirtualTrack:: TrackGetPriority (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332194"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="23036-103">Metodo IAMTimelineVirtualTrack:: TrackGetPriority</span><span class="sxs-lookup"><span data-stu-id="23036-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="23036-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="23036-104">\[Deprecated.</span></span> <span data-ttu-id="23036-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23036-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="23036-106">Il `TrackGetPriority` metodo recupera il livello di priorità dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="23036-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="23036-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23036-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="23036-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23036-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23036-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="23036-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="23036-110">Puntatore a una variabile che riceve il livello di priorità.</span><span class="sxs-lookup"><span data-stu-id="23036-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="23036-111">Se l'oggetto non fa parte di una sequenza temporale, il valore viene impostato su-1.</span><span class="sxs-lookup"><span data-stu-id="23036-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23036-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23036-112">Return value</span></span>

<span data-ttu-id="23036-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23036-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23036-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23036-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23036-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="23036-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23036-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="23036-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="23036-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="23036-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="23036-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="23036-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23036-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23036-119">Requirements</span></span>



| <span data-ttu-id="23036-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23036-120">Requirement</span></span> | <span data-ttu-id="23036-121">Valore</span><span class="sxs-lookup"><span data-stu-id="23036-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23036-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23036-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23036-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="23036-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="23036-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="23036-124">Library</span></span><br/> | <dl> <span data-ttu-id="23036-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23036-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23036-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23036-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23036-127">**Interfaccia IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="23036-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="23036-128">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="23036-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




