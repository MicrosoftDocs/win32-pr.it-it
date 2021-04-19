---
description: Il metodo FixMediaTimes arrotonda i valori temporali specificati al limite del frame più vicino, in base a quanto definito dalla frequenza dei fotogrammi di output. In generale, le applicazioni non devono chiamare questo metodo.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Metodo IAMTimelineSrc:: FixMediaTimes (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324263"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="c70da-104">Metodo IAMTimelineSrc:: FixMediaTimes</span><span class="sxs-lookup"><span data-stu-id="c70da-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="c70da-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c70da-105">\[Deprecated.</span></span> <span data-ttu-id="c70da-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c70da-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c70da-107">Il `FixMediaTimes` Metodo arrotonda i valori temporali specificati al limite del frame più vicino, in base a quanto definito dalla frequenza dei fotogrammi di output.</span><span class="sxs-lookup"><span data-stu-id="c70da-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="c70da-108">In generale, le applicazioni non devono chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c70da-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c70da-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c70da-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c70da-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c70da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c70da-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="c70da-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c70da-112">Puntatore a una variabile che contiene l'ora di inizio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c70da-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="c70da-113">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="c70da-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="c70da-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c70da-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c70da-115">Puntatore a una variabile che contiene l'ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c70da-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="c70da-116">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="c70da-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c70da-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c70da-117">Return value</span></span>

<span data-ttu-id="c70da-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c70da-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c70da-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c70da-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c70da-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c70da-120">Remarks</span></span>

<span data-ttu-id="c70da-121">Questo metodo è simile al metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , ma conserva il rapporto originale tra tempi di supporto e tempi di sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="c70da-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="c70da-122">L'arrotondamento dei tempi al limite del frame più vicino potrebbe causare la distorsione del rapporto.</span><span class="sxs-lookup"><span data-stu-id="c70da-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="c70da-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c70da-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c70da-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c70da-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c70da-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c70da-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c70da-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c70da-126">Requirements</span></span>



| <span data-ttu-id="c70da-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c70da-127">Requirement</span></span> | <span data-ttu-id="c70da-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c70da-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c70da-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c70da-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c70da-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c70da-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c70da-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="c70da-131">Library</span></span><br/> | <dl> <span data-ttu-id="c70da-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c70da-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c70da-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c70da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c70da-134">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="c70da-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="c70da-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c70da-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




