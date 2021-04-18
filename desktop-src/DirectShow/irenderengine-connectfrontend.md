---
description: Il metodo ConnectFrontEnd compila il front-end del grafico di filtro dalla sequenza temporale corrente.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Metodo IRenderEngine:: ConnectFrontEnd (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330396"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="5c7c7-103">Metodo IRenderEngine:: ConnectFrontEnd</span><span class="sxs-lookup"><span data-stu-id="5c7c7-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="5c7c7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-104">\[Deprecated.</span></span> <span data-ttu-id="5c7c7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c7c7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5c7c7-106">Il `ConnectFrontEnd` metodo compila il front-end del grafico di filtro dalla sequenza temporale corrente.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c7c7-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="5c7c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c7c7-108">Parameters</span></span>

<span data-ttu-id="5c7c7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c7c7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c7c7-110">Return value</span></span>

<span data-ttu-id="5c7c7-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c7c7-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5c7c7-112">Tra i possibili valori restituiti sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c7c7-112">Possible return values include the following:</span></span>



| <span data-ttu-id="5c7c7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c7c7-113">Return code</span></span>                                                                                                  | <span data-ttu-id="5c7c7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c7c7-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c7c7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="5c7c7-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="5c7c7-117"><dt>**S \_ avvisa \_ OUTPUTRESET**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="5c7c7-118">Il rendering della parte del grafico è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="5c7c7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="5c7c7-120">Nessuna sequenza temporale impostata per questo motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="5c7c7-121"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="5c7c7-122">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="5c7c7-123"><dt>**\_motore di rendering E \_ \_ \_ danneggiato**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="5c7c7-124">L'operazione non è riuscita perché il rendering del progetto non è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5c7c7-125"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="5c7c7-126">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="5c7c7-127"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="5c7c7-128">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5c7c7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c7c7-129">Remarks</span></span>

<span data-ttu-id="5c7c7-130">Questo metodo non compila la parte di rendering del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="5c7c7-131">L'applicazione deve connettere i pin di output sul front-end ai filtri di rendering desiderati:</span><span class="sxs-lookup"><span data-stu-id="5c7c7-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="5c7c7-132">Per visualizzare l'anteprima, chiamare il metodo [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .</span><span class="sxs-lookup"><span data-stu-id="5c7c7-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="5c7c7-133">Per restituire un file, chiamare [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) per recuperare il pin di output per ogni gruppo, quindi connettere i pin a un filtro multiplexer.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="5c7c7-134">Se si usa il motore di rendering di base, i pin di output sul front-end producono dati non compressi.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="5c7c7-135">Se si usa il motore di rendering intelligente, i pin di output producono dati compressi.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="5c7c7-136">Se si modifica la sequenza temporale dopo aver compilato il grafico del filtro, è necessario chiamare `ConnectFrontEnd` di nuovo per ricompilare il front-end.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="5c7c7-137">Il metodo conserva la parte di rendering del grafo quando possibile.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="5c7c7-138">Tuttavia, se si aggiunge o Elimina un gruppo o si modifica l'ordine dei gruppi, `ConnectFrontEnd` Elimina la parte di rendering e l'applicazione deve ricompilarla.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="5c7c7-139">Se il metodo elimina la parte di rendering, restituisce S \_ WARN \_ OUTPUTRESET.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="5c7c7-140">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c7c7-141">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c7c7-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5c7c7-142">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c7c7-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c7c7-143">Requirements</span></span>



| <span data-ttu-id="5c7c7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7c7-144">Requirement</span></span> | <span data-ttu-id="5c7c7-145">Valore</span><span class="sxs-lookup"><span data-stu-id="5c7c7-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7c7-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c7c7-146">Header</span></span><br/>  | <dl> <span data-ttu-id="5c7c7-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5c7c7-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c7c7-148">Library</span></span><br/> | <dl> <span data-ttu-id="5c7c7-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c7c7-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7c7-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c7c7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7c7-151">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="5c7c7-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="5c7c7-152">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="5c7c7-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




