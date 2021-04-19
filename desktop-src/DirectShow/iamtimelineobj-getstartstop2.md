---
description: "Il metodo GetStartStop2 recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto. Questo metodo è equivalente a IAMTimelineObj:: GetStartStop, ma accetta valori REFTIME."
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Metodo IAMTimelineObj:: GetStartStop2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327108"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="dabee-104">Metodo IAMTimelineObj:: GetStartStop2</span><span class="sxs-lookup"><span data-stu-id="dabee-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="dabee-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dabee-105">\[Deprecated.</span></span> <span data-ttu-id="dabee-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dabee-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dabee-107">Il `GetStartStop2` metodo recupera le ore di inizio e di fine dell'oggetto, relative all'elemento padre dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dabee-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="dabee-108">Questo metodo è equivalente a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="dabee-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="dabee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dabee-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="dabee-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dabee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dabee-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="dabee-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="dabee-112">Riceve l'ora di inizio, in secondi.</span><span class="sxs-lookup"><span data-stu-id="dabee-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="dabee-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="dabee-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="dabee-114">Riceve l'ora di arresto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="dabee-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dabee-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dabee-115">Return value</span></span>

<span data-ttu-id="dabee-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dabee-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dabee-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dabee-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dabee-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="dabee-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dabee-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="dabee-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dabee-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dabee-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dabee-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dabee-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dabee-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dabee-122">Requirements</span></span>



| <span data-ttu-id="dabee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dabee-123">Requirement</span></span> | <span data-ttu-id="dabee-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dabee-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dabee-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dabee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dabee-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dabee-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dabee-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="dabee-127">Library</span></span><br/> | <dl> <span data-ttu-id="dabee-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dabee-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dabee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dabee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabee-130">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="dabee-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="dabee-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="dabee-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




