---
title: Messaggio LVM_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per tutto o parte di un elemento nella visualizzazione corrente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemRect di ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Controlli di Windows Message LVM_GETITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048646"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="e033b-105">\_Messaggio GETITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="e033b-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="e033b-106">Recupera il rettangolo di delimitazione per tutto o parte di un elemento nella visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e033b-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="e033b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="e033b-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e033b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e033b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e033b-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e033b-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e033b-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e033b-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="e033b-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e033b-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e033b-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e033b-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="e033b-113">Quando il messaggio viene inviato, il membro **sinistro** di questa struttura viene usato per specificare la parte dell'elemento della visualizzazione elenco da cui recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e033b-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="e033b-114">Deve essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e033b-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="e033b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e033b-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="e033b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e033b-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="e033b-117"><dt>**limiti di LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e033b-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="e033b-118">Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="e033b-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="e033b-119"><dt>**\_icona LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="e033b-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="e033b-120">Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola.</span><span class="sxs-lookup"><span data-stu-id="e033b-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="e033b-121"><dt>**\_etichetta LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="e033b-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="e033b-122">Restituisce il rettangolo di delimitazione del testo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e033b-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="e033b-123"><dt>**\_SELECTBOUNDS LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="e033b-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="e033b-124">Restituisce l'Unione dei \_ rettangoli LVIR Icon e LVIR \_ Label, ma esclude le colonne nella visualizzazione report.</span><span class="sxs-lookup"><span data-stu-id="e033b-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e033b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e033b-125">Return value</span></span>

<span data-ttu-id="e033b-126">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e033b-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e033b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e033b-127">Requirements</span></span>



| <span data-ttu-id="e033b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e033b-128">Requirement</span></span> | <span data-ttu-id="e033b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e033b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e033b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e033b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e033b-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e033b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e033b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e033b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e033b-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e033b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e033b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e033b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e033b-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e033b-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

