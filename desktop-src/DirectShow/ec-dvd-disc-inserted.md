---
description: Segnala che è stato inserito un disco DVD nell'unità.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327430"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="8fd47-103">\_disco DVD \_ EC \_ inserito</span><span class="sxs-lookup"><span data-stu-id="8fd47-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="8fd47-104">Segnala che è stato inserito un disco DVD nell'unità.</span><span class="sxs-lookup"><span data-stu-id="8fd47-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fd47-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fd47-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8fd47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8fd47-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="8fd47-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="8fd47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8fd47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8fd47-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="8fd47-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fd47-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fd47-110">Remarks</span></span>

<span data-ttu-id="8fd47-111">La riproduzione inizia automaticamente quando viene inserito un disco.</span><span class="sxs-lookup"><span data-stu-id="8fd47-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="8fd47-112">L'applicazione non deve eseguire alcuna azione speciale in risposta a questo evento.</span><span class="sxs-lookup"><span data-stu-id="8fd47-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="8fd47-113">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="8fd47-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd47-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fd47-114">Requirements</span></span>



| <span data-ttu-id="8fd47-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd47-115">Requirement</span></span> | <span data-ttu-id="8fd47-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8fd47-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd47-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fd47-117">Header</span></span><br/> | <dl> <span data-ttu-id="8fd47-118"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fd47-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd47-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fd47-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd47-120">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="8fd47-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8fd47-121">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="8fd47-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8fd47-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8fd47-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




