---
title: Messaggio TVM_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetInsertMarkColor di TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Controlli di Windows Message TVM_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120102"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="099df-105">\_Messaggio SETINSERTMARKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="099df-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="099df-106">Imposta il colore utilizzato per creare il segno di inserimento per la visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="099df-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="099df-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetInsertMarkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="099df-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="099df-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="099df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="099df-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="099df-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="099df-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="099df-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="099df-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="099df-112">Valore di [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="099df-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099df-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="099df-113">Return value</span></span>

<span data-ttu-id="099df-114">Restituisce un valore **COLORREF** che contiene il colore del segno di inserimento precedente.</span><span class="sxs-lookup"><span data-stu-id="099df-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="099df-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="099df-115">Requirements</span></span>



| <span data-ttu-id="099df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="099df-116">Requirement</span></span> | <span data-ttu-id="099df-117">Valore</span><span class="sxs-lookup"><span data-stu-id="099df-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="099df-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="099df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="099df-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="099df-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="099df-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="099df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="099df-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="099df-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="099df-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="099df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="099df-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="099df-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099df-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="099df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099df-125">**\_GETINSERTMARKCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="099df-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

