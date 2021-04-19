---
description: Definisce la funzione di callback&\# 8212, implementata nell'app&\# 8212; specificata per la funzione WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: Funzione di callback WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311656"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="0296c-103">Visualizzazione della funzione di callback di callback di \_ \_ \_ notifica sink \_</span><span class="sxs-lookup"><span data-stu-id="0296c-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="0296c-104">La funzione di **\_ \_ \_ \_ richiamata della notifica di sink di visualizzazione della direttiva GMA** definisce la funzione di callback, che viene implementata nell'app, specificata per la funzione [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .</span><span class="sxs-lookup"><span data-stu-id="0296c-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0296c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0296c-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="0296c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0296c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0296c-107">*pvContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0296c-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0296c-108">Puntatore di contesto facoltativo passato alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="0296c-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0296c-109">*pNotification* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0296c-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0296c-110">Puntatore a uno struct che contiene i dati sulla notifica del sink di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0296c-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="0296c-111">*pNotificationResult* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0296c-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0296c-112">Puntatore a uno struct che contiene i dati che l'app può impostare facoltativamente per indicare il risultato dell'elaborazione della notifica del sink di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0296c-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0296c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0296c-113">Requirements</span></span>



| <span data-ttu-id="0296c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0296c-114">Requirement</span></span> | <span data-ttu-id="0296c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0296c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0296c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0296c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0296c-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0296c-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0296c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0296c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0296c-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0296c-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0296c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0296c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0296c-121"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="0296c-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




