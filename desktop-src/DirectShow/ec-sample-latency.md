---
description: Specifica la distanza di pianificazione di un componente per l'elaborazione degli esempi.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324152"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="ed94e-103">\_ \_ latenza campione EC</span><span class="sxs-lookup"><span data-stu-id="ed94e-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="ed94e-104">Specifica la distanza di pianificazione di un componente per l'elaborazione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="ed94e-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed94e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed94e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed94e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ed94e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ed94e-107">(**const reference \_ Time** \* ) la distanza dietro il componente, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="ed94e-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="ed94e-108">Se questo valore è positivo, il componente è dietro la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ed94e-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="ed94e-109">Se questo valore è negativo, il componente precede la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ed94e-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="ed94e-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ed94e-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ed94e-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="ed94e-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ed94e-112">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="ed94e-112">Default Action</span></span>

<span data-ttu-id="ed94e-113">No.</span><span class="sxs-lookup"><span data-stu-id="ed94e-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed94e-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ed94e-114">Remarks</span></span>

<span data-ttu-id="ed94e-115">Un presentatore personalizzato per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) può inviare questo messaggio a EVR per inviare una notifica a EVR se il Presenter è dietro la pianificazione o in anticipo.</span><span class="sxs-lookup"><span data-stu-id="ed94e-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="ed94e-116">Il modo più semplice per calcolare *lParam1* è: *QPC Now*   *QPC target*, dove *QPC ora* è l'ora di clock e *QPC target* è l'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="ed94e-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed94e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed94e-117">Requirements</span></span>



| <span data-ttu-id="ed94e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed94e-118">Requirement</span></span> | <span data-ttu-id="ed94e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ed94e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed94e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed94e-120">Header</span></span><br/> | <dl> <span data-ttu-id="ed94e-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed94e-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed94e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed94e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed94e-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="ed94e-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ed94e-124">Come scrivere un presentatore EVR</span><span class="sxs-lookup"><span data-stu-id="ed94e-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

