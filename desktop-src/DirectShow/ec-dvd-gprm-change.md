---
description: Inviato quando viene modificato il valore di un registro parametri generale (GPRM).
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325657"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="5654d-103">\_ \_ Modifica GPRM DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="5654d-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="5654d-104">Inviato quando viene modificato il valore di un registro parametri generale (GPRM).</span><span class="sxs-lookup"><span data-stu-id="5654d-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="5654d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5654d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5654d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5654d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5654d-107">Indice in base zero del valore GPRM modificato.</span><span class="sxs-lookup"><span data-stu-id="5654d-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="5654d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5654d-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5654d-109">I 16 bit inferiori contengono il nuovo valore GPRM.</span><span class="sxs-lookup"><span data-stu-id="5654d-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5654d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5654d-110">Remarks</span></span>

<span data-ttu-id="5654d-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5654d-111">This event is disabled by default.</span></span> <span data-ttu-id="5654d-112">Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.</span><span class="sxs-lookup"><span data-stu-id="5654d-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5654d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5654d-113">Requirements</span></span>



| <span data-ttu-id="5654d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5654d-114">Requirement</span></span> | <span data-ttu-id="5654d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5654d-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5654d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5654d-116">Header</span></span><br/> | <dl> <span data-ttu-id="5654d-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5654d-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5654d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5654d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5654d-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="5654d-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="5654d-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="5654d-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5654d-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5654d-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5654d-122">**IDvdInfo2::GetAllGPRMs**</span><span class="sxs-lookup"><span data-stu-id="5654d-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




