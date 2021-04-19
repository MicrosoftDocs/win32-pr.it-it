---
description: Segnala che è stata avviata una modifica della frequenza nella riproduzione DVD.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326644"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="550ea-103">\_modifica della \_ frequenza di riproduzione DVD \_ EC \_</span><span class="sxs-lookup"><span data-stu-id="550ea-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="550ea-104">Segnala che è stata avviata una modifica della frequenza nella riproduzione DVD.</span><span class="sxs-lookup"><span data-stu-id="550ea-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="550ea-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="550ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="550ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="550ea-107">Valore LONG che indica la nuova velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="550ea-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="550ea-108">Il valore è la velocità effettiva di riproduzione moltiplicata per 10.000, quindi la velocità di riproduzione è uguale a 10000,0/ *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="550ea-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="550ea-109">I valori minori di zero indicano la modalità di riproduzione inversa e i valori maggiori di zero indicano la modalità di riproduzione in modalità diretta.</span><span class="sxs-lookup"><span data-stu-id="550ea-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="550ea-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="550ea-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="550ea-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="550ea-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="550ea-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="550ea-112">Remarks</span></span>

<span data-ttu-id="550ea-113">Questo evento viene generato nel dominio del titolo.</span><span class="sxs-lookup"><span data-stu-id="550ea-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="550ea-114">La *frequenza* di riproduzione è l'inverso della *velocità* di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="550ea-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="550ea-115">Se ad esempio la velocità di riproduzione è 2x, la frequenza è 0,5.</span><span class="sxs-lookup"><span data-stu-id="550ea-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="550ea-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="550ea-116">Requirements</span></span>



| <span data-ttu-id="550ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="550ea-117">Requirement</span></span> | <span data-ttu-id="550ea-118">Valore</span><span class="sxs-lookup"><span data-stu-id="550ea-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="550ea-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="550ea-119">Header</span></span><br/> | <dl> <span data-ttu-id="550ea-120"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="550ea-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550ea-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="550ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550ea-122">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="550ea-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="550ea-123">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="550ea-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="550ea-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="550ea-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




