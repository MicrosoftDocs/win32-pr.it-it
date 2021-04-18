---
description: Segnala che il numero di angoli disponibili è stato modificato o che il numero dell'angolo corrente è stato modificato.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331113"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="14a5a-103">\_ \_ Modifica angolo DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="14a5a-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="14a5a-104">Segnala che il numero di angoli disponibili è stato modificato o che il numero dell'angolo corrente è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="14a5a-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="14a5a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="14a5a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a5a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="14a5a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="14a5a-107">Valore **DWORD** che indica il numero di angoli disponibili.</span><span class="sxs-lookup"><span data-stu-id="14a5a-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="14a5a-108">Quando il numero di angoli disponibili è 1, il video corrente non è multiangolo.</span><span class="sxs-lookup"><span data-stu-id="14a5a-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="14a5a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="14a5a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="14a5a-110">Valore **DWORD** che indica il numero dell'angolo corrente.</span><span class="sxs-lookup"><span data-stu-id="14a5a-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14a5a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="14a5a-111">Remarks</span></span>

<span data-ttu-id="14a5a-112">I numeri degli angoli sono compresi tra 1 e 9.</span><span class="sxs-lookup"><span data-stu-id="14a5a-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="14a5a-113">Il numero dell'angolo corrente può essere modificato automaticamente con un comando di navigazione creato sul disco e tramite il controllo delle applicazioni tramite l'interfaccia [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="14a5a-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="14a5a-114">Questo evento viene generato in tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="14a5a-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a5a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14a5a-115">Requirements</span></span>



| <span data-ttu-id="14a5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a5a-116">Requirement</span></span> | <span data-ttu-id="14a5a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="14a5a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a5a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14a5a-118">Header</span></span><br/> | <dl> <span data-ttu-id="14a5a-119"><dt>Dvdevcode. h (include dshow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14a5a-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a5a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14a5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a5a-121">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="14a5a-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="14a5a-122">Codici di notifica degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="14a5a-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="14a5a-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="14a5a-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




