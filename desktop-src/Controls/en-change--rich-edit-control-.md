---
title: Codice di notifica EN_CHANGE (Rich Edit) (winuser. h)
description: Notifica a una finestra host del controllo Rich Edit senza finestra che si è verificata una modifica. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE (Rich Edit) il codice di notifica controlli di Windows
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964049"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="1d3ef-105">\_Modifica del codice di notifica (Rich Edit)</span><span class="sxs-lookup"><span data-stu-id="1d3ef-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="1d3ef-106">Notifica a una finestra host del controllo Rich Edit senza finestra che si è verificata una modifica.</span><span class="sxs-lookup"><span data-stu-id="1d3ef-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="1d3ef-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3ef-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1d3ef-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d3ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d3ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d3ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d3ef-110">Struttura [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) che specifica la modifica apportata.</span><span class="sxs-lookup"><span data-stu-id="1d3ef-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d3ef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d3ef-111">Return value</span></span>

<span data-ttu-id="1d3ef-112">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1d3ef-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d3ef-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d3ef-113">Remarks</span></span>

<span data-ttu-id="1d3ef-114">Per ricevere \_ i codici di notifica delle modifiche, specificare la [**\_ modifica ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3ef-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d3ef-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d3ef-115">Requirements</span></span>



| <span data-ttu-id="1d3ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d3ef-116">Requirement</span></span> | <span data-ttu-id="1d3ef-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1d3ef-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3ef-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d3ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3ef-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d3ef-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1d3ef-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d3ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3ef-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d3ef-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d3ef-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d3ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d3ef-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d3ef-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3ef-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d3ef-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3ef-125">**TxNotify**</span><span class="sxs-lookup"><span data-stu-id="1d3ef-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





