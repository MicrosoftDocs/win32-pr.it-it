---
description: Callback che notifica all'host le informazioni sull'immagine delle fasi della pipeline restituite dalla richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342046"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="66a1e-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>Metodo IPipeLineStagesCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="66a1e-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="66a1e-104">Callback che notifica all'host le informazioni sull'immagine delle fasi della pipeline restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="66a1e-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66a1e-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="66a1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66a1e-106">Parameters</span></span>

<span data-ttu-id="66a1e-107">*stageId* </span><span class="sxs-lookup"><span data-stu-id="66a1e-107">*stageId* </span></span>  
<span data-ttu-id="66a1e-108">Fase della pipeline rappresentata nei risultati.</span><span class="sxs-lookup"><span data-stu-id="66a1e-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="66a1e-109">*Eid* </span><span class="sxs-lookup"><span data-stu-id="66a1e-109">*eid* </span></span>  
<span data-ttu-id="66a1e-110">Evento rappresentato nei risultati.</span><span class="sxs-lookup"><span data-stu-id="66a1e-110">The event represented in the results.</span></span>

<span data-ttu-id="66a1e-111">*Larghezza* </span><span class="sxs-lookup"><span data-stu-id="66a1e-111">*width* </span></span>  
<span data-ttu-id="66a1e-112">Larghezza dell'immagine di visualizzazione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="66a1e-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="66a1e-113">*altezza* </span><span class="sxs-lookup"><span data-stu-id="66a1e-113">*height* </span></span>  
<span data-ttu-id="66a1e-114">Altezza dell'immagine della visualizzazione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="66a1e-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="66a1e-115">*formato* </span><span class="sxs-lookup"><span data-stu-id="66a1e-115">*format* </span></span>  
<span data-ttu-id="66a1e-116">Formato dell'immagine di visualizzazione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="66a1e-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="66a1e-117">*dimensioni* </span><span class="sxs-lookup"><span data-stu-id="66a1e-117">*size* </span></span>  
<span data-ttu-id="66a1e-118">Dimensione dell'immagine in byte.</span><span class="sxs-lookup"><span data-stu-id="66a1e-118">The size of the image in bytes.</span></span>

<span data-ttu-id="66a1e-119">*\_buffer count5* </span><span class="sxs-lookup"><span data-stu-id="66a1e-119">*count5\_buffer* </span></span>  
<span data-ttu-id="66a1e-120">Immagine della visualizzazione della pipeline.</span><span class="sxs-lookup"><span data-stu-id="66a1e-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="66a1e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66a1e-121">Return value</span></span>

<span data-ttu-id="66a1e-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="66a1e-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66a1e-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66a1e-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a1e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66a1e-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="66a1e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66a1e-125">Header</span></span></p></td><td><span data-ttu-id="66a1e-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="66a1e-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="66a1e-127"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="66a1e-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="66a1e-128">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="66a1e-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
