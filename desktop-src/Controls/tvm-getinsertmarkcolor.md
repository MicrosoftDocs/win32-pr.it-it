---
title: Messaggio TVM_GETINSERTMARKCOLOR (COMmctrl. h)
description: Recupera il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetInsertMarkColor di TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Controlli di Windows Message TVM_GETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964847"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="84e50-105">\_Messaggio GETINSERTMARKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="84e50-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="84e50-106">Recupera il colore utilizzato per creare il segno di inserimento per la visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="84e50-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="84e50-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetInsertMarkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="84e50-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="84e50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="84e50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e50-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84e50-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="84e50-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84e50-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="84e50-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84e50-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="84e50-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="84e50-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e50-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84e50-113">Return value</span></span>

<span data-ttu-id="84e50-114">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il colore del segno di inserimento corrente.</span><span class="sxs-lookup"><span data-stu-id="84e50-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e50-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84e50-115">Requirements</span></span>



| <span data-ttu-id="84e50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84e50-116">Requirement</span></span> | <span data-ttu-id="84e50-117">Valore</span><span class="sxs-lookup"><span data-stu-id="84e50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84e50-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84e50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84e50-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84e50-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84e50-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84e50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84e50-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84e50-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84e50-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84e50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e50-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e50-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84e50-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84e50-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84e50-125">**\_SETINSERTMARKCOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="84e50-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

