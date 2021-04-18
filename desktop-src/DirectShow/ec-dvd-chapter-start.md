---
description: Segnala che il lettore DVD ha avviato la riproduzione di un nuovo programma nel \_ dominio del titolo del dominio DVD \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325187"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="06666-103">\_inizio del \_ capitolo del DVD EC \_</span><span class="sxs-lookup"><span data-stu-id="06666-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="06666-104">Segnala che il lettore DVD ha avviato la riproduzione di un nuovo programma nel \_ dominio del titolo del dominio DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="06666-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="06666-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="06666-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06666-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="06666-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="06666-107">Valore **DWORD** che indica il nuovo numero di capitolo (programma).</span><span class="sxs-lookup"><span data-stu-id="06666-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="06666-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="06666-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="06666-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="06666-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06666-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="06666-110">Remarks</span></span>

<span data-ttu-id="06666-111">Solo i film lineari semplici segnalano questo evento.</span><span class="sxs-lookup"><span data-stu-id="06666-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="06666-112">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="06666-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="06666-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06666-113">Requirements</span></span>



| <span data-ttu-id="06666-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="06666-114">Requirement</span></span> | <span data-ttu-id="06666-115">Valore</span><span class="sxs-lookup"><span data-stu-id="06666-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06666-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06666-116">Header</span></span><br/> | <dl> <span data-ttu-id="06666-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06666-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06666-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06666-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06666-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="06666-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="06666-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="06666-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="06666-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="06666-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="06666-122">**\_Enumerazione del dominio DVD**</span><span class="sxs-lookup"><span data-stu-id="06666-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




