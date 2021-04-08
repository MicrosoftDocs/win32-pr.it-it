---
title: Messaggio LVM_SETITEM (COMmctrl. h)
description: Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È anche possibile inviare \_ l'elemento per impostare il testo di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItem ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Controlli di Windows Message LVM_SETITEM
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048127"
---
# <a name="lvm_setitem-message"></a><span data-ttu-id="84f7d-106">\_Messaggio SETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="84f7d-106">LVM\_SETITEM message</span></span>

<span data-ttu-id="84f7d-107">Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="84f7d-107">Sets some or all of a list-view item's attributes.</span></span> <span data-ttu-id="84f7d-108">È anche possibile inviare \_ l'elemento per impostare il testo di un elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="84f7d-108">You can also send LVM\_SETITEM to set the text of a subitem.</span></span> <span data-ttu-id="84f7d-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItem ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="84f7d-109">You can send this message explicitly or by using the [**ListView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="84f7d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="84f7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f7d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84f7d-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84f7d-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84f7d-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84f7d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84f7d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84f7d-114">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene gli attributi del nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="84f7d-114">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="84f7d-115">I membri **iItem** e **iSubItem** identificano l'elemento o l'elemento secondario e il membro **mask** specifica gli attributi da impostare.</span><span class="sxs-lookup"><span data-stu-id="84f7d-115">The **iItem** and **iSubItem** members identify the item or subitem, and the **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="84f7d-116">Se il membro **mask** specifica il \_ valore di testo LVIF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="84f7d-116">If the **mask** member specifies the LVIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span> <span data-ttu-id="84f7d-117">Se il membro **mask** specifica il \_ valore dello stato LVIF, il membro **stateMask** specifica quali Stati dell'elemento modificare e il membro di **stato** contiene i valori per tali Stati.</span><span class="sxs-lookup"><span data-stu-id="84f7d-117">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member specifies which item states to change and the **state** member contains the values for those states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f7d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84f7d-118">Return value</span></span>

<span data-ttu-id="84f7d-119">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="84f7d-119">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f7d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="84f7d-120">Remarks</span></span>

<span data-ttu-id="84f7d-121">Per impostare gli attributi di un elemento della visualizzazione elenco, impostare il membro **iItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sull'indice dell'elemento e impostare il membro **iSubItem** su zero.</span><span class="sxs-lookup"><span data-stu-id="84f7d-121">To set the attributes of a list-view item, set the **iItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the index of the item, and set the **iSubItem** member to zero.</span></span> <span data-ttu-id="84f7d-122">Per un elemento, è possibile impostare i membri **state**, **pszText**, **IImage** e **lParam** della struttura **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="84f7d-122">For an item, you can set the **state**, **pszText**, **iImage**, and **lParam** members of the **LVITEM** structure.</span></span>

<span data-ttu-id="84f7d-123">Per impostare il testo di un elemento secondario, impostare i membri **iItem** e **iSubItem** per indicare l'elemento secondario specifico e usare il membro **pszText** per specificare il testo.</span><span class="sxs-lookup"><span data-stu-id="84f7d-123">To set the text of a subitem, set the **iItem** and **iSubItem** members to indicate the specific subitem, and use the **pszText** member to specify the text.</span></span> <span data-ttu-id="84f7d-124">In alternativa, è possibile usare la [**macro \_ SetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) per impostare il testo di un elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="84f7d-124">Alternatively, you can use the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro to set the text of a subitem.</span></span> <span data-ttu-id="84f7d-125">Non è possibile impostare i membri **state** o **lParam** per gli elementi secondari perché gli elementi secondari non dispongono di questi attributi.</span><span class="sxs-lookup"><span data-stu-id="84f7d-125">You cannot set the **state** or **lParam** members for subitems because subitems do not have these attributes.</span></span> <span data-ttu-id="84f7d-126">Nella versione 4,70 e successive, è possibile impostare il membro **IImage** per gli elementi secondari.</span><span class="sxs-lookup"><span data-stu-id="84f7d-126">In version 4.70 and later, you can set the **iImage** member for subitems.</span></span> <span data-ttu-id="84f7d-127">Se il controllo elenco-visualizzazione ha lo stile esteso [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) , verrà visualizzata l'immagine dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="84f7d-127">The subitem image will be displayed if the list-view control has the [**LVS\_EX\_SUBITEMIMAGES**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="84f7d-128">Le versioni precedenti ignoreranno l'immagine dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="84f7d-128">Previous versions will ignore the subitem image.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f7d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84f7d-129">Requirements</span></span>



| <span data-ttu-id="84f7d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f7d-130">Requirement</span></span> | <span data-ttu-id="84f7d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="84f7d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84f7d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f7d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="84f7d-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84f7d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84f7d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f7d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="84f7d-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84f7d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84f7d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84f7d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f7d-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f7d-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="84f7d-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="84f7d-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="84f7d-139">**LVM \_ SETITEMW** (Unicode) e **LVM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="84f7d-139">**LVM\_SETITEMW** (Unicode) and **LVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





