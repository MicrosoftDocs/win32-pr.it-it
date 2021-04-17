---
description: Callback che notifica all'host le fasi della pipeline utilizzate dalla chiamata di richiamo della richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: GetSupportedStages'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521137"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="cf9bf-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Metodo IPipeLineStagesCallback:: GetSupportedStages</span><span class="sxs-lookup"><span data-stu-id="cf9bf-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="cf9bf-104">Callback che notifica all'host le fasi della pipeline utilizzate dalla chiamata di richiamo della richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf9bf-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="cf9bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf9bf-106">Parameters</span></span>

<span data-ttu-id="cf9bf-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="cf9bf-107">*numColumns* </span></span>  
<span data-ttu-id="cf9bf-108">Numero di fasi restituite.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-108">The number of stages returned.</span></span>

<span data-ttu-id="cf9bf-109">*\_pStages count0* </span><span class="sxs-lookup"><span data-stu-id="cf9bf-109">*count0\_pStages* </span></span>  
<span data-ttu-id="cf9bf-110">Fasi della pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-110">The pipeline stages.</span></span>

<span data-ttu-id="cf9bf-111">*swapChainWidth* </span><span class="sxs-lookup"><span data-stu-id="cf9bf-111">*swapChainWidth* </span></span>  
<span data-ttu-id="cf9bf-112">Larghezza della catena di scambio associata con la chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="cf9bf-113">Viene usato quando si richiedono le immagini di anteprima della pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="cf9bf-114">*swapChainHeight* </span><span class="sxs-lookup"><span data-stu-id="cf9bf-114">*swapChainHeight* </span></span>  
<span data-ttu-id="cf9bf-115">Altezza della catena di scambio associata con la chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="cf9bf-116">Viene usato quando si richiedono le immagini di anteprima della pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf9bf-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf9bf-117">Return value</span></span>

<span data-ttu-id="cf9bf-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cf9bf-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf9bf-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf9bf-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9bf-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf9bf-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cf9bf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf9bf-121">Header</span></span></p></td><td><span data-ttu-id="cf9bf-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cf9bf-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cf9bf-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cf9bf-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cf9bf-124">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="cf9bf-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
