---
title: Messaggio WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: Il messaggio di errore di notifica di WM \_ ADSPROP \_ \_ aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando la funzione ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119846"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="25f3c-104">\_Messaggio di \_ errore di notifica di WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="25f3c-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="25f3c-105">Il messaggio di **errore di notifica di WM \_ \_ \_ ADSPROP** aggiunge un messaggio di errore a un elenco di messaggi di errore visualizzati chiamando la funzione [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="25f3c-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="25f3c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25f3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f3c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="25f3c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="25f3c-108">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="25f3c-108">Handle of the notification object.</span></span> <span data-ttu-id="25f3c-109">Si tratta del parametro *hNotifyObject* ottenuto da [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="25f3c-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="25f3c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25f3c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25f3c-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="25f3c-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="25f3c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25f3c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25f3c-113">Puntatore a una struttura [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) che contiene i dati del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="25f3c-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f3c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25f3c-114">Return value</span></span>

<span data-ttu-id="25f3c-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="25f3c-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f3c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="25f3c-116">Remarks</span></span>

<span data-ttu-id="25f3c-117">La funzione [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) è il metodo preferito per l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="25f3c-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="25f3c-118">I messaggi di errore aggiunti dal messaggio di **errore di notifica di WM \_ \_ \_ ADSPROP** vengono accumulati fino a quando non viene chiamato [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="25f3c-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="25f3c-119">**ADsPropShowErrorDialog** combina e Visualizza i messaggi di errore accumulati.</span><span class="sxs-lookup"><span data-stu-id="25f3c-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="25f3c-120">Quando la finestra di dialogo di errore viene rilasciata, i messaggi di errore accumulati vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="25f3c-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f3c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25f3c-121">Requirements</span></span>



| <span data-ttu-id="25f3c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f3c-122">Requirement</span></span> | <span data-ttu-id="25f3c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="25f3c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25f3c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25f3c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25f3c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25f3c-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="25f3c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25f3c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25f3c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25f3c-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="25f3c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25f3c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f3c-129"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f3c-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f3c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25f3c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f3c-131">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="25f3c-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="25f3c-132">**ADSPROPERROR**</span><span class="sxs-lookup"><span data-stu-id="25f3c-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="25f3c-133">**ADsPropSendErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="25f3c-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="25f3c-134">**ADsPropShowErrorDialog**</span><span class="sxs-lookup"><span data-stu-id="25f3c-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





