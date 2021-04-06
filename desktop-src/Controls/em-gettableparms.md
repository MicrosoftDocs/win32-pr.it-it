---
title: Messaggio di EM_GETTABLEPARMS (RichEdit. h)
description: Recupera i parametri della tabella per una riga della tabella e i parametri della cella per il numero di celle specificato.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Controlli di Windows Message EM_GETTABLEPARMS
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873710"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="47d39-104">\_Messaggio GETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="47d39-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="47d39-105">Recupera i parametri della tabella per una riga della tabella e i parametri della cella per il numero di celle specificato.</span><span class="sxs-lookup"><span data-stu-id="47d39-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="47d39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47d39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d39-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47d39-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47d39-108">Puntatore a una struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="47d39-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47d39-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47d39-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47d39-110">Puntatore a una struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="47d39-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d39-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47d39-111">Return value</span></span>

<span data-ttu-id="47d39-112">Restituisce \_ OK se ha esito positivo o uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="47d39-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="47d39-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="47d39-113">Return code</span></span>                                                                                    | <span data-ttu-id="47d39-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47d39-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47d39-115"><dt>**E \_ Non riuscita**</dt></span><span class="sxs-lookup"><span data-stu-id="47d39-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="47d39-116">Non è possibile apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="47d39-116">Changes cannot be made.</span></span> <span data-ttu-id="47d39-117">Questa situazione può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico.</span><span class="sxs-lookup"><span data-stu-id="47d39-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="47d39-118">Si verifica anche se le tabelle sono disabilitate se il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) imposta il valore **\_ \_ rilevante ses ex** .</span><span class="sxs-lookup"><span data-stu-id="47d39-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="47d39-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47d39-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="47d39-120">Il valore *wParam* o *lParam* è null o punta a una struttura non valida.</span><span class="sxs-lookup"><span data-stu-id="47d39-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="47d39-121">Il membro **cbRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere uguale a `sizeof(TABLEROWPARMS)` o sizeof (TABLEROWPARMS) 2 \* sizeof (Long).</span><span class="sxs-lookup"><span data-stu-id="47d39-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="47d39-122">Il secondo valore è la dimensione della struttura **TABLEROWPARMS** richedit 4,1.</span><span class="sxs-lookup"><span data-stu-id="47d39-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="47d39-123">Il membro **cbCell** della struttura **TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="47d39-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="47d39-124">La posizione del carattere di query deve trovarsi in un delimitatore di riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="47d39-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="47d39-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47d39-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="47d39-126">La memoria disponibile è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="47d39-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="47d39-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="47d39-127">Remarks</span></span>

<span data-ttu-id="47d39-128">Questo messaggio ottiene i parametri della tabella per la riga nella posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) e il numero di celle specificate dal membro **cCells** della struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="47d39-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="47d39-129">La posizione del carattere specificata dal membro **cpStartRow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere all'inizio della riga della tabella o al delimitatore finale della riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="47d39-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="47d39-130">Se **cpStartRow** è impostato su 1, la posizione del carattere viene fornita dalla selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="47d39-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="47d39-131">In questo caso, posizionare la selezione alla fine della riga (tra il contrassegno della cella e il delimitatore finale della riga della tabella) oppure selezionare la riga.</span><span class="sxs-lookup"><span data-stu-id="47d39-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d39-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47d39-132">Requirements</span></span>



| <span data-ttu-id="47d39-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d39-133">Requirement</span></span> | <span data-ttu-id="47d39-134">Valore</span><span class="sxs-lookup"><span data-stu-id="47d39-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47d39-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47d39-135">Minimum supported client</span></span><br/> | <span data-ttu-id="47d39-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47d39-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="47d39-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47d39-137">Minimum supported server</span></span><br/> | <span data-ttu-id="47d39-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47d39-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47d39-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47d39-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="47d39-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="47d39-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d39-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47d39-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d39-142">**\_SETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="47d39-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





