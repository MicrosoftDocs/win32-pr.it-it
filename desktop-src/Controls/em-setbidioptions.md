---
title: Messaggio di EM_SETBIDIOPTIONS (RichEdit. h)
description: Il \_ messaggio SETBIDIOPTIONS em imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Controlli di Windows Message EM_SETBIDIOPTIONS
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121046"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="2197c-104">\_Messaggio SETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="2197c-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="2197c-105">Il **messaggio \_ SETBIDIOPTIONS em** imposta lo stato corrente delle opzioni bidirezionali nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2197c-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2197c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2197c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2197c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2197c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2197c-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2197c-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2197c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2197c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2197c-110">Puntatore a una struttura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) che indica come impostare lo stato delle opzioni bidirezionali nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2197c-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2197c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2197c-111">Return value</span></span>

<span data-ttu-id="2197c-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="2197c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2197c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2197c-113">Remarks</span></span>

<span data-ttu-id="2197c-114">Il controllo Rich Edit deve essere in modalità testo normale o **em \_ SETBIDIOPTIONS** non eseguirà alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="2197c-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="2197c-115">Nei controlli testo normale, **em \_ SETBIDIOPTIONS** determina automaticamente la direzione e/o l'allineamento del paragrafo in base alle regole di contesto.</span><span class="sxs-lookup"><span data-stu-id="2197c-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="2197c-116">Queste regole affermano che la direzione e/o l'allineamento derivano dal primo carattere sicuro nel controllo.</span><span class="sxs-lookup"><span data-stu-id="2197c-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="2197c-117">Un carattere sicuro è uno dei quali è possibile determinare la direzione del testo (vedere Unicode Standard Version 2,0).</span><span class="sxs-lookup"><span data-stu-id="2197c-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="2197c-118">La direzione e/o l'allineamento del paragrafo viene applicato al formato predefinito.</span><span class="sxs-lookup"><span data-stu-id="2197c-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="2197c-119">**Em \_ SETBIDIOPTIONS** passa il formato di paragrafo predefinito a RTL (da destra a sinistra) se trova un carattere RTL,</span><span class="sxs-lookup"><span data-stu-id="2197c-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="2197c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2197c-120">Requirements</span></span>



| <span data-ttu-id="2197c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2197c-121">Requirement</span></span> | <span data-ttu-id="2197c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2197c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2197c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2197c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2197c-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2197c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2197c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2197c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2197c-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2197c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2197c-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2197c-127">Redistributable</span></span><br/>          | <span data-ttu-id="2197c-128">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="2197c-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="2197c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2197c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2197c-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2197c-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2197c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2197c-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2197c-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2197c-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2197c-133">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="2197c-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="2197c-134">**\_GETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="2197c-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





