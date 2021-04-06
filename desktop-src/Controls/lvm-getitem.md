---
title: Messaggio LVM_GETITEM (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Controlli di Windows Message LVM_GETITEM
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742994"
---
# <a name="lvm_getitem-message"></a><span data-ttu-id="19d1f-105">\_Messaggio GETITEM LVM</span><span class="sxs-lookup"><span data-stu-id="19d1f-105">LVM\_GETITEM message</span></span>

<span data-ttu-id="19d1f-106">Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="19d1f-106">Retrieves some or all of a list-view item's attributes.</span></span> <span data-ttu-id="19d1f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="19d1f-107">You can send this message explicitly or by using the [**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="19d1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19d1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19d1f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="19d1f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="19d1f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="19d1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19d1f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19d1f-112">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica le informazioni per recuperare e ricevere informazioni sull'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="19d1f-112">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that specifies the information to retrieve and receives information about the list-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d1f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19d1f-113">Return value</span></span>

<span data-ttu-id="19d1f-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="19d1f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d1f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="19d1f-115">Remarks</span></span>

<span data-ttu-id="19d1f-116">Quando viene inviato il messaggio **LVM \_ GetItem** , i membri **iItem** e **iSubItem** identificano l'elemento o l'elemento secondario per il recupero delle informazioni su e il membro **mask** specifica gli attributi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="19d1f-116">When the **LVM\_GETITEM** message is sent, the **iItem** and **iSubItem** members identify the item or subitem to retrieve information about and the **mask** member specifies which attributes to retrieve.</span></span> <span data-ttu-id="19d1f-117">Per un elenco di valori possibili, vedere la descrizione della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="19d1f-117">For a list of possible values, see the description of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

<span data-ttu-id="19d1f-118">Se il \_ flag di testo LVIF è impostato nel membro **mask** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri nel buffer.</span><span class="sxs-lookup"><span data-stu-id="19d1f-118">If the LVIF\_TEXT flag is set in the **mask** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span> <span data-ttu-id="19d1f-119">Le applicazioni non devono presupporre che il testo venga necessariamente inserito nel buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="19d1f-119">Applications should not assume that the text will necessarily be placed in the specified buffer.</span></span> <span data-ttu-id="19d1f-120">Il controllo può invece modificare il membro **pszText** della struttura in modo che punti al nuovo testo, anziché posizionarlo nel buffer.</span><span class="sxs-lookup"><span data-stu-id="19d1f-120">The control may instead change the **pszText** member of the structure to point to the new text, rather than place it in the buffer.</span></span>

<span data-ttu-id="19d1f-121">Se il membro **mask** specifica il \_ valore dello stato LVIF, è necessario che il membro **stateMask** specifichi i bit di stato dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="19d1f-121">If the **mask** member specifies the LVIF\_STATE value, the **stateMask** member must specify the item state bits to retrieve.</span></span> <span data-ttu-id="19d1f-122">Nell'output il membro di **stato** contiene i valori dei bit di stato specificati.</span><span class="sxs-lookup"><span data-stu-id="19d1f-122">On output, the **state** member contains the values of the specified state bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d1f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19d1f-123">Requirements</span></span>



| <span data-ttu-id="19d1f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19d1f-124">Requirement</span></span> | <span data-ttu-id="19d1f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="19d1f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19d1f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19d1f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19d1f-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19d1f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19d1f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19d1f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19d1f-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19d1f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19d1f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19d1f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="19d1f-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d1f-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="19d1f-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="19d1f-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19d1f-133">**LVM \_ GETITEMW** (Unicode) e **LVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19d1f-133">**LVM\_GETITEMW** (Unicode) and **LVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





