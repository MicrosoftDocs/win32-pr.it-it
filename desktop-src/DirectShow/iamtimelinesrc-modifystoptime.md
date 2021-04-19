---
description: Il metodo ModifyStopTime imposta l'ora di arresto, relativa alla sequenza temporale.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Metodo IAMTimelineSrc:: ModifyStopTime (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332750"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="1f372-103">Metodo IAMTimelineSrc:: ModifyStopTime</span><span class="sxs-lookup"><span data-stu-id="1f372-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="1f372-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1f372-104">\[Deprecated.</span></span> <span data-ttu-id="1f372-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f372-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f372-106">Il `ModifyStopTime` metodo imposta l'ora di arresto, relativa alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="1f372-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f372-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f372-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="1f372-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f372-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f372-109">*Stop*</span><span class="sxs-lookup"><span data-stu-id="1f372-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="1f372-110">Nuova ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1f372-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f372-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f372-111">Return value</span></span>

<span data-ttu-id="1f372-112">Restituisce S \_ OK o e \_ INVALIDARG se l'ora specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="1f372-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f372-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f372-113">Remarks</span></span>

<span data-ttu-id="1f372-114">Questo metodo equivale a chiamare [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) con l'ora di inizio originale e una nuova ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="1f372-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="1f372-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1f372-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1f372-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1f372-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1f372-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1f372-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f372-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f372-118">Requirements</span></span>



| <span data-ttu-id="1f372-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f372-119">Requirement</span></span> | <span data-ttu-id="1f372-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1f372-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f372-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f372-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1f372-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f372-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1f372-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="1f372-123">Library</span></span><br/> | <dl> <span data-ttu-id="1f372-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f372-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f372-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f372-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f372-126">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="1f372-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="1f372-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1f372-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




