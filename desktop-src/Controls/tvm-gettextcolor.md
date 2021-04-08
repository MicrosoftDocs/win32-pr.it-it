---
title: Messaggio TVM_GETTEXTCOLOR (COMmctrl. h)
description: Recupera il colore del testo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTextColor di TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Controlli di Windows Message TVM_GETTEXTCOLOR
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048107"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="3db69-105">\_Messaggio GETTEXTCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="3db69-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="3db69-106">Recupera il colore del testo corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="3db69-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="3db69-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTextColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="3db69-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3db69-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3db69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3db69-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3db69-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3db69-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3db69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3db69-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3db69-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3db69-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db69-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3db69-113">Return value</span></span>

<span data-ttu-id="3db69-114">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo corrente.</span><span class="sxs-lookup"><span data-stu-id="3db69-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="3db69-115">Se questo valore è-1, il controllo Usa il colore di sistema per il colore del testo.</span><span class="sxs-lookup"><span data-stu-id="3db69-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db69-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3db69-116">Requirements</span></span>



| <span data-ttu-id="3db69-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db69-117">Requirement</span></span> | <span data-ttu-id="3db69-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3db69-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3db69-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3db69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3db69-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3db69-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3db69-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3db69-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3db69-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3db69-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3db69-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3db69-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db69-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3db69-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db69-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3db69-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db69-126">**\_SETTEXTCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="3db69-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

