---
description: Esegue l'inizializzazione necessaria per consentire all'app chiamante di diventare un sink di visualizzazione Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Funzione WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528158"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="03cd9-103">WFDDisplaySinkStart (funzione)</span><span class="sxs-lookup"><span data-stu-id="03cd9-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="03cd9-104">Esegue l'inizializzazione necessaria per consentire all'app chiamante di diventare un sink di visualizzazione Miracast.</span><span class="sxs-lookup"><span data-stu-id="03cd9-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="03cd9-105">L'app dovrebbe chiamarla una volta all'avvio.</span><span class="sxs-lookup"><span data-stu-id="03cd9-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cd9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03cd9-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="03cd9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="03cd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03cd9-108">*uDeviceCategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cd9-109">Categoria del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03cd9-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="03cd9-110">*uSubCategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cd9-111">Sottocategoria del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03cd9-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="03cd9-112">*pCallbackContext* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03cd9-113">Puntatore di contesto facoltativo che viene passato alla funzione di callback specificata nel parametro *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="03cd9-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="03cd9-114">*pfnCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cd9-115">Puntatore alla funzione di callback da chiamare ogni volta che è presente una notifica per l'app.</span><span class="sxs-lookup"><span data-stu-id="03cd9-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="03cd9-116">Le notifiche che è possibile inviare sono descritte [**in \_ \_ \_ \_ richiamata della notifica del sink di visualizzazione della direttiva**](wfd-display-sink-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="03cd9-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03cd9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03cd9-117">Return value</span></span>

<span data-ttu-id="03cd9-118">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="03cd9-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="03cd9-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="03cd9-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="03cd9-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="03cd9-120">Return code</span></span>                                                                                          | <span data-ttu-id="03cd9-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03cd9-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="03cd9-122"><dt>**ERRORE \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="03cd9-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="03cd9-123">Il sink di visualizzazione non è supportato in questo hardware.</span><span class="sxs-lookup"><span data-stu-id="03cd9-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03cd9-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="03cd9-124">Remarks</span></span>

<span data-ttu-id="03cd9-125">Questa funzione esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="03cd9-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="03cd9-126">Rende individuabile il PC</span><span class="sxs-lookup"><span data-stu-id="03cd9-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="03cd9-127">Imposta le informazioni sul dispositivo P2P in modo da riflettere la categoria e la sottocategoria specificata</span><span class="sxs-lookup"><span data-stu-id="03cd9-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="03cd9-128">Imposta la Miracast IEs su tutti i frame diretti di Wi-Fi con il tipo di dispositivo come sink</span><span class="sxs-lookup"><span data-stu-id="03cd9-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="03cd9-129">Registra il callback specificato da richiamare ogni volta che è presente una connessione in ingresso</span><span class="sxs-lookup"><span data-stu-id="03cd9-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="03cd9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03cd9-130">Requirements</span></span>



| <span data-ttu-id="03cd9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="03cd9-131">Requirement</span></span> | <span data-ttu-id="03cd9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="03cd9-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="03cd9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03cd9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03cd9-134">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="03cd9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03cd9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03cd9-136">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="03cd9-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03cd9-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="03cd9-137">End of client support</span></span><br/>    | <span data-ttu-id="03cd9-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="03cd9-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="03cd9-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="03cd9-139">End of server support</span></span><br/>    | <span data-ttu-id="03cd9-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="03cd9-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="03cd9-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03cd9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03cd9-142"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="03cd9-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="03cd9-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="03cd9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="03cd9-144"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03cd9-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="03cd9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="03cd9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03cd9-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03cd9-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cd9-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03cd9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cd9-148">**richiamata della notifica del sink di \_ visualizzazione della direttiva. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="03cd9-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




