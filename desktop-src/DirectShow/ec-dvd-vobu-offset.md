---
description: 'EC_DVD_VOBU_Offset: inviato quando lo strumento di navigazione DVD analizza un pacchetto PCI.'
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119769"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="b2a1e-103">EC \_ DVD \_ VOBU \_ Offset</span><span class="sxs-lookup"><span data-stu-id="b2a1e-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="b2a1e-104">Inviato quando lo strumento [di navigazione DVD](dvd-navigator-filter.md) analizza un pacchetto PCI.</span><span class="sxs-lookup"><span data-stu-id="b2a1e-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2a1e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2a1e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a1e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b2a1e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b2a1e-107">Offset del blocco dell'unità oggetto video (VOBU) più recente.</span><span class="sxs-lookup"><span data-stu-id="b2a1e-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="b2a1e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b2a1e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b2a1e-109">Numero del set di titoli video (VTSN) corrente.</span><span class="sxs-lookup"><span data-stu-id="b2a1e-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2a1e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2a1e-110">Remarks</span></span>

<span data-ttu-id="b2a1e-111">Questo evento è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b2a1e-111">This event is disabled by default.</span></span> <span data-ttu-id="b2a1e-112">Per abilitare questo evento, chiamare [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **\_ DVD EnableLoggingEvents** su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="b2a1e-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a1e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2a1e-113">Requirements</span></span>



| <span data-ttu-id="b2a1e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2a1e-114">Requirement</span></span> | <span data-ttu-id="b2a1e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b2a1e-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a1e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2a1e-116">Header</span></span><br/> | <dl> <span data-ttu-id="b2a1e-117"><dt>Dvdevcode.h (includere Dshow.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2a1e-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2a1e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2a1e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a1e-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="b2a1e-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b2a1e-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="b2a1e-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b2a1e-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b2a1e-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




