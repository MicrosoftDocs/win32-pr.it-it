---
title: Codice di notifica TVN_SELCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione sta per passare da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- Controlli di Windows per il codice di notifica TVN_SELCHANGING
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048252"
---
# <a name="tvn_selchanging-notification-code"></a><span data-ttu-id="60746-105">\_Codice di notifica SELCHANGING di TVN</span><span class="sxs-lookup"><span data-stu-id="60746-105">TVN\_SELCHANGING notification code</span></span>

<span data-ttu-id="60746-106">Notifica alla finestra padre di un controllo di visualizzazione albero che la selezione sta per passare da un elemento a un altro.</span><span class="sxs-lookup"><span data-stu-id="60746-106">Notifies a tree-view control's parent window that the selection is about to change from one item to another.</span></span> <span data-ttu-id="60746-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="60746-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="60746-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="60746-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60746-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60746-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60746-110">Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="60746-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="60746-111">I membri **itemOld** e **itemNew** contengono informazioni valide sull'elemento attualmente selezionato e sull'elemento appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="60746-111">The **itemOld** and **itemNew** members contain valid information about the currently selected item and the newly selected item.</span></span> <span data-ttu-id="60746-112">Il membro dell' **azione** indica se un'azione del mouse o della tastiera sta causando la modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="60746-112">The **action** member indicates whether a mouse or keyboard action is causing the selection to change.</span></span> <span data-ttu-id="60746-113">Per un elenco di valori possibili, vedere la descrizione del codice di notifica di [TVN \_ SELCHANGED](tvn-selchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="60746-113">For a list of possible values, see the description of the [TVN\_SELCHANGED](tvn-selchanged.md) notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60746-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60746-114">Return value</span></span>

<span data-ttu-id="60746-115">Restituisce **true** per impedire la modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="60746-115">Returns **TRUE** to prevent the selection from changing.</span></span>

## <a name="remarks"></a><span data-ttu-id="60746-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="60746-116">Remarks</span></span>

<span data-ttu-id="60746-117">Quando si rispondo a questo codice di notifica, le applicazioni non devono eliminare gli elementi che stanno ottenendo o non hanno perso la selezione.</span><span class="sxs-lookup"><span data-stu-id="60746-117">When responding to this notification code, applications should not delete the items that are gaining or losing the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="60746-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60746-118">Requirements</span></span>



| <span data-ttu-id="60746-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="60746-119">Requirement</span></span> | <span data-ttu-id="60746-120">Valore</span><span class="sxs-lookup"><span data-stu-id="60746-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60746-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60746-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60746-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60746-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60746-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60746-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60746-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60746-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60746-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60746-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="60746-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60746-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="60746-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="60746-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="60746-128">**TVN \_ SELCHANGINGW** (Unicode) e **TVN \_ SELCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="60746-128">**TVN\_SELCHANGINGW** (Unicode) and **TVN\_SELCHANGINGA** (ANSI)</span></span><br/>           |



 

 





