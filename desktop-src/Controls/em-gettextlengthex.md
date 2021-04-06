---
title: Messaggio di EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcola la lunghezza del testo in diversi modi. Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Controlli di Windows Message EM_GETTEXTLENGTHEX
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873709"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="9d358-105">\_Messaggio GetTextLengthEx em</span><span class="sxs-lookup"><span data-stu-id="9d358-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="9d358-106">Calcola la lunghezza del testo in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="9d358-106">Calculates text length in various ways.</span></span> <span data-ttu-id="9d358-107">Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo.</span><span class="sxs-lookup"><span data-stu-id="9d358-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d358-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d358-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d358-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d358-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d358-110">Puntatore a una struttura [**GetTextLengthEx**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) che riceve le informazioni sulla lunghezza del testo.</span><span class="sxs-lookup"><span data-stu-id="9d358-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="9d358-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d358-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d358-112">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9d358-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d358-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d358-113">Return value</span></span>

<span data-ttu-id="9d358-114">Il messaggio restituisce il numero di **TCHAR** nel controllo di modifica, a seconda dell'impostazione dei flag nella struttura [**GetTextLengthEx**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) .</span><span class="sxs-lookup"><span data-stu-id="9d358-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="9d358-115">Se sono stati impostati flag incompatibili nel membro **Flags** , il messaggio restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9d358-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="9d358-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d358-116">Remarks</span></span>

<span data-ttu-id="9d358-117">Questo messaggio è un modo rapido e semplice per determinare il numero di caratteri nella versione Unicode del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9d358-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="9d358-118">Tuttavia, per una tabella codici di destinazione non Unicode, è possibile che si converta in una combinazione di caratteri a byte singolo e a byte doppio.</span><span class="sxs-lookup"><span data-stu-id="9d358-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d358-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d358-119">Requirements</span></span>



| <span data-ttu-id="9d358-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d358-120">Requirement</span></span> | <span data-ttu-id="9d358-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9d358-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d358-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d358-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d358-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d358-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d358-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d358-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d358-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d358-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d358-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d358-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d358-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d358-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d358-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d358-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d358-129">**GETTEXTLENGTHEX**</span><span class="sxs-lookup"><span data-stu-id="9d358-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





