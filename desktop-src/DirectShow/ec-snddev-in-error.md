---
description: Si è verificato un errore del dispositivo in un filtro di acquisizione audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332054"
---
# <a name="ec_snddev_in_error"></a><span data-ttu-id="97437-103">EC \_ SNDDEV \_ in \_ errore</span><span class="sxs-lookup"><span data-stu-id="97437-103">EC\_SNDDEV\_IN\_ERROR</span></span>

<span data-ttu-id="97437-104">Si è verificato un errore del dispositivo in un filtro di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="97437-104">A device error has occurred in an audio capture filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="97437-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="97437-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97437-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="97437-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="97437-107">Valore DWORD dal tipo enumerato [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , che indica il modo in cui è stato eseguito l'accesso al dispositivo quando si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="97437-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="97437-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="97437-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="97437-109">Valore DWORD che indica l'errore restituito dalla chiamata al dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="97437-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="97437-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="97437-110">Default Action</span></span>

<span data-ttu-id="97437-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="97437-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="97437-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97437-112">Requirements</span></span>



| <span data-ttu-id="97437-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="97437-113">Requirement</span></span> | <span data-ttu-id="97437-114">Valore</span><span class="sxs-lookup"><span data-stu-id="97437-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97437-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97437-115">Header</span></span><br/> | <dl> <span data-ttu-id="97437-116"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="97437-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97437-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97437-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97437-118">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="97437-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="97437-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="97437-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




