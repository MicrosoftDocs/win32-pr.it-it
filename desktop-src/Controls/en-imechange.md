---
title: Codice di notifica EN_IMECHANGE (RichEdit. h)
description: Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- Controlli di Windows per il codice di notifica EN_IMECHANGE
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048397"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="997f7-104">\_Codice di notifica en IMECHANGE</span><span class="sxs-lookup"><span data-stu-id="997f7-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="997f7-105">Notifica all'elemento padre di un controllo Rich Edit che lo stato di conversione IME è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="997f7-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="997f7-106">Questo codice di notifica è disponibile *solo* per le versioni in lingua asiatica del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="997f7-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="997f7-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="997f7-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="997f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="997f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="997f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="997f7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="997f7-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="997f7-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="997f7-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="997f7-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="997f7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="997f7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="997f7-113">Handle per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="997f7-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="997f7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="997f7-114">Return value</span></span>

<span data-ttu-id="997f7-115">Questo codice di notifica restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="997f7-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="997f7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="997f7-116">Remarks</span></span>

<span data-ttu-id="997f7-117">Per ricevere \_ i codici di notifica en IMECHANGE, specificare [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="997f7-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="997f7-118">Questo codice di notifica è supportato solo nella versione asiatica di Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="997f7-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="997f7-119">Non è supportata nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="997f7-119">It is not supported in later versions.</span></span> <span data-ttu-id="997f7-120">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="997f7-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="997f7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="997f7-121">Requirements</span></span>



| <span data-ttu-id="997f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="997f7-122">Requirement</span></span> | <span data-ttu-id="997f7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="997f7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="997f7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="997f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="997f7-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="997f7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="997f7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="997f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="997f7-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="997f7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="997f7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="997f7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="997f7-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="997f7-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997f7-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="997f7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="997f7-131">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="997f7-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="997f7-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="997f7-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="997f7-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="997f7-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="997f7-134">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="997f7-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

