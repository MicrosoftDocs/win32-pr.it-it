---
title: Messaggio TVM_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetTextColor di TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Controlli di Windows Message TVM_SETTEXTCOLOR
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741999"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="8383b-105">\_Messaggio SETTEXTCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="8383b-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="8383b-106">Imposta il colore del testo del controllo.</span><span class="sxs-lookup"><span data-stu-id="8383b-106">Sets the text color of the control.</span></span> <span data-ttu-id="8383b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetTextColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="8383b-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8383b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8383b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8383b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8383b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8383b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8383b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8383b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8383b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8383b-112">Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del testo.</span><span class="sxs-lookup"><span data-stu-id="8383b-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="8383b-113">Se questo argomento è-1, il controllo verrà ripristinato utilizzando il colore di sistema per il colore del testo.</span><span class="sxs-lookup"><span data-stu-id="8383b-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8383b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8383b-114">Return value</span></span>

<span data-ttu-id="8383b-115">Restituisce un valore **COLORREF** che rappresenta il colore del testo precedente.</span><span class="sxs-lookup"><span data-stu-id="8383b-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="8383b-116">Se questo valore è-1, il controllo Usa il colore di sistema per il colore del testo.</span><span class="sxs-lookup"><span data-stu-id="8383b-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="8383b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8383b-117">Requirements</span></span>



| <span data-ttu-id="8383b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8383b-118">Requirement</span></span> | <span data-ttu-id="8383b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8383b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8383b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8383b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8383b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8383b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8383b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8383b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8383b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8383b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8383b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8383b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8383b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8383b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8383b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8383b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8383b-127">**\_GETTEXTCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="8383b-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

