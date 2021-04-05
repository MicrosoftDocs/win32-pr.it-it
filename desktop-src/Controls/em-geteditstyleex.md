---
title: Messaggio di EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera i flag di stile di modifica estesa correnti.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Controlli di Windows Message EM_GETEDITSTYLEEX
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873913"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="b9d15-104">\_Messaggio GETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="b9d15-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="b9d15-105">Recupera i flag di stile di modifica estesa correnti.</span><span class="sxs-lookup"><span data-stu-id="b9d15-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="b9d15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9d15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d15-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9d15-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d15-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9d15-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b9d15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9d15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d15-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b9d15-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d15-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9d15-111">Return value</span></span>

<span data-ttu-id="b9d15-112">Restituisce i flag di stile di modifica estesa, che possono includere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9d15-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="b9d15-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b9d15-113">Return code</span></span>                                                                                                | <span data-ttu-id="b9d15-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9d15-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9d15-115"><dt>**SES \_ es \_ HANDLEFRIENDLYURL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="b9d15-116">Consente di visualizzare i collegamenti con nome descrittivo con lo stesso colore del testo e la sottostruttura dei collegamenti automatici, a condizione che la formattazione temporanea non sia usata o usi il colore automatico del testo (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="b9d15-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="b9d15-117"><dt>**\_multitouch es \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="b9d15-118">Abilita il supporto tocco in Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b9d15-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="b9d15-119">Sono incluse selezione, posizionamento del cursore e chiamata al menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b9d15-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="b9d15-120">Quando questo flag non è impostato, il tocco viene emulato dai comandi del mouse, che non prendono in considerazione le specifiche della modalità tocco (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="b9d15-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="b9d15-121"><dt>**SES \_ es \_ NOACETATESELECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="b9d15-122">Visualizza il testo selezionato usando il testo di selezione di Windows classico e i colori di sfondo anziché il colore dell'acetato di sfondo (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="b9d15-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="b9d15-123"><dt>**SES \_ ex \_ nomath**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="b9d15-124">Disabilita l'inserimento di zone matematiche (impostazione predefinita: 1).</span><span class="sxs-lookup"><span data-stu-id="b9d15-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="b9d15-125">Per abilitare la modifica e la visualizzazione della matematica, inviare il messaggio [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) con *wParam* impostato su 0 e *lParam* impostato su **ses \_ ex \_ nomath**.</span><span class="sxs-lookup"><span data-stu-id="b9d15-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="b9d15-126"><dt>**SES \_ es \_ notevole**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="b9d15-127">Disabilitare l'inserimento di tabelle.</span><span class="sxs-lookup"><span data-stu-id="b9d15-127">Disable insertion of tables.</span></span> <span data-ttu-id="b9d15-128">Il [**messaggio \_ INSERTTABLE em**](em-inserttable.md) restituisce **e \_ non riesce** e le tabelle RTF vengono ignorate (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="b9d15-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="b9d15-129"><dt>**SES \_ es \_ USESINGLELINE**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="b9d15-130">Consentire a un controllo su più righe di agire come un controllo a riga singola con la possibilità di scorrere verticalmente quando l'altezza a riga singola è maggiore dell'altezza della finestra (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="b9d15-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="b9d15-131"><dt>**\_HIDETEMPFORMAT ses**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="b9d15-132">Nascondere la formattazione temporanea creata quando [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) viene chiamato con **tomApplyTmp**.</span><span class="sxs-lookup"><span data-stu-id="b9d15-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="b9d15-133">Questa formattazione, ad esempio, viene usata dai selezionatori ortografici per visualizzare una sottolineatura ondulata sotto parole probabilmente errate.</span><span class="sxs-lookup"><span data-stu-id="b9d15-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="b9d15-134"><dt>**SES \_ es \_ USEMOUSEWPARAM**</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="b9d15-135">Usare *wParam* per gestire il messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e non chiamare [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="b9d15-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="b9d15-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9d15-136">Requirements</span></span>



| <span data-ttu-id="b9d15-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9d15-137">Requirement</span></span> | <span data-ttu-id="b9d15-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b9d15-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d15-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d15-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b9d15-140">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b9d15-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b9d15-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9d15-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b9d15-142">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b9d15-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b9d15-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9d15-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9d15-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d15-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d15-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9d15-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d15-146">**\_SETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="b9d15-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

