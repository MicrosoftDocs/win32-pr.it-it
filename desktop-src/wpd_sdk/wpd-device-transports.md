---
description: Il \_ \_ tipo di enumerazione trasporti dispositivi WPD specifica la relazione di ereditarietà per un servizio. Questa enumerazione viene utilizzata dalla proprietà di \_ trasporto del dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumerazione WPD_DEVICE_TRANSPORTS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324208"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="8d76c-104">\_ \_ Enumerazione trasporti dispositivi WPD</span><span class="sxs-lookup"><span data-stu-id="8d76c-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="8d76c-105">Il tipo di enumerazione [**\_ \_ trasporti dispositivi WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) specifica la relazione di ereditarietà per un servizio.</span><span class="sxs-lookup"><span data-stu-id="8d76c-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="8d76c-106">Questa enumerazione viene utilizzata dalla proprietà **di \_ \_ trasporto del dispositivo WPD** .</span><span class="sxs-lookup"><span data-stu-id="8d76c-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d76c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d76c-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="8d76c-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="8d76c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8d76c-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD \_ trasporto dispositivo non \_ \_ specificato**</span><span class="sxs-lookup"><span data-stu-id="8d76c-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="8d76c-110">Tipo di trasporto non specificato.</span><span class="sxs-lookup"><span data-stu-id="8d76c-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="8d76c-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_ \_ USB trasporto dispositivi \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="8d76c-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="8d76c-112">Il dispositivo è connesso tramite USB.</span><span class="sxs-lookup"><span data-stu-id="8d76c-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="8d76c-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_ \_ IP trasporto dispositivi \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="8d76c-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="8d76c-114">Il dispositivo è connesso tramite Internet Protocol (IP).</span><span class="sxs-lookup"><span data-stu-id="8d76c-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="8d76c-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_ \_ Bluetooth trasporto dispositivi \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="8d76c-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="8d76c-116">Il dispositivo è connesso tramite Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="8d76c-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d76c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d76c-117">Requirements</span></span>



| <span data-ttu-id="8d76c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d76c-118">Requirement</span></span> | <span data-ttu-id="8d76c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8d76c-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d76c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d76c-120">Header</span></span><br/> | <dl> <span data-ttu-id="8d76c-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d76c-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

