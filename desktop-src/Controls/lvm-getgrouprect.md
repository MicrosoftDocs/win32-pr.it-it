---
title: Messaggio LVM_GETGROUPRECT (COMmctrl. h)
description: Ottiene il rettangolo per un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupRect di ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Controlli di Windows Message LVM_GETGROUPRECT
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963805"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="41a9f-105">\_Messaggio GETGROUPRECT LVM</span><span class="sxs-lookup"><span data-stu-id="41a9f-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="41a9f-106">Ottiene il rettangolo per un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="41a9f-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="41a9f-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .</span><span class="sxs-lookup"><span data-stu-id="41a9f-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41a9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41a9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a9f-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41a9f-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a9f-110">Specifica il gruppo per **iGroupId** (vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="41a9f-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="41a9f-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="41a9f-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41a9f-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere informazioni sul gruppo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="41a9f-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="41a9f-113">Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="41a9f-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="41a9f-114">Il processo chiamante è responsabile dell'allocazione della memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="41a9f-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="41a9f-115">Impostare il membro **superiore** di [**Rect**](/previous-versions//dd162897(v=vs.85)) su uno dei flag seguenti per specificare le coordinate del rettangolo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="41a9f-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="41a9f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="41a9f-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="41a9f-117">Significato</span><span class="sxs-lookup"><span data-stu-id="41a9f-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="41a9f-118"><dt>**\_gruppo LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="41a9f-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="41a9f-119">Coordinate dell'intero gruppo espanso.</span><span class="sxs-lookup"><span data-stu-id="41a9f-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="41a9f-120"><dt>**\_intestazione LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="41a9f-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="41a9f-121">Coordinate dell'intestazione Only (gruppo compresso).</span><span class="sxs-lookup"><span data-stu-id="41a9f-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="41a9f-122"><dt>**\_etichetta LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="41a9f-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="41a9f-123">Solo coordinate dell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="41a9f-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="41a9f-124"><dt>**\_SUBSETLINK LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="41a9f-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="41a9f-125">Coordinate del solo collegamento del subset (subset di markup).</span><span class="sxs-lookup"><span data-stu-id="41a9f-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="41a9f-126">Un controllo visualizzazione elenco può limitare il numero di elementi visibili visualizzati in ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="41a9f-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="41a9f-127">Viene visualizzato un collegamento all'utente per consentire all'utente di espandere il gruppo.</span><span class="sxs-lookup"><span data-stu-id="41a9f-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="41a9f-128">Questo flag restituirà il rettangolo di delimitazione del collegamento del subset se il gruppo è un subset (stato del gruppo di LVGS \_ subset, vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **stato** membro).</span><span class="sxs-lookup"><span data-stu-id="41a9f-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="41a9f-129">Questo flag viene fornito in modo che le applicazioni di accessibilità possano trovare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="41a9f-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a9f-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41a9f-130">Return value</span></span>

<span data-ttu-id="41a9f-131">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="41a9f-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a9f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41a9f-132">Requirements</span></span>



| <span data-ttu-id="41a9f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a9f-133">Requirement</span></span> | <span data-ttu-id="41a9f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="41a9f-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41a9f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a9f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="41a9f-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41a9f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41a9f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a9f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="41a9f-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41a9f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41a9f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41a9f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a9f-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a9f-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

