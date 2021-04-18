---
title: Messaggio WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Un'estensione della finestra delle proprietà Active Directory chiama ADsPropGetInitInfo per ottenere i dati relativi all'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517601"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="f4403-104">WM \_ ADSPROP \_ notifica \_ PAGEINIT messaggio</span><span class="sxs-lookup"><span data-stu-id="f4403-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="f4403-105">Un'estensione della finestra delle proprietà Active Directory chiama [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) per ottenere i dati relativi all'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4403-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="f4403-106">La funzione **ADsPropGetInitInfo** invia il messaggio **WM \_ ADSPROP \_ Notify \_ PAGEINIT** all'oggetto notifica per ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="f4403-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="f4403-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4403-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4403-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f4403-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f4403-109">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="f4403-109">Handle of the notification object.</span></span> <span data-ttu-id="f4403-110">Si tratta del parametro *hNotifyObject* ottenuto da una chiamata a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="f4403-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="f4403-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4403-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4403-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f4403-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f4403-113">*pADsPropInitParams*</span><span class="sxs-lookup"><span data-stu-id="f4403-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="f4403-114">Puntatore a una struttura [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) che riceve le informazioni sull'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="f4403-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="f4403-115">Si tratta del parametro *pInitParams* passato a [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="f4403-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4403-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4403-116">Return value</span></span>

<span data-ttu-id="f4403-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f4403-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4403-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4403-118">Requirements</span></span>



| <span data-ttu-id="f4403-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4403-119">Requirement</span></span> | <span data-ttu-id="f4403-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f4403-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4403-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4403-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4403-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4403-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="f4403-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4403-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4403-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4403-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="f4403-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4403-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4403-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4403-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4403-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4403-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4403-128">Messaggi in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f4403-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="f4403-129">**ADsPropGetInitInfo**</span><span class="sxs-lookup"><span data-stu-id="f4403-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="f4403-130">**ADSPROPINITPARAMS**</span><span class="sxs-lookup"><span data-stu-id="f4403-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





