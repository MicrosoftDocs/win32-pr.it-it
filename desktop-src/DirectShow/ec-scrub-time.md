---
description: Specifica il timestamp per il passaggio del frame più recente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329261"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="70225-103">\_tempo di scrub EC \_</span><span class="sxs-lookup"><span data-stu-id="70225-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="70225-104">Specifica il timestamp per il passaggio del frame più recente.</span><span class="sxs-lookup"><span data-stu-id="70225-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="70225-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="70225-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70225-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="70225-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="70225-107">(**DWORD**) Inferiore 32 bit del timestamp.</span><span class="sxs-lookup"><span data-stu-id="70225-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="70225-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="70225-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="70225-109">(**DWORD**) 32 bit superiori del timestamp.</span><span class="sxs-lookup"><span data-stu-id="70225-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="70225-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="70225-110">Default Action</span></span>

<span data-ttu-id="70225-111">No.</span><span class="sxs-lookup"><span data-stu-id="70225-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="70225-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="70225-112">Remarks</span></span>

<span data-ttu-id="70225-113">Il presentatore per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) Invia questo messaggio al EVR quando completa un passaggio del frame.</span><span class="sxs-lookup"><span data-stu-id="70225-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="70225-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70225-114">Requirements</span></span>



| <span data-ttu-id="70225-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70225-115">Requirement</span></span> | <span data-ttu-id="70225-116">Valore</span><span class="sxs-lookup"><span data-stu-id="70225-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70225-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70225-117">Header</span></span><br/> | <dl> <span data-ttu-id="70225-118"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="70225-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70225-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70225-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70225-120">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="70225-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




