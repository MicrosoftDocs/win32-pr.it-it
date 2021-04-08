---
title: Messaggio LVM_GETVIEWRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di tutti gli elementi nel controllo elenco-visualizzazione. La visualizzazione elenco deve essere visualizzata nell'icona o nella visualizzazione icona piccola. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetViewRect di ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Controlli di Windows Message LVM_GETVIEWRECT
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048642"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="6e5be-106">\_Messaggio GETVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="6e5be-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="6e5be-107">Recupera il rettangolo di delimitazione di tutti gli elementi nel controllo elenco-visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6e5be-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="6e5be-108">La visualizzazione elenco deve essere visualizzata nell'icona o nella visualizzazione icona piccola.</span><span class="sxs-lookup"><span data-stu-id="6e5be-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="6e5be-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetViewRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .</span><span class="sxs-lookup"><span data-stu-id="6e5be-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e5be-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e5be-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5be-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e5be-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e5be-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6e5be-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e5be-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e5be-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e5be-114">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="6e5be-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="6e5be-115">Tutte le coordinate sono relative all'area visibile del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="6e5be-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5be-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e5be-116">Return value</span></span>

<span data-ttu-id="6e5be-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e5be-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5be-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e5be-118">Requirements</span></span>



| <span data-ttu-id="6e5be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e5be-119">Requirement</span></span> | <span data-ttu-id="6e5be-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6e5be-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5be-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e5be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5be-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e5be-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e5be-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e5be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5be-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e5be-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e5be-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e5be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e5be-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e5be-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

