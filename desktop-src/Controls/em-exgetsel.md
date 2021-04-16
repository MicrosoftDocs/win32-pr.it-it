---
title: Messaggio di EM_EXGETSEL (RichEdit. h)
description: Recupera le posizioni dei caratteri iniziali e finali della selezione in un controllo Rich Edit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- Controlli di Windows Message EM_EXGETSEL
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477596"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="acc19-104">\_Messaggio EXGETSEL em</span><span class="sxs-lookup"><span data-stu-id="acc19-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="acc19-105">Recupera le posizioni dei caratteri iniziali e finali della selezione in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="acc19-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="acc19-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="acc19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc19-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acc19-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acc19-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="acc19-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="acc19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acc19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acc19-110">Struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che riceve l'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="acc19-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc19-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acc19-111">Return value</span></span>

<span data-ttu-id="acc19-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="acc19-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc19-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acc19-113">Requirements</span></span>



| <span data-ttu-id="acc19-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc19-114">Requirement</span></span> | <span data-ttu-id="acc19-115">Valore</span><span class="sxs-lookup"><span data-stu-id="acc19-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acc19-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="acc19-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acc19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acc19-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="acc19-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="acc19-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acc19-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acc19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc19-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc19-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc19-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acc19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc19-123">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="acc19-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





