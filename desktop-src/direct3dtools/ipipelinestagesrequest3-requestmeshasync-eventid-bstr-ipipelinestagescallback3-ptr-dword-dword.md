---
description: Richiesta asincrona per ottenere i dati di mesh dall'evento specificato.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesRequest3:: RequestMeshAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303840"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="ae004-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>Metodo IPipeLineStagesRequest3:: RequestMeshAsync</span><span class="sxs-lookup"><span data-stu-id="ae004-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="ae004-104">Richiesta asincrona per ottenere i dati di mesh dall'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="ae004-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae004-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae004-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ae004-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae004-106">Parameters</span></span>

<span data-ttu-id="ae004-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="ae004-107">*eventID* </span></span>  
<span data-ttu-id="ae004-108">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="ae004-108">The specified event.</span></span>

<span data-ttu-id="ae004-109">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="ae004-109">*meshFilename* </span></span>  
<span data-ttu-id="ae004-110">Stringa COM contenente il percorso del file in cui vengono scritti i dati della mesh.</span><span class="sxs-lookup"><span data-stu-id="ae004-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="ae004-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ae004-111">*requestCallback* </span></span>  
<span data-ttu-id="ae004-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="ae004-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ae004-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ae004-113">*requestCookie* </span></span>  
<span data-ttu-id="ae004-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="ae004-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ae004-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ae004-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ae004-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ae004-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae004-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae004-117">Return value</span></span>

<span data-ttu-id="ae004-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae004-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae004-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae004-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae004-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae004-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ae004-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae004-121">Header</span></span></p></td><td><span data-ttu-id="ae004-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ae004-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ae004-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ae004-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ae004-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="ae004-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
