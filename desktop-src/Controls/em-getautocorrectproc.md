---
title: Messaggio di EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Ottiene un puntatore alla funzione AutoCorrectProc definita dall'applicazione.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Controlli di Windows Message EM_GETAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477116"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="63c53-104">\_Messaggio GETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="63c53-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="63c53-105">Ottiene un puntatore alla funzione [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63c53-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="63c53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c53-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63c53-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63c53-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="63c53-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="63c53-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63c53-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63c53-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="63c53-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c53-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63c53-111">Return value</span></span>

<span data-ttu-id="63c53-112">Restituisce un puntatore alla funzione [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63c53-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c53-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63c53-113">Requirements</span></span>



| <span data-ttu-id="63c53-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c53-114">Requirement</span></span> | <span data-ttu-id="63c53-115">Valore</span><span class="sxs-lookup"><span data-stu-id="63c53-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63c53-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63c53-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63c53-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="63c53-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="63c53-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63c53-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63c53-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="63c53-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63c53-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63c53-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c53-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c53-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c53-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63c53-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c53-123">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="63c53-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="63c53-124">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="63c53-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="63c53-125">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="63c53-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





