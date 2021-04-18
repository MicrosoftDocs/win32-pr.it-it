---
description: Il metodo GetNextVTrack recupera la traccia virtuale successiva dopo una traccia virtuale specificata.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Metodo IAMTimelineComp:: GetNextVTrack (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332045"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="79fd6-103">Metodo IAMTimelineComp:: GetNextVTrack</span><span class="sxs-lookup"><span data-stu-id="79fd6-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="79fd6-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="79fd6-104">\[Deprecated.</span></span> <span data-ttu-id="79fd6-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79fd6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="79fd6-106">Il `GetNextVTrack` metodo recupera la traccia virtuale successiva dopo una traccia virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="79fd6-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fd6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79fd6-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="79fd6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="79fd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fd6-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="79fd6-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="79fd6-110">Puntatore alla traccia virtuale precedente oppure **null** per recuperare il primo tracciato virtuale nella composizione.</span><span class="sxs-lookup"><span data-stu-id="79fd6-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="79fd6-111">*ppNextVirtualTrack* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79fd6-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79fd6-112">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale successiva, in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="79fd6-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fd6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79fd6-113">Return value</span></span>

<span data-ttu-id="79fd6-114">Restituisce \_ OK se il metodo recupera una traccia virtuale o S \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="79fd6-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79fd6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="79fd6-115">Remarks</span></span>

<span data-ttu-id="79fd6-116">Se il metodo ha esito positivo, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="79fd6-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="79fd6-117">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="79fd6-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="79fd6-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="79fd6-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="79fd6-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="79fd6-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="79fd6-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="79fd6-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79fd6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79fd6-121">Requirements</span></span>



| <span data-ttu-id="79fd6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fd6-122">Requirement</span></span> | <span data-ttu-id="79fd6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="79fd6-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79fd6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79fd6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="79fd6-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="79fd6-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="79fd6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="79fd6-126">Library</span></span><br/> | <dl> <span data-ttu-id="79fd6-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79fd6-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79fd6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79fd6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fd6-129">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="79fd6-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="79fd6-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="79fd6-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




