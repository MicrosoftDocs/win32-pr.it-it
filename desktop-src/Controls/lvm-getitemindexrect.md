---
title: Messaggio LVM_GETITEMINDEXRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetItemIndexRect di ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Controlli di Windows Message LVM_GETITEMINDEXRECT
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478521"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="fca81-105">\_Messaggio GETITEMINDEXRECT LVM</span><span class="sxs-lookup"><span data-stu-id="fca81-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="fca81-106">Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="fca81-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="fca81-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetItemIndexRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .</span><span class="sxs-lookup"><span data-stu-id="fca81-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fca81-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fca81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca81-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fca81-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fca81-110">Puntatore a una struttura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento padre dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="fca81-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="fca81-111">Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri.</span><span class="sxs-lookup"><span data-stu-id="fca81-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="fca81-112">*wParam* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fca81-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fca81-113">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fca81-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fca81-114">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate.</span><span class="sxs-lookup"><span data-stu-id="fca81-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="fca81-115">Il processo chiamante è responsabile dell'allocazione di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="fca81-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="fca81-116">*lParam* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fca81-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="fca81-117">Imposta il membro **superiore** sull'indice dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="fca81-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="fca81-118">Impostare il membro **Left** su uno dei valori seguenti, che indica la parte dell'elemento secondario per cui deve essere recuperato il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="fca81-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="fca81-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fca81-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="fca81-120">Significato</span><span class="sxs-lookup"><span data-stu-id="fca81-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="fca81-121"><dt>**limiti di LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fca81-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="fca81-122">Restituisce il rettangolo di delimitazione dell'intero elemento secondario, incluse l'icona e l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="fca81-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="fca81-123"><dt>**\_icona LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="fca81-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="fca81-124">Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="fca81-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="fca81-125"><dt>**\_etichetta LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="fca81-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="fca81-126">Restituisce il rettangolo di delimitazione del testo dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="fca81-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca81-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fca81-127">Return value</span></span>

<span data-ttu-id="fca81-128">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fca81-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca81-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fca81-129">Requirements</span></span>



| <span data-ttu-id="fca81-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca81-130">Requirement</span></span> | <span data-ttu-id="fca81-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fca81-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fca81-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fca81-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fca81-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fca81-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fca81-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fca81-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fca81-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fca81-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fca81-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fca81-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fca81-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca81-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

