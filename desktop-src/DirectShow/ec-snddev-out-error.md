---
description: Si è verificato un errore del dispositivo in un filtro renderer audio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332051"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="42db3-103">\_errore SNDDEV \_ EC \_</span><span class="sxs-lookup"><span data-stu-id="42db3-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="42db3-104">Si è verificato un errore del dispositivo in un filtro renderer audio.</span><span class="sxs-lookup"><span data-stu-id="42db3-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="42db3-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="42db3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42db3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="42db3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="42db3-107">Valore DWORD dal tipo enumerato [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , che indica il modo in cui è stato eseguito l'accesso al dispositivo quando si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="42db3-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="42db3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="42db3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="42db3-109">Valore DWORD che indica l'errore restituito dalla chiamata al dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="42db3-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="42db3-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="42db3-110">Default Action</span></span>

<span data-ttu-id="42db3-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="42db3-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="42db3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42db3-112">Requirements</span></span>



| <span data-ttu-id="42db3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="42db3-113">Requirement</span></span> | <span data-ttu-id="42db3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="42db3-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42db3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42db3-115">Header</span></span><br/> | <dl> <span data-ttu-id="42db3-116"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="42db3-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42db3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42db3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42db3-118">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="42db3-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="42db3-119">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="42db3-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




