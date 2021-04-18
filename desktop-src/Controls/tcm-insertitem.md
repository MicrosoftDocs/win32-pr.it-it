---
title: Messaggio TCM_INSERTITEM (COMmctrl. h)
description: Inserisce una nuova scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Controlli di Windows Message TCM_INSERTITEM
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302360"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="dd150-105">\_Messaggio INSERTITEM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="dd150-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="dd150-106">Inserisce una nuova scheda in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="dd150-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="dd150-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="dd150-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd150-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd150-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd150-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd150-110">Indice della nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="dd150-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="dd150-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd150-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd150-112">Puntatore a una struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) che specifica gli attributi della scheda. I membri **dwState** e **dwStateMask** di questa struttura vengono ignorati da questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="dd150-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd150-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd150-113">Return value</span></span>

<span data-ttu-id="dd150-114">Restituisce l'indice della nuova scheda se ha esito positivo oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dd150-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd150-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd150-115">Requirements</span></span>



| <span data-ttu-id="dd150-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd150-116">Requirement</span></span> | <span data-ttu-id="dd150-117">Valore</span><span class="sxs-lookup"><span data-stu-id="dd150-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd150-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd150-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd150-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd150-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd150-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd150-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd150-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd150-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd150-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd150-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd150-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd150-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dd150-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dd150-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dd150-125">**TCM \_ INSERTITEMW** (Unicode) e **TCM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dd150-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





