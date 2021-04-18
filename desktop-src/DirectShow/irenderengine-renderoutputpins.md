---
description: Il metodo RenderOutputPins crea la parte in anteprima del grafico del filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Metodo IRenderEngine:: RenderOutputPins (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330791"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="5a089-103">Metodo IRenderEngine:: RenderOutputPins</span><span class="sxs-lookup"><span data-stu-id="5a089-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="5a089-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5a089-104">\[Deprecated.</span></span> <span data-ttu-id="5a089-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a089-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5a089-106">Il `RenderOutputPins` metodo crea la parte in anteprima del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="5a089-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a089-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a089-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="5a089-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a089-108">Parameters</span></span>

<span data-ttu-id="5a089-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5a089-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a089-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a089-110">Return value</span></span>

<span data-ttu-id="5a089-111">Restituisce valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a089-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="5a089-112">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="5a089-112">The following are possible values:</span></span>



| <span data-ttu-id="5a089-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a089-113">Return code</span></span>                                                                                                  | <span data-ttu-id="5a089-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a089-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a089-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="5a089-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a089-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5a089-117"><dt>**\_non è \_ stato \_ eseguito il rendering dell'audio di \_ VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="5a089-118">Non è possibile riprodurre il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="5a089-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="5a089-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="5a089-120">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="5a089-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="5a089-121"><dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="5a089-122">L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5a089-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5a089-123"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="5a089-124">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5a089-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="5a089-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a089-125">Remarks</span></span>

<span data-ttu-id="5a089-126">Prima di chiamare questo metodo, chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo.</span><span class="sxs-lookup"><span data-stu-id="5a089-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="5a089-127">Per eseguire un'operazione diversa dall'anteprima, non chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5a089-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="5a089-128">In alternativa, chiamare [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per ottenere i puntatori ai pin di output.</span><span class="sxs-lookup"><span data-stu-id="5a089-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="5a089-129">Se non è presente alcuna scheda audio nel computer dell'utente, questo metodo restituisce l'audio VFW non sottoposto a \_ \_ \_ \_ rendering.</span><span class="sxs-lookup"><span data-stu-id="5a089-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="5a089-130">In questo caso non sarà presente un'anteprima audio, ma l'anteprima video non è interessata.</span><span class="sxs-lookup"><span data-stu-id="5a089-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="5a089-131">Se il PIN è da un gruppo video, questo metodo crea una finestra video.</span><span class="sxs-lookup"><span data-stu-id="5a089-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="5a089-132">Il thread chiamante deve inviare messaggi, ad esempio per spostare la finestra o rispondere ai clic del mouse nell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="5a089-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="5a089-133">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5a089-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5a089-134">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5a089-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5a089-135">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5a089-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5a089-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a089-136">Requirements</span></span>



| <span data-ttu-id="5a089-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a089-137">Requirement</span></span> | <span data-ttu-id="5a089-138">Valore</span><span class="sxs-lookup"><span data-stu-id="5a089-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a089-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a089-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5a089-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5a089-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a089-141">Library</span></span><br/> | <dl> <span data-ttu-id="5a089-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a089-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a089-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a089-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a089-144">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="5a089-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="5a089-145">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5a089-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




