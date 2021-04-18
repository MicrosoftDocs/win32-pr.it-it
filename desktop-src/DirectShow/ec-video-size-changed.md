---
description: Le dimensioni del video nativo sono state modificate.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328334"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="1f94a-103">\_dimensioni del video EC \_ \_ modificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="1f94a-104">Le dimensioni del video nativo sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="1f94a-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f94a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f94a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f94a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1f94a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1f94a-107">(**DWORD**) WORD di ordine inferiore specifica la nuova larghezza, in pixel; WORD di ordine superiore specifica la nuova altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1f94a-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1f94a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1f94a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1f94a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="1f94a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="1f94a-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="1f94a-110">Default Action</span></span>

<span data-ttu-id="1f94a-111">No.</span><span class="sxs-lookup"><span data-stu-id="1f94a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f94a-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1f94a-112">Remarks</span></span>

<span data-ttu-id="1f94a-113">I renderer video possono inviare questo evento se rilevano una modifica nelle dimensioni del video nativo.</span><span class="sxs-lookup"><span data-stu-id="1f94a-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="1f94a-114">Il [video di mixaggio 7](video-mixing-renderer-filter-7.md) (VMR-7) e il [renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9) inviano questo evento in modalità finestra, ma non in modalità senza finestra o in modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="1f94a-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="1f94a-115">Per ulteriori informazioni sulla modalità finestra in VMR, vedere rendering del [video](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="1f94a-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f94a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f94a-116">Requirements</span></span>



| <span data-ttu-id="1f94a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f94a-117">Requirement</span></span> | <span data-ttu-id="1f94a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1f94a-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f94a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f94a-119">Header</span></span><br/> | <dl> <span data-ttu-id="1f94a-120"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f94a-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f94a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f94a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f94a-122">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="1f94a-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1f94a-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f94a-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




