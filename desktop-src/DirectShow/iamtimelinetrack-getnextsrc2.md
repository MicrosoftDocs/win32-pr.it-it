---
description: "Il metodo GetNextSrc2 Cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva. Questo metodo è equivalente a IAMTimelineTrack:: GetNextSrc, ma accetta un valore REFTIME."
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Metodo IAMTimelineTrack:: GetNextSrc2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325638"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="f15f1-104">Metodo IAMTimelineTrack:: GetNextSrc2</span><span class="sxs-lookup"><span data-stu-id="f15f1-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="f15f1-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f15f1-105">\[Deprecated.</span></span> <span data-ttu-id="f15f1-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f15f1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f15f1-107">Il `GetNextSrc2` metodo cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="f15f1-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="f15f1-108">Questo metodo è equivalente a [**IAMTimelineTrack:: GetNextSrc**](iamtimelinetrack-getnextsrc.md), ma accetta un valore [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="f15f1-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15f1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f15f1-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="f15f1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f15f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15f1-111">*ppSrc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f15f1-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f15f1-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="f15f1-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f15f1-113">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="f15f1-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="f15f1-114">In input, contiene l'ora di inizio della ricerca, in secondi.</span><span class="sxs-lookup"><span data-stu-id="f15f1-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="f15f1-115">Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine.</span><span class="sxs-lookup"><span data-stu-id="f15f1-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="f15f1-116">Se il metodo non recupera un'origine, il valore diventa non valido e non deve essere usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f15f1-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15f1-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f15f1-117">Return value</span></span>

<span data-ttu-id="f15f1-118">Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f15f1-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15f1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f15f1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f15f1-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f15f1-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f15f1-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f15f1-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f15f1-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f15f1-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f15f1-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f15f1-123">Requirements</span></span>



| <span data-ttu-id="f15f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15f1-124">Requirement</span></span> | <span data-ttu-id="f15f1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f15f1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15f1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f15f1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f15f1-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15f1-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f15f1-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f15f1-128">Library</span></span><br/> | <dl> <span data-ttu-id="f15f1-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f15f1-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15f1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f15f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15f1-131">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="f15f1-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="f15f1-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f15f1-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




