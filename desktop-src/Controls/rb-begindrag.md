---
title: Messaggio RB_BEGINDRAG (COMmctrl. h)
description: Inserisce il controllo Rebar in modalità di trascinamento della selezione. Questo messaggio non comporta l' \_ invio di una notifica RBN BEGINDRAG.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Controlli di Windows Message RB_BEGINDRAG
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477890"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="e1296-105">\_Messaggio BEGINDRAG RB</span><span class="sxs-lookup"><span data-stu-id="e1296-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="e1296-106">Inserisce il controllo Rebar in modalità di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="e1296-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="e1296-107">Questo messaggio non comporta l'invio di una notifica [RBN \_ BEGINDRAG](rbn-begindrag.md) .</span><span class="sxs-lookup"><span data-stu-id="e1296-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1296-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1296-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1296-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1296-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1296-110">Indice in base zero della banda che avrà effetto sull'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="e1296-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="e1296-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1296-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1296-112">Valore **DWORD** che contiene le coordinate iniziali del mouse.</span><span class="sxs-lookup"><span data-stu-id="e1296-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="e1296-113">La coordinata orizzontale è contenuta in LOWORD e la coordinata verticale è contenuta in HIWORD.</span><span class="sxs-lookup"><span data-stu-id="e1296-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="e1296-114">Se si passa (**DWORD**)-1, il controllo Rebar utilizzerà la posizione del mouse nell'ultima volta in cui il thread del controllo ha chiamato [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="e1296-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1296-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1296-115">Return value</span></span>

<span data-ttu-id="e1296-116">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e1296-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1296-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1296-117">Remarks</span></span>

<span data-ttu-id="e1296-118">I **messaggi \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)e [**RB \_ ENDDRAG**](rb-enddrag.md) consentono di implementare un'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) per un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="e1296-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="e1296-119">Inviare il messaggio **RB \_ BEGINDRAG** in risposta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), inviare il messaggio **RB \_ DRAGMOVE** in risposta a [**IDropTarget::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)e il messaggio **RB \_ ENDDRAG** in risposta a [**IDropTarget::D por**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="e1296-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1296-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1296-120">Requirements</span></span>



| <span data-ttu-id="e1296-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1296-121">Requirement</span></span> | <span data-ttu-id="e1296-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e1296-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1296-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1296-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e1296-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1296-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e1296-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1296-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e1296-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1296-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e1296-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1296-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1296-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1296-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

