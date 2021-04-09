---
title: Messaggio TTM_ADJUSTRECT (COMmctrl. h)
description: Calcola il rettangolo di visualizzazione del testo di un controllo ToolTip dal rettangolo della finestra o dal rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- Controlli di Windows Message TTM_ADJUSTRECT
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964244"
---
# <a name="ttm_adjustrect-message"></a><span data-ttu-id="da372-104">\_Messaggio TTM ADJUSTRECT</span><span class="sxs-lookup"><span data-stu-id="da372-104">TTM\_ADJUSTRECT message</span></span>

<span data-ttu-id="da372-105">Calcola il rettangolo di visualizzazione del testo di un controllo ToolTip dal rettangolo della finestra o dal rettangolo della finestra della descrizione comando necessario per visualizzare un rettangolo di visualizzazione del testo specificato.</span><span class="sxs-lookup"><span data-stu-id="da372-105">Calculates a tooltip control's text display rectangle from its window rectangle, or the tooltip window rectangle needed to display a specified text display rectangle.</span></span>

## <a name="parameters"></a><span data-ttu-id="da372-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da372-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da372-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da372-108">Valore che specifica l'operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="da372-108">Value that specifies which operation to perform.</span></span> <span data-ttu-id="da372-109">Se **true**, *lParam* viene usato per specificare un rettangolo di visualizzazione del testo e riceve il rettangolo della finestra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="da372-109">If **TRUE**, *lParam* is used to specify a text-display rectangle and it receives the corresponding window rectangle.</span></span> <span data-ttu-id="da372-110">Se **false**, *lParam* viene usato per specificare un rettangolo della finestra e riceve il rettangolo di visualizzazione del testo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="da372-110">If **FALSE**, *lParam* is used to specify a window rectangle and it receives the corresponding text display rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="da372-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da372-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da372-112">Struttura **Rect** per mantenere un rettangolo della finestra della descrizione comando o un rettangolo di visualizzazione del testo.</span><span class="sxs-lookup"><span data-stu-id="da372-112">**RECT** structure to hold either a tooltip window rectangle or a text display rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da372-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da372-113">Return value</span></span>

<span data-ttu-id="da372-114">Restituisce un valore diverso da zero se il rettangolo viene regolato correttamente e restituisce zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="da372-114">Returns a nonzero value if the rectangle is successfully adjusted, and returns zero if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="da372-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="da372-115">Remarks</span></span>

<span data-ttu-id="da372-116">Questo messaggio è particolarmente utile quando si desidera utilizzare un controllo ToolTip per visualizzare il testo completo di una stringa che in genere viene troncata.</span><span class="sxs-lookup"><span data-stu-id="da372-116">This message is particularly useful when you want to use a tooltip control to display the full text of a string that is usually truncated.</span></span> <span data-ttu-id="da372-117">Viene comunemente usato con i controlli ListView e TreeView.</span><span class="sxs-lookup"><span data-stu-id="da372-117">It is commonly used with listview and treeview controls.</span></span> <span data-ttu-id="da372-118">Questo messaggio viene in genere inviato in risposta a un codice di notifica [TTN \_ show](ttn-show.md) per poter posizionare correttamente il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="da372-118">You typically send this message in response to a [TTN\_SHOW](ttn-show.md) notification code so that you can position the tooltip control properly.</span></span>

<span data-ttu-id="da372-119">Il rettangolo della finestra della descrizione comando è leggermente più grande del rettangolo di visualizzazione del testo che delimita la stringa della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="da372-119">The tooltip window rectangle is somewhat larger than the text display rectangle that bounds the tooltip string.</span></span> <span data-ttu-id="da372-120">Anche l'origine della finestra viene spostata verso l'alto e verso sinistra dall'origine del rettangolo di visualizzazione del testo.</span><span class="sxs-lookup"><span data-stu-id="da372-120">The window origin is also offset up and to the left from the origin of the text display rectangle.</span></span> <span data-ttu-id="da372-121">Per posizionare il rettangolo di visualizzazione del testo, è necessario calcolare il rettangolo della finestra corrispondente e utilizzare tale rettangolo per posizionare la descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="da372-121">To position the text display rectangle, you must calculate the corresponding window rectangle and use that rectangle to position the tooltip.</span></span> <span data-ttu-id="da372-122">**TTM \_ ADJUSTRECT** gestisce automaticamente questo calcolo.</span><span class="sxs-lookup"><span data-stu-id="da372-122">**TTM\_ADJUSTRECT** handles this calculation for you.</span></span>

<span data-ttu-id="da372-123">Se si imposta *wParam* su **true**, **TTM \_ ADJUSTRECT** acquisisce le dimensioni e la posizione del rettangolo di visualizzazione del testo della descrizione comando desiderato e passa di nuovo le dimensioni e la posizione della finestra della descrizione comando necessaria per visualizzare il testo nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="da372-123">If you set *wParam* to **TRUE**, **TTM\_ADJUSTRECT** takes the size and position of the desired tooltip text display rectangle, and passes back the size and position of the tooltip window needed to display the text in the specified position.</span></span> <span data-ttu-id="da372-124">Se si imposta *wParam* su **false**, è possibile specificare un rettangolo della finestra della descrizione comando e **TTM \_ ADJUSTRECT** restituirà le dimensioni e la posizione del rettangolo di testo.</span><span class="sxs-lookup"><span data-stu-id="da372-124">If you set *wParam* to **FALSE**, you can specify a tooltip window rectangle and **TTM\_ADJUSTRECT** will return the size and position of its text rectangle.</span></span>

<span data-ttu-id="da372-125">Il frammento di codice seguente illustra l'uso del messaggio **TTM \_ ADJUSTRECT** per posizionare un controllo ToolTip per visualizzare il testo completo della stringa di un controllo al posto di una stringa troncata.</span><span class="sxs-lookup"><span data-stu-id="da372-125">The following code fragment illustrates the use of the **TTM\_ADJUSTRECT** message to position a tooltip control to display the full text of a control's string in place of a truncated string.</span></span> <span data-ttu-id="da372-126">La funzione **GetMyItemRect** definita dall'applicazione restituisce il rettangolo di testo che sarà necessario per visualizzare il testo della descrizione comando direttamente sulla stringa troncata.</span><span class="sxs-lookup"><span data-stu-id="da372-126">The application-defined **GetMyItemRect** function returns the text rectangle that will be needed to display the tooltip text directly over the truncated string.</span></span> <span data-ttu-id="da372-127">I dettagli relativi all'implementazione di questa funzione dipenderanno dal particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="da372-127">The details of how this function is implemented will depend on the particular control.</span></span> <span data-ttu-id="da372-128">**TTM \_ ADJUSTRECT** viene usato per inviare questo rettangolo di testo al controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="da372-128">**TTM\_ADJUSTRECT** is used to send this text rectangle to the tooltip control.</span></span> <span data-ttu-id="da372-129">Restituisce un rettangolo della finestra posizionata e dimensionato in modo appropriato che viene quindi usato per posizionare la finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="da372-129">It returns an appropriately sized and positioned window rectangle that is then used to position the tooltip window.</span></span>


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a><span data-ttu-id="da372-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da372-130">Requirements</span></span>



| <span data-ttu-id="da372-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="da372-131">Requirement</span></span> | <span data-ttu-id="da372-132">Valore</span><span class="sxs-lookup"><span data-stu-id="da372-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da372-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da372-133">Minimum supported client</span></span><br/> | <span data-ttu-id="da372-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da372-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da372-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da372-135">Minimum supported server</span></span><br/> | <span data-ttu-id="da372-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da372-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da372-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da372-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="da372-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da372-138"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





