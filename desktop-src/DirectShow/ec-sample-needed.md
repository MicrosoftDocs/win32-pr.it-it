---
description: Richiede un nuovo esempio di input dal filtro renderer video avanzato (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324149"
---
# <a name="ec_sample_needed"></a><span data-ttu-id="edbee-103">\_esempio EC \_ necessario</span><span class="sxs-lookup"><span data-stu-id="edbee-103">EC\_SAMPLE\_NEEDED</span></span>

<span data-ttu-id="edbee-104">Richiede un nuovo esempio di input dal filtro [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="edbee-104">Requests a new input sample from the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="edbee-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="edbee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbee-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="edbee-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="edbee-107">Identificatore del flusso di input che necessita di un nuovo input.</span><span class="sxs-lookup"><span data-stu-id="edbee-107">Identifier of the input stream that needs new input.</span></span>

</dd> <dt>

<span data-ttu-id="edbee-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="edbee-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="edbee-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="edbee-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="edbee-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="edbee-110">Default Action</span></span>

<span data-ttu-id="edbee-111">No.</span><span class="sxs-lookup"><span data-stu-id="edbee-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbee-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="edbee-112">Remarks</span></span>

<span data-ttu-id="edbee-113">Il mixer per il filtro EVR Invia questo messaggio quando è necessario un nuovo esempio di input.</span><span class="sxs-lookup"><span data-stu-id="edbee-113">The mixer for the EVR filter sends this message when it needs a new input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbee-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edbee-114">Requirements</span></span>



| <span data-ttu-id="edbee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbee-115">Requirement</span></span> | <span data-ttu-id="edbee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="edbee-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="edbee-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edbee-117">Header</span></span><br/> | <dl> <span data-ttu-id="edbee-118"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="edbee-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbee-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edbee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbee-120">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="edbee-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




