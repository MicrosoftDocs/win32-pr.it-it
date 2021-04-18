---
description: Il metodo GetStartStop recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Metodo IAMTimelineObj:: GetStartStop (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327110"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="a61fd-103">Metodo IAMTimelineObj:: GetStartStop</span><span class="sxs-lookup"><span data-stu-id="a61fd-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="a61fd-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a61fd-104">\[Deprecated.</span></span> <span data-ttu-id="a61fd-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a61fd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a61fd-106">Il `GetStartStop` metodo recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a61fd-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a61fd-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="a61fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a61fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a61fd-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="a61fd-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a61fd-110">Riceve l'ora di inizio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="a61fd-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a61fd-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="a61fd-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a61fd-112">Riceve l'ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="a61fd-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a61fd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a61fd-113">Return value</span></span>

<span data-ttu-id="a61fd-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a61fd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a61fd-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a61fd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a61fd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a61fd-116">Remarks</span></span>

<span data-ttu-id="a61fd-117">Le composizioni, i gruppi e le tracce hanno sempre l'ora di inizio 0.</span><span class="sxs-lookup"><span data-stu-id="a61fd-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="a61fd-118">Durante il rendering, DES Arrotonda gli orari di inizio e di fine di un oggetto al limite di frame più vicino.</span><span class="sxs-lookup"><span data-stu-id="a61fd-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="a61fd-119">Tuttavia, DES non sovrascrive i tempi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a61fd-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="a61fd-120">Se si modifica la frequenza dei fotogrammi del gruppo, i tempi arrotondati vengono sempre calcolati a partire dai tempi originali.</span><span class="sxs-lookup"><span data-stu-id="a61fd-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="a61fd-121">Per altre informazioni, [ora in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="a61fd-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="a61fd-122">Per determinare le ore di inizio e di fine nel progetto di cui è stato eseguito il rendering, passare i valori restituiti da `GetStartStop` al metodo [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) .</span><span class="sxs-lookup"><span data-stu-id="a61fd-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="a61fd-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a61fd-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a61fd-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a61fd-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a61fd-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a61fd-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a61fd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a61fd-126">Requirements</span></span>



| <span data-ttu-id="a61fd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a61fd-127">Requirement</span></span> | <span data-ttu-id="a61fd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a61fd-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a61fd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a61fd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a61fd-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a61fd-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a61fd-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a61fd-131">Library</span></span><br/> | <dl> <span data-ttu-id="a61fd-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a61fd-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a61fd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a61fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61fd-134">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a61fd-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="a61fd-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a61fd-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




