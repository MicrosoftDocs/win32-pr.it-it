---
description: Richiesta asincrona di ottenere immagini di anteprima per la finestra Fasi pipeline grafica.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521850"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="eaeb8-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>Metodo IPipeLineStagesRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="eaeb8-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="eaeb8-104">Richiesta asincrona di ottenere immagini di anteprima per la finestra Fasi pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaeb8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaeb8-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="eaeb8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaeb8-106">Parameters</span></span>

<span data-ttu-id="eaeb8-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-107">*eventID* </span></span>  
<span data-ttu-id="eaeb8-108">ID dell'evento grafico per cui vengono richieste le immagini.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="eaeb8-109">*numStages* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-109">*numStages* </span></span>  
<span data-ttu-id="eaeb8-110">Numero di fasi della pipeline richieste per le immagini.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="eaeb8-111">*\_stageIds count1* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="eaeb8-112">ID delle fasi della pipeline richieste per le immagini.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="eaeb8-113">*Larghezza* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-113">*width* </span></span>  
<span data-ttu-id="eaeb8-114">Larghezza delle immagini richieste.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-114">The width of the requested images.</span></span>

<span data-ttu-id="eaeb8-115">*altezza* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-115">*height* </span></span>  
<span data-ttu-id="eaeb8-116">Altezza delle immagini richieste.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-116">The height of the requested images.</span></span>

<span data-ttu-id="eaeb8-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-117">*requestCallback* </span></span>  
<span data-ttu-id="eaeb8-118">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="eaeb8-119">*getMeshData* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-119">*getMeshData* </span></span>  
<span data-ttu-id="eaeb8-120">true per restituire i dati mesh; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="eaeb8-121">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-121">*requestCookie* </span></span>  
<span data-ttu-id="eaeb8-122">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="eaeb8-123">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="eaeb8-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="eaeb8-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="eaeb8-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaeb8-125">Return value</span></span>

<span data-ttu-id="eaeb8-126">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eaeb8-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eaeb8-127">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eaeb8-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaeb8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaeb8-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eaeb8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaeb8-129">Header</span></span></p></td><td><span data-ttu-id="eaeb8-130">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eaeb8-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eaeb8-131"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eaeb8-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eaeb8-132">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="eaeb8-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
