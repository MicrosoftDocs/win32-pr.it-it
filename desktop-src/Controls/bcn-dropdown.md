---
title: Codice di notifica BCN_DROPDOWN (winuser. h)
description: Inviato quando l'utente fa clic su una freccia a discesa di un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di un messaggio di \_ notifica WM.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- Controlli di Windows per il codice di notifica BCN_DROPDOWN
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301396"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="3f83e-105">\_Codice di notifica a discesa BCN</span><span class="sxs-lookup"><span data-stu-id="3f83e-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="3f83e-106">Inviato quando l'utente fa clic su una freccia a discesa di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="3f83e-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="3f83e-107">La finestra padre del controllo riceve questo codice di notifica sotto forma di un messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3f83e-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3f83e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f83e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f83e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f83e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f83e-110">Puntatore a una struttura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="3f83e-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="3f83e-111">Il membro **rcButton** è impostato in modo da descrivere l'area a discesa.</span><span class="sxs-lookup"><span data-stu-id="3f83e-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f83e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f83e-112">Return value</span></span>

<span data-ttu-id="3f83e-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3f83e-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f83e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f83e-114">Remarks</span></span>

<span data-ttu-id="3f83e-115">Il ricevitore di notifiche esegue il cast di **lParam** per recuperare la struttura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="3f83e-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="3f83e-116">**WParam** contiene l'ID del controllo che invia questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3f83e-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="3f83e-117">Il controllo Button deve avere uno stile del pulsante a discesa.</span><span class="sxs-lookup"><span data-stu-id="3f83e-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f83e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f83e-118">Requirements</span></span>



| <span data-ttu-id="3f83e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f83e-119">Requirement</span></span> | <span data-ttu-id="3f83e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3f83e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f83e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f83e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3f83e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f83e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f83e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f83e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3f83e-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f83e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f83e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f83e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f83e-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f83e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





