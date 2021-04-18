---
description: Segnala l'inizio di qualsiasi ancora (PGC, Cell o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325652"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="ae374-103">\_DVD EC \_ ancora \_ acceso</span><span class="sxs-lookup"><span data-stu-id="ae374-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="ae374-104">Segnala l'inizio di qualsiasi ancora (PGC, Cell o VOBU).</span><span class="sxs-lookup"><span data-stu-id="ae374-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="ae374-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae374-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae374-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ae374-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ae374-107">Valore booleano (**bool**) che indica se i pulsanti sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="ae374-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="ae374-108">Zero (0) indica che i pulsanti sono disponibili, quindi il metodo [**IDVDControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="ae374-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="ae374-109">Uno (1) indica che non è disponibile alcun pulsante, pertanto **IDVDControl2:: StillOff** funzionerà.</span><span class="sxs-lookup"><span data-stu-id="ae374-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="ae374-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ae374-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ae374-111">Valore **DWORD** che indica il numero di secondi per cui durerà ancora.</span><span class="sxs-lookup"><span data-stu-id="ae374-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="ae374-112">0xFFFFFFFF indica ancora un infinito, ovvero attendere fino a quando l'utente preme un pulsante o fino a quando l'applicazione non chiama [**IDVDControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span><span class="sxs-lookup"><span data-stu-id="ae374-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae374-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae374-113">Remarks</span></span>

<span data-ttu-id="ae374-114">Tutte le combinazioni di pulsanti sono comunque possibili (i pulsanti accesi rimangono accesi, i pulsanti su con ancora disattivato, il pulsante disattivato con ancora acceso, il pulsante disattivato con ancora disattivato).</span><span class="sxs-lookup"><span data-stu-id="ae374-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="ae374-115">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="ae374-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae374-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae374-116">Requirements</span></span>



| <span data-ttu-id="ae374-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae374-117">Requirement</span></span> | <span data-ttu-id="ae374-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ae374-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae374-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae374-119">Header</span></span><br/> | <dl> <span data-ttu-id="ae374-120"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae374-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae374-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae374-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae374-122">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="ae374-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ae374-123">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="ae374-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ae374-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae374-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




