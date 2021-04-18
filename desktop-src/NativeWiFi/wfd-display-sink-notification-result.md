---
description: Descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di un sink di visualizzazione notifica \_ nella \_ \_ funzione di richiamata della notifica del sink di visualizzazione della direttiva \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Struttura WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318263"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="0d550-103">\_Struttura del \_ risultato della notifica del sink di visualizzazione della \_ direttiva. \_</span><span class="sxs-lookup"><span data-stu-id="0d550-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="0d550-104">La struttura del risultato della notifica del sink di visualizzazione della direttiva per la visualizzazione del sink descrive il risultato che è possibile impostare facoltativamente dopo l'elaborazione di un sink di visualizzazione notifica nella funzione di [**\_ \_ \_ \_ richiamata della notifica di sink**](wfd-display-sink-notification-callback.md) **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0d550-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d550-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d550-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="0d550-106">Members</span><span class="sxs-lookup"><span data-stu-id="0d550-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d550-107">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="0d550-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-108">[**Intestazione dell' \_ \_ \_ oggetto \_ sink di visualizzazione della direttiva**](wfd-display-sink-object-header.md) , che descrive i dati inclusi nel risultato della notifica.</span><span class="sxs-lookup"><span data-stu-id="0d550-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="0d550-109">**type**</span><span class="sxs-lookup"><span data-stu-id="0d550-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-110">Un valore del tipo di notifica del sink di visualizzazione della direttiva, che indica il tipo di risultato della notifica. [**\_ \_ \_ \_**](wfd-display-sink-notification-type.md)</span><span class="sxs-lookup"><span data-stu-id="0d550-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="0d550-111">Questo parametro determina inoltre le informazioni da utilizzare nell'Unione sottostante.</span><span class="sxs-lookup"><span data-stu-id="0d550-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="0d550-112">**ProvisioningData**</span><span class="sxs-lookup"><span data-stu-id="0d550-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-113">Informazioni sul risultato di una richiesta di provisioning.</span><span class="sxs-lookup"><span data-stu-id="0d550-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="0d550-114">Usare questa se il *tipo* ha il valore **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="0d550-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="0d550-115">**ConfigMethod**</span><span class="sxs-lookup"><span data-stu-id="0d550-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-116">Metodo per visualizzare l'interfaccia utente per l'accettazione interattiva.</span><span class="sxs-lookup"><span data-stu-id="0d550-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="0d550-117">**uPassKeyLength**</span><span class="sxs-lookup"><span data-stu-id="0d550-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-118">Il numero di caratteri wide nella *passkey*, senza contare alcun carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="0d550-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="0d550-119">**Passkey**</span><span class="sxs-lookup"><span data-stu-id="0d550-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-120">Contiene il tasto pass come matrice di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="0d550-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="0d550-121">\_ \_ \_ \_ \_ La lunghezza di passkey massima delle informazioni WPS del sink \_ di direttiva è definita come valore (8).</span><span class="sxs-lookup"><span data-stu-id="0d550-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0d550-122">**ReconnectData**</span><span class="sxs-lookup"><span data-stu-id="0d550-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-123">Informazioni sul risultato di una richiesta di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="0d550-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="0d550-124">Usare questa se il *tipo* ha il valore **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="0d550-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="0d550-125">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="0d550-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="0d550-126">Puntatore a una stringa con terminazione NULL che descrive il profilo.</span><span class="sxs-lookup"><span data-stu-id="0d550-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d550-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d550-127">Requirements</span></span>



| <span data-ttu-id="0d550-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d550-128">Requirement</span></span> | <span data-ttu-id="0d550-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0d550-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d550-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d550-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d550-131">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d550-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d550-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d550-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d550-133">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d550-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0d550-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d550-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d550-135"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d550-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




