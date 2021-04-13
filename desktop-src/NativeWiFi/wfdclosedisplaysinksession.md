---
description: Pulisce lo stato della sessione aperta o della sessione attualmente aperta.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Funzione WFDDisplaySinkCloseSession (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528159"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="25bc7-103">WFDDisplaySinkCloseSession (funzione)</span><span class="sxs-lookup"><span data-stu-id="25bc7-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="25bc7-104">Pulisce lo stato della sessione aperta o della sessione attualmente aperta.</span><span class="sxs-lookup"><span data-stu-id="25bc7-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="25bc7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25bc7-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="25bc7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25bc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25bc7-107">*hSessionHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25bc7-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25bc7-108">Il punto di controllo ricevuto tramite la [**\_ \_ \_ \_ richiamata del callback della notifica del sink di visualizzazione**](wfd-display-sink-notification-callback.md) più recente che ne include uno.</span><span class="sxs-lookup"><span data-stu-id="25bc7-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25bc7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25bc7-109">Return value</span></span>

<span data-ttu-id="25bc7-110">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="25bc7-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="25bc7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="25bc7-111">Remarks</span></span>

<span data-ttu-id="25bc7-112">L'app può chiamare questa funzione per terminare la sessione Miracast per qualsiasi motivo.</span><span class="sxs-lookup"><span data-stu-id="25bc7-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="25bc7-113">Non è necessario che l'app lo chiami quando riceve il tipo **DisconnectedNotification** nel callback.</span><span class="sxs-lookup"><span data-stu-id="25bc7-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="25bc7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25bc7-114">Requirements</span></span>



| <span data-ttu-id="25bc7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25bc7-115">Requirement</span></span> | <span data-ttu-id="25bc7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="25bc7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="25bc7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25bc7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25bc7-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25bc7-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="25bc7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25bc7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25bc7-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25bc7-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25bc7-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="25bc7-121">End of client support</span></span><br/>    | <span data-ttu-id="25bc7-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="25bc7-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="25bc7-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="25bc7-123">End of server support</span></span><br/>    | <span data-ttu-id="25bc7-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="25bc7-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="25bc7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25bc7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25bc7-126"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="25bc7-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="25bc7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="25bc7-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="25bc7-128"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25bc7-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="25bc7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="25bc7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25bc7-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25bc7-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25bc7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25bc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25bc7-132">**richiamata della notifica del sink di \_ visualizzazione della direttiva. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25bc7-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




