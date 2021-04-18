---
title: Messaggio SB_GETRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di una parte in una finestra di stato.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- Controlli di Windows Message SB_GETRECT
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478101"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="74d03-104">\_Messaggio SB GETrect</span><span class="sxs-lookup"><span data-stu-id="74d03-104">SB\_GETRECT message</span></span>

<span data-ttu-id="74d03-105">Recupera il rettangolo di delimitazione di una parte in una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="74d03-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="74d03-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74d03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74d03-108">Indice in base zero della parte di cui deve essere recuperato il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="74d03-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="74d03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74d03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74d03-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="74d03-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d03-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74d03-111">Return value</span></span>

<span data-ttu-id="74d03-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="74d03-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d03-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74d03-113">Requirements</span></span>



| <span data-ttu-id="74d03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d03-114">Requirement</span></span> | <span data-ttu-id="74d03-115">Valore</span><span class="sxs-lookup"><span data-stu-id="74d03-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74d03-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74d03-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74d03-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74d03-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74d03-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74d03-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74d03-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74d03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d03-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d03-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

