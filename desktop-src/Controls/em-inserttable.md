---
title: Messaggio di EM_INSERTTABLE (RichEdit. h)
description: Inserisce una o più righe di tabella identiche con celle vuote.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Controlli di Windows Message EM_INSERTTABLE
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475556"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="7bc99-104">\_Messaggio INSERTTABLE em</span><span class="sxs-lookup"><span data-stu-id="7bc99-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="7bc99-105">Inserisce una o più righe di tabella identiche con celle vuote.</span><span class="sxs-lookup"><span data-stu-id="7bc99-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="7bc99-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bc99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc99-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7bc99-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc99-108">Puntatore a una struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="7bc99-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7bc99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bc99-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc99-110">Puntatore a una struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="7bc99-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bc99-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bc99-111">Return value</span></span>

<span data-ttu-id="7bc99-112">Restituisce \_ OK se la tabella viene inserita oppure un codice di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7bc99-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc99-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bc99-113">Remarks</span></span>

<span data-ttu-id="7bc99-114">Se il membro **cpStartRow** di [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) è 1, questo messaggio Elimina il testo selezionato, se presente, e quindi inserisce righe della tabella vuote con i parametri di riga e di cella forniti da *wParam* e *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7bc99-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="7bc99-115">Lascia la selezione che punta all'inizio della prima cella nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="7bc99-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="7bc99-116">Il client può quindi popolare le celle della tabella puntando alla selezione (o a un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) ai vari contrassegni di fine cella e inserendo e formattando il testo desiderato.</span><span class="sxs-lookup"><span data-stu-id="7bc99-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="7bc99-117">Tale testo può includere righe della tabella nidificata.</span><span class="sxs-lookup"><span data-stu-id="7bc99-117">Such text can include nested table rows.</span></span> <span data-ttu-id="7bc99-118">In alternativa, se il membro **cpStartRow** di **TABLEROWPARMS** è maggiore o uguale a 0, le righe della tabella vengono inserite nella posizione del carattere specificata da **cpStartRow**.</span><span class="sxs-lookup"><span data-stu-id="7bc99-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="7bc99-119">Questa operazione modifica solo la selezione corrente se la tabella viene inserita all'interno del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="7bc99-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="7bc99-120">Una tabella Microsoft Rich Edit è costituita da una sequenza di righe di tabella che, a sua volta, è costituita da sequenze di paragrafi.</span><span class="sxs-lookup"><span data-stu-id="7bc99-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="7bc99-121">Una riga di tabella inizia con il paragrafo speciale delimitatore di due caratteri U + FFF9 U + d e termina con il paragrafo di delimitatore di due caratteri U + FFFB U + d.</span><span class="sxs-lookup"><span data-stu-id="7bc99-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="7bc99-122">Ogni cella viene terminata dal contrassegno di cella U + 0007, che viene considerato come un segno di fine del paragrafo rigido esattamente come U + d (CR).</span><span class="sxs-lookup"><span data-stu-id="7bc99-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="7bc99-123">La riga della tabella e i parametri delle celle vengono considerati come formattazione speciale dei delimitatori di riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="7bc99-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="7bc99-124">La formattazione contiene le informazioni contenute nella struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="7bc99-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="7bc99-125">I parametri della cella forniti dalla struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) vengono archiviati in una versione espansa della matrice di schede.</span><span class="sxs-lookup"><span data-stu-id="7bc99-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="7bc99-126">Questo formato consente di annidare le tabelle all'interno di altre tabelle, fino a un massimo di quindici livelli di profondità.</span><span class="sxs-lookup"><span data-stu-id="7bc99-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc99-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bc99-127">Requirements</span></span>



| <span data-ttu-id="7bc99-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bc99-128">Requirement</span></span> | <span data-ttu-id="7bc99-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7bc99-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc99-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bc99-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc99-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7bc99-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7bc99-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bc99-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc99-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7bc99-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bc99-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bc99-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bc99-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bc99-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bc99-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bc99-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc99-137">**\_INSERTIMAGE em**</span><span class="sxs-lookup"><span data-stu-id="7bc99-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





