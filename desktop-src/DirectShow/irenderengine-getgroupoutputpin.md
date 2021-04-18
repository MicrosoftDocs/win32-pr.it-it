---
description: Il metodo GetGroupOutputPin Recupera il pin di output per il gruppo specificato.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Metodo IRenderEngine:: GetGroupOutputPin (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330394"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="10641-103">Metodo IRenderEngine:: GetGroupOutputPin</span><span class="sxs-lookup"><span data-stu-id="10641-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="10641-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="10641-104">\[Deprecated.</span></span> <span data-ttu-id="10641-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10641-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="10641-106">Il `GetGroupOutputPin` metodo recupera il pin di output per il gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="10641-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="10641-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10641-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="10641-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10641-109">*Gruppo*</span><span class="sxs-lookup"><span data-stu-id="10641-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="10641-110">Indice in base zero che specifica il gruppo.</span><span class="sxs-lookup"><span data-stu-id="10641-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="10641-111">*ppRenderPin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="10641-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10641-112">Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="10641-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10641-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10641-113">Return value</span></span>

<span data-ttu-id="10641-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10641-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="10641-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10641-115">Possible values include the following:</span></span>



| <span data-ttu-id="10641-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="10641-116">Return code</span></span>                                                                                                  | <span data-ttu-id="10641-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10641-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10641-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="10641-119">Il gruppo non ha un pin di output.</span><span class="sxs-lookup"><span data-stu-id="10641-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="10641-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="10641-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="10641-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="10641-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="10641-123">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="10641-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="10641-124"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="10641-125">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="10641-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="10641-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="10641-127">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="10641-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="10641-128"><dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="10641-129">L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="10641-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="10641-130"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="10641-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="10641-131">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="10641-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="10641-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="10641-132">Remarks</span></span>

<span data-ttu-id="10641-133">Prima di chiamare questo metodo, chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafo.</span><span class="sxs-lookup"><span data-stu-id="10641-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="10641-134">Ogni gruppo rappresenta un singolo flusso multimediale e il front-end ha un pin di output corrispondente.</span><span class="sxs-lookup"><span data-stu-id="10641-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="10641-135">È possibile utilizzare questo metodo per creare la parte di rendering di un grafo di scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="10641-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="10641-136">Connettere i pin di output ai filtri multiplexer e ai filtri del writer di file.</span><span class="sxs-lookup"><span data-stu-id="10641-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="10641-137">Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="10641-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="10641-138">Per l'anteprima, non è necessario chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="10641-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="10641-139">È sufficiente chiamare **ConnectFrontEnd** seguito da [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="10641-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="10641-140">Se il metodo restituisce S \_ OK, l'interfaccia **Ipin** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="10641-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="10641-141">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="10641-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="10641-142">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="10641-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="10641-143">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="10641-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="10641-144">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="10641-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10641-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10641-145">Requirements</span></span>



| <span data-ttu-id="10641-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="10641-146">Requirement</span></span> | <span data-ttu-id="10641-147">Valore</span><span class="sxs-lookup"><span data-stu-id="10641-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10641-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10641-148">Header</span></span><br/>  | <dl> <span data-ttu-id="10641-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="10641-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="10641-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="10641-150">Library</span></span><br/> | <dl> <span data-ttu-id="10641-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10641-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10641-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10641-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10641-153">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="10641-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="10641-154">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="10641-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




