---
title: Messaggio di EM_SETTABLEPARMS (RichEdit. h)
description: Modifica i parametri delle righe in una tabella.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Controlli di Windows Message EM_SETTABLEPARMS
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964051"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="d9bd6-104">\_Messaggio SETTABLEPARMS em</span><span class="sxs-lookup"><span data-stu-id="d9bd6-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="d9bd6-105">Modifica i parametri delle righe in una tabella.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9bd6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9bd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bd6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9bd6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9bd6-108">Puntatore a una struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="d9bd6-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d9bd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9bd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9bd6-110">Puntatore a una struttura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="d9bd6-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bd6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9bd6-111">Return value</span></span>

<span data-ttu-id="d9bd6-112">Restituisce \_ OK se ha esito positivo o uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="d9bd6-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d9bd6-113">Return code</span></span>                                                                                    | <span data-ttu-id="d9bd6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9bd6-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9bd6-115"><dt>**E \_ Non riuscita**</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="d9bd6-116">Non è possibile apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-116">Changes cannot be made.</span></span> <span data-ttu-id="d9bd6-117">Questa situazione può verificarsi se il controllo è un controllo di testo normale o a riga singola o se il punto di inserimento si trova all'interno di un oggetto matematico.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="d9bd6-118">Si verifica anche se le tabelle sono disabilitate o se il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) imposta il valore **\_ \_ rilevante ses ex** .</span><span class="sxs-lookup"><span data-stu-id="d9bd6-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d9bd6-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="d9bd6-120">Il valore *wParam* o *lParam* è null o punta a una struttura non valida.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="d9bd6-121">Il membro **cCell** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve essere almeno 1 e non superiore a 63.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="d9bd6-122">Il membro **cbRow** deve essere uguale a `sizeof(TABLEROWPARMS)` o `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="d9bd6-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="d9bd6-123">Il secondo valore è la dimensione della struttura **TABLEROWPARMS** richedit 4,1.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="d9bd6-124">Il membro **cbCell** di **TABLEROWPARMS** deve essere uguale a `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="d9bd6-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="d9bd6-125">Il punto di inserimento deve trovarsi all'inizio di una tabella o all'interno di una riga di tabella e il numero di celle può essere modificato solo di uno.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="d9bd6-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="d9bd6-127">La memoria disponibile è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d9bd6-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9bd6-128">Remarks</span></span>

<span data-ttu-id="d9bd6-129">Questo messaggio modifica i parametri del numero di righe specificato dal membro **Crow** della struttura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , se la tabella contiene molte righe consecutive.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="d9bd6-130">Se **Crow** è minore di 0, il messaggio scorre fino alla fine della tabella.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="d9bd6-131">Se il nuovo numero di celle è diverso dal numero di celle corrente per + 1 o 1, inserisce o Elimina la cella in corrispondenza dell'indice specificato dal membro **iCell** di **TABLEROWPARMS**.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="d9bd6-132">La riga della tabella iniziale è identificata da una posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="d9bd6-133">Questa posizione viene specificata dai membri **cpStartRow** con valori maggiori o uguali a zero.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="d9bd6-134">La posizione deve essere all'interno della riga della tabella, ma non all'interno di una tabella nidificata, a meno che non si desideri modificare i parametri della tabella.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="d9bd6-135">Se il membro **cpStartRow** è 1, la posizione del carattere viene fornita dalla selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="d9bd6-136">A questo scopo, posizionare la selezione in un punto qualsiasi all'interno della riga della tabella oppure selezionare la riga con la fine attiva della selezione alla fine della riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="d9bd6-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9bd6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9bd6-137">Requirements</span></span>



| <span data-ttu-id="d9bd6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9bd6-138">Requirement</span></span> | <span data-ttu-id="d9bd6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="d9bd6-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bd6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bd6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d9bd6-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d9bd6-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d9bd6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9bd6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d9bd6-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d9bd6-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9bd6-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9bd6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9bd6-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9bd6-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9bd6-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9bd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd6-147">**\_GETTABLEPARMS em**</span><span class="sxs-lookup"><span data-stu-id="d9bd6-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





