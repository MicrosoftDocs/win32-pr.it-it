---
description: '<span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Metodo ISingleEventRequest::RequestAsync: non usato.'
MS-HAID: vspixengine.ISingleEventRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo ISingleEventRequest::RequestAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C85CAF18-6953-4C5D-9491-5F5A5F28C580
api_name:
- ISingleEventRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6365614d8a787ea4b252e04ae4e03c4e69ac2283
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107039"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="204f9-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Metodo ISingleEventRequest::RequestAsync</span><span class="sxs-lookup"><span data-stu-id="204f9-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="204f9-104">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="204f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="204f9-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventId,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="204f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="204f9-106">Parameters</span></span>

<span data-ttu-id="204f9-107">*Eventid* </span><span class="sxs-lookup"><span data-stu-id="204f9-107">*eventId* </span></span>  
<span data-ttu-id="204f9-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-108">Not used.</span></span>

<span data-ttu-id="204f9-109">*Numcolumns* </span><span class="sxs-lookup"><span data-stu-id="204f9-109">*numColumns* </span></span>  
<span data-ttu-id="204f9-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-110">Not used.</span></span>

<span data-ttu-id="204f9-111">*colonne \_ count1* </span><span class="sxs-lookup"><span data-stu-id="204f9-111">*count1\_columns* </span></span>  
<span data-ttu-id="204f9-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-112">Not used.</span></span>

<span data-ttu-id="204f9-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="204f9-113">*requestCallback* </span></span>  
<span data-ttu-id="204f9-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-114">Not used.</span></span>

<span data-ttu-id="204f9-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="204f9-115">*requestCookie* </span></span>  
<span data-ttu-id="204f9-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-116">Not used.</span></span>

<span data-ttu-id="204f9-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="204f9-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="204f9-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="204f9-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="204f9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="204f9-119">Return value</span></span>

<span data-ttu-id="204f9-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="204f9-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="204f9-121">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="204f9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="204f9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="204f9-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="204f9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="204f9-123">Header</span></span></p></td><td><span data-ttu-id="204f9-124">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="204f9-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="204f9-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="204f9-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="204f9-126">**ISingleEventRequest**</span><span class="sxs-lookup"><span data-stu-id="204f9-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
