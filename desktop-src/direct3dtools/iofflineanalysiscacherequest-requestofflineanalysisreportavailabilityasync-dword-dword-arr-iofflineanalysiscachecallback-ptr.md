---
description: Richieste di memorizzazione nella cache del report di analisi offline dei frame specificati.
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IOfflineAnalysisCacheRequest:: RequestOfflineAnalysisReportAvailabilityAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522745"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="120e2-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>Metodo IOfflineAnalysisCacheRequest:: RequestOfflineAnalysisReportAvailabilityAsync</span><span class="sxs-lookup"><span data-stu-id="120e2-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="120e2-104">Richieste di memorizzazione nella cache del report di analisi offline dei frame specificati.</span><span class="sxs-lookup"><span data-stu-id="120e2-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="120e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="120e2-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="120e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="120e2-106">Parameters</span></span>

<span data-ttu-id="120e2-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="120e2-107">*numFrames* </span></span>  
<span data-ttu-id="120e2-108">Numero di frame per i quali generare i report di analisi.</span><span class="sxs-lookup"><span data-stu-id="120e2-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="120e2-109">*\_frameNumbers count0* </span><span class="sxs-lookup"><span data-stu-id="120e2-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="120e2-110">Frame specificati.</span><span class="sxs-lookup"><span data-stu-id="120e2-110">The specified frames.</span></span>

<span data-ttu-id="120e2-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="120e2-111">*requestCallback* </span></span>  
<span data-ttu-id="120e2-112">Indirizzo di un callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="120e2-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="120e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="120e2-113">Return value</span></span>

<span data-ttu-id="120e2-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="120e2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="120e2-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="120e2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="120e2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="120e2-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="120e2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="120e2-117">Header</span></span></p></td><td><span data-ttu-id="120e2-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="120e2-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="120e2-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="120e2-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="120e2-120">**IOfflineAnalysisCacheRequest**</span><span class="sxs-lookup"><span data-stu-id="120e2-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
