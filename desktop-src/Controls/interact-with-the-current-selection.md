---
title: Come interagire con la selezione corrente
description: L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724282"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="9bc94-103">Come interagire con la selezione corrente</span><span class="sxs-lookup"><span data-stu-id="9bc94-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="9bc94-104">L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera.</span><span class="sxs-lookup"><span data-stu-id="9bc94-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="9bc94-105">La *selezione corrente* è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere.</span><span class="sxs-lookup"><span data-stu-id="9bc94-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="9bc94-106">Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando viene modificata e mostrare o nascondere l'evidenziazione della selezione.</span><span class="sxs-lookup"><span data-stu-id="9bc94-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9bc94-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="9bc94-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9bc94-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="9bc94-108">Technologies</span></span>

-   [<span data-ttu-id="9bc94-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="9bc94-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9bc94-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9bc94-110">Prerequisites</span></span>

-   <span data-ttu-id="9bc94-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="9bc94-111">C/C++</span></span>
-   <span data-ttu-id="9bc94-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="9bc94-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9bc94-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="9bc94-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="9bc94-114">Interagire con la selezione corrente</span><span class="sxs-lookup"><span data-stu-id="9bc94-114">Interact with the Current Selection</span></span>

<span data-ttu-id="9bc94-115">Per determinare la selezione corrente in un controllo Rich Edit, usare il [**messaggio \_ EXGETSEL em**](em-exgetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="9bc94-116">Per impostare la selezione corrente, utilizzare il [**messaggio \_ EXSETSEL em**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="9bc94-117">La struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) viene utilizzata con entrambi i messaggi e specifica un intervallo di caratteri.</span><span class="sxs-lookup"><span data-stu-id="9bc94-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="9bc94-118">Per recuperare informazioni sul contenuto della selezione corrente, è possibile usare il messaggio [**\_ SELECTIONTYPE em**](em-selectiontype.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="9bc94-119">Un'applicazione può rilevare quando la selezione corrente viene modificata elaborando il codice di notifica [en \_ selChange](en-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="9bc94-120">Il codice di notifica specifica una struttura [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) contenente informazioni sulla nuova selezione.</span><span class="sxs-lookup"><span data-stu-id="9bc94-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="9bc94-121">Un controllo Rich Edit invia questo codice di notifica solo se lo si Abilita usando il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="9bc94-122">Per impostazione predefinita, un controllo Rich Edit Mostra e nasconde l'evidenziazione della selezione quando ottiene lo stato attivo e lo perde.</span><span class="sxs-lookup"><span data-stu-id="9bc94-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="9bc94-123">È possibile mostrare o nascondere l'evidenziazione della selezione in qualsiasi momento usando il messaggio [**\_ HIDESELECTION em**](em-hideselection.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="9bc94-124">Ad esempio, un'applicazione potrebbe fornire una finestra di dialogo di ricerca per trovare il testo in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9bc94-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="9bc94-125">L'applicazione potrebbe selezionare testo corrispondente senza chiudere la finestra di dialogo. in questo caso, è necessario usare il messaggio **\_ HIDESELECTION em** per evidenziare la selezione.</span><span class="sxs-lookup"><span data-stu-id="9bc94-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="9bc94-126">Come per i controlli di modifica, è possibile specificare lo stile della finestra [**es \_ NOHIDESEL**](edit-control-styles.md) per evitare che un controllo Rich Edit nasconda l'evidenziazione della selezione quando perde lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="9bc94-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="9bc94-127">In alternativa all'uso dei messaggi [**em \_ EXGETSEL**](em-exgetsel.md) e [**em \_ EXSETSEL**](em-exsetsel.md) , è possibile recuperare e impostare la selezione corrente usando i messaggi [**em \_ GETSEL**](em-getsel.md) e [**em \_ SETSEL**](em-setsel.md) Edit Control.</span><span class="sxs-lookup"><span data-stu-id="9bc94-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="9bc94-128">Il **\_ GETSEL** di messaggi em indici di tipo carattere a 2 16 bit nel valore restituito a 32 bit e pertanto funziona solo per le selezioni che rientrano interamente nei primi 64K.</span><span class="sxs-lookup"><span data-stu-id="9bc94-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="9bc94-129">Tuttavia, un controllo Rich Edit non conterrà mai più di 32K caratteri di testo, a meno che non si estenda questo limite usando il messaggio [**em \_ LIMITTEXT**](em-limittext.md) o [**em \_ EXLIMITTEXT**](em-exlimittext.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc94-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="9bc94-130">Per le selezioni che si estendono oltre i primi 64 KB di testo, il messaggio **em \_ GETSEL** restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="9bc94-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="9bc94-131">In tal caso, è ancora possibile utilizzare i valori restituiti in *wParam* e *lParam* per trovare i caratteri iniziale e finale della selezione.</span><span class="sxs-lookup"><span data-stu-id="9bc94-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bc94-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bc94-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bc94-133">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="9bc94-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="9bc94-134">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9bc94-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




