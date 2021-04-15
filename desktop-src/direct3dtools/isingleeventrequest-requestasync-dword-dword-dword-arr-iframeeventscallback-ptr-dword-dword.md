---
description: Non usato.
MS-HAID: vspixengine.ISingleEventRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo ISingleEventRequest:: RequestAsync'
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
ms.openlocfilehash: 6e6c78a7402082e4ca5222038bd3f5bd63c3cf7b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521521"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="d5d4a-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>Metodo ISingleEventRequest:: RequestAsync</span><span class="sxs-lookup"><span data-stu-id="d5d4a-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="d5d4a-104">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d4a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5d4a-105">Syntax</span></span>


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

## <a name="parameters"></a><span data-ttu-id="d5d4a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5d4a-106">Parameters</span></span>

<span data-ttu-id="d5d4a-107">*eventId* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-107">*eventId* </span></span>  
<span data-ttu-id="d5d4a-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-108">Not used.</span></span>

<span data-ttu-id="d5d4a-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-109">*numColumns* </span></span>  
<span data-ttu-id="d5d4a-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-110">Not used.</span></span>

<span data-ttu-id="d5d4a-111">*\_colonne count1* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-111">*count1\_columns* </span></span>  
<span data-ttu-id="d5d4a-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-112">Not used.</span></span>

<span data-ttu-id="d5d4a-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-113">*requestCallback* </span></span>  
<span data-ttu-id="d5d4a-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-114">Not used.</span></span>

<span data-ttu-id="d5d4a-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-115">*requestCookie* </span></span>  
<span data-ttu-id="d5d4a-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-116">Not used.</span></span>

<span data-ttu-id="d5d4a-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d5d4a-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d5d4a-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5d4a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5d4a-119">Return value</span></span>

<span data-ttu-id="d5d4a-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d5d4a-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5d4a-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5d4a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d4a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5d4a-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d5d4a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5d4a-123">Header</span></span></p></td><td><span data-ttu-id="d5d4a-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d5d4a-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d5d4a-125"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d5d4a-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d5d4a-126">**ISingleEventRequest**</span><span class="sxs-lookup"><span data-stu-id="d5d4a-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
