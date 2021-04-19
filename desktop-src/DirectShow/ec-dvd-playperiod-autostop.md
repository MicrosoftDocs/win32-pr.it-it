---
description: Indica che lo strumento di spostamento ha terminato la riproduzione del segmento specificato in una chiamata a IDvdControl2::P layPeriodInTitleAutoStop.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326642"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="33ce1-103">\_autostop \_ PLAYPERIOD DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="33ce1-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="33ce1-104">Indica che lo strumento di spostamento ha terminato la riproduzione del segmento specificato in una chiamata a [**IDVDControl2::P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span><span class="sxs-lookup"><span data-stu-id="33ce1-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="33ce1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="33ce1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ce1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="33ce1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="33ce1-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="33ce1-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="33ce1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="33ce1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="33ce1-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="33ce1-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33ce1-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="33ce1-110">Remarks</span></span>

<span data-ttu-id="33ce1-111">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="33ce1-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="33ce1-112">Questo evento viene inviato anche quando la riproduzione viene annullata prima che lo strumento di spostamento completi la riproduzione del segmento specificato.</span><span class="sxs-lookup"><span data-stu-id="33ce1-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ce1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ce1-113">Requirements</span></span>



| <span data-ttu-id="33ce1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ce1-114">Requirement</span></span> | <span data-ttu-id="33ce1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="33ce1-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ce1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33ce1-116">Header</span></span><br/> | <dl> <span data-ttu-id="33ce1-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33ce1-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ce1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ce1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ce1-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="33ce1-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="33ce1-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="33ce1-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="33ce1-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="33ce1-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="33ce1-122">**IDvdControl2::P layPeriodInTitleAutoStop**</span><span class="sxs-lookup"><span data-stu-id="33ce1-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




