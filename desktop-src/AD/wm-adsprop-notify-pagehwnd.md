---
title: Messaggio WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Un'estensione della finestra delle proprietà del servizio Active Directory directory chiama ADsPropSetHwnd per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121062"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="83321-104">WM \_ ADSPROP \_ notifica \_ PAGEHWND messaggio</span><span class="sxs-lookup"><span data-stu-id="83321-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="83321-105">Un'estensione della finestra delle proprietà del servizio Active Directory directory chiama [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) per informare l'oggetto notifica dell'handle della finestra della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="83321-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="83321-106">La funzione **ADsPropSetHwnd** invia il messaggio di notifica **\_ \_ \_ PAGEHWND di WM ADSPROP** all'oggetto notifica, che informa l'oggetto notifica dell'handle della finestra della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="83321-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="83321-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="83321-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83321-108">*hNotifyObj*</span><span class="sxs-lookup"><span data-stu-id="83321-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="83321-109">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="83321-109">The handle of the notification object.</span></span> <span data-ttu-id="83321-110">Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="83321-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="83321-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="83321-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="83321-112">Handle di finestra della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="83321-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="83321-113">*ptzTitle*</span><span class="sxs-lookup"><span data-stu-id="83321-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="83321-114">Puntatore a un buffer **WCHAR** con terminazione null che contiene il titolo della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="83321-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83321-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83321-115">Return value</span></span>

<span data-ttu-id="83321-116">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="83321-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83321-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="83321-117">Remarks</span></span>

<span data-ttu-id="83321-118">Un'estensione della finestra delle proprietà Active Directory in genere chiama la funzione [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="83321-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="83321-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83321-119">Requirements</span></span>



| <span data-ttu-id="83321-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="83321-120">Requirement</span></span> | <span data-ttu-id="83321-121">Valore</span><span class="sxs-lookup"><span data-stu-id="83321-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="83321-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83321-122">Minimum supported client</span></span><br/> | <span data-ttu-id="83321-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83321-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="83321-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83321-124">Minimum supported server</span></span><br/> | <span data-ttu-id="83321-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83321-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="83321-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83321-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="83321-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="83321-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83321-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83321-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83321-129">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="83321-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="83321-130">**ADsPropSetHwnd**</span><span class="sxs-lookup"><span data-stu-id="83321-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="83321-131">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="83321-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="83321-132">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="83321-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

