---
title: Messaggio di EM_GETPARAFORMAT (RichEdit. h)
description: Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Controlli di Windows Message EM_GETPARAFORMAT
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964757"
---
# <a name="em_getparaformat-message"></a><span data-ttu-id="667c5-104">\_Messaggio GETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="667c5-104">EM\_GETPARAFORMAT message</span></span>

<span data-ttu-id="667c5-105">Recupera la formattazione del paragrafo della selezione corrente in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="667c5-105">Retrieves the paragraph formatting of the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="667c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="667c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="667c5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="667c5-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="667c5-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="667c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="667c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="667c5-110">Puntatore a una struttura [**PARAformata**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che riceve gli attributi di formattazione del paragrafo della selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="667c5-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure that receives the paragraph formatting attributes of the current selection.</span></span>

<span data-ttu-id="667c5-111">Se viene selezionato più di un paragrafo, la struttura riceve gli attributi del primo paragrafo e il membro **dwMask** specifica quali attributi sono coerenti nell'intera selezione.</span><span class="sxs-lookup"><span data-stu-id="667c5-111">If more than one paragraph is selected, the structure receives the attributes of the first paragraph, and the **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span>

<span data-ttu-id="667c5-112">Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , che è un'estensione della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="667c5-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="667c5-113">Prima di inviare il messaggio **\_ GETPARAFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="667c5-113">Before sending the **EM\_GETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="667c5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="667c5-114">Return value</span></span>

<span data-ttu-id="667c5-115">Questo messaggio restituisce il valore del membro **dwMask** della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="667c5-115">This message returns the value of the **dwMask** member of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="667c5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="667c5-116">Requirements</span></span>



| <span data-ttu-id="667c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="667c5-117">Requirement</span></span> | <span data-ttu-id="667c5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="667c5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="667c5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="667c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="667c5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="667c5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="667c5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="667c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="667c5-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="667c5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="667c5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="667c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="667c5-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="667c5-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="667c5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="667c5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="667c5-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="667c5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="667c5-127">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="667c5-127">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="667c5-128">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="667c5-128">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





