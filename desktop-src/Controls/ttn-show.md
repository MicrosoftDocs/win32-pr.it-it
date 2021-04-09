---
title: Codice di notifica TTN_SHOW (COMmctrl. h)
description: Notifica alla finestra del proprietario che un controllo ToolTip sta per essere visualizzato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- Controlli di Windows per il codice di notifica TTN_SHOW
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964288"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="33b1a-105">TTN \_ Mostra il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="33b1a-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="33b1a-106">Notifica alla finestra del proprietario che un controllo ToolTip sta per essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="33b1a-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="33b1a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="33b1a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="33b1a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33b1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b1a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33b1a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33b1a-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="33b1a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b1a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33b1a-111">Return value</span></span>

<span data-ttu-id="33b1a-112">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="33b1a-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="33b1a-113">Per visualizzare la descrizione comando nel percorso predefinito, restituire zero.</span><span class="sxs-lookup"><span data-stu-id="33b1a-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="33b1a-114">Per personalizzare la posizione della descrizione comando, riposizionare la finestra della descrizione comando con la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) e restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="33b1a-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="33b1a-115">Per le versioni precedenti alla 4,70, non viene restituito alcun valore.</span><span class="sxs-lookup"><span data-stu-id="33b1a-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="33b1a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="33b1a-116">Remarks</span></span>

<span data-ttu-id="33b1a-117">Un rettangolo della finestra descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo e l'origine viene sfalsata verso l'alto e verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="33b1a-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="33b1a-118">Se è necessario posizionare in modo accurato il rettangolo di visualizzazione del testo di una descrizione comando, il messaggio [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) converte un rettangolo di visualizzazione del testo nel rettangolo corrispondente della finestra della descrizione comando e viceversa.</span><span class="sxs-lookup"><span data-stu-id="33b1a-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b1a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33b1a-119">Requirements</span></span>



| <span data-ttu-id="33b1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33b1a-120">Requirement</span></span> | <span data-ttu-id="33b1a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="33b1a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33b1a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33b1a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33b1a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33b1a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33b1a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33b1a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33b1a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33b1a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33b1a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33b1a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

