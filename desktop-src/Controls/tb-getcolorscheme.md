---
title: Messaggio TB_GETCOLORSCHEME (COMmctrl. h)
description: Recupera le informazioni sulla combinazione di colori dal controllo Toolbar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Controlli di Windows Message TB_GETCOLORSCHEME
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477105"
---
# <a name="tb_getcolorscheme-message"></a><span data-ttu-id="b1bac-104">TB \_ GETCOLORSCHEME messaggio</span><span class="sxs-lookup"><span data-stu-id="b1bac-104">TB\_GETCOLORSCHEME message</span></span>

<span data-ttu-id="b1bac-105">Recupera le informazioni sulla combinazione di colori dal controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="b1bac-105">Retrieves the color scheme information from the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1bac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1bac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1bac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b1bac-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b1bac-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b1bac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1bac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1bac-110">Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che riceverà le informazioni sulla combinazione di colori.</span><span class="sxs-lookup"><span data-stu-id="b1bac-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that will receive the color scheme information.</span></span> <span data-ttu-id="b1bac-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(ColorScheme).</span><span class="sxs-lookup"><span data-stu-id="b1bac-111">You must set the **cbSize** member of this structure to **sizeof**(COLORSCHEME) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1bac-112">Return value</span></span>

<span data-ttu-id="b1bac-113">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b1bac-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bac-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1bac-114">Requirements</span></span>



| <span data-ttu-id="b1bac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1bac-115">Requirement</span></span> | <span data-ttu-id="b1bac-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b1bac-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1bac-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bac-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1bac-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1bac-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1bac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bac-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1bac-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1bac-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1bac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1bac-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bac-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bac-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1bac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bac-124">**TB \_ SETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="b1bac-124">**TB\_SETCOLORSCHEME**</span></span>](tb-setcolorscheme.md)
</dt> </dl>

 

 





