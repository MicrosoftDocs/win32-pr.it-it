---
description: Richiesta asincrona di ottenere i frame dell'elenco acquisiti nel log di grafica.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameListRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048917"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="aa54d-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>Metodo IFrameListRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="aa54d-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="aa54d-104">Richiesta asincrona di ottenere i frame dell'elenco acquisiti nel log di grafica.</span><span class="sxs-lookup"><span data-stu-id="aa54d-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa54d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa54d-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="aa54d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa54d-106">Parameters</span></span>

<span data-ttu-id="aa54d-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="aa54d-107">*requestCallback* </span></span>  
<span data-ttu-id="aa54d-108">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="aa54d-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="aa54d-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="aa54d-109">*requestCookie* </span></span>  
<span data-ttu-id="aa54d-110">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="aa54d-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="aa54d-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="aa54d-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="aa54d-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="aa54d-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa54d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa54d-113">Return value</span></span>

<span data-ttu-id="aa54d-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aa54d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa54d-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa54d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa54d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa54d-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aa54d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa54d-117">Header</span></span></p></td><td><span data-ttu-id="aa54d-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aa54d-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aa54d-119"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aa54d-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aa54d-120">**IFrameListRequest**</span><span class="sxs-lookup"><span data-stu-id="aa54d-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 
