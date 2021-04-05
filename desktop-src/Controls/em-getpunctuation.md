---
title: Messaggio di EM_GETPUNCTUATION (RichEdit. h)
description: Ottiene i caratteri di punteggiatura correnti per il controllo Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Controlli di Windows Message EM_GETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120850"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="83bb9-104">\_Messaggio GETpunteggiation em</span><span class="sxs-lookup"><span data-stu-id="83bb9-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="83bb9-105">Ottiene i caratteri di punteggiatura correnti per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="83bb9-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="83bb9-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="83bb9-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="83bb9-107">Non è supportata nelle versioni successive di Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="83bb9-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="83bb9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83bb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bb9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83bb9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83bb9-110">Il tipo di punteggiatura può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="83bb9-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="83bb9-111">Valore</span><span class="sxs-lookup"><span data-stu-id="83bb9-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="83bb9-112">Significato</span><span class="sxs-lookup"><span data-stu-id="83bb9-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="83bb9-113"><dt>**COMPUTER \_ leader**</dt></span><span class="sxs-lookup"><span data-stu-id="83bb9-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="83bb9-114">Caratteri di punteggiatura iniziali</span><span class="sxs-lookup"><span data-stu-id="83bb9-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="83bb9-115"><dt>**PC che \_ segue**</dt></span><span class="sxs-lookup"><span data-stu-id="83bb9-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="83bb9-116">Caratteri di punteggiatura seguenti</span><span class="sxs-lookup"><span data-stu-id="83bb9-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="83bb9-117"><dt>**\_DElimitatore PC**</dt></span><span class="sxs-lookup"><span data-stu-id="83bb9-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="83bb9-118">Delimitatore</span><span class="sxs-lookup"><span data-stu-id="83bb9-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="83bb9-119"><dt>**OVERFLOW del PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83bb9-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="83bb9-120">Non supportato</span><span class="sxs-lookup"><span data-stu-id="83bb9-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="83bb9-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83bb9-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83bb9-122">Puntatore a una struttura di [**punteggiatura**](/windows/desktop/api/Richedit/ns-richedit-punctuation) che riceve i caratteri di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="83bb9-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bb9-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83bb9-123">Return value</span></span>

<span data-ttu-id="83bb9-124">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="83bb9-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="83bb9-125">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="83bb9-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="83bb9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83bb9-126">Requirements</span></span>



| <span data-ttu-id="83bb9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="83bb9-127">Requirement</span></span> | <span data-ttu-id="83bb9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="83bb9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83bb9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83bb9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83bb9-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83bb9-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83bb9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83bb9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83bb9-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83bb9-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83bb9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83bb9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="83bb9-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="83bb9-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83bb9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83bb9-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="83bb9-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="83bb9-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83bb9-137">**\_punteggiatura em**</span><span class="sxs-lookup"><span data-stu-id="83bb9-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="83bb9-138">**PUNTEGGIATURA**</span><span class="sxs-lookup"><span data-stu-id="83bb9-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





