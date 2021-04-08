---
title: Messaggio TVM_HITTEST (COMmctrl. h)
description: Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di TreeView HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Controlli di Windows Message TVM_HITTEST
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048104"
---
# <a name="tvm_hittest-message"></a><span data-ttu-id="a1b76-105">Messaggio di HITTEST di TVM \_</span><span class="sxs-lookup"><span data-stu-id="a1b76-105">TVM\_HITTEST message</span></span>

<span data-ttu-id="a1b76-106">Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="a1b76-106">Determines the location of the specified point relative to the client area of a tree-view control.</span></span> <span data-ttu-id="a1b76-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="a1b76-107">You can send this message explicitly or by using the [**TreeView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1b76-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1b76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b76-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1b76-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a1b76-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a1b76-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a1b76-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1b76-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b76-112">Puntatore a una struttura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="a1b76-112">Pointer to a [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) structure.</span></span> <span data-ttu-id="a1b76-113">Quando il messaggio viene inviato, il membro **PT** specifica le coordinate del punto da testare.</span><span class="sxs-lookup"><span data-stu-id="a1b76-113">When the message is sent, the **pt** member specifies the coordinates of the point to test.</span></span> <span data-ttu-id="a1b76-114">Quando il messaggio viene restituito, il membro **Hite** è l'handle per l'elemento in corrispondenza del punto specificato o **null** se nessun elemento occupa il punto.</span><span class="sxs-lookup"><span data-stu-id="a1b76-114">When the message returns, the **hItem** member is the handle to the item at the specified point or **NULL** if no item occupies the point.</span></span> <span data-ttu-id="a1b76-115">Inoltre, quando il messaggio viene restituito, il membro **Flags** è un valore di hit test che indica la posizione del punto specificato.</span><span class="sxs-lookup"><span data-stu-id="a1b76-115">Also, when the message returns, the **flags** member is a hit test value that indicates the location of the specified point.</span></span> <span data-ttu-id="a1b76-116">Per un elenco di valori di hit test, vedere la descrizione della struttura **TVHITTESTINFO** .</span><span class="sxs-lookup"><span data-stu-id="a1b76-116">For a list of hit test values, see the description of the **TVHITTESTINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b76-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1b76-117">Return value</span></span>

<span data-ttu-id="a1b76-118">Restituisce l'handle per l'elemento della visualizzazione struttura ad albero che occupa il punto specificato o **null** se nessun elemento occupa il punto.</span><span class="sxs-lookup"><span data-stu-id="a1b76-118">Returns the handle to the tree-view item that occupies the specified point, or **NULL** if no item occupies the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b76-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1b76-119">Requirements</span></span>



| <span data-ttu-id="a1b76-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b76-120">Requirement</span></span> | <span data-ttu-id="a1b76-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b76-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b76-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1b76-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b76-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1b76-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1b76-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1b76-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b76-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1b76-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1b76-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1b76-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b76-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b76-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





