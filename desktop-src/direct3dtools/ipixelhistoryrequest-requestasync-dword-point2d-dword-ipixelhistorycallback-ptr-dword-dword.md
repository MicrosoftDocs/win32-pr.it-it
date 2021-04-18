---
description: Richiede un elenco di risultati della Cronologia pixel nel pixel specificato, il rendering sincronizzati/UAV e il frame.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixelHistoryRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522729"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="f8810-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>Metodo IPixelHistoryRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="f8810-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="f8810-104">Richiede un elenco di risultati della Cronologia pixel nel pixel specificato, il rendering sincronizzati/UAV e il frame.</span><span class="sxs-lookup"><span data-stu-id="f8810-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8810-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8810-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f8810-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8810-106">Parameters</span></span>

<span data-ttu-id="f8810-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="f8810-107">*frameNumber* </span></span>  
<span data-ttu-id="f8810-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="f8810-108">The specified frame.</span></span>

<span data-ttu-id="f8810-109">*pixel* </span><span class="sxs-lookup"><span data-stu-id="f8810-109">*pixel* </span></span>  
<span data-ttu-id="f8810-110">Pixel specificato.</span><span class="sxs-lookup"><span data-stu-id="f8810-110">The specified pixel.</span></span>

<span data-ttu-id="f8810-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="f8810-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="f8810-112">Destinazione di rendering specificata.</span><span class="sxs-lookup"><span data-stu-id="f8810-112">The specified render target.</span></span>

<span data-ttu-id="f8810-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f8810-113">*requestCallback* </span></span>  
<span data-ttu-id="f8810-114">Indirizzo di un callback utilizzato per notifify l'host dei risultati.</span><span class="sxs-lookup"><span data-stu-id="f8810-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="f8810-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="f8810-115">*requestCookie* </span></span>  
<span data-ttu-id="f8810-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="f8810-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f8810-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="f8810-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f8810-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f8810-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8810-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8810-119">Return value</span></span>

<span data-ttu-id="f8810-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8810-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8810-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8810-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8810-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8810-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8810-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8810-123">Header</span></span></p></td><td><span data-ttu-id="f8810-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f8810-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f8810-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f8810-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f8810-126">**IPixelHistoryRequest**</span><span class="sxs-lookup"><span data-stu-id="f8810-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
