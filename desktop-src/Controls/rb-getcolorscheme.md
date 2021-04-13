---
title: Messaggio RB_GETCOLORSCHEME (COMmctrl. h)
description: Recupera le informazioni sulla combinazione di colori dal controllo Rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- Controlli di Windows Message RB_GETCOLORSCHEME
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d154fd14b93127aa22148f2882f70018225cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518279"
---
# <a name="rb_getcolorscheme-message"></a><span data-ttu-id="562d4-104">\_Messaggio GETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="562d4-104">RB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="562d4-105">Recupera le informazioni sulla combinazione di colori dal controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="562d4-105">Retrieves the color scheme information from the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="562d4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="562d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="562d4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="562d4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="562d4-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="562d4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="562d4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="562d4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="562d4-110">Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che riceverà le informazioni sulla combinazione di colori.</span><span class="sxs-lookup"><span data-stu-id="562d4-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="562d4-111">Prima di inviare questo messaggio, è necessario impostare il membro **dwSize** della struttura su **sizeof**(ColorScheme).</span><span class="sxs-lookup"><span data-stu-id="562d4-111">You must set the **dwSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="562d4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="562d4-112">Return value</span></span>

<span data-ttu-id="562d4-113">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="562d4-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="562d4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562d4-114">Requirements</span></span>



| <span data-ttu-id="562d4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="562d4-115">Requirement</span></span> | <span data-ttu-id="562d4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="562d4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="562d4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="562d4-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="562d4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="562d4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="562d4-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="562d4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="562d4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="562d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="562d4-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="562d4-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562d4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562d4-124">**RB \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="562d4-124">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
</dt> </dl>

 

 





