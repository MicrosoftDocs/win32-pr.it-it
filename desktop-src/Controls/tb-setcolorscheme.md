---
title: Messaggio TB_SETCOLORSCHEME (COMmctrl. h)
description: Imposta le informazioni sulla combinazione di colori per il controllo Toolbar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Controlli di Windows Message TB_SETCOLORSCHEME
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874493"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="577c3-104">TB \_ SETCOLORSCHEME messaggio</span><span class="sxs-lookup"><span data-stu-id="577c3-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="577c3-105">Imposta le informazioni sulla combinazione di colori per il controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="577c3-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="577c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="577c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="577c3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="577c3-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="577c3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="577c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="577c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="577c3-110">Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che contiene le informazioni sulla combinazione di colori.</span><span class="sxs-lookup"><span data-stu-id="577c3-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577c3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="577c3-111">Return value</span></span>

<span data-ttu-id="577c3-112">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="577c3-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="577c3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="577c3-113">Remarks</span></span>

<span data-ttu-id="577c3-114">Il controllo toolbar utilizza le informazioni sulla combinazione di colori quando si disegnano gli elementi 3D nel controllo.</span><span class="sxs-lookup"><span data-stu-id="577c3-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="577c3-115">Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="577c3-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="577c3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="577c3-116">Requirements</span></span>



| <span data-ttu-id="577c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="577c3-117">Requirement</span></span> | <span data-ttu-id="577c3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="577c3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="577c3-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="577c3-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="577c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="577c3-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="577c3-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="577c3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="577c3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="577c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="577c3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="577c3-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577c3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="577c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577c3-126">**TB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="577c3-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





