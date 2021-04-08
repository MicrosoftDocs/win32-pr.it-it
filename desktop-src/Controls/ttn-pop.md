---
title: Codice di notifica TTN_POP (COMmctrl. h)
description: Notifica alla finestra del proprietario che una descrizione comando sta per essere nascosta. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- Controlli di Windows per il codice di notifica TTN_POP
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741447"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="02992-105">\_Codice di notifica pop TTN</span><span class="sxs-lookup"><span data-stu-id="02992-105">TTN\_POP notification code</span></span>

<span data-ttu-id="02992-106">Notifica alla finestra del proprietario che una descrizione comando sta per essere nascosta.</span><span class="sxs-lookup"><span data-stu-id="02992-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="02992-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="02992-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="02992-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="02992-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02992-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02992-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02992-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="02992-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02992-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02992-111">Return value</span></span>

<span data-ttu-id="02992-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="02992-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="02992-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02992-113">Requirements</span></span>



| <span data-ttu-id="02992-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02992-114">Requirement</span></span> | <span data-ttu-id="02992-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02992-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02992-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02992-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02992-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02992-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02992-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02992-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02992-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02992-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02992-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02992-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02992-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02992-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





