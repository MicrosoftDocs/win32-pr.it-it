---
description: Il metodo SetFilterGraph specifica un grafico di filtro per il motore di rendering da usare.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Metodo IRenderEngine:: SetFilterGraph (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333581"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="f1fd7-103">Metodo IRenderEngine:: SetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="f1fd7-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="f1fd7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-104">\[Deprecated.</span></span> <span data-ttu-id="f1fd7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1fd7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f1fd7-106">Il `SetFilterGraph` metodo specifica un grafico di filtro per il motore di rendering da usare.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fd7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1fd7-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="f1fd7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1fd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1fd7-109">*pFG*</span><span class="sxs-lookup"><span data-stu-id="f1fd7-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="f1fd7-110">Puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1fd7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1fd7-111">Return value</span></span>

<span data-ttu-id="f1fd7-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="f1fd7-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f1fd7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1fd7-113">Return code</span></span>                                                                                            | <span data-ttu-id="f1fd7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1fd7-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f1fd7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd7-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f1fd7-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="f1fd7-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd7-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="f1fd7-118">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="f1fd7-119"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd7-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="f1fd7-120">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1fd7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1fd7-121">Remarks</span></span>

<span data-ttu-id="f1fd7-122">Per la maggior parte delle applicazioni non è necessario chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="f1fd7-123">È più tipico consentire al motore di rendering di compilare il grafo, chiamando il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fd7-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="f1fd7-124">Questo metodo ha esito negativo se il motore di rendering dispone già di un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="f1fd7-125">Non recuperare mai un puntatore a un grafico di filtro creato da un motore di rendering e quindi usarlo come parametro per questo metodo su un altro motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="f1fd7-126">Questa operazione causerà risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="f1fd7-127">Il metodo **ConnectFrontEnd** rimuove qualsiasi grafico filtro esistente, ma mantiene la stessa istanza del gestore del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="f1fd7-128">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1fd7-129">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1fd7-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1fd7-130">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f1fd7-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1fd7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1fd7-131">Requirements</span></span>



| <span data-ttu-id="f1fd7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1fd7-132">Requirement</span></span> | <span data-ttu-id="f1fd7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f1fd7-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1fd7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1fd7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f1fd7-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd7-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f1fd7-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1fd7-136">Library</span></span><br/> | <dl> <span data-ttu-id="f1fd7-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1fd7-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1fd7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1fd7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1fd7-139">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f1fd7-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f1fd7-140">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f1fd7-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




