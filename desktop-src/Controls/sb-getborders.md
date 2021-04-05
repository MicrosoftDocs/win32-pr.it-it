---
title: Messaggio SB_GETBORDERS (COMmctrl. h)
description: Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Controlli di Windows Message SB_GETBORDERS
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120706"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="1dfaf-104">\_Messaggio SB GETborders</span><span class="sxs-lookup"><span data-stu-id="1dfaf-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="1dfaf-105">Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dfaf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dfaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfaf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dfaf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1dfaf-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1dfaf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dfaf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfaf-110">Puntatore a una matrice di interi con tre elementi.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="1dfaf-111">Il primo elemento riceve la larghezza del bordo orizzontale, il secondo riceve la larghezza del bordo verticale e il terzo riceve la larghezza del bordo tra i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfaf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dfaf-112">Return value</span></span>

<span data-ttu-id="1dfaf-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dfaf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dfaf-114">Remarks</span></span>

<span data-ttu-id="1dfaf-115">I bordi determinano la spaziatura tra il bordo esterno della finestra e i rettangoli all'interno della finestra che contengono testo.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="1dfaf-116">I bordi determinano anche la spaziatura tra i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="1dfaf-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfaf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dfaf-117">Requirements</span></span>



| <span data-ttu-id="1dfaf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfaf-118">Requirement</span></span> | <span data-ttu-id="1dfaf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1dfaf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfaf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dfaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfaf-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dfaf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1dfaf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dfaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfaf-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1dfaf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dfaf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dfaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfaf-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfaf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





