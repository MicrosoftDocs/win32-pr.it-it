---
description: Il metodo GetRecursiveLayerOfType esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera l'ennesima traccia virtuale dall'ordinamento.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Metodo IAMTimelineComp:: GetRecursiveLayerOfType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332039"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="38bfa-103">Metodo IAMTimelineComp:: GetRecursiveLayerOfType</span><span class="sxs-lookup"><span data-stu-id="38bfa-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="38bfa-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="38bfa-104">\[Deprecated.</span></span> <span data-ttu-id="38bfa-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38bfa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38bfa-106">Il `GetRecursiveLayerOfType` metodo esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera la traccia virtuale *n* dall'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38bfa-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="38bfa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38bfa-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="38bfa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38bfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38bfa-109">*ppVirtualTrack* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38bfa-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38bfa-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della traccia virtuale.</span><span class="sxs-lookup"><span data-stu-id="38bfa-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="38bfa-111">*WhichLayer*</span><span class="sxs-lookup"><span data-stu-id="38bfa-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="38bfa-112">Specifica la traccia virtuale da recuperare, indicizzata da zero.</span><span class="sxs-lookup"><span data-stu-id="38bfa-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="38bfa-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="38bfa-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="38bfa-114">Membro del tipo [**di \_ \_ tipo principale della sequenza temporale**](timeline-major-type.md) enumerato che specifica se includere tracce nella ricerca.</span><span class="sxs-lookup"><span data-stu-id="38bfa-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38bfa-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38bfa-115">Return value</span></span>

<span data-ttu-id="38bfa-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="38bfa-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="38bfa-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="38bfa-117">Return code</span></span>                                                                                  | <span data-ttu-id="38bfa-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38bfa-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="38bfa-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38bfa-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="38bfa-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="38bfa-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="38bfa-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38bfa-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="38bfa-122">Nessun oggetto del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="38bfa-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="38bfa-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="38bfa-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="38bfa-124">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="38bfa-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="38bfa-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="38bfa-125">Remarks</span></span>

<span data-ttu-id="38bfa-126">In genere, un'applicazione non deve chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="38bfa-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="38bfa-127">Se il parametro di *tipo* è una sequenza temporale di \_ \_ tipo principale \_ , il primo ordine di profondità include le tracce.</span><span class="sxs-lookup"><span data-stu-id="38bfa-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="38bfa-128">In caso contrario, include solo le composizioni e i gruppi.</span><span class="sxs-lookup"><span data-stu-id="38bfa-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="38bfa-129">L'oggetto stesso è incluso nell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38bfa-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="38bfa-130">Nella disposizione seguente, ad esempio, a partire dalla composizione A, l'ordinamento sarà B, C, F, D, E, A.</span><span class="sxs-lookup"><span data-stu-id="38bfa-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="38bfa-132">Se il metodo ha esito positivo, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="38bfa-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="38bfa-133">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="38bfa-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="38bfa-134">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="38bfa-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38bfa-135">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="38bfa-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38bfa-136">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="38bfa-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38bfa-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38bfa-137">Requirements</span></span>



| <span data-ttu-id="38bfa-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="38bfa-138">Requirement</span></span> | <span data-ttu-id="38bfa-139">Valore</span><span class="sxs-lookup"><span data-stu-id="38bfa-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38bfa-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38bfa-140">Header</span></span><br/>  | <dl> <span data-ttu-id="38bfa-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="38bfa-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38bfa-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="38bfa-142">Library</span></span><br/> | <dl> <span data-ttu-id="38bfa-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38bfa-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38bfa-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38bfa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38bfa-145">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="38bfa-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="38bfa-146">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="38bfa-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




