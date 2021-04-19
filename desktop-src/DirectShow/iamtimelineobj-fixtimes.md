---
description: Il metodo FixTimes Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Metodo IAMTimelineObj:: FixTimes (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333592"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="814bd-103">Metodo IAMTimelineObj:: FixTimes</span><span class="sxs-lookup"><span data-stu-id="814bd-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="814bd-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="814bd-104">\[Deprecated.</span></span> <span data-ttu-id="814bd-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="814bd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="814bd-106">Il `FixTimes` Metodo Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre.</span><span class="sxs-lookup"><span data-stu-id="814bd-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="814bd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="814bd-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="814bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="814bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814bd-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="814bd-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="814bd-110">Puntatore a una variabile che contiene l'ora di inizio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="814bd-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="814bd-111">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="814bd-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="814bd-112">*pStop*</span><span class="sxs-lookup"><span data-stu-id="814bd-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="814bd-113">Puntatore a una variabile che contiene l'ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="814bd-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="814bd-114">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="814bd-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814bd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="814bd-115">Return value</span></span>

<span data-ttu-id="814bd-116">Restituisce \_ OK se ha esito positivo o E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="814bd-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="814bd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="814bd-117">Remarks</span></span>

<span data-ttu-id="814bd-118">Durante il rendering, DES Arrotonda gli orari di inizio e di fine dell'oggetto al limite del frame più vicino.</span><span class="sxs-lookup"><span data-stu-id="814bd-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="814bd-119">Tuttavia, DES non sovrascrive i tempi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="814bd-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="814bd-120">Se si modifica la frequenza dei fotogrammi del gruppo, i tempi arrotondati vengono sempre calcolati a partire dai tempi originali.</span><span class="sxs-lookup"><span data-stu-id="814bd-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="814bd-121">Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="814bd-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="814bd-122">Utilizzare questo metodo per determinare gli orari di inizio e di fine accurati nel progetto sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="814bd-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="814bd-123">Ad esempio, è consigliabile cercare l'ora arrotondata, anziché l'ora di inizio e di fine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="814bd-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="814bd-124">Chiamare [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) per ottenere l'ora originale e passare tali valori a `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="814bd-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="814bd-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="814bd-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="814bd-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="814bd-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="814bd-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="814bd-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="814bd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="814bd-128">Requirements</span></span>



| <span data-ttu-id="814bd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="814bd-129">Requirement</span></span> | <span data-ttu-id="814bd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="814bd-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="814bd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="814bd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="814bd-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="814bd-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="814bd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="814bd-133">Library</span></span><br/> | <dl> <span data-ttu-id="814bd-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="814bd-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814bd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="814bd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814bd-136">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="814bd-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="814bd-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="814bd-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




