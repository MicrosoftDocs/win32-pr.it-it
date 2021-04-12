---
description: Callback che notifica all'host che le fasi della pipeline non sono in grado di restituire i dati mesh per l'evento specificato nella richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: MeshDataNotAvailableCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482581"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="8e8b3-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Metodo IPipeLineStagesCallback:: MeshDataNotAvailableCallback</span><span class="sxs-lookup"><span data-stu-id="8e8b3-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="8e8b3-104">Callback che notifica all'host che le fasi della pipeline non sono in grado di restituire i dati mesh per l'evento specificato nella richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e8b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e8b3-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="8e8b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e8b3-106">Parameters</span></span>

<span data-ttu-id="8e8b3-107">*numberStages* </span><span class="sxs-lookup"><span data-stu-id="8e8b3-107">*numberStages* </span></span>  
<span data-ttu-id="8e8b3-108">Numero di errori di fase restituiti.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-108">The number of stage errors returned.</span></span>

<span data-ttu-id="8e8b3-109">*\_errori count0* </span><span class="sxs-lookup"><span data-stu-id="8e8b3-109">*count0\_errors* </span></span>  
<span data-ttu-id="8e8b3-110">Errori della fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-110">The pipeline stage errors.</span></span>

<span data-ttu-id="8e8b3-111">*Larghezza* </span><span class="sxs-lookup"><span data-stu-id="8e8b3-111">*width* </span></span>  
<span data-ttu-id="8e8b3-112">Larghezza della catena di scambio associata con la chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="8e8b3-113">Viene usato quando si richiedono le immagini di anteprima della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="8e8b3-114">*altezza* </span><span class="sxs-lookup"><span data-stu-id="8e8b3-114">*height* </span></span>  
<span data-ttu-id="8e8b3-115">Altezza della catena di scambio associata con la chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="8e8b3-116">Viene usato quando si richiedono le immagini di anteprima della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="8e8b3-117">*Eid* </span><span class="sxs-lookup"><span data-stu-id="8e8b3-117">*eid* </span></span>  
<span data-ttu-id="8e8b3-118">Evento rappresentato nei risultati.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e8b3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e8b3-119">Return value</span></span>

<span data-ttu-id="8e8b3-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e8b3-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e8b3-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e8b3-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8b3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e8b3-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e8b3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e8b3-123">Header</span></span></p></td><td><span data-ttu-id="8e8b3-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8e8b3-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e8b3-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8e8b3-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e8b3-126">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="8e8b3-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
