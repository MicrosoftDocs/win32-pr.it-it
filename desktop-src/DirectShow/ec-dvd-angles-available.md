---
description: Indica se un blocco angolo viene riprodotto e le modifiche dell'angolo possono essere eseguite.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331111"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="d9b73-103">\_angoli DVD \_ EC \_ disponibili</span><span class="sxs-lookup"><span data-stu-id="d9b73-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="d9b73-104">Indica se un blocco angolo viene riprodotto e le modifiche dell'angolo possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="d9b73-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9b73-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9b73-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b73-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d9b73-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d9b73-107">Valore booleano (**bool**) che indica se un blocco angolo viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="d9b73-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="d9b73-108">Zero (0) indica che la riproduzione non è in un blocco angolo e gli angoli non sono disponibili, uno (1) indica che viene riprodotto un blocco angolo e che possono essere eseguite modifiche dell'angolo.</span><span class="sxs-lookup"><span data-stu-id="d9b73-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="d9b73-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d9b73-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d9b73-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="d9b73-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9b73-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9b73-111">Remarks</span></span>

<span data-ttu-id="d9b73-112">Le modifiche apportate all'angolo non sono limitate ai blocchi angolari e la manifestazione della modifica dell'angolo può essere visualizzata solo in un blocco di angoli.</span><span class="sxs-lookup"><span data-stu-id="d9b73-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b73-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b73-113">Requirements</span></span>



| <span data-ttu-id="d9b73-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b73-114">Requirement</span></span> | <span data-ttu-id="d9b73-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b73-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b73-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9b73-116">Header</span></span><br/> | <dl> <span data-ttu-id="d9b73-117"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9b73-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b73-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b73-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b73-119">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="d9b73-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d9b73-120">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="d9b73-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d9b73-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9b73-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




