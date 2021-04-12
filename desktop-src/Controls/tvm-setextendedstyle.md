---
title: Messaggio TVM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Informa il controllo di visualizzazione albero per impostare gli stili estesi. Inviare questo messaggio o usare la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Controlli di Windows Message TVM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517956"
---
# <a name="tvm_setextendedstyle-message"></a><span data-ttu-id="9af2a-105">\_Messaggio SETEXTENDEDSTYLE TVM</span><span class="sxs-lookup"><span data-stu-id="9af2a-105">TVM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="9af2a-106">Informa il controllo di visualizzazione albero per impostare gli stili estesi.</span><span class="sxs-lookup"><span data-stu-id="9af2a-106">Informs the tree-view control to set extended styles.</span></span> <span data-ttu-id="9af2a-107">Inviare questo messaggio o usare la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="9af2a-107">Send this message or use the macro [**TreeView\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="9af2a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9af2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9af2a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af2a-110">Maschera utilizzata per selezionare gli stili da impostare.</span><span class="sxs-lookup"><span data-stu-id="9af2a-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="9af2a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9af2a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9af2a-112">Valore che indica lo stile esteso.</span><span class="sxs-lookup"><span data-stu-id="9af2a-112">Value that indicates the extended style.</span></span> <span data-ttu-id="9af2a-113">Per altre informazioni sugli stili, vedere [stili estesi del controllo di visualizzazione albero](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9af2a-113">For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af2a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9af2a-114">Return value</span></span>

<span data-ttu-id="9af2a-115">Se il messaggio ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9af2a-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9af2a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9af2a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af2a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9af2a-117">Remarks</span></span>

<span data-ttu-id="9af2a-118">Gli stili estesi per un controllo di visualizzazione albero non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.</span><span class="sxs-lookup"><span data-stu-id="9af2a-118">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af2a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9af2a-119">Requirements</span></span>



| <span data-ttu-id="9af2a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af2a-120">Requirement</span></span> | <span data-ttu-id="9af2a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9af2a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9af2a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af2a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9af2a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9af2a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9af2a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9af2a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9af2a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9af2a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9af2a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9af2a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9af2a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9af2a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

