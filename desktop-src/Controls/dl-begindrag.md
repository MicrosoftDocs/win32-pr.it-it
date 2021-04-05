---
title: Codice di notifica DL_BEGINDRAG (COMmctrl. h)
description: Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento. Una casella di riepilogo di trascinamento Invia questo codice di notifica sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere trascinare i messaggi della casella di riepilogo.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- Controlli di Windows per il codice di notifica DL_BEGINDRAG
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874722"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="417da-106">\_Codice di notifica BEGINDRAG DL</span><span class="sxs-lookup"><span data-stu-id="417da-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="417da-107">Notifica alla finestra padre della casella di riepilogo di trascinamento che l'utente ha fatto clic con il pulsante sinistro del mouse su un elemento.</span><span class="sxs-lookup"><span data-stu-id="417da-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="417da-108">Una casella di riepilogo di trascinamento Invia questo codice di notifica sotto forma di messaggio elenco di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="417da-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="417da-109">Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="417da-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="417da-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="417da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="417da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="417da-112">Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica BEGINDRAG DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="417da-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417da-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="417da-113">Return value</span></span>

<span data-ttu-id="417da-114">Restituisce **true** per avviare l'operazione di trascinamento oppure **false** per impedire l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="417da-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="417da-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="417da-115">Remarks</span></span>

<span data-ttu-id="417da-116">Quando si elabora questo codice di notifica, una routine della finestra determina in genere l'elemento dell'elenco in corrispondenza della posizione del cursore specificata tramite la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="417da-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="417da-117">Restituisce quindi **true** o **false**, a seconda che l'elemento debba essere trascinato.</span><span class="sxs-lookup"><span data-stu-id="417da-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="417da-118">Prima di restituire **true**, la routine della finestra deve salvare l'indice dell'elemento di elenco in modo che l'applicazione conosca quale elemento spostare o copiare al termine dell'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="417da-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="417da-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="417da-119">Requirements</span></span>



| <span data-ttu-id="417da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="417da-120">Requirement</span></span> | <span data-ttu-id="417da-121">Valore</span><span class="sxs-lookup"><span data-stu-id="417da-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="417da-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="417da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="417da-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="417da-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="417da-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="417da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="417da-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="417da-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="417da-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="417da-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="417da-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="417da-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





