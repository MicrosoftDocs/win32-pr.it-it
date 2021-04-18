---
description: Il metodo SetOutputFPS imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Metodo IAMTimelineGroup:: SetOutputFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331627"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="cf202-103">Metodo IAMTimelineGroup:: SetOutputFPS</span><span class="sxs-lookup"><span data-stu-id="cf202-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="cf202-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="cf202-104">\[Deprecated.</span></span> <span data-ttu-id="cf202-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf202-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf202-106">Il `SetOutputFPS` metodo imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="cf202-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf202-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf202-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="cf202-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf202-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="cf202-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="cf202-110">Frequenza dei fotogrammi di output per questo gruppo, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="cf202-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="cf202-111">Il valore non può essere uguale a zero e non può contenere più di sette cifre dopo la posizione decimale.</span><span class="sxs-lookup"><span data-stu-id="cf202-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf202-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf202-112">Return value</span></span>

<span data-ttu-id="cf202-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cf202-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf202-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf202-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf202-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf202-115">Remarks</span></span>

<span data-ttu-id="cf202-116">L'output sottoposto a rendering da questo gruppo viene eseguito alla frequenza dei fotogrammi specificata e tutte le modifiche apportate al materiale di origine vengono arrotondate al limite del frame più vicino, come definito dalla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="cf202-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="cf202-117">Per ottenere prestazioni ottimali, usare la stessa frequenza dei fotogrammi per tutti i gruppi, video e audio.</span><span class="sxs-lookup"><span data-stu-id="cf202-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="cf202-118">Il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) sovrascrive la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="cf202-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="cf202-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="cf202-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf202-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf202-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf202-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cf202-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf202-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf202-122">Requirements</span></span>



| <span data-ttu-id="cf202-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf202-123">Requirement</span></span> | <span data-ttu-id="cf202-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cf202-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf202-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf202-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cf202-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf202-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf202-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf202-127">Library</span></span><br/> | <dl> <span data-ttu-id="cf202-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf202-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf202-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf202-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf202-130">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="cf202-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="cf202-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cf202-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




