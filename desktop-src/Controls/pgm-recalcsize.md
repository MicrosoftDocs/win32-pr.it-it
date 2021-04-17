---
title: Messaggio PGM_RECALCSIZE (COMmctrl. h)
description: Impone al controllo pager di ricalcolare la dimensione della finestra contenuta. L'invio di questo messaggio comporterà l'invio di una \_ notifica PGN CALCSIZE. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro RecalcSize del cercapersone.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Controlli di Windows Message PGM_RECALCSIZE
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476312"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="38c25-106">\_Messaggio RECALCSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="38c25-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="38c25-107">Impone al controllo pager di ricalcolare la dimensione della finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="38c25-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="38c25-108">L'invio di questo messaggio comporterà l'invio di una notifica [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="38c25-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="38c25-109">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ RecalcSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .</span><span class="sxs-lookup"><span data-stu-id="38c25-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="38c25-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="38c25-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c25-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38c25-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="38c25-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="38c25-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="38c25-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38c25-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="38c25-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="38c25-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c25-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38c25-115">Return value</span></span>

<span data-ttu-id="38c25-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="38c25-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c25-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38c25-117">Requirements</span></span>



| <span data-ttu-id="38c25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38c25-118">Requirement</span></span> | <span data-ttu-id="38c25-119">Valore</span><span class="sxs-lookup"><span data-stu-id="38c25-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38c25-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38c25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38c25-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38c25-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38c25-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38c25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38c25-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38c25-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38c25-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38c25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38c25-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c25-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





