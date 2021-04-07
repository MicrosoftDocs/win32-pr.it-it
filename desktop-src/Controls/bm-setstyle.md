---
title: Messaggio BM_SETSTYLE (winuser. h)
description: Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro di tipo Button.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Controlli di Windows Message BM_SETSTYLE
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963943"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="5f574-105">\_Messaggio SESTYLE BM</span><span class="sxs-lookup"><span data-stu-id="5f574-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="5f574-106">Imposta lo stile di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="5f574-106">Sets the style of a button.</span></span> <span data-ttu-id="5f574-107">È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ tipo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .</span><span class="sxs-lookup"><span data-stu-id="5f574-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f574-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f574-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f574-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f574-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f574-110">Stile del pulsante.</span><span class="sxs-lookup"><span data-stu-id="5f574-110">The button style.</span></span> <span data-ttu-id="5f574-111">Questo parametro può essere una combinazione di stili dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="5f574-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="5f574-112">Per una tabella di stili di pulsante, vedere [stili dei pulsanti](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="5f574-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f574-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f574-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f574-114">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di *lParam* è un valore **bool** che specifica se il pulsante deve essere ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="5f574-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="5f574-115">Il valore **true** riestrae il pulsante; il valore **false** non consente di ricreare il pulsante.</span><span class="sxs-lookup"><span data-stu-id="5f574-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f574-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f574-116">Return value</span></span>

<span data-ttu-id="5f574-117">Questo messaggio restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="5f574-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f574-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f574-118">Requirements</span></span>



| <span data-ttu-id="5f574-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f574-119">Requirement</span></span> | <span data-ttu-id="5f574-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5f574-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f574-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f574-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f574-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f574-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f574-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f574-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f574-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5f574-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f574-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f574-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f574-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f574-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

