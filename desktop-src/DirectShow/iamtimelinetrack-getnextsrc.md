---
description: Il metodo GetNextSrc Cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Metodo IAMTimelineTrack:: GetNextSrc (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325174"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="5f192-103">Metodo IAMTimelineTrack:: GetNextSrc</span><span class="sxs-lookup"><span data-stu-id="5f192-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="5f192-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5f192-104">\[Deprecated.</span></span> <span data-ttu-id="5f192-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f192-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f192-106">Il `GetNextSrc` metodo cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="5f192-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f192-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f192-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="5f192-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f192-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f192-109">*ppSrc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5f192-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f192-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="5f192-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5f192-111">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="5f192-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="5f192-112">Puntatore a una variabile che contiene l'ora di inizio della ricerca, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="5f192-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="5f192-113">Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine.</span><span class="sxs-lookup"><span data-stu-id="5f192-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="5f192-114">Se il metodo non recupera un'origine, il valore diventa non valido e non deve essere usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f192-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f192-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f192-115">Return value</span></span>

<span data-ttu-id="5f192-116">Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5f192-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f192-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f192-117">Remarks</span></span>

<span data-ttu-id="5f192-118">Se l'ora specificata dalla *piedinatura* è compresa tra l'ora di inizio e di fine di un'origine, il metodo recupera tale origine.</span><span class="sxs-lookup"><span data-stu-id="5f192-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="5f192-119">Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="5f192-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="5f192-120">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5f192-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="5f192-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5f192-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f192-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5f192-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f192-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5f192-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f192-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f192-124">Requirements</span></span>



| <span data-ttu-id="5f192-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f192-125">Requirement</span></span> | <span data-ttu-id="5f192-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5f192-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f192-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f192-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5f192-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f192-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f192-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f192-129">Library</span></span><br/> | <dl> <span data-ttu-id="5f192-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f192-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f192-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f192-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f192-132">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="5f192-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="5f192-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5f192-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




