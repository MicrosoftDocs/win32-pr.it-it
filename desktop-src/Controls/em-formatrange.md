---
title: Messaggio di EM_FORMATRANGE (RichEdit. h)
description: Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Controlli di Windows Message EM_FORMATRANGE
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873941"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="1e8de-104">\_Messaggio FormatRange em</span><span class="sxs-lookup"><span data-stu-id="1e8de-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="1e8de-105">Formatta un intervallo di testo in un controllo Rich Edit per un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="1e8de-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e8de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e8de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e8de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e8de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e8de-108">Specifica se eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="1e8de-108">Specifies whether to render the text.</span></span> <span data-ttu-id="1e8de-109">Se questo parametro è diverso da zero, viene eseguito il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="1e8de-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="1e8de-110">In caso contrario, il testo viene semplicemente misurato.</span><span class="sxs-lookup"><span data-stu-id="1e8de-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="1e8de-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e8de-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e8de-112">Struttura [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contenente informazioni sul dispositivo di output oppure **null** per liberare informazioni memorizzate nella cache dal controllo.</span><span class="sxs-lookup"><span data-stu-id="1e8de-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e8de-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e8de-113">Return value</span></span>

<span data-ttu-id="1e8de-114">Questo messaggio restituisce l'indice dell'ultimo carattere che rientra nell'area, più 1.</span><span class="sxs-lookup"><span data-stu-id="1e8de-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e8de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e8de-115">Remarks</span></span>

<span data-ttu-id="1e8de-116">Questo messaggio viene in genere usato per formattare il contenuto del controllo Rich Edit per un dispositivo di output, ad esempio una stampante.</span><span class="sxs-lookup"><span data-stu-id="1e8de-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="1e8de-117">Dopo aver usato questo messaggio per formattare un intervallo di testo, è importante liberare le informazioni memorizzate nella cache inviando nuovamente **em \_ FormatRange** , ma con *lParam* impostato su **null**. in caso contrario, si verificherà una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="1e8de-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="1e8de-118">Inoltre, dopo aver usato questo messaggio per un dispositivo, è necessario liberare le informazioni memorizzate nella cache prima di riutilizzarlo per un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="1e8de-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e8de-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e8de-119">Requirements</span></span>



| <span data-ttu-id="1e8de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e8de-120">Requirement</span></span> | <span data-ttu-id="1e8de-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1e8de-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e8de-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e8de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e8de-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e8de-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e8de-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e8de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e8de-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e8de-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e8de-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e8de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e8de-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e8de-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e8de-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e8de-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e8de-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1e8de-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e8de-130">**\_DISPLAYBAND em**</span><span class="sxs-lookup"><span data-stu-id="1e8de-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="1e8de-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1e8de-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e8de-132">Stampa di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="1e8de-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





