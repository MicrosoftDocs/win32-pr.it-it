---
description: Richiesta asincrona di ottenere lo stack di chiamate RVA (relativi indirizzi virtuali) dell'evento specificato.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ICallStackRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225417"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="18d04-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>Metodo ICallStackRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="18d04-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="18d04-104">Richiesta asincrona di ottenere lo stack di chiamate RVA (relativi indirizzi virtuali) dell'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="18d04-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18d04-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="18d04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18d04-106">Parameters</span></span>

<span data-ttu-id="18d04-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="18d04-107">*eventID* </span></span>  
<span data-ttu-id="18d04-108">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="18d04-108">The specified event.</span></span>

<span data-ttu-id="18d04-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="18d04-109">*requestCallback* </span></span>  
<span data-ttu-id="18d04-110">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="18d04-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="18d04-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="18d04-111">*requestCookie* </span></span>  
<span data-ttu-id="18d04-112">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="18d04-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="18d04-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="18d04-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="18d04-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="18d04-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="18d04-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18d04-115">Return value</span></span>

<span data-ttu-id="18d04-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="18d04-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18d04-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18d04-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d04-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18d04-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="18d04-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18d04-119">Header</span></span></p></td><td><span data-ttu-id="18d04-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="18d04-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="18d04-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18d04-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="18d04-122">**ICallStackRequest**</span><span class="sxs-lookup"><span data-stu-id="18d04-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
