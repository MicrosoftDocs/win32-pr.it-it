---
title: Codice di notifica DL_DRAGGING (COMmctrl. h)
description: Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- Controlli di Windows per il codice di notifica DL_DRAGGING
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519334"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="26d5a-104">Codice di notifica per il \_ trascinamento DL</span><span class="sxs-lookup"><span data-stu-id="26d5a-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="26d5a-105">Segnala che l'utente ha spostato il mouse durante il trascinamento di un elemento.</span><span class="sxs-lookup"><span data-stu-id="26d5a-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="26d5a-106">\_Anche il trascinamento DL DL viene inviato periodicamente durante il trascinamento anche se il mouse non viene spostato.</span><span class="sxs-lookup"><span data-stu-id="26d5a-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="26d5a-107">Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="26d5a-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="26d5a-108">Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="26d5a-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="26d5a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26d5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d5a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26d5a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26d5a-111">Identificatore di controllo della casella di riepilogo di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="26d5a-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="26d5a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26d5a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26d5a-113">Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica di trascinamento DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="26d5a-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d5a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26d5a-114">Return value</span></span>

<span data-ttu-id="26d5a-115">Il valore restituito determina il tipo di cursore del mouse che deve essere impostato dall'elenco di trascinamento. può essere il valore DL \_ STOPCURSOR, DL \_ COPYCURSOR o DL \_ MOVECURSOR.</span><span class="sxs-lookup"><span data-stu-id="26d5a-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="26d5a-116">Se viene restituito qualsiasi altro valore, il cursore non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="26d5a-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d5a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="26d5a-117">Remarks</span></span>

<span data-ttu-id="26d5a-118">Una routine della finestra elabora in genere il \_ codice di notifica di trascinamento del DL, determinando l'elemento sotto il cursore e quindi disegnando un'icona di inserimento.</span><span class="sxs-lookup"><span data-stu-id="26d5a-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="26d5a-119">Per recuperare l'elemento sotto il cursore, utilizzare la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , specificando **true** per il parametro *bAutoScroll* .</span><span class="sxs-lookup"><span data-stu-id="26d5a-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="26d5a-120">Questa opzione fa in modo che la casella di riepilogo di trascinamento scorra periodicamente se il cursore si trova sopra o sotto la relativa area client.</span><span class="sxs-lookup"><span data-stu-id="26d5a-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="26d5a-121">Per creare l'icona Inserisci, utilizzare la funzione [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .</span><span class="sxs-lookup"><span data-stu-id="26d5a-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d5a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26d5a-122">Requirements</span></span>



| <span data-ttu-id="26d5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d5a-123">Requirement</span></span> | <span data-ttu-id="26d5a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="26d5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26d5a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26d5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="26d5a-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26d5a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26d5a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26d5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="26d5a-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26d5a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26d5a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26d5a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d5a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d5a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





