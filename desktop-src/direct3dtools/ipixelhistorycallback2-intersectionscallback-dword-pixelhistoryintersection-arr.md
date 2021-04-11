---
description: Callback che notifica all'host le informazioni di intersezione della Cronologia pixel restituite dalla richiesta associata.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPixelHistoryCallback2:: IntersectionsCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124344"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="131ff-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>Metodo IPixelHistoryCallback2:: IntersectionsCallback</span><span class="sxs-lookup"><span data-stu-id="131ff-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="131ff-104">Callback che notifica all'host le informazioni di intersezione della Cronologia pixel restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="131ff-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="131ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="131ff-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="131ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="131ff-106">Parameters</span></span>

<span data-ttu-id="131ff-107">*conteggio* </span><span class="sxs-lookup"><span data-stu-id="131ff-107">*count* </span></span>  
<span data-ttu-id="131ff-108">Numero di intersezioni di Cronologia pixel.</span><span class="sxs-lookup"><span data-stu-id="131ff-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="131ff-109">*intersezioni count0 \_* </span><span class="sxs-lookup"><span data-stu-id="131ff-109">*count0\_intersections* </span></span>  
<span data-ttu-id="131ff-110">Intersezioni della Cronologia pixel.</span><span class="sxs-lookup"><span data-stu-id="131ff-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="131ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="131ff-111">Return value</span></span>

<span data-ttu-id="131ff-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="131ff-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="131ff-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="131ff-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="131ff-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="131ff-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="131ff-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="131ff-115">Header</span></span></p></td><td><span data-ttu-id="131ff-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="131ff-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="131ff-117"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="131ff-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="131ff-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="131ff-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
