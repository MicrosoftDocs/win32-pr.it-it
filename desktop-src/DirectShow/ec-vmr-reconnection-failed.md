---
description: Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328333"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="cf3ea-103">\_riconnessione VMR EC \_ \_ non riuscita</span><span class="sxs-lookup"><span data-stu-id="cf3ea-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="cf3ea-104">Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.</span><span class="sxs-lookup"><span data-stu-id="cf3ea-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf3ea-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf3ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf3ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cf3ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cf3ea-107">(**HRESULT**) Codice di stato restituito da [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input di VMR che non ha superato la riconnessione.</span><span class="sxs-lookup"><span data-stu-id="cf3ea-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="cf3ea-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cf3ea-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cf3ea-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="cf3ea-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf3ea-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf3ea-110">Remarks</span></span>

<span data-ttu-id="cf3ea-111">Questo evento viene inviato alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cf3ea-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3ea-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf3ea-112">Requirements</span></span>



| <span data-ttu-id="cf3ea-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf3ea-113">Requirement</span></span> | <span data-ttu-id="cf3ea-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cf3ea-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3ea-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf3ea-115">Header</span></span><br/> | <dl> <span data-ttu-id="cf3ea-116"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ea-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3ea-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf3ea-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3ea-118">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="cf3ea-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cf3ea-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf3ea-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




