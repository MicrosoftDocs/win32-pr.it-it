---
title: Messaggio di EM_GETCHARFORMAT (RichEdit. h)
description: Determina la formattazione dei caratteri in un controllo Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Controlli di Windows Message EM_GETCHARFORMAT
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048448"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="06c0b-104">\_Messaggio GETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="06c0b-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="06c0b-105">Determina la formattazione dei caratteri in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="06c0b-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="06c0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06c0b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c0b-108">Specifica l'intervallo di testo da cui recuperare la formattazione.</span><span class="sxs-lookup"><span data-stu-id="06c0b-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="06c0b-109">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="06c0b-109">It can be one of the following values.</span></span>



| <span data-ttu-id="06c0b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="06c0b-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="06c0b-111">Significato</span><span class="sxs-lookup"><span data-stu-id="06c0b-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="06c0b-112"><dt>**\_impostazione predefinita SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="06c0b-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="06c0b-113">Formattazione dei caratteri predefinita.</span><span class="sxs-lookup"><span data-stu-id="06c0b-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="06c0b-114"><dt>**\_selezione SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="06c0b-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="06c0b-115">Formattazione dei caratteri della selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="06c0b-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06c0b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06c0b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c0b-117">Struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) che riceve gli attributi del primo carattere.</span><span class="sxs-lookup"><span data-stu-id="06c0b-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="06c0b-118">Il membro **dwMask** specifica quali attributi sono coerenti nell'intera selezione.</span><span class="sxs-lookup"><span data-stu-id="06c0b-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="06c0b-119">Se, ad esempio, l'intera selezione è in corsivo o non in corsivo, \_ viene impostato cfm Italic; se la selezione è parzialmente in corsivo e non è in parte, cfm \_ corsivo non è impostato.</span><span class="sxs-lookup"><span data-stu-id="06c0b-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="06c0b-120">Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , che è un'estensione della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="06c0b-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="06c0b-121">Prima di inviare il messaggio **\_ GETCHARFORMAT em** , impostare il membro **cbSize** della struttura per indicare la versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="06c0b-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c0b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06c0b-122">Return value</span></span>

<span data-ttu-id="06c0b-123">Questo messaggio restituisce il valore del membro **dwMask** della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="06c0b-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c0b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c0b-124">Requirements</span></span>



| <span data-ttu-id="06c0b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c0b-125">Requirement</span></span> | <span data-ttu-id="06c0b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="06c0b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c0b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c0b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="06c0b-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06c0b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06c0b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c0b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="06c0b-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06c0b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c0b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c0b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c0b-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c0b-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c0b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06c0b-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="06c0b-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="06c0b-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06c0b-135">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="06c0b-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="06c0b-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="06c0b-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





