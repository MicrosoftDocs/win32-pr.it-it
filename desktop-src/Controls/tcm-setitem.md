---
title: Messaggio TCM_SETITEM (COMmctrl. h)
description: Imposta alcuni o tutti gli attributi di una scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Controlli di Windows Message TCM_SETITEM
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739887"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="3344e-105">\_Messaggio SEtitem (TCM)</span><span class="sxs-lookup"><span data-stu-id="3344e-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="3344e-106">Imposta alcuni o tutti gli attributi di una scheda.</span><span class="sxs-lookup"><span data-stu-id="3344e-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="3344e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .</span><span class="sxs-lookup"><span data-stu-id="3344e-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3344e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3344e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3344e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3344e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3344e-110">Indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3344e-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="3344e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3344e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3344e-112">Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che contiene gli attributi del nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="3344e-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="3344e-113">Il membro **mask** specifica gli attributi da impostare.</span><span class="sxs-lookup"><span data-stu-id="3344e-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="3344e-114">Se il membro **mask** specifica il \_ valore di testo TCIF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3344e-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3344e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3344e-115">Return value</span></span>

<span data-ttu-id="3344e-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3344e-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3344e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3344e-117">Requirements</span></span>



| <span data-ttu-id="3344e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3344e-118">Requirement</span></span> | <span data-ttu-id="3344e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3344e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3344e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3344e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3344e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3344e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3344e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3344e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3344e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3344e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3344e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3344e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3344e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3344e-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3344e-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3344e-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3344e-127">**TCM \_ SETITEMW** (Unicode) e **TCM \_ seitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3344e-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





