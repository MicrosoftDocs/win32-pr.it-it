---
title: Messaggio LVM_GETITEMTEXT (COMmctrl. h)
description: Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemText di ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Controlli di Windows Message LVM_GETITEMTEXT
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120986"
---
# <a name="lvm_getitemtext-message"></a><span data-ttu-id="8a015-105">\_Messaggio GETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="8a015-105">LVM\_GETITEMTEXT message</span></span>

<span data-ttu-id="8a015-106">Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="8a015-106">Retrieves the text of a list-view item or subitem.</span></span> <span data-ttu-id="8a015-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="8a015-107">You can send this message explicitly or by using the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a015-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a015-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a015-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a015-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a015-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="8a015-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="8a015-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a015-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a015-112">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="8a015-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="8a015-113">Per recuperare il testo dell'elemento, impostare **iSubItem** su zero.</span><span class="sxs-lookup"><span data-stu-id="8a015-113">To retrieve the item text, set **iSubItem** to zero.</span></span> <span data-ttu-id="8a015-114">Per recuperare il testo di un elemento secondario, impostare **iSubItem** sull'indice dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="8a015-114">To retrieve the text of a subitem, set **iSubItem** to the subitem's index.</span></span> <span data-ttu-id="8a015-115">Il membro **pszText** punta a un buffer che riceve il testo.</span><span class="sxs-lookup"><span data-stu-id="8a015-115">The **pszText** member points to a buffer that receives the text.</span></span> <span data-ttu-id="8a015-116">Il membro **cchTextMax** specifica il numero di caratteri nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8a015-116">The **cchTextMax** member specifies the number of characters in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a015-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a015-117">Return value</span></span>

<span data-ttu-id="8a015-118">Se si invia questo messaggio in modo esplicito, viene restituito il numero di caratteri nel membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="8a015-118">If you send this message explicitly, it returns the number of characters in the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a015-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a015-119">Remarks</span></span>

<span data-ttu-id="8a015-120">È anche possibile inviare questo messaggio chiamando la macro [**\_ GetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .</span><span class="sxs-lookup"><span data-stu-id="8a015-120">You can also send this message by calling the [**ListView\_GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) macro.</span></span> <span data-ttu-id="8a015-121">Tuttavia, questa macro non restituisce la lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="8a015-121">However, this macro does not return the string length.</span></span>

<span data-ttu-id="8a015-122">**LVM \_ GETITEMTEXT** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8a015-122">**LVM\_GETITEMTEXT** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a015-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a015-123">Requirements</span></span>



| <span data-ttu-id="8a015-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a015-124">Requirement</span></span> | <span data-ttu-id="8a015-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8a015-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a015-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a015-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a015-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a015-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a015-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a015-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a015-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a015-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a015-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a015-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a015-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a015-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8a015-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8a015-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a015-133">**LVM \_ GETITEMTEXTW** (Unicode) e **LVM \_ GETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a015-133">**LVM\_GETITEMTEXTW** (Unicode) and **LVM\_GETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





