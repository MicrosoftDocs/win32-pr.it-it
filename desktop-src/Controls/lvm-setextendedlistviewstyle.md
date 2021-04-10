---
title: Messaggio LVM_SETEXTENDEDLISTVIEWSTYLE (COMmctrl. h)
description: Imposta gli stili estesi nei controlli visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetExtendedListViewStyle o ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Controlli di Windows Message LVM_SETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963765"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="fdd96-105">\_Messaggio SETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="fdd96-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="fdd96-106">Imposta gli stili estesi nei controlli visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="fdd96-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="fdd96-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="fdd96-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdd96-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdd96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd96-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdd96-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd96-110">Valore **DWORD** che specifica quali stili in *lParam* devono essere interessati.</span><span class="sxs-lookup"><span data-stu-id="fdd96-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="fdd96-111">Questo parametro può essere una combinazione di [**stili di List-View estesa**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="fdd96-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="fdd96-112">Solo gli stili estesi in *wParam* verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="fdd96-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="fdd96-113">Tutti gli altri stili verranno mantenuti così come sono.</span><span class="sxs-lookup"><span data-stu-id="fdd96-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="fdd96-114">Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fdd96-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="fdd96-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdd96-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdd96-116">Valore **DWORD** che specifica gli stili del controllo visualizzazione elenco esteso da impostare.</span><span class="sxs-lookup"><span data-stu-id="fdd96-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="fdd96-117">Questo parametro può essere una combinazione di [**stili di List-View estesa**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="fdd96-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="fdd96-118">Gli stili che non sono impostati, ma che vengono specificati in *wParam*, vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="fdd96-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd96-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdd96-119">Return value</span></span>

<span data-ttu-id="fdd96-120">Restituisce un valore **DWORD** che contiene gli stili del controllo visualizzazione elenco esteso precedente.</span><span class="sxs-lookup"><span data-stu-id="fdd96-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd96-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdd96-121">Remarks</span></span>

<span data-ttu-id="fdd96-122">Il parametro *wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti.</span><span class="sxs-lookup"><span data-stu-id="fdd96-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="fdd96-123">Se ad esempio si passa [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) per *wParam* e 0 per *lParam*, lo stile **LVS \_ ex \_ FULLROWSELECT** verrà cancellato, ma tutti gli altri stili rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="fdd96-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="fdd96-124">Per motivi di compatibilità con le versioni precedenti, la macro [**\_ SetExtendedListViewStyle di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) non è stata aggiornata per l'uso di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="fdd96-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="fdd96-125">Per usare il valore *wParam* , usare la [**macro \_ SetExtendedListViewStyleEx di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="fdd96-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="fdd96-126">Quando si usa questo messaggio per impostare lo stile della [**\_ \_ casella di controllo LVS ex**](extended-list-view-styles.md) , qualsiasi indice di immagine di stato impostato in precedenza verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="fdd96-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="fdd96-127">Tutte le caselle di controllo verranno inizializzate sullo stato deselezionato.</span><span class="sxs-lookup"><span data-stu-id="fdd96-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="fdd96-128">L'indice dell'immagine di stato è contenuto in bit da 12 a 15 del membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="fdd96-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd96-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdd96-129">Requirements</span></span>



| <span data-ttu-id="fdd96-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd96-130">Requirement</span></span> | <span data-ttu-id="fdd96-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fdd96-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd96-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdd96-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd96-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fdd96-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdd96-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdd96-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd96-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fdd96-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdd96-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdd96-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd96-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd96-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





