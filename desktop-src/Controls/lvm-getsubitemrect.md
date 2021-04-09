---
title: Messaggio LVM_GETSUBITEMRECT (COMmctrl. h)
description: Recupera le informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Controlli di Windows Message LVM_GETSUBITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120978"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="2e467-104">\_Messaggio GETSUBITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="2e467-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="2e467-105">Recupera le informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="2e467-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="2e467-106">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetSubItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (scelta consigliata).</span><span class="sxs-lookup"><span data-stu-id="2e467-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="2e467-107">Questo messaggio deve essere utilizzato solo con i controlli visualizzazione elenco che utilizzano lo stile del [**\_ report LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2e467-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e467-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e467-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e467-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e467-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e467-110">Indice dell'elemento padre dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="2e467-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="2e467-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e467-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e467-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul rettangolo di delimitazione dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="2e467-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="2e467-113">I membri devono essere inizializzati in base alle relazioni membro/valore seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e467-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="2e467-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2e467-114">Value</span></span>                                                                                                                             | <span data-ttu-id="2e467-115">Significato</span><span class="sxs-lookup"><span data-stu-id="2e467-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="2e467-116"><dt>**In alto**</dt></span><span class="sxs-lookup"><span data-stu-id="2e467-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="2e467-117">Indice in base uno dell'elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="2e467-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="2e467-118"><dt>**sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="2e467-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="2e467-119">Valore del flag (vedere la sezione Osservazioni).</span><span class="sxs-lookup"><span data-stu-id="2e467-119">Flag value (see remarks).</span></span> <span data-ttu-id="2e467-120">Indica la parte dell'elemento secondario della visualizzazione elenco per la quale recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="2e467-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e467-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e467-121">Return value</span></span>

<span data-ttu-id="2e467-122">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2e467-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e467-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e467-123">Remarks</span></span>

<span data-ttu-id="2e467-124">Di seguito sono riportati i valori di flag che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="2e467-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="2e467-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e467-125">Requirement</span></span> | <span data-ttu-id="2e467-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2e467-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e467-127">**Valore flag**</span><span class="sxs-lookup"><span data-stu-id="2e467-127">**Flag Value**</span></span> | <span data-ttu-id="2e467-128">**Significato**</span><span class="sxs-lookup"><span data-stu-id="2e467-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="2e467-129">limiti di LVIR \_</span><span class="sxs-lookup"><span data-stu-id="2e467-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="2e467-130">Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="2e467-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="2e467-131">\_icona LVIR</span><span class="sxs-lookup"><span data-stu-id="2e467-131">LVIR\_ICON</span></span>     | <span data-ttu-id="2e467-132">Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola.</span><span class="sxs-lookup"><span data-stu-id="2e467-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="2e467-133">\_etichetta LVIR</span><span class="sxs-lookup"><span data-stu-id="2e467-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="2e467-134">Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="2e467-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="2e467-135">Si tratta di un limite identico a LVIR \_ .</span><span class="sxs-lookup"><span data-stu-id="2e467-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2e467-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e467-136">Requirements</span></span>



| <span data-ttu-id="2e467-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e467-137">Requirement</span></span> | <span data-ttu-id="2e467-138">Valore</span><span class="sxs-lookup"><span data-stu-id="2e467-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e467-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e467-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2e467-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e467-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e467-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e467-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2e467-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e467-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e467-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e467-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e467-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e467-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

