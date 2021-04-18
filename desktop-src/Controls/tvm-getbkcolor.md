---
title: Messaggio TVM_GETBKCOLOR (COMmctrl. h)
description: Recupera il colore di sfondo corrente del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetBkColor di TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Controlli di Windows Message TVM_GETBKCOLOR
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302279"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="472ec-105">\_Messaggio GETBKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="472ec-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="472ec-106">Recupera il colore di sfondo corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="472ec-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="472ec-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetBkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="472ec-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="472ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="472ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="472ec-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="472ec-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="472ec-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="472ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="472ec-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="472ec-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="472ec-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472ec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="472ec-113">Return value</span></span>

<span data-ttu-id="472ec-114">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo corrente.</span><span class="sxs-lookup"><span data-stu-id="472ec-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="472ec-115">Se questo valore è-1, il controllo Usa il colore di sistema per il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="472ec-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="472ec-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="472ec-116">Requirements</span></span>



| <span data-ttu-id="472ec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="472ec-117">Requirement</span></span> | <span data-ttu-id="472ec-118">Valore</span><span class="sxs-lookup"><span data-stu-id="472ec-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="472ec-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="472ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="472ec-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="472ec-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="472ec-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="472ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="472ec-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="472ec-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="472ec-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="472ec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="472ec-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="472ec-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="472ec-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="472ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472ec-126">**\_SETBKCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="472ec-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

