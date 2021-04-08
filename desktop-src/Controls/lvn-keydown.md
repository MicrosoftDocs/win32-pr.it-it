---
title: Codice di notifica LVN_KEYDOWN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata premuta una chiave. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- Controlli di Windows per il codice di notifica LVN_KEYDOWN
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965011"
---
# <a name="lvn_keydown-notification-code"></a><span data-ttu-id="e807f-105">\_Codice di notifica KeyDown LVN</span><span class="sxs-lookup"><span data-stu-id="e807f-105">LVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="e807f-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata premuta una chiave.</span><span class="sxs-lookup"><span data-stu-id="e807f-106">Notifies a list-view control's parent window that a key has been pressed.</span></span> <span data-ttu-id="e807f-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e807f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e807f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e807f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e807f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e807f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e807f-110">Puntatore a una struttura [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) .</span><span class="sxs-lookup"><span data-stu-id="e807f-110">Pointer to an [**NMLVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e807f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e807f-111">Return value</span></span>

<span data-ttu-id="e807f-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e807f-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e807f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e807f-113">Requirements</span></span>



| <span data-ttu-id="e807f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e807f-114">Requirement</span></span> | <span data-ttu-id="e807f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e807f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e807f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e807f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e807f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e807f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e807f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e807f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e807f-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e807f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e807f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e807f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e807f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e807f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





