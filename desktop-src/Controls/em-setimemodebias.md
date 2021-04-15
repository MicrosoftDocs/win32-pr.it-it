---
title: Messaggio di EM_SETIMEMODEBIAS (RichEdit. h)
description: Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Controlli di Windows Message EM_SETIMEMODEBIAS
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477320"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="0a48e-104">\_Messaggio SETIMEMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="0a48e-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="0a48e-105">Impostare la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="0a48e-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a48e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a48e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a48e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a48e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a48e-108">Valore di distorsione della modalità IME.</span><span class="sxs-lookup"><span data-stu-id="0a48e-108">IME mode bias value.</span></span> <span data-ttu-id="0a48e-109">Può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a48e-109">It can be one of the following.</span></span>



| <span data-ttu-id="0a48e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="0a48e-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="0a48e-111">Significato</span><span class="sxs-lookup"><span data-stu-id="0a48e-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="0a48e-112"><dt>**\_PLAURALCLAUSE SMODE \_ FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="0a48e-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="0a48e-113">Imposta la distorsione della modalità IME su Name.</span><span class="sxs-lookup"><span data-stu-id="0a48e-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="0a48e-114"><dt>**\_SMODE FMI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a48e-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="0a48e-115">Nessuna distorsione.</span><span class="sxs-lookup"><span data-stu-id="0a48e-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="0a48e-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a48e-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a48e-117">Deve corrispondere al valore *wParam*.</span><span class="sxs-lookup"><span data-stu-id="0a48e-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a48e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a48e-118">Return value</span></span>

<span data-ttu-id="0a48e-119">Questo messaggio restituisce la nuova impostazione di distorsione della modalità IME.</span><span class="sxs-lookup"><span data-stu-id="0a48e-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a48e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a48e-120">Remarks</span></span>

<span data-ttu-id="0a48e-121">Quando l'IME genera un elenco di scelte alternative per un set di caratteri, questo messaggio imposta i criteri in base ai quali verranno visualizzate alcune delle scelte nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0a48e-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="0a48e-122">Per impostare la distorsione della modalità TSF (Text Services Framework), usare [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="0a48e-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="0a48e-123">Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .</span><span class="sxs-lookup"><span data-stu-id="0a48e-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a48e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a48e-124">Requirements</span></span>



| <span data-ttu-id="0a48e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a48e-125">Requirement</span></span> | <span data-ttu-id="0a48e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0a48e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a48e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a48e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0a48e-128">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a48e-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a48e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a48e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0a48e-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a48e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a48e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a48e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a48e-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a48e-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a48e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a48e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a48e-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0a48e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a48e-135">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="0a48e-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="0a48e-136">**\_SETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="0a48e-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





