---
title: Messaggio di EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Controlli di Windows Message EM_GETBIDIOPTIONS
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120015"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="c0183-104">\_Messaggio GETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="c0183-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="c0183-105">Indica lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c0183-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0183-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0183-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0183-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0183-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c0183-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0183-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0183-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0183-110">Struttura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che riceve lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c0183-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0183-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0183-111">Return value</span></span>

<span data-ttu-id="c0183-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c0183-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0183-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0183-113">Remarks</span></span>

<span data-ttu-id="c0183-114">Questo messaggio imposta i valori dei membri **wMask** e **wEffects** sul valore dello stato corrente delle opzioni bidirezionali nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c0183-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0183-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0183-115">Requirements</span></span>



| <span data-ttu-id="c0183-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0183-116">Requirement</span></span> | <span data-ttu-id="c0183-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c0183-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0183-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0183-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0183-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0183-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0183-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0183-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0183-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0183-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0183-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c0183-122">Redistributable</span></span><br/>          | <span data-ttu-id="c0183-123">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="c0183-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="c0183-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0183-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0183-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0183-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0183-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0183-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0183-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c0183-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0183-128">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="c0183-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="c0183-129">**\_SETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="c0183-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





