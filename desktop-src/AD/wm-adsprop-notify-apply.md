---
title: Messaggio WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Un'estensione della finestra delle proprietà del servizio Active Directory directory invia il \_ \_ \_ messaggio di richiesta di notifica di WM ADSPROP all'oggetto notifica se la pagina delle proprietà del gestore di applicazione PSN ha \_ esito positivo.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302304"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="a74a7-104">\_Messaggio di \_ richiesta di notifica di WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="a74a7-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="a74a7-105">Un'estensione della finestra delle proprietà del servizio Active Directory directory invia il messaggio di **\_ richiesta di \_ notifica \_ di WM ADSPROP** all'oggetto notifica se la pagina delle proprietà del gestore di applicazione PSN ha \_ esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a74a7-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="a74a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a74a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a74a7-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a74a7-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a74a7-108">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="a74a7-108">The handle of the notification object.</span></span> <span data-ttu-id="a74a7-109">Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="a74a7-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="a74a7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a74a7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74a7-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a74a7-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a74a7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a74a7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a74a7-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a74a7-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a74a7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a74a7-114">Return value</span></span>

<span data-ttu-id="a74a7-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a74a7-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74a7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a74a7-116">Remarks</span></span>

<span data-ttu-id="a74a7-117">Quando si aggiungono pagine allo snap-in MMC di gestione Active Directory, Active Directory finestre delle proprietà di MMC creano gli oggetti notifica mediante una chiamata alla funzione [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , quindi passa l'handle dell'oggetto notifica a ogni pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a74a7-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74a7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a74a7-118">Requirements</span></span>



| <span data-ttu-id="a74a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a74a7-119">Requirement</span></span> | <span data-ttu-id="a74a7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a74a7-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a74a7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a74a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a74a7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a74a7-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="a74a7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a74a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a74a7-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a74a7-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="a74a7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a74a7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74a7-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="a74a7-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74a7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a74a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74a7-128">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="a74a7-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="a74a7-129">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a74a7-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





