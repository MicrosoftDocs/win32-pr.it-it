---
title: Messaggio di EM_HIDESELECTION (RichEdit. h)
description: Il \_ messaggio HIDESELECTION em nasconde o Mostra la selezione in un controllo Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Controlli di Windows Message EM_HIDESELECTION
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963832"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="d76e9-104">\_Messaggio HIDESELECTION em</span><span class="sxs-lookup"><span data-stu-id="d76e9-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="d76e9-105">Il **messaggio \_ HIDESELECTION em** nasconde o Mostra la selezione in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d76e9-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d76e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d76e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d76e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76e9-108">Valore che specifica se nascondere o mostrare la selezione.</span><span class="sxs-lookup"><span data-stu-id="d76e9-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="d76e9-109">Se questo parametro è zero, viene visualizzata la selezione.</span><span class="sxs-lookup"><span data-stu-id="d76e9-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="d76e9-110">In caso contrario, la selezione sarà nascosta.</span><span class="sxs-lookup"><span data-stu-id="d76e9-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="d76e9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d76e9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d76e9-112">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d76e9-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76e9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d76e9-113">Return value</span></span>

<span data-ttu-id="d76e9-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d76e9-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d76e9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d76e9-115">Requirements</span></span>



| <span data-ttu-id="d76e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d76e9-116">Requirement</span></span> | <span data-ttu-id="d76e9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d76e9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d76e9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d76e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d76e9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d76e9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d76e9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d76e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d76e9-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d76e9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d76e9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d76e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76e9-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d76e9-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





