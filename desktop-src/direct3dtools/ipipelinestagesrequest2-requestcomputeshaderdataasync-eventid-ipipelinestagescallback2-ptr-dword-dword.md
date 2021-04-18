---
description: Richiesta asincrona per ottenere i dati di compute shader per la distribuzione specificata.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest2:: RequestComputeShaderDataAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304308"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="21a94-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest2:: RequestComputeShaderDataAsync</span><span class="sxs-lookup"><span data-stu-id="21a94-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="21a94-104">Richiesta asincrona per ottenere i dati di compute shader per la distribuzione specificata.</span><span class="sxs-lookup"><span data-stu-id="21a94-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21a94-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="21a94-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21a94-106">Parameters</span></span>

<span data-ttu-id="21a94-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="21a94-107">*eventID* </span></span>  
<span data-ttu-id="21a94-108">Evento di invio specificato.</span><span class="sxs-lookup"><span data-stu-id="21a94-108">The specified dispatch event.</span></span>

<span data-ttu-id="21a94-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="21a94-109">*requestCallback* </span></span>  
<span data-ttu-id="21a94-110">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="21a94-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="21a94-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="21a94-111">*requestCookie* </span></span>  
<span data-ttu-id="21a94-112">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="21a94-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="21a94-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="21a94-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="21a94-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="21a94-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="21a94-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21a94-115">Return value</span></span>

<span data-ttu-id="21a94-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21a94-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21a94-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21a94-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a94-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21a94-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="21a94-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21a94-119">Header</span></span></p></td><td><span data-ttu-id="21a94-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="21a94-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="21a94-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="21a94-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="21a94-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="21a94-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
