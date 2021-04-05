---
title: Codice di notifica DL_DROPPED (COMmctrl. h)
description: Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse. Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento. Per ulteriori informazioni, vedere trascinare i messaggi della casella di riepilogo.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- Controlli di Windows per il codice di notifica DL_DROPPED
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874725"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="f9e99-106">\_Codice di notifica eliminato DL</span><span class="sxs-lookup"><span data-stu-id="f9e99-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="f9e99-107">Segnala che l'utente ha completato un'operazione di trascinamento rilasciando il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9e99-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="f9e99-108">Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="f9e99-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="f9e99-109">Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="f9e99-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f9e99-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9e99-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e99-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9e99-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9e99-112">Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica rilasciato DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="f9e99-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9e99-113">Return value</span></span>

<span data-ttu-id="f9e99-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f9e99-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e99-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9e99-115">Remarks</span></span>

<span data-ttu-id="f9e99-116">Questo codice di notifica viene in genere elaborato inserendo l'elemento trascinato nell'elenco davanti all'elemento sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="f9e99-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="f9e99-117">Per recuperare l'indice dell'elemento in corrispondenza della posizione del cursore, utilizzare la funzione [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="f9e99-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="f9e99-118">Si noti che il \_ codice di notifica eliminato DL viene inviato anche se il cursore non si trova in un elemento elenco.</span><span class="sxs-lookup"><span data-stu-id="f9e99-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="f9e99-119">In tal caso, **LBItemFromPt** restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="f9e99-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e99-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9e99-120">Requirements</span></span>



| <span data-ttu-id="f9e99-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e99-121">Requirement</span></span> | <span data-ttu-id="f9e99-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f9e99-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e99-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e99-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e99-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9e99-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9e99-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e99-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e99-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9e99-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9e99-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9e99-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e99-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e99-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





