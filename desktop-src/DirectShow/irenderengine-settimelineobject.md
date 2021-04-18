---
description: Il metodo SetTimelineObject imposta la sequenza temporale per il motore di rendering da usare.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'Metodo IRenderEngine:: SetTimelineObject (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330779"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="89382-103">Metodo IRenderEngine:: SetTimelineObject</span><span class="sxs-lookup"><span data-stu-id="89382-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="89382-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="89382-104">\[Deprecated.</span></span> <span data-ttu-id="89382-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="89382-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="89382-106">Il `SetTimelineObject` metodo imposta la sequenza temporale per il motore di rendering da usare.</span><span class="sxs-lookup"><span data-stu-id="89382-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="89382-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89382-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="89382-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89382-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89382-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="89382-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="89382-110">Puntatore all'interfaccia [**IAMTimeline**](iamtimeline.md) dell'oggetto della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="89382-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89382-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89382-111">Return value</span></span>

<span data-ttu-id="89382-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="89382-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="89382-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="89382-113">Return code</span></span>                                                                                            | <span data-ttu-id="89382-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89382-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="89382-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89382-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="89382-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="89382-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="89382-117"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="89382-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="89382-118">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="89382-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="89382-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="89382-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="89382-120">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="89382-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="89382-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="89382-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="89382-122">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="89382-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="89382-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="89382-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="89382-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="89382-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="89382-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="89382-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="89382-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="89382-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="89382-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89382-127">Requirements</span></span>



| <span data-ttu-id="89382-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="89382-128">Requirement</span></span> | <span data-ttu-id="89382-129">Valore</span><span class="sxs-lookup"><span data-stu-id="89382-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89382-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89382-130">Header</span></span><br/>  | <dl> <span data-ttu-id="89382-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="89382-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="89382-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="89382-132">Library</span></span><br/> | <dl> <span data-ttu-id="89382-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89382-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89382-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89382-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89382-135">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="89382-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="89382-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="89382-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




