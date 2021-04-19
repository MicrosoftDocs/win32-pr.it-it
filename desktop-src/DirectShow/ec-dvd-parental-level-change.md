---
description: Segnala che il livello padre del contenuto DVD creato sta per essere modificato.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326646"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="fa481-103">\_modifica a \_ livello padre \_ DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="fa481-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="fa481-104">Segnala che il livello padre del contenuto DVD creato sta per essere modificato.</span><span class="sxs-lookup"><span data-stu-id="fa481-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa481-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa481-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa481-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fa481-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fa481-107">Valore LONG che rappresenta il nuovo set di livelli padre nel lettore.</span><span class="sxs-lookup"><span data-stu-id="fa481-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="fa481-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fa481-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fa481-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="fa481-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa481-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa481-110">Remarks</span></span>

<span data-ttu-id="fa481-111">Il filtro dello [strumento di spostamento DVD](dvd-navigator-filter.md) non supporta le modifiche a livello padre durante lo streaming in risposta ai comandi SetTmpPML su un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="fa481-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa481-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa481-112">Requirements</span></span>



| <span data-ttu-id="fa481-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa481-113">Requirement</span></span> | <span data-ttu-id="fa481-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fa481-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa481-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa481-115">Header</span></span><br/> | <dl> <span data-ttu-id="fa481-116"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa481-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa481-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa481-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa481-118">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="fa481-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="fa481-119">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="fa481-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fa481-120">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa481-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




