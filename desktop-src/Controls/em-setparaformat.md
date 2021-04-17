---
title: Messaggio di EM_SETPARAFORMAT (RichEdit. h)
description: Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Controlli di Windows Message EM_SETPARAFORMAT
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476337"
---
# <a name="em_setparaformat-message"></a><span data-ttu-id="c7fda-104">\_Messaggio SETPARAFORMAT em</span><span class="sxs-lookup"><span data-stu-id="c7fda-104">EM\_SETPARAFORMAT message</span></span>

<span data-ttu-id="c7fda-105">Imposta la formattazione del paragrafo per la selezione corrente in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c7fda-105">Sets the paragraph formatting for the current selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7fda-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7fda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fda-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7fda-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fda-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c7fda-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7fda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7fda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fda-110">Puntatore a una struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) che specifica i nuovi attributi di formattazione del paragrafo.</span><span class="sxs-lookup"><span data-stu-id="c7fda-110">Pointer to a [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure specifying the new paragraph formatting attributes.</span></span> <span data-ttu-id="c7fda-111">Vengono modificati solo gli attributi specificati dal membro **dwMask** .</span><span class="sxs-lookup"><span data-stu-id="c7fda-111">Only the attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="c7fda-112">Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , che è un'estensione della struttura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .</span><span class="sxs-lookup"><span data-stu-id="c7fda-112">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure, which is an extension of the [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) structure.</span></span> <span data-ttu-id="c7fda-113">Prima di inviare il messaggio **\_ SETPARAFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="c7fda-113">Before sending the **EM\_SETPARAFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fda-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7fda-114">Return value</span></span>

<span data-ttu-id="c7fda-115">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c7fda-115">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c7fda-116">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c7fda-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fda-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7fda-117">Requirements</span></span>



| <span data-ttu-id="c7fda-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fda-118">Requirement</span></span> | <span data-ttu-id="c7fda-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c7fda-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fda-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fda-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7fda-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7fda-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fda-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7fda-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7fda-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7fda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fda-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fda-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fda-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7fda-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7fda-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c7fda-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7fda-128">**PARAFORMAT**</span><span class="sxs-lookup"><span data-stu-id="c7fda-128">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[<span data-ttu-id="c7fda-129">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="c7fda-129">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





