---
title: Messaggio LVM_SETITEMTEXT (COMmctrl. h)
description: Modifica il testo di un elemento o di un elemento secondario della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemText di ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Controlli di Windows Message LVM_SETITEMTEXT
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873893"
---
# <a name="lvm_setitemtext-message"></a><span data-ttu-id="49ab7-105">\_Messaggio SETITEMTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="49ab7-105">LVM\_SETITEMTEXT message</span></span>

<span data-ttu-id="49ab7-106">Modifica il testo di un elemento o di un elemento secondario della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="49ab7-106">Changes the text of a list-view item or subitem.</span></span> <span data-ttu-id="49ab7-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .</span><span class="sxs-lookup"><span data-stu-id="49ab7-107">You can send this message explicitly or by using the [**ListView\_SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49ab7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49ab7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ab7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49ab7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49ab7-110">Indice in base zero dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="49ab7-110">Zero-based index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="49ab7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49ab7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49ab7-112">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="49ab7-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="49ab7-113">Il membro **iSubItem** è l'indice dell'elemento secondario oppure può essere zero per impostare l'etichetta dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="49ab7-113">The **iSubItem** member is the index of the subitem, or it can be zero to set the item label.</span></span> <span data-ttu-id="49ab7-114">Il membro **pszText** è l'indirizzo di una stringa con terminazione null che contiene il nuovo testo. può anche essere **null**.</span><span class="sxs-lookup"><span data-stu-id="49ab7-114">The **pszText** member is the address of a null-terminated string containing the new text; it can also be **NULL**.</span></span> <span data-ttu-id="49ab7-115">Il membro **pszText** può anche essere LPSTR \_ TEXTCALLBACK per indicare un elemento di callback per il quale la finestra padre archivia il testo.</span><span class="sxs-lookup"><span data-stu-id="49ab7-115">The **pszText** member can also be LPSTR\_TEXTCALLBACK to indicate a callback item for which the parent window stores the text.</span></span> <span data-ttu-id="49ab7-116">In questo caso, il controllo elenco-visualizzazione Invia all'elemento padre un codice di notifica [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) quando è necessario il testo.</span><span class="sxs-lookup"><span data-stu-id="49ab7-116">In this case, the list-view control sends the parent an [**LVN\_GETDISPINFO**](lvn-getdispinfo.md) notification code when it needs the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ab7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49ab7-117">Return value</span></span>

<span data-ttu-id="49ab7-118">Se si invia questo messaggio in modo esplicito, viene restituito **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="49ab7-118">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ab7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49ab7-119">Requirements</span></span>



| <span data-ttu-id="49ab7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ab7-120">Requirement</span></span> | <span data-ttu-id="49ab7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="49ab7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49ab7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ab7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49ab7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49ab7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49ab7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ab7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49ab7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49ab7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49ab7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49ab7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ab7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ab7-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="49ab7-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="49ab7-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49ab7-129">**LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49ab7-129">**LVM\_SETITEMTEXTW** (Unicode) and **LVM\_SETITEMTEXTA** (ANSI)</span></span><br/>           |



 

 





