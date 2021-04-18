---
description: Richiede un elenco di eventi che generano una modifica nel pixel, nella destinazione di rendering/UAV e nel frame specificati.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixelHistoryRequest2:: RequestIntersections'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521554"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="5d018-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>Metodo IPixelHistoryRequest2:: RequestIntersections</span><span class="sxs-lookup"><span data-stu-id="5d018-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="5d018-104">Richiede un elenco di eventi che generano una modifica nel pixel, nella destinazione di rendering/UAV e nel frame specificati.</span><span class="sxs-lookup"><span data-stu-id="5d018-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d018-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d018-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5d018-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d018-106">Parameters</span></span>

<span data-ttu-id="5d018-107">*NumeroFrame* </span><span class="sxs-lookup"><span data-stu-id="5d018-107">*frameNumber* </span></span>  
<span data-ttu-id="5d018-108">Frame specificato.</span><span class="sxs-lookup"><span data-stu-id="5d018-108">The specified frame.</span></span>

<span data-ttu-id="5d018-109">*pixel* </span><span class="sxs-lookup"><span data-stu-id="5d018-109">*pixel* </span></span>  
<span data-ttu-id="5d018-110">Pixel specificato.</span><span class="sxs-lookup"><span data-stu-id="5d018-110">The specified pixel.</span></span>

<span data-ttu-id="5d018-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="5d018-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="5d018-112">Indirizzo della destinazione di rendering specificata.</span><span class="sxs-lookup"><span data-stu-id="5d018-112">The address of the specified render target</span></span>

<span data-ttu-id="5d018-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="5d018-113">*requestCallback* </span></span>  
<span data-ttu-id="5d018-114">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="5d018-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5d018-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="5d018-115">*requestCookie* </span></span>  
<span data-ttu-id="5d018-116">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="5d018-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5d018-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="5d018-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5d018-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5d018-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d018-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d018-119">Return value</span></span>

<span data-ttu-id="5d018-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d018-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d018-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d018-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d018-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d018-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5d018-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d018-123">Header</span></span></p></td><td><span data-ttu-id="5d018-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5d018-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5d018-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5d018-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5d018-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="5d018-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
