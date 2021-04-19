---
description: Descrive la notifica passata alla funzione di \_ \_ richiamata della notifica del sink di visualizzazione della direttiva \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Struttura WFD_DISPLAY_SINK_NOTIFICATION (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311655"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="4236f-103">\_Struttura di \_ notifica del sink di visualizzazione della direttiva. \_</span><span class="sxs-lookup"><span data-stu-id="4236f-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="4236f-104">La struttura di **notifica del sink di visualizzazione della direttiva GMA \_ \_ \_** descrive la notifica passata alla funzione di [**callback di notifica del \_ \_ sink di \_ \_ visualizzazione**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="4236f-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4236f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4236f-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="4236f-106">Members</span><span class="sxs-lookup"><span data-stu-id="4236f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4236f-107">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="4236f-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-108">[**Intestazione dell' \_ \_ \_ oggetto \_ sink di visualizzazione della direttiva**](wfd-display-sink-object-header.md) , che descrive i dati inclusi nella notifica.</span><span class="sxs-lookup"><span data-stu-id="4236f-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-109">**type**</span><span class="sxs-lookup"><span data-stu-id="4236f-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-110">Un valore del tipo di notifica del sink di visualizzazione della direttiva, che indica il tipo di notifica. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md)</span><span class="sxs-lookup"><span data-stu-id="4236f-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="4236f-111">Questo parametro determina inoltre le informazioni da utilizzare nell'Unione sottostante.</span><span class="sxs-lookup"><span data-stu-id="4236f-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-112">**strRemoteDeviceName**</span><span class="sxs-lookup"><span data-stu-id="4236f-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-113">Contiene una stringa a terminazione NULL che contiene il nome del dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="4236f-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="4236f-114">\_ \_ \_ \_ La lunghezza massima del nome dispositivo del sink di direttiva \_ viene definita come valore (32).</span><span class="sxs-lookup"><span data-stu-id="4236f-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="4236f-115">**RemoteDeviceAddress**</span><span class="sxs-lookup"><span data-stu-id="4236f-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-116">Un [**\_ \_ indirizzo Mac DOT11**](dot11-mac-address-type.md) che contiene il BSSID del dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="4236f-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-117">**ProvisioningRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="4236f-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-118">Informazioni su una richiesta di provisioning.</span><span class="sxs-lookup"><span data-stu-id="4236f-118">Info about a provisioning request.</span></span> <span data-ttu-id="4236f-119">Usare questa se il *tipo* ha il valore **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="4236f-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="4236f-120">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="4236f-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-121">Handle della sessione.</span><span class="sxs-lookup"><span data-stu-id="4236f-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-122">**PossibleConfigMethods**</span><span class="sxs-lookup"><span data-stu-id="4236f-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-123">Metodi possibili per visualizzare l'interfaccia utente per l'accettazione interattiva.</span><span class="sxs-lookup"><span data-stu-id="4236f-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4236f-124">**ReconnectRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="4236f-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-125">Informazioni su una richiesta di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="4236f-125">Info about a reconnect request.</span></span> <span data-ttu-id="4236f-126">Usare questa se il *tipo* ha il valore **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="4236f-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="4236f-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="4236f-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-128">ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="4236f-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4236f-129">**ConnectedInfo**</span><span class="sxs-lookup"><span data-stu-id="4236f-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-130">Informazioni su una notifica connessa.</span><span class="sxs-lookup"><span data-stu-id="4236f-130">Info about a connected notification.</span></span> <span data-ttu-id="4236f-131">Usare questa se il *tipo* ha il valore **ConnectedNotification**.</span><span class="sxs-lookup"><span data-stu-id="4236f-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="4236f-132">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="4236f-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-133">Handle della sessione.</span><span class="sxs-lookup"><span data-stu-id="4236f-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-134">**guidSessionInterface**</span><span class="sxs-lookup"><span data-stu-id="4236f-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-135">GUID che indica l'interfaccia di sessione.</span><span class="sxs-lookup"><span data-stu-id="4236f-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="4236f-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-137">ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="4236f-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-138">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="4236f-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-139">Puntatore a una stringa con terminazione NULL che descrive il profilo.</span><span class="sxs-lookup"><span data-stu-id="4236f-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="4236f-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-141">Indirizzo locale.</span><span class="sxs-lookup"><span data-stu-id="4236f-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="4236f-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-143">Indirizzo remoto.</span><span class="sxs-lookup"><span data-stu-id="4236f-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="4236f-144">**uRTSPPort**</span><span class="sxs-lookup"><span data-stu-id="4236f-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="4236f-145">Porta RTSP.</span><span class="sxs-lookup"><span data-stu-id="4236f-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4236f-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4236f-146">Requirements</span></span>



| <span data-ttu-id="4236f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4236f-147">Requirement</span></span> | <span data-ttu-id="4236f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="4236f-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4236f-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4236f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4236f-150">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4236f-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4236f-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4236f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4236f-152">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4236f-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4236f-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4236f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4236f-154"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="4236f-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




