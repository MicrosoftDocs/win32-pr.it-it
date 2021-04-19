---
description: Segnala che è stato rimosso un disco DVD.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327436"
---
# <a name="ec_dvd_disc_ejected"></a><span data-ttu-id="d777b-103">\_disco DVD \_ EC \_ rimosso</span><span class="sxs-lookup"><span data-stu-id="d777b-103">EC\_DVD\_DISC\_EJECTED</span></span>

<span data-ttu-id="d777b-104">Segnala che è stato rimosso un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="d777b-104">Signals that a DVD disc was ejected.</span></span>

## <a name="parameters"></a><span data-ttu-id="d777b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d777b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d777b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d777b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d777b-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="d777b-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="d777b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d777b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d777b-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="d777b-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d777b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d777b-110">Remarks</span></span>

<span data-ttu-id="d777b-111">La riproduzione viene arrestata automaticamente quando viene espulso un disco.</span><span class="sxs-lookup"><span data-stu-id="d777b-111">Playback automatically stops when a disc is ejected.</span></span> <span data-ttu-id="d777b-112">L'applicazione non deve eseguire alcuna azione speciale in risposta a questo evento.</span><span class="sxs-lookup"><span data-stu-id="d777b-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="d777b-113">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="d777b-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d777b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d777b-114">Requirements</span></span>



| <span data-ttu-id="d777b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d777b-115">Requirement</span></span> | <span data-ttu-id="d777b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d777b-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d777b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d777b-117">Header</span></span><br/> | <dl> <span data-ttu-id="d777b-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d777b-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d777b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d777b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d777b-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="d777b-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d777b-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="d777b-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d777b-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d777b-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




