---
title: Messaggio di EM_SETPUNCTUATION (RichEdit. h)
description: Imposta i caratteri di punteggiatura per un controllo Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Controlli di Windows Message EM_SETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121030"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="3903c-104">\_Messaggio di DEpunteggiatura em</span><span class="sxs-lookup"><span data-stu-id="3903c-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="3903c-105">Imposta i caratteri di punteggiatura per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3903c-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="3903c-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="3903c-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="3903c-107">Non è supportata nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3903c-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="3903c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3903c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3903c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3903c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3903c-110">Specifica il tipo di punteggiatura. i possibili valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="3903c-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="3903c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3903c-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3903c-112">Significato</span><span class="sxs-lookup"><span data-stu-id="3903c-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="3903c-113"><dt>**COMPUTER \_ leader**</dt></span><span class="sxs-lookup"><span data-stu-id="3903c-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="3903c-114">Caratteri di punteggiatura iniziali.</span><span class="sxs-lookup"><span data-stu-id="3903c-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="3903c-115"><dt>**PC che \_ segue**</dt></span><span class="sxs-lookup"><span data-stu-id="3903c-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="3903c-116">Caratteri di punteggiatura seguenti.</span><span class="sxs-lookup"><span data-stu-id="3903c-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="3903c-117"><dt>**\_DElimitatore PC**</dt></span><span class="sxs-lookup"><span data-stu-id="3903c-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="3903c-118">Delimitatore.</span><span class="sxs-lookup"><span data-stu-id="3903c-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="3903c-119"><dt>**Computer \_ OVERFLOW**</dt></span><span class="sxs-lookup"><span data-stu-id="3903c-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="3903c-120">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="3903c-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="3903c-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3903c-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3903c-122">Puntatore a una struttura di [**punteggiatura**](/windows/desktop/api/Richedit/ns-richedit-punctuation) che contiene i caratteri di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="3903c-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3903c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3903c-123">Return value</span></span>

<span data-ttu-id="3903c-124">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3903c-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3903c-125">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3903c-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3903c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3903c-126">Requirements</span></span>



| <span data-ttu-id="3903c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3903c-127">Requirement</span></span> | <span data-ttu-id="3903c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3903c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3903c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3903c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3903c-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3903c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3903c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3903c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3903c-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3903c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3903c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3903c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3903c-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3903c-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3903c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3903c-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="3903c-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3903c-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3903c-137">**\_GETpunteggiatura em**</span><span class="sxs-lookup"><span data-stu-id="3903c-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="3903c-138">**PUNTEGGIATURA**</span><span class="sxs-lookup"><span data-stu-id="3903c-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





