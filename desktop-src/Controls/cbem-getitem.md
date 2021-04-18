---
title: Messaggio CBEM_GETITEM (COMmctrl. h)
description: Ottiene le informazioni sugli elementi per un elemento ComboBoxEx specificato.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Controlli di Windows Message CBEM_GETITEM
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302298"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="37976-104">CBEM \_ messaggio GETitem</span><span class="sxs-lookup"><span data-stu-id="37976-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="37976-105">Ottiene le informazioni sugli elementi per un elemento ComboBoxEx specificato.</span><span class="sxs-lookup"><span data-stu-id="37976-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="37976-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37976-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37976-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="37976-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="37976-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="37976-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37976-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37976-110">Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che riceve le informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="37976-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37976-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37976-111">Return value</span></span>

<span data-ttu-id="37976-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="37976-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="37976-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="37976-113">Remarks</span></span>

<span data-ttu-id="37976-114">Quando il messaggio viene inviato, è necessario impostare i membri **iItem** e **mask** della struttura per indicare l'indice dell'elemento di destinazione e il tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="37976-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="37976-115">Gli altri membri vengono impostati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="37976-115">Other members are set as needed.</span></span> <span data-ttu-id="37976-116">Ad esempio, per recuperare il testo, è necessario impostare il \_ flag di testo CBEIF in **mask** e assegnare un valore a **cchTextMax**.</span><span class="sxs-lookup"><span data-stu-id="37976-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="37976-117">Se si imposta il membro **iItem** su-1, verrà recuperato l'elemento visualizzato nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="37976-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="37976-118">Se il \_ flag di testo CBEIF è impostato nel membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , il controllo può modificare il membro **pszText** della struttura in modo che punti al nuovo testo anziché riempire il buffer con il testo richiesto.</span><span class="sxs-lookup"><span data-stu-id="37976-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="37976-119">Le applicazioni non devono presupporre che il testo venga sempre inserito nel buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="37976-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="37976-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37976-120">Requirements</span></span>



| <span data-ttu-id="37976-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="37976-121">Requirement</span></span> | <span data-ttu-id="37976-122">Valore</span><span class="sxs-lookup"><span data-stu-id="37976-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37976-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37976-123">Minimum supported client</span></span><br/> | <span data-ttu-id="37976-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37976-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37976-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37976-125">Minimum supported server</span></span><br/> | <span data-ttu-id="37976-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37976-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37976-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37976-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="37976-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37976-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="37976-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="37976-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37976-130">**CBEM \_ GETITEMW** (Unicode) e **CBEM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37976-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





