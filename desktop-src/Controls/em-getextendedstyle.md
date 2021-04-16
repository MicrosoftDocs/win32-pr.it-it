---
title: Messaggio EM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera lo stile esteso per un controllo di modifica. Inviare questo messaggio in modo esplicito o usando la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controlli di Windows Message EM_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477921"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="e2069-105">Messaggio EM_GETEXTENDEDSTYLE (COMmctrl. h)</span><span class="sxs-lookup"><span data-stu-id="e2069-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="e2069-106">Recupera lo stile esteso per un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="e2069-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="e2069-107">Inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="e2069-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2069-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2069-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2069-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2069-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e2069-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2069-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2069-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e2069-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e2069-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2069-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2069-113">Return value</span></span>

<span data-ttu-id="e2069-114">Restituisce il valore dello stile esteso. Per altre informazioni sugli stili, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e2069-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2069-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2069-115">Remarks</span></span>

<span data-ttu-id="e2069-116">Gli stili estesi per un controllo di modifica non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.</span><span class="sxs-lookup"><span data-stu-id="e2069-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2069-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2069-117">Requirements</span></span>



| <span data-ttu-id="e2069-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2069-118">Requirement</span></span> | <span data-ttu-id="e2069-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e2069-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2069-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2069-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2069-121">Solo app desktop Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2069-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2069-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2069-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2069-123">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="e2069-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2069-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2069-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2069-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2069-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

