---
title: Messaggio LVM_SETITEMCOUNT (COMmctrl. h)
description: Consente al controllo di visualizzazione elenco di allocare memoria per il numero specificato di elementi o di impostare il numero virtuale di elementi in un controllo di visualizzazione elenco virtuale.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Controlli di Windows Message LVM_SETITEMCOUNT
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119334"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="aa8e1-104">\_Messaggio SETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="aa8e1-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="aa8e1-105">Consente al controllo di visualizzazione elenco di allocare memoria per il numero specificato di elementi o di impostare il numero virtuale di elementi in un [controllo di visualizzazione elenco virtuale](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aa8e1-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="aa8e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa8e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa8e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8e1-108">Numero di elementi che il controllo di visualizzazione elenco conterrà infine.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="aa8e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa8e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8e1-110">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="aa8e1-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="aa8e1-111">Valori che specificano il comportamento del controllo visualizzazione elenco dopo la reimpostazione del numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="aa8e1-112">Questo valore può essere una combinazione dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="aa8e1-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="aa8e1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aa8e1-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="aa8e1-114">Significato</span><span class="sxs-lookup"><span data-stu-id="aa8e1-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="aa8e1-115"><dt>**\_NOINVALIDATEALL LVSICF**</dt></span><span class="sxs-lookup"><span data-stu-id="aa8e1-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="aa8e1-116">Il controllo di visualizzazione elenco non verrà ridisegnato a meno che gli elementi interessati non siano attualmente in visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="aa8e1-117"><dt>**LVSICF \_ NOscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="aa8e1-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="aa8e1-118">Il controllo elenco-visualizzazione non modifica la posizione di scorrimento quando cambia il numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa8e1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa8e1-119">Return value</span></span>

<span data-ttu-id="aa8e1-120">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa8e1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa8e1-121">Remarks</span></span>

<span data-ttu-id="aa8e1-122">La modalità di allocazione della memoria dipende dal modo in cui è stato creato il controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="aa8e1-123">È possibile inviare questo messaggio in modo esplicito o usare le macro [**ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) o [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .</span><span class="sxs-lookup"><span data-stu-id="aa8e1-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="aa8e1-124">Per ulteriori informazioni, vedere [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="aa8e1-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="aa8e1-125">Se il controllo elenco-visualizzazione è stato creato senza lo stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) , l'invio di questo messaggio fa in modo che il controllo allochi le strutture di dati interne per il numero specificato di elementi.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="aa8e1-126">In questo modo si impedisce al controllo di allocare le strutture di dati ogni volta che viene aggiunto un elemento.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="aa8e1-127">Se il controllo elenco-visualizzazione è stato creato con lo stile [**LVS \_ OWNERDATA**](list-view-window-styles.md) (visualizzazione elenco virtuale), l'invio di questo messaggio consente di impostare il numero virtuale di elementi contenuti nel controllo.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="aa8e1-128">Il parametro *lParam* è destinato solo ai controlli visualizzazione elenco che usano gli stili [**LVS \_ OWNERDATA**](list-view-window-styles.md) e [**LVS \_ report**](list-view-window-styles.md) o [**LVS \_ List**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8e1-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="aa8e1-129">Quando la visualizzazione elenco di controllo comune è una visualizzazione elenco virtualizzata ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), è presente un limite di 100 milioni elementi nella visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="aa8e1-130">In questo scenario **LVM \_ SETITEMCOUNT** restituirà false se il valore di *wParam* è 100.000.001.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8e1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa8e1-131">Requirements</span></span>



| <span data-ttu-id="aa8e1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa8e1-132">Requirement</span></span> | <span data-ttu-id="aa8e1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="aa8e1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8e1-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa8e1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8e1-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa8e1-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa8e1-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa8e1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8e1-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa8e1-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa8e1-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa8e1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa8e1-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa8e1-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

