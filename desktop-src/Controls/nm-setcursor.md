---
title: Codice di notifica NM_SETCURSOR (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo sta impostando il cursore in risposta a un \_ messaggio del cursore WM. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- Controlli di Windows per il codice di notifica NM_SETCURSOR
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119455"
---
# <a name="nm_setcursor-notification-code"></a><span data-ttu-id="90798-105">\_Codice di notifica del SECURSORE Nm</span><span class="sxs-lookup"><span data-stu-id="90798-105">NM\_SETCURSOR notification code</span></span>

<span data-ttu-id="90798-106">Notifica alla finestra padre di un controllo che il controllo sta impostando il cursore in risposta a un messaggio del [**\_ cursore WM**](/windows/desktop/menurc/wm-setcursor) .</span><span class="sxs-lookup"><span data-stu-id="90798-106">Notifies a control's parent window that the control is setting the cursor in response to a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message.</span></span> <span data-ttu-id="90798-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90798-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="90798-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90798-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90798-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90798-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90798-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="90798-110">A pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90798-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90798-111">Return value</span></span>

<span data-ttu-id="90798-112">Restituisce zero per consentire al controllo di impostare il cursore o un valore diverso da zero per impedire al controllo di impostare il cursore.</span><span class="sxs-lookup"><span data-stu-id="90798-112">Return zero to enable the control to set the cursor or nonzero to prevent the control from setting the cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="90798-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90798-113">Requirements</span></span>



| <span data-ttu-id="90798-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90798-114">Requirement</span></span> | <span data-ttu-id="90798-115">Valore</span><span class="sxs-lookup"><span data-stu-id="90798-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90798-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90798-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90798-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90798-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90798-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90798-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90798-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90798-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90798-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90798-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90798-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90798-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

