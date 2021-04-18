---
description: Un dispositivo Plug and Play è stato rimosso o è stato nuovamente disponibile.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331117"
---
# <a name="ec_device_lost"></a><span data-ttu-id="cd88c-103">\_dispositivo EC \_ perso</span><span class="sxs-lookup"><span data-stu-id="cd88c-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="cd88c-104">Un dispositivo Plug and Play è stato rimosso o è stato nuovamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="cd88c-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd88c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd88c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd88c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cd88c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cd88c-107">(**IUnknown** \* ) Puntatore all'interfaccia **IUnknown** del filtro che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd88c-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="cd88c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cd88c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cd88c-109">Zero se il dispositivo è stato rimosso oppure 1 se il dispositivo è nuovamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="cd88c-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cd88c-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="cd88c-110">Default Action</span></span>

<span data-ttu-id="cd88c-111">No.</span><span class="sxs-lookup"><span data-stu-id="cd88c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd88c-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cd88c-112">Remarks</span></span>

<span data-ttu-id="cd88c-113">Quando il dispositivo diventa nuovamente disponibile, lo stato precedente del filtro di dispositivo non è più valido.</span><span class="sxs-lookup"><span data-stu-id="cd88c-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="cd88c-114">Per usare il dispositivo, l'applicazione deve ricompilare il grafo.</span><span class="sxs-lookup"><span data-stu-id="cd88c-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd88c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd88c-115">Requirements</span></span>



| <span data-ttu-id="cd88c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd88c-116">Requirement</span></span> | <span data-ttu-id="cd88c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd88c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd88c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd88c-118">Header</span></span><br/> | <dl> <span data-ttu-id="cd88c-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd88c-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd88c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd88c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd88c-121">Notifica di rimozione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cd88c-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="cd88c-122">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="cd88c-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="cd88c-123">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cd88c-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




