---
description: Il metodo GetFilterGraph Recupera il grafico di filtro creato dal motore di rendering, se disponibile.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Metodo IRenderEngine:: GetFilterGraph (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324416"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="ea61d-103">Metodo IRenderEngine:: GetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="ea61d-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="ea61d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ea61d-104">\[Deprecated.</span></span> <span data-ttu-id="ea61d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ea61d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ea61d-106">Il `GetFilterGraph` metodo recupera il grafico di filtro creato dal motore di rendering, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="ea61d-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea61d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea61d-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="ea61d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea61d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea61d-109">*ppFG* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea61d-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea61d-110">Riceve un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="ea61d-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="ea61d-111">Riceve il valore **null** se non è presente alcun grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="ea61d-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea61d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea61d-112">Return value</span></span>

<span data-ttu-id="ea61d-113">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ea61d-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ea61d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ea61d-114">Return code</span></span>                                                                                            | <span data-ttu-id="ea61d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea61d-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ea61d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea61d-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ea61d-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ea61d-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="ea61d-118"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="ea61d-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="ea61d-119">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="ea61d-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="ea61d-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea61d-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="ea61d-121">Puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="ea61d-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ea61d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea61d-122">Remarks</span></span>

<span data-ttu-id="ea61d-123">Usare il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="ea61d-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="ea61d-124">Per l'anteprima, usare [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) per completare il grafo.</span><span class="sxs-lookup"><span data-stu-id="ea61d-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="ea61d-125">Per l'output del file, connettere il front-end a una combinazione di MUX/file writer.</span><span class="sxs-lookup"><span data-stu-id="ea61d-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="ea61d-126">Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="ea61d-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="ea61d-127">Il grafico risultante può essere eseguito, sospeso, arrestato e cercato; Tuttavia, non è possibile modificare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ea61d-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="ea61d-128">In caso di restituzione, se il valore di *\* ppFG* è diverso da **null**, l'interfaccia **IGraphBuilder** include un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="ea61d-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="ea61d-129">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ea61d-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="ea61d-130">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ea61d-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ea61d-131">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ea61d-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ea61d-132">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ea61d-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea61d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea61d-133">Requirements</span></span>



| <span data-ttu-id="ea61d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea61d-134">Requirement</span></span> | <span data-ttu-id="ea61d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ea61d-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea61d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea61d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ea61d-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea61d-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ea61d-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea61d-138">Library</span></span><br/> | <dl> <span data-ttu-id="ea61d-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea61d-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea61d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea61d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea61d-141">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="ea61d-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="ea61d-142">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ea61d-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




