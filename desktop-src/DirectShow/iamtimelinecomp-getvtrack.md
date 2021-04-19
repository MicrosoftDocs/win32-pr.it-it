---
description: Il metodo GetVTrack recupera la traccia virtuale alla priorità specificata.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'Metodo IAMTimelineComp:: GetVTrack (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332038"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="add3e-103">Metodo IAMTimelineComp:: GetVTrack</span><span class="sxs-lookup"><span data-stu-id="add3e-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="add3e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="add3e-104">\[Deprecated.</span></span> <span data-ttu-id="add3e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="add3e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="add3e-106">Il `GetVTrack` metodo recupera la traccia virtuale alla priorità specificata.</span><span class="sxs-lookup"><span data-stu-id="add3e-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="add3e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="add3e-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="add3e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="add3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add3e-109">*ppVirtualTrack* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="add3e-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="add3e-110">Riceve l'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale.</span><span class="sxs-lookup"><span data-stu-id="add3e-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="add3e-111">*Che*</span><span class="sxs-lookup"><span data-stu-id="add3e-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="add3e-112">Priorità della traccia virtuale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="add3e-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add3e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="add3e-113">Return value</span></span>

<span data-ttu-id="add3e-114">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="add3e-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="add3e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="add3e-115">Return code</span></span>                                                                                  | <span data-ttu-id="add3e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="add3e-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="add3e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="add3e-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="add3e-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="add3e-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="add3e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="add3e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="add3e-120">Nessuna traccia virtuale con la priorità specificata.</span><span class="sxs-lookup"><span data-stu-id="add3e-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="add3e-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="add3e-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="add3e-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="add3e-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="add3e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="add3e-123">Remarks</span></span>

<span data-ttu-id="add3e-124">Se il metodo ha esito positivo, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="add3e-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="add3e-125">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="add3e-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="add3e-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="add3e-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="add3e-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="add3e-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="add3e-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="add3e-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="add3e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add3e-129">Requirements</span></span>



| <span data-ttu-id="add3e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="add3e-130">Requirement</span></span> | <span data-ttu-id="add3e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="add3e-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="add3e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="add3e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="add3e-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="add3e-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="add3e-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="add3e-134">Library</span></span><br/> | <dl> <span data-ttu-id="add3e-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="add3e-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add3e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="add3e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add3e-137">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="add3e-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="add3e-138">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="add3e-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




