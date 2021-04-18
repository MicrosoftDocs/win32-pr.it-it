---
title: Messaggio TCM_GETITEM (COMmctrl. h)
description: Recupera le informazioni su una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItem di TabCtrl.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Controlli di Windows Message TCM_GETITEM
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302364"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="49e7f-105">TCM- \_ messaggio GETitem</span><span class="sxs-lookup"><span data-stu-id="49e7f-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="49e7f-106">Recupera le informazioni su una scheda in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="49e7f-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="49e7f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItem di TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .</span><span class="sxs-lookup"><span data-stu-id="49e7f-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49e7f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49e7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49e7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e7f-110">Indice della scheda.</span><span class="sxs-lookup"><span data-stu-id="49e7f-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="49e7f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49e7f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49e7f-112">Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica le informazioni per recuperare e ricevere informazioni sulla scheda. Quando il messaggio viene inviato, il membro **mask** specifica gli attributi da restituire.</span><span class="sxs-lookup"><span data-stu-id="49e7f-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="49e7f-113">Se il membro **mask** specifica il \_ valore di testo TCIF, il membro **pszText** deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro **cchTextMax** deve specificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="49e7f-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e7f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49e7f-114">Return value</span></span>

<span data-ttu-id="49e7f-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="49e7f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e7f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="49e7f-116">Remarks</span></span>

<span data-ttu-id="49e7f-117">Se il \_ flag di testo TCIF è impostato nel membro **mask** della struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto.</span><span class="sxs-lookup"><span data-stu-id="49e7f-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="49e7f-118">Il controllo può impostare il membro **pszText** su **null** per indicare che all'elemento non è associato alcun testo.</span><span class="sxs-lookup"><span data-stu-id="49e7f-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e7f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49e7f-119">Requirements</span></span>



| <span data-ttu-id="49e7f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e7f-120">Requirement</span></span> | <span data-ttu-id="49e7f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="49e7f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49e7f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49e7f-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49e7f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49e7f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49e7f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49e7f-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49e7f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49e7f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49e7f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e7f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e7f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="49e7f-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="49e7f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49e7f-129">**TCM \_ GETITEMW** (Unicode) e **TCM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49e7f-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





