---
title: Messaggio LVM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Controlli di Windows Message LVM_INSERTITEM
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302286"
---
# <a name="lvm_insertitem-message"></a><span data-ttu-id="478ca-105">\_Messaggio INSERTITEM di LVM</span><span class="sxs-lookup"><span data-stu-id="478ca-105">LVM\_INSERTITEM message</span></span>

<span data-ttu-id="478ca-106">Inserisce un nuovo elemento in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="478ca-106">Inserts a new item in a list-view control.</span></span> <span data-ttu-id="478ca-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="478ca-107">You can send this message explicitly or by using the [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="478ca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="478ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="478ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="478ca-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="478ca-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="478ca-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="478ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="478ca-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="478ca-112">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica gli attributi dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="478ca-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the attributes of the list-view item.</span></span> <span data-ttu-id="478ca-113">Usare il membro **iItem** per specificare l'indice in base zero in corrispondenza del quale deve essere inserito il nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="478ca-113">Use the **iItem** member to specify the zero-based index at which the new item should be inserted.</span></span> <span data-ttu-id="478ca-114">Se questo valore è maggiore del numero di elementi attualmente contenuti nel controllo ListView, il nuovo elemento verrà aggiunto alla fine dell'elenco e sarà assegnato l'indice corretto.</span><span class="sxs-lookup"><span data-stu-id="478ca-114">If this value is greater than the number of items currently contained by the listview, the new item will be appended to the end of the list and assigned the correct index.</span></span> <span data-ttu-id="478ca-115">Esaminare il valore restituito del messaggio per determinare l'indice effettivo assegnato all'elemento.</span><span class="sxs-lookup"><span data-stu-id="478ca-115">Examine the message's return value to determine the actual index assigned to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="478ca-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="478ca-116">Return value</span></span>

<span data-ttu-id="478ca-117">Restituisce l'indice del nuovo elemento, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="478ca-117">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="478ca-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="478ca-118">Remarks</span></span>

<span data-ttu-id="478ca-119">Non è possibile usare [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o **LVM \_ InsertItem** per inserire elementi secondari.</span><span class="sxs-lookup"><span data-stu-id="478ca-119">You cannot use [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) or **LVM\_INSERTITEM** to insert subitems.</span></span> <span data-ttu-id="478ca-120">Il membro **iSubItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="478ca-120">The **iSubItem** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure must be zero.</span></span> <span data-ttu-id="478ca-121">Per informazioni sull'impostazione degli elementi secondari, vedere l' [**\_ argomento LVM**](lvm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="478ca-121">See [**LVM\_SETITEM**](lvm-setitem.md) for information on setting subitems.</span></span>

<span data-ttu-id="478ca-122">Se per un controllo di visualizzazione elenco è impostato lo stile [**LVS \_ ex \_**](extended-list-view-styles.md) , qualsiasi valore inserito in bit da 12 a 15 del membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="478ca-122">If a list-view control has the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style set, any value placed in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure will be ignored.</span></span> <span data-ttu-id="478ca-123">Quando viene aggiunto un elemento con questo set di stili, questo viene sempre impostato sullo stato deselezionato.</span><span class="sxs-lookup"><span data-stu-id="478ca-123">When an item is added with this style set, it will always be set to the unchecked state.</span></span>

<span data-ttu-id="478ca-124">Se un controllo di visualizzazione elenco dispone dello stile della finestra [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , un **messaggio \_ INSERTITEM INSERTITEM** avrà esito negativo se si tenta di inserire un elemento con LPSTR TEXTCALLBACK \_ come valore per il relativo membro **pszText** .</span><span class="sxs-lookup"><span data-stu-id="478ca-124">If a list-view control has either the [**LVS\_SORTASCENDING**](list-view-window-styles.md) or [**LVS\_SORTDESCENDING**](list-view-window-styles.md) window style, an **LVM\_INSERTITEM** message will fail if you try to insert an item that has LPSTR\_TEXTCALLBACK as the value for its **pszText** member.</span></span>

<span data-ttu-id="478ca-125">Il **messaggio \_ INSERTITEM INSERTITEM** inserisce il nuovo elemento nella posizione corretta nell'ordinamento se si verificano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="478ca-125">The **LVM\_INSERTITEM** message will insert the new item in the proper position in the sort order if the following conditions hold:</span></span>

-   <span data-ttu-id="478ca-126">Si sta usando uno degli \_ stili SORTXXX di LVS.</span><span class="sxs-lookup"><span data-stu-id="478ca-126">You are using one of the LVS\_SORTXXX styles.</span></span>
-   <span data-ttu-id="478ca-127">Non si usa lo stile [**\_ OWNERDRAW di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="478ca-127">You are not using the [**LVS\_OWNERDRAW**](list-view-window-styles.md) style.</span></span>
-   <span data-ttu-id="478ca-128">Il membro **pszText** della struttura a cui punta **pItem** non è impostato su LPSTR \_ TEXTCALLBACK.</span><span class="sxs-lookup"><span data-stu-id="478ca-128">The **pszText** member of the structure pointed to by **pitem** is not set to LPSTR\_TEXTCALLBACK.</span></span>

<span data-ttu-id="478ca-129">Se la struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) non contiene LVIF \_ GROUPID nel membro **mask** , il valore del membro **iGroupId** è i \_ GROUPIDCALLBACK per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="478ca-129">If the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure does not contain LVIF\_GROUPID in the **mask** member, the value of the **iGroupId** member is I\_GROUPIDCALLBACK by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="478ca-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="478ca-130">Requirements</span></span>



| <span data-ttu-id="478ca-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="478ca-131">Requirement</span></span> | <span data-ttu-id="478ca-132">Valore</span><span class="sxs-lookup"><span data-stu-id="478ca-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="478ca-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="478ca-133">Minimum supported client</span></span><br/> | <span data-ttu-id="478ca-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="478ca-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="478ca-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="478ca-135">Minimum supported server</span></span><br/> | <span data-ttu-id="478ca-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="478ca-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="478ca-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="478ca-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="478ca-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="478ca-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="478ca-139">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="478ca-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="478ca-140">**LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="478ca-140">**LVM\_INSERTITEMW** (Unicode) and **LVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





