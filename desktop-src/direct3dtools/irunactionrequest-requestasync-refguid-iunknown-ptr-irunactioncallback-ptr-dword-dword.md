---
description: Richiesta asincrona di avvio di un'azione (ad esempio, acquisizione di un frame) nel motore.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IRunActionRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125361"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="4a296-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>Metodo IRunActionRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="4a296-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="4a296-104">Richiesta asincrona di avvio di un'azione (ad esempio, acquisizione di un frame) nel motore.</span><span class="sxs-lookup"><span data-stu-id="4a296-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a296-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a296-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4a296-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a296-106">Parameters</span></span>

<span data-ttu-id="4a296-107">*azione* </span><span class="sxs-lookup"><span data-stu-id="4a296-107">*action* </span></span>  
<span data-ttu-id="4a296-108">Azione specificata.</span><span class="sxs-lookup"><span data-stu-id="4a296-108">The specified action.</span></span>

<span data-ttu-id="4a296-109">*actionPayload* </span><span class="sxs-lookup"><span data-stu-id="4a296-109">*actionPayload* </span></span>  
<span data-ttu-id="4a296-110">Payload dell'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="4a296-110">The payload of the specified action.</span></span>

<span data-ttu-id="4a296-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4a296-111">*requestCallback* </span></span>  
<span data-ttu-id="4a296-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="4a296-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4a296-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4a296-113">*requestCookie* </span></span>  
<span data-ttu-id="4a296-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="4a296-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4a296-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4a296-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4a296-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4a296-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a296-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a296-117">Return value</span></span>

<span data-ttu-id="4a296-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a296-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a296-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a296-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a296-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a296-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4a296-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a296-121">Header</span></span></p></td><td><span data-ttu-id="4a296-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4a296-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4a296-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4a296-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4a296-124">**IRunActionRequest**</span><span class="sxs-lookup"><span data-stu-id="4a296-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
