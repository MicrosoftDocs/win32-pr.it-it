---
title: Messaggio WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Un'estensione della finestra delle proprietà di Active Directory Invia il \_ \_ \_ messaggio di uscita di notifica di WM ADSPROP all'oggetto notifica quando l'oggetto notifica non è più necessario.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964764"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="6c75a-104">\_Messaggio di \_ uscita notifica ADSPROP \_ WM</span><span class="sxs-lookup"><span data-stu-id="6c75a-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="6c75a-105">Un'estensione della finestra delle proprietà di Active Directory Invia il messaggio di **\_ uscita di \_ notifica \_ di WM ADSPROP** all'oggetto notifica quando l'oggetto notifica non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="6c75a-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="6c75a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c75a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6c75a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6c75a-108">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="6c75a-108">The handle of the notification object.</span></span> <span data-ttu-id="6c75a-109">Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="6c75a-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="6c75a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c75a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c75a-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6c75a-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c75a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c75a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c75a-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6c75a-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c75a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c75a-114">Return value</span></span>

<span data-ttu-id="6c75a-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6c75a-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c75a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c75a-116">Remarks</span></span>

<span data-ttu-id="6c75a-117">L'oggetto notifica verrà eliminato in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6c75a-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="6c75a-118">Quando il messaggio è stato inviato, l'handle dell'oggetto notifica deve essere considerato non valido.</span><span class="sxs-lookup"><span data-stu-id="6c75a-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c75a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c75a-119">Requirements</span></span>



| <span data-ttu-id="6c75a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c75a-120">Requirement</span></span> | <span data-ttu-id="6c75a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6c75a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c75a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c75a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c75a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c75a-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="6c75a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c75a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c75a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c75a-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="6c75a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c75a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c75a-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c75a-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c75a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c75a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c75a-129">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="6c75a-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="6c75a-130">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6c75a-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





