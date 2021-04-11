---
title: Messaggio LVM_SETITEMSTATE (COMmctrl. h)
description: Modifica lo stato di un elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemState di ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Controlli di Windows Message LVM_SETITEMSTATE
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119934"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="efbf8-105">\_Messaggio SETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="efbf8-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="efbf8-106">Modifica lo stato di un elemento in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="efbf8-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="efbf8-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .</span><span class="sxs-lookup"><span data-stu-id="efbf8-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="efbf8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efbf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbf8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efbf8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efbf8-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="efbf8-110">Index of the list-view item.</span></span> <span data-ttu-id="efbf8-111">Se questo parametro è-1, la modifica dello stato viene applicata a tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="efbf8-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="efbf8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efbf8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efbf8-113">Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="efbf8-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="efbf8-114">Il membro **stateMask** specifica quali bit di stato modificare e il membro di **stato** contiene i nuovi valori per tali bit.</span><span class="sxs-lookup"><span data-stu-id="efbf8-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="efbf8-115">Gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="efbf8-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbf8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efbf8-116">Return value</span></span>

<span data-ttu-id="efbf8-117">Se si invia questo messaggio in modo esplicito, viene restituito **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efbf8-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="efbf8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="efbf8-118">Remarks</span></span>

<span data-ttu-id="efbf8-119">Il valore dello stato di un elemento include un set di flag di bit che indicano lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efbf8-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="efbf8-120">Il valore dello stato può includere anche gli indici dell'elenco immagini che indicano l'immagine di stato e l'immagine sovrapposta dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efbf8-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbf8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbf8-121">Requirements</span></span>



| <span data-ttu-id="efbf8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbf8-122">Requirement</span></span> | <span data-ttu-id="efbf8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="efbf8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efbf8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbf8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="efbf8-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efbf8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efbf8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbf8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="efbf8-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efbf8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efbf8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efbf8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="efbf8-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="efbf8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





