---
title: Messaggio TVM_GETITEM (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Controlli di Windows Message TVM_GETITEM
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121699"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="41771-105">\_Messaggio TVM GETitem</span><span class="sxs-lookup"><span data-stu-id="41771-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="41771-106">Recupera alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="41771-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="41771-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="41771-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41771-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41771-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41771-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41771-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41771-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="41771-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41771-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41771-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41771-112">Puntatore a una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che specifica le informazioni per recuperare e ricevere informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="41771-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="41771-113">Con la [versione 4,71](common-control-versions.md) e successive, è invece possibile usare una struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="41771-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41771-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41771-114">Return value</span></span>

<span data-ttu-id="41771-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="41771-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41771-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="41771-116">Remarks</span></span>

<span data-ttu-id="41771-117">Quando il messaggio viene inviato, il membro **hitet** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento per il quale recuperare le informazioni e il membro **mask** specifica gli attributi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="41771-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="41771-118">Se il \_ flag di testo TVIF è impostato nel membro **mask** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri nel buffer.</span><span class="sxs-lookup"><span data-stu-id="41771-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="41771-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41771-119">Requirements</span></span>



| <span data-ttu-id="41771-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="41771-120">Requirement</span></span> | <span data-ttu-id="41771-121">Valore</span><span class="sxs-lookup"><span data-stu-id="41771-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41771-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41771-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41771-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41771-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41771-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41771-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41771-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41771-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41771-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41771-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41771-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41771-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="41771-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="41771-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41771-129">**TVM \_ GETITEMW** (Unicode) e **TVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41771-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





