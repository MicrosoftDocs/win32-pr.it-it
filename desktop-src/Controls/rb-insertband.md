---
title: Messaggio RB_INSERTBAND (COMmctrl. h)
description: Inserisce una nuova banda in un controllo Rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Controlli di Windows Message RB_INSERTBAND
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874685"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="1b224-104">\_Messaggio INSERTBAND RB</span><span class="sxs-lookup"><span data-stu-id="1b224-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="1b224-105">Inserisce una nuova banda in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="1b224-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b224-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b224-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b224-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b224-108">Indice in base zero della posizione in cui verrà inserita la banda.</span><span class="sxs-lookup"><span data-stu-id="1b224-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="1b224-109">Se questo parametro viene impostato su-1, il controllo aggiungerà la nuova banda nell'ultima posizione.</span><span class="sxs-lookup"><span data-stu-id="1b224-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="1b224-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b224-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b224-111">Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da inserire.</span><span class="sxs-lookup"><span data-stu-id="1b224-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="1b224-112">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(REBARBANDINFO).</span><span class="sxs-lookup"><span data-stu-id="1b224-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b224-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b224-113">Return value</span></span>

<span data-ttu-id="1b224-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1b224-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b224-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b224-115">Requirements</span></span>



| <span data-ttu-id="1b224-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b224-116">Requirement</span></span> | <span data-ttu-id="1b224-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1b224-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b224-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b224-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b224-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b224-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b224-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b224-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b224-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b224-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b224-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b224-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b224-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b224-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1b224-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1b224-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1b224-125">**RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1b224-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





