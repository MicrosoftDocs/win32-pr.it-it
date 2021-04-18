---
description: Segnala che un pulsante di menu DVD è stato attivato automaticamente per istruzioni sul disco. Questo errore si verifica quando si verifica il timeout di un menu e il disco ha specificato un pulsante da attivare automaticamente.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331284"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="d488f-103">\_pulsante DVD \_ EC \_ \_ attivato automaticamente</span><span class="sxs-lookup"><span data-stu-id="d488f-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="d488f-104">Segnala che un pulsante di menu DVD è stato attivato automaticamente per istruzioni sul disco. Questo errore si verifica quando si verifica il timeout di un menu e il disco ha specificato un pulsante da attivare automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d488f-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="d488f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d488f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d488f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d488f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d488f-107">Valore **DWORD** che indica il pulsante attivato.</span><span class="sxs-lookup"><span data-stu-id="d488f-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="d488f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d488f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d488f-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="d488f-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="d488f-110">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="d488f-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d488f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d488f-111">Requirements</span></span>



| <span data-ttu-id="d488f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d488f-112">Requirement</span></span> | <span data-ttu-id="d488f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d488f-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d488f-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d488f-114">Header</span></span><br/> | <dl> <span data-ttu-id="d488f-115"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d488f-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d488f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d488f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d488f-117">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="d488f-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d488f-118">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="d488f-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d488f-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d488f-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




