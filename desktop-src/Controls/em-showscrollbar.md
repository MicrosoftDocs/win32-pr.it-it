---
title: Messaggio di EM_SHOWSCROLLBAR (RichEdit. h)
description: Consente di visualizzare o nascondere una delle barre di scorrimento nella finestra host di un controllo Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Controlli di Windows Message EM_SHOWSCROLLBAR
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964117"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="cf967-104">\_Messaggio SHOWSCROLLBAR em</span><span class="sxs-lookup"><span data-stu-id="cf967-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="cf967-105">Consente di visualizzare o nascondere una delle barre di scorrimento nella finestra host di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cf967-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf967-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf967-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf967-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf967-108">Identifica la barra di scorrimento da visualizzare: orizzontale o verticale.</span><span class="sxs-lookup"><span data-stu-id="cf967-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="cf967-109">Questo parametro deve essere **SB \_ Vert** o **SB \_ orizzontalmente**.</span><span class="sxs-lookup"><span data-stu-id="cf967-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="cf967-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf967-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf967-111">Consente di specificare se visualizzare o nascondere la barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cf967-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="cf967-112">Specificare **true** per visualizzare la barra di scorrimento e **false** per nasconderlo.</span><span class="sxs-lookup"><span data-stu-id="cf967-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf967-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf967-113">Return value</span></span>

<span data-ttu-id="cf967-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="cf967-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf967-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf967-115">Remarks</span></span>

<span data-ttu-id="cf967-116">Questo metodo è valido solo quando il controllo è attivo sul posto.</span><span class="sxs-lookup"><span data-stu-id="cf967-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="cf967-117">Le chiamate effettuate mentre il controllo è inattivo potrebbero non riuscire.</span><span class="sxs-lookup"><span data-stu-id="cf967-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf967-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf967-118">Requirements</span></span>



| <span data-ttu-id="cf967-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf967-119">Requirement</span></span> | <span data-ttu-id="cf967-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cf967-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf967-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf967-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cf967-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf967-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf967-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf967-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cf967-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf967-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf967-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf967-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf967-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf967-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf967-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf967-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf967-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="cf967-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf967-129">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="cf967-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="cf967-130">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="cf967-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





