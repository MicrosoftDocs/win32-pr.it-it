---
description: Richiede un elenco di primitive da una particolare intersezione. Per ulteriori informazioni, vedere la funzione membro RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixelHistoryRequest2:: RequestPrimitives'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303952"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="ba392-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>Metodo IPixelHistoryRequest2:: RequestPrimitives</span><span class="sxs-lookup"><span data-stu-id="ba392-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="ba392-105">Richiede un elenco di primitive da una particolare intersezione.</span><span class="sxs-lookup"><span data-stu-id="ba392-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="ba392-106">Per ulteriori informazioni, vedere la funzione membro RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="ba392-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba392-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba392-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ba392-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba392-108">Parameters</span></span>

<span data-ttu-id="ba392-109">*intersezione* </span><span class="sxs-lookup"><span data-stu-id="ba392-109">*intersection* </span></span>  
<span data-ttu-id="ba392-110">Indirizzo dell'intersezione specificata.</span><span class="sxs-lookup"><span data-stu-id="ba392-110">The address of the specified intersection.</span></span>

<span data-ttu-id="ba392-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ba392-111">*requestCallback* </span></span>  
<span data-ttu-id="ba392-112">Indirizzo del callback utilizzato per notificare all'host i risultati.</span><span class="sxs-lookup"><span data-stu-id="ba392-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ba392-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ba392-113">*requestCookie* </span></span>  
<span data-ttu-id="ba392-114">Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.</span><span class="sxs-lookup"><span data-stu-id="ba392-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ba392-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ba392-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ba392-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ba392-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba392-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba392-117">Return value</span></span>

<span data-ttu-id="ba392-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba392-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba392-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba392-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba392-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba392-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ba392-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba392-121">Header</span></span></p></td><td><span data-ttu-id="ba392-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ba392-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ba392-123"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ba392-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ba392-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="ba392-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
