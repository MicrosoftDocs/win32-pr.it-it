---
description: Inviato quando viene modificato il valore di un registro di parametri di sistema (SPRM).
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325653"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="28c00-103">\_ \_ Modifica SPRM DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="28c00-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="28c00-104">Inviato quando viene modificato il valore di un registro di parametri di sistema (SPRM).</span><span class="sxs-lookup"><span data-stu-id="28c00-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="28c00-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="28c00-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="28c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="28c00-107">Indice in base zero del valore SPRM modificato.</span><span class="sxs-lookup"><span data-stu-id="28c00-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="28c00-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="28c00-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="28c00-109">I 16 bit inferiori contengono il nuovo valore SPRM.</span><span class="sxs-lookup"><span data-stu-id="28c00-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28c00-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="28c00-110">Remarks</span></span>

<span data-ttu-id="28c00-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="28c00-111">This event is disabled by default.</span></span> <span data-ttu-id="28c00-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="28c00-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28c00-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28c00-113">Requirements</span></span>



| <span data-ttu-id="28c00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c00-114">Requirement</span></span> | <span data-ttu-id="28c00-115">Valore</span><span class="sxs-lookup"><span data-stu-id="28c00-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c00-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28c00-116">Header</span></span><br/> | <dl> <span data-ttu-id="28c00-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28c00-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c00-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28c00-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c00-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="28c00-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="28c00-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="28c00-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="28c00-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="28c00-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="28c00-122">**IDvdInfo2::GetAllSPRMs**</span><span class="sxs-lookup"><span data-stu-id="28c00-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




