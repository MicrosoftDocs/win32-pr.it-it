---
title: Messaggio di EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Imposta la procedura estesa di Word break per un controllo Rich Edit.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Controlli di Windows Message EM_SETWORDBREAKPROCEX
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964050"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="a45cb-104">\_Messaggio SETWORDBREAKPROCEX em</span><span class="sxs-lookup"><span data-stu-id="a45cb-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="a45cb-105">Imposta la procedura estesa di Word break per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a45cb-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a45cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a45cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a45cb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45cb-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a45cb-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a45cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a45cb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a45cb-110">Puntatore a una funzione [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) o **null** per utilizzare la procedura predefinita.</span><span class="sxs-lookup"><span data-stu-id="a45cb-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45cb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a45cb-111">Return value</span></span>

<span data-ttu-id="a45cb-112">Questo messaggio restituisce l'indirizzo della precedente procedura di Breaking di Word estesa.</span><span class="sxs-lookup"><span data-stu-id="a45cb-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a45cb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a45cb-113">Requirements</span></span>



| <span data-ttu-id="a45cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45cb-114">Requirement</span></span> | <span data-ttu-id="a45cb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a45cb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a45cb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a45cb-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a45cb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a45cb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a45cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a45cb-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a45cb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a45cb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a45cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a45cb-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a45cb-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45cb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a45cb-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a45cb-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a45cb-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a45cb-124">**EditWordBreakProcEx**</span><span class="sxs-lookup"><span data-stu-id="a45cb-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="a45cb-125">**\_GETWORDBREAKPROCEX em**</span><span class="sxs-lookup"><span data-stu-id="a45cb-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





