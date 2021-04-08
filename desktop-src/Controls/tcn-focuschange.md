---
title: Codice di notifica TCN_FOCUSCHANGE (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che lo stato attivo del pulsante è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- Controlli di Windows per il codice di notifica TCN_FOCUSCHANGE
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739866"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="f5777-105">\_Codice di notifica FOCUSCHANGE di TCN</span><span class="sxs-lookup"><span data-stu-id="f5777-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="f5777-106">Notifica alla finestra padre di un controllo struttura a schede che lo stato attivo del pulsante è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f5777-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="f5777-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f5777-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f5777-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5777-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5777-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5777-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5777-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="f5777-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5777-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5777-111">Return value</span></span>

<span data-ttu-id="f5777-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f5777-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5777-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5777-113">Requirements</span></span>



| <span data-ttu-id="f5777-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5777-114">Requirement</span></span> | <span data-ttu-id="f5777-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5777-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5777-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5777-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5777-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5777-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5777-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5777-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5777-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5777-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5777-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5777-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5777-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5777-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





