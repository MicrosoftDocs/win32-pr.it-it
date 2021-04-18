---
title: Messaggio TVM_SETAUTOSCROLLINFO (COMmctrl. h)
description: Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetAutoScrollInfo di TreeView.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Controlli di Windows Message TVM_SETAUTOSCROLLINFO
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301394"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="97079-105">\_Messaggio SETAUTOSCROLLINFO TVM</span><span class="sxs-lookup"><span data-stu-id="97079-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="97079-106">Imposta le informazioni utilizzate per determinare le caratteristiche di scorrimento automatico.</span><span class="sxs-lookup"><span data-stu-id="97079-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="97079-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetAutoScrollInfo di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="97079-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97079-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97079-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97079-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97079-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97079-110">Specifica i pixel al secondo.</span><span class="sxs-lookup"><span data-stu-id="97079-110">Specifies pixels per second.</span></span> <span data-ttu-id="97079-111">L'offset da scorrere è diviso per il *wParam* per determinare la durata totale dello scorrimento automatico.</span><span class="sxs-lookup"><span data-stu-id="97079-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="97079-112">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97079-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97079-113">Specifica l'intervallo di tempo di ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="97079-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="97079-114">Ricreare ogni intervallo di elasped fino a quando l'elemento non viene spostato nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97079-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="97079-115">Dato *wParam*, viene calcolata la posizione dell'elemento e si verifica un ridisegno.</span><span class="sxs-lookup"><span data-stu-id="97079-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="97079-116">Impostare questo valore per creare lo scorrimento uniforme.</span><span class="sxs-lookup"><span data-stu-id="97079-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97079-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97079-117">Return value</span></span>

<span data-ttu-id="97079-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="97079-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97079-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="97079-119">Remarks</span></span>

<span data-ttu-id="97079-120">Le informazioni di scorrimento automatico vengono utilizzate per scorrere un elemento non visibile nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="97079-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="97079-121">Il controllo deve avere lo stile esteso [**\_ \_ AUTOHSCROLL TV ex**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="97079-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="97079-122">Per informazioni sugli stili estesi, vedere Tree-View controllare gli stili estesi.</span><span class="sxs-lookup"><span data-stu-id="97079-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="97079-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97079-123">Requirements</span></span>



| <span data-ttu-id="97079-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97079-124">Requirement</span></span> | <span data-ttu-id="97079-125">Valore</span><span class="sxs-lookup"><span data-stu-id="97079-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97079-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97079-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97079-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97079-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97079-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97079-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97079-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97079-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97079-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97079-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="97079-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97079-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





