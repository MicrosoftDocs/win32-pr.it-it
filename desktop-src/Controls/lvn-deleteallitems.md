---
title: Codice di notifica LVN_DELETEALLITEMS (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che tutti gli elementi del controllo stanno per essere eliminati. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Controlli di Windows per il codice di notifica LVN_DELETEALLITEMS
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965016"
---
# <a name="lvn_deleteallitems-notification-code"></a><span data-ttu-id="a425b-105">\_Codice di notifica DELETEALLITEMS di LVN</span><span class="sxs-lookup"><span data-stu-id="a425b-105">LVN\_DELETEALLITEMS notification code</span></span>

<span data-ttu-id="a425b-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che tutti gli elementi del controllo stanno per essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="a425b-106">Notifies a list-view control's parent window that all items in the control are about to be deleted.</span></span> <span data-ttu-id="a425b-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a425b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a425b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a425b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a425b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a425b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a425b-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="a425b-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="a425b-111">Il membro **iItem** è-1 e gli altri membri sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="a425b-111">The **iItem** member is -1, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a425b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a425b-112">Return value</span></span>

<span data-ttu-id="a425b-113">Per visualizzare i codici di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) successivi, restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="a425b-113">To suppress subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **TRUE**.</span></span>

<span data-ttu-id="a425b-114">Per ricevere i codici di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) successivi, restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="a425b-114">To receive subsequent [LVN\_DELETEITEM](lvn-deleteitem.md) notification codes, return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a425b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a425b-115">Remarks</span></span>

<span data-ttu-id="a425b-116">Un controllo elenco-visualizzazione Invia il codice di notifica [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) quando viene eliminato definitivamente o quando riceve il messaggio **LVM \_ DELETEALLITEMS** .</span><span class="sxs-lookup"><span data-stu-id="a425b-116">A list-view control sends the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) notification code when it is destroyed or when it receives the **LVM\_DELETEALLITEMS** message.</span></span> <span data-ttu-id="a425b-117">Se **LVM \_ DELETEALLITEMS** non restituisce **true**, il controllo invierà anche un codice di notifica [ \_ DeleteItem LVN](lvn-deleteitem.md) quando ogni elemento viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="a425b-117">If **LVM\_DELETEALLITEMS** does not return **TRUE**, the control will also send an [LVN\_DELETEITEM](lvn-deleteitem.md) notification code as each item is deleted.</span></span>

<span data-ttu-id="a425b-118">Se il gestore di messaggi [**\_ DELETEALLITEMS LVM**](lvm-deleteallitems.md) si trova in una routine della finestra di dialogo, restituire **true** dalla routine della finestra di dialogo e utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT per impostare il valore restituito del messaggio.</span><span class="sxs-lookup"><span data-stu-id="a425b-118">If the [**LVM\_DELETEALLITEMS**](lvm-deleteallitems.md) message handler is in a dialog box procedure, return **TRUE** from the dialog box procedure, and use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set the message return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a425b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a425b-119">Requirements</span></span>



| <span data-ttu-id="a425b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a425b-120">Requirement</span></span> | <span data-ttu-id="a425b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a425b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a425b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a425b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a425b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a425b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a425b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a425b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a425b-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a425b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a425b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a425b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a425b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a425b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

