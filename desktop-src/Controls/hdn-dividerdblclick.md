---
title: Codice di notifica HDN_DIVIDERDBLCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sull'area del divisore del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- Controlli di Windows per il codice di notifica HDN_DIVIDERDBLCLICK
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048776"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="3fc3e-105">\_Codice di notifica DIVIDERDBLCLICK di HDN</span><span class="sxs-lookup"><span data-stu-id="3fc3e-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="3fc3e-106">Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto doppio clic sull'area del divisore del controllo.</span><span class="sxs-lookup"><span data-stu-id="3fc3e-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="3fc3e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3fc3e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3fc3e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fc3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc3e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fc3e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc3e-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento il cui divisore è stato fatto doppio clic.</span><span class="sxs-lookup"><span data-stu-id="3fc3e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fc3e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fc3e-111">Return value</span></span>

<span data-ttu-id="3fc3e-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3fc3e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc3e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fc3e-113">Requirements</span></span>



| <span data-ttu-id="3fc3e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc3e-114">Requirement</span></span> | <span data-ttu-id="3fc3e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3fc3e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc3e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc3e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc3e-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fc3e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fc3e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc3e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc3e-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fc3e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fc3e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fc3e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc3e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc3e-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3fc3e-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3fc3e-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3fc3e-123">**HDN \_ DIVIDERDBLCLICKW** (Unicode) e **HDN \_ DIVIDERDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3fc3e-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 





