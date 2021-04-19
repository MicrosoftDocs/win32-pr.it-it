---
description: Definisce il tipo di notifica passato alla \_ \_ funzione di \_ richiamata della notifica del sink di visualizzazione della direttiva \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Enumerazione WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311654"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="c306e-103">\_Enumerazione del \_ tipo di notifica del sink di visualizzazione della \_ direttiva. \_</span><span class="sxs-lookup"><span data-stu-id="c306e-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="c306e-104">Il tipo enumerato del tipo di notifica del sink di visualizzazione della direttiva. definisce il tipo di notifica passato alla funzione di [**\_ \_ \_ \_ richiamata della notifica del sink di visualizzazione della direttiva**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c306e-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c306e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c306e-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c306e-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c306e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c306e-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="c306e-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="c306e-108">La notifica è una richiesta di provisioning.</span><span class="sxs-lookup"><span data-stu-id="c306e-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="c306e-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="c306e-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="c306e-110">La notifica è una richiesta di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="c306e-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="c306e-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="c306e-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="c306e-112">La notifica è una notifica connessa.</span><span class="sxs-lookup"><span data-stu-id="c306e-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="c306e-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="c306e-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="c306e-114">La notifica è una notifica disconnessa.</span><span class="sxs-lookup"><span data-stu-id="c306e-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c306e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c306e-115">Requirements</span></span>



| <span data-ttu-id="c306e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c306e-116">Requirement</span></span> | <span data-ttu-id="c306e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c306e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c306e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c306e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c306e-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c306e-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c306e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c306e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c306e-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c306e-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c306e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c306e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c306e-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="c306e-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




