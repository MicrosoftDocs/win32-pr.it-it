---
description: Il metodo GetTimelineObject recupera la sequenza temporale attualmente utilizzata dal motore di rendering.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Metodo IRenderEngine:: GetTimelineObject (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330796"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="5a4e7-103">Metodo IRenderEngine:: GetTimelineObject</span><span class="sxs-lookup"><span data-stu-id="5a4e7-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="5a4e7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-104">\[Deprecated.</span></span> <span data-ttu-id="5a4e7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a4e7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a4e7-106">Il `GetTimelineObject` metodo recupera la sequenza temporale attualmente utilizzata dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a4e7-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="5a4e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a4e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a4e7-109">*ppTimeline* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a4e7-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4e7-110">Riceve un puntatore all'interfaccia [**IAMTimeline**](iamtimeline.md) della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="5a4e7-111">Riceve il valore **null** se non è presente alcuna sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a4e7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a4e7-112">Return value</span></span>

<span data-ttu-id="5a4e7-113">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="5a4e7-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="5a4e7-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a4e7-114">Return code</span></span>                                                                                            | <span data-ttu-id="5a4e7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a4e7-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5a4e7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e7-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="5a4e7-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="5a4e7-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e7-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="5a4e7-119">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="5a4e7-120"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e7-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="5a4e7-121">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a4e7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a4e7-122">Remarks</span></span>

<span data-ttu-id="5a4e7-123">In caso di restituzione, se il valore di *\* ppTimeline* è diverso da **null**, l'interfaccia **IAMTimeline** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="5a4e7-124">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="5a4e7-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a4e7-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a4e7-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a4e7-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5a4e7-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a4e7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a4e7-128">Requirements</span></span>



| <span data-ttu-id="5a4e7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a4e7-129">Requirement</span></span> | <span data-ttu-id="5a4e7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5a4e7-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a4e7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5a4e7-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e7-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a4e7-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a4e7-133">Library</span></span><br/> | <dl> <span data-ttu-id="5a4e7-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e7-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a4e7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a4e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4e7-136">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="5a4e7-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="5a4e7-137">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5a4e7-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




