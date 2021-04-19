---
description: Il metodo GetNextTrans recupera la prima transizione visualizzata all'ora specificata o successiva.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Metodo IAMTimelineTransable:: GetNextTrans (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324000"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="ddae5-103">Metodo IAMTimelineTransable:: GetNextTrans</span><span class="sxs-lookup"><span data-stu-id="ddae5-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="ddae5-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ddae5-104">\[Deprecated.</span></span> <span data-ttu-id="ddae5-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ddae5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ddae5-106">Il `GetNextTrans` metodo recupera la prima transizione visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="ddae5-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddae5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddae5-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="ddae5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddae5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddae5-109">*ppTrans* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ddae5-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddae5-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="ddae5-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ddae5-111">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="ddae5-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ddae5-112">Puntatore a una variabile che specifica l'ora in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ddae5-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="ddae5-113">In input, questo valore specifica l'ora da cui trovare la transizione.</span><span class="sxs-lookup"><span data-stu-id="ddae5-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="ddae5-114">Nell'output, se viene recuperata una transizione, questo valore viene impostato sull'ora di arresto della transizione.</span><span class="sxs-lookup"><span data-stu-id="ddae5-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddae5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddae5-115">Return value</span></span>

<span data-ttu-id="ddae5-116">Restituisce \_ OK se il metodo recupera una transizione o S \_ false se non trova una transizione.</span><span class="sxs-lookup"><span data-stu-id="ddae5-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="ddae5-117">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="ddae5-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddae5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddae5-118">Remarks</span></span>

<span data-ttu-id="ddae5-119">L'ora di inizio della transizione potrebbe essere inferiore al tempo specificato in *pin*, se la transizione si estende al tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="ddae5-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="ddae5-120">Se il metodo restituisce S \_ OK, l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="ddae5-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="ddae5-121">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ddae5-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="ddae5-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ddae5-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ddae5-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddae5-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ddae5-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ddae5-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ddae5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddae5-125">Requirements</span></span>



| <span data-ttu-id="ddae5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddae5-126">Requirement</span></span> | <span data-ttu-id="ddae5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ddae5-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddae5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddae5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ddae5-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddae5-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ddae5-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddae5-130">Library</span></span><br/> | <dl> <span data-ttu-id="ddae5-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddae5-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddae5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddae5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddae5-133">**Interfaccia IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="ddae5-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="ddae5-134">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ddae5-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




