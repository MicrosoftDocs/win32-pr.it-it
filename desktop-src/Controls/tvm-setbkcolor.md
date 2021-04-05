---
title: Messaggio TVM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkColor di TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Controlli di Windows Message TVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874010"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="75112-105">\_Messaggio SETBKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="75112-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="75112-106">Imposta il colore di sfondo del controllo.</span><span class="sxs-lookup"><span data-stu-id="75112-106">Sets the background color of the control.</span></span> <span data-ttu-id="75112-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="75112-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="75112-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75112-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75112-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75112-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="75112-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75112-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="75112-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75112-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75112-112">Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="75112-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="75112-113">Se questo valore è-1, il controllo verrà ripristinato utilizzando il colore di sistema per il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="75112-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75112-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75112-114">Return value</span></span>

<span data-ttu-id="75112-115">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo precedente.</span><span class="sxs-lookup"><span data-stu-id="75112-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="75112-116">Se questo valore è-1, il controllo Usa il colore di sistema per il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="75112-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="75112-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75112-117">Requirements</span></span>



| <span data-ttu-id="75112-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75112-118">Requirement</span></span> | <span data-ttu-id="75112-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75112-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75112-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75112-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75112-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75112-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75112-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75112-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75112-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75112-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75112-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75112-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75112-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75112-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75112-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75112-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75112-127">**\_GETBKCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="75112-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

