---
description: Richiesta asincrona per ottenere i file di origine associati all'stack di un evento.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISourceFileInfoRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304335"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="8e2c7-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>Metodo ISourceFileInfoRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="8e2c7-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="8e2c7-104">Richiesta asincrona per ottenere i file di origine associati all'stack di un evento.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2c7-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="8e2c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e2c7-106">Parameters</span></span>

<span data-ttu-id="8e2c7-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="8e2c7-107">*eventID* </span></span>  
<span data-ttu-id="8e2c7-108">Evento specificato.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-108">The specified event.</span></span>

<span data-ttu-id="8e2c7-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="8e2c7-109">*requestCallback* </span></span>  
<span data-ttu-id="8e2c7-110">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="8e2c7-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="8e2c7-111">*requestCookie* </span></span>  
<span data-ttu-id="8e2c7-112">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="8e2c7-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="8e2c7-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="8e2c7-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e2c7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e2c7-115">Return value</span></span>

<span data-ttu-id="8e2c7-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e2c7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e2c7-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e2c7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e2c7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e2c7-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e2c7-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e2c7-119">Header</span></span></p></td><td><span data-ttu-id="8e2c7-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8e2c7-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e2c7-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8e2c7-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e2c7-122">**ISourceFileInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="8e2c7-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
