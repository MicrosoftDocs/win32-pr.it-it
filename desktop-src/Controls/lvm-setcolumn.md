---
title: Messaggio LVM_SETCOLUMN (COMmctrl. h)
description: Imposta gli attributi di una colonna della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView secolumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Controlli di Windows Message LVM_SETCOLUMN
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964256"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="0c16a-105">\_Messaggio di colonna LVM</span><span class="sxs-lookup"><span data-stu-id="0c16a-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="0c16a-106">Imposta gli attributi di una colonna della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0c16a-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="0c16a-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ secolumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .</span><span class="sxs-lookup"><span data-stu-id="0c16a-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c16a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c16a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c16a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c16a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c16a-110">Indice della colonna.</span><span class="sxs-lookup"><span data-stu-id="0c16a-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="0c16a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c16a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c16a-112">Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene i nuovi attributi della colonna.</span><span class="sxs-lookup"><span data-stu-id="0c16a-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="0c16a-113">Il membro **mask** specifica gli attributi di colonna da impostare.</span><span class="sxs-lookup"><span data-stu-id="0c16a-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="0c16a-114">Se il membro **mask** specifica il \_ valore di testo LVCF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0c16a-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c16a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c16a-115">Return value</span></span>

<span data-ttu-id="0c16a-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0c16a-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c16a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c16a-117">Requirements</span></span>



| <span data-ttu-id="0c16a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c16a-118">Requirement</span></span> | <span data-ttu-id="0c16a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0c16a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c16a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c16a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0c16a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c16a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c16a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c16a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0c16a-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c16a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c16a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c16a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c16a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c16a-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0c16a-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0c16a-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0c16a-127">**LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0c16a-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





