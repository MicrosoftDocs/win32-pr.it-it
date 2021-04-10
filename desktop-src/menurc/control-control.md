---
title: Controllo controllo
description: Definisce un controllo definito dall'utente.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menu di controllo controllo e altre risorse
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963015"
---
# <a name="control-control"></a><span data-ttu-id="929db-104">Controllo controllo</span><span class="sxs-lookup"><span data-stu-id="929db-104">CONTROL control</span></span>

<span data-ttu-id="929db-105">Definisce un controllo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="929db-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="929db-106"><span id="class"></span><span id="CLASS"></span>*classe*</span><span class="sxs-lookup"><span data-stu-id="929db-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="929db-107">Nome ridefinito, stringa di caratteri o valore Unsigned Integer a 16 bit che definisce la classe.</span><span class="sxs-lookup"><span data-stu-id="929db-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="929db-108">Può trattarsi di una delle classi di controlli. per un elenco delle classi di controlli, vedere il primo elenco che segue questa descrizione.</span><span class="sxs-lookup"><span data-stu-id="929db-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="929db-109">Se il valore è un nome ridefinito fornito dall'applicazione, deve essere una stringa racchiusa tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="929db-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="929db-110"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="929db-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="929db-111">Nome o valore intero ridefinito che specifica lo stile del controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="929db-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="929db-112">Il significato esatto dello *stile* dipende dal valore della *classe* .</span><span class="sxs-lookup"><span data-stu-id="929db-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="929db-113">Le sezioni che seguono questa descrizione mostrano le classi di controlli e gli stili corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="929db-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="929db-114">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="929db-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="929db-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="929db-115">Remarks</span></span>

<span data-ttu-id="929db-116">Nelle sezioni seguenti sono descritte le sei classi di controllo possibili.</span><span class="sxs-lookup"><span data-stu-id="929db-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="929db-117">Classe del controllo Button</span><span class="sxs-lookup"><span data-stu-id="929db-117">The Button Control Class</span></span>

<span data-ttu-id="929db-118">Un controllo Button è una piccola finestra figlio rettangolare che l'utente può attivare o disattivare facendo clic su di esso con il mouse.</span><span class="sxs-lookup"><span data-stu-id="929db-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="929db-119">I controlli Button possono essere usati singolarmente o in gruppi e possono essere etichettati o visualizzati senza testo.</span><span class="sxs-lookup"><span data-stu-id="929db-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="929db-120">I controlli pulsante in genere cambiano aspetto quando l'utente fa clic su di essi.</span><span class="sxs-lookup"><span data-stu-id="929db-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="929db-121">Gli stili dei pulsanti sono descritti nell'argomento: [stili dei pulsanti](../controls/button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="929db-122">Classe del controllo casella combinata</span><span class="sxs-lookup"><span data-stu-id="929db-122">The Combo Box Control Class</span></span>

<span data-ttu-id="929db-123">I controlli casella combinata sono costituiti da un campo di selezione simile a un controllo di modifica più una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="929db-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="929db-124">È possibile che la casella di riepilogo venga visualizzata in qualsiasi momento o venga rilasciata quando l'utente seleziona una "casella di riepilogo" accanto al campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="929db-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="929db-125">A seconda dello stile della casella combinata, l'utente può o non può modificare il contenuto del campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="929db-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="929db-126">Se la casella di riepilogo è visibile, la digitazione dei caratteri nella casella di selezione comporterà l'evidenziazione della prima voce che corrisponde ai caratteri digitati.</span><span class="sxs-lookup"><span data-stu-id="929db-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="929db-127">Viceversa, la selezione di un elemento nella casella di riepilogo Visualizza il testo selezionato nel campo di selezione.</span><span class="sxs-lookup"><span data-stu-id="929db-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="929db-128">Gli stili del controllo casella combinata sono descritti nel seguente argomento: [stili casella combinata](../controls/combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="929db-129">Classe del controllo di modifica</span><span class="sxs-lookup"><span data-stu-id="929db-129">The Edit Control Class</span></span>

<span data-ttu-id="929db-130">Un controllo di modifica è una finestra figlio rettangolare in cui l'utente può immettere testo dalla tastiera.</span><span class="sxs-lookup"><span data-stu-id="929db-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="929db-131">L'utente seleziona il controllo e lo mette in stato attivo per l'input facendo clic sul mouse al suo interno o premendo il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="929db-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="929db-132">L'utente può immettere testo quando il controllo Visualizza un punto di inserimento lampeggiante.</span><span class="sxs-lookup"><span data-stu-id="929db-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="929db-133">È possibile utilizzare il mouse per spostare il cursore e selezionare i caratteri da sostituire oppure per posizionare il cursore per l'inserimento di caratteri.</span><span class="sxs-lookup"><span data-stu-id="929db-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="929db-134">È possibile utilizzare il tasto BACKSPACE per eliminare i caratteri.</span><span class="sxs-lookup"><span data-stu-id="929db-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="929db-135">I controlli di modifica usano il tipo di carattere a passo fisso e visualizzano caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="929db-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="929db-136">Espandendo i caratteri di tabulazione in tutti i caratteri di spazio necessari per spostare il cursore alla successiva tabulazione.</span><span class="sxs-lookup"><span data-stu-id="929db-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="929db-137">Si presuppone che le tabulazioni si trovino in ogni ottavo punto.</span><span class="sxs-lookup"><span data-stu-id="929db-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="929db-138">Gli stili di modifica del controllo sono descritti nell'argomento seguente: [modificare gli stili dei controlli](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="929db-139">Classe del controllo casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="929db-139">The List Box Control Class</span></span>

<span data-ttu-id="929db-140">I controlli casella di riepilogo sono costituiti da un elenco di stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="929db-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="929db-141">Il controllo viene usato ogni volta che un'applicazione deve presentare un elenco di nomi, ad esempio nomi file, che l'utente può visualizzare e selezionare.</span><span class="sxs-lookup"><span data-stu-id="929db-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="929db-142">L'utente può selezionare una stringa posizionando il puntatore del mouse sulla stringa e facendo clic su un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="929db-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="929db-143">Quando si seleziona una stringa, questa viene evidenziata e un messaggio di notifica viene passato alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="929db-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="929db-144">È possibile utilizzare una barra di scorrimento con un controllo casella di riepilogo per scorrere gli elenchi che sono troppo lunghi o troppo larghi per la finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="929db-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="929db-145">Gli stili del controllo casella di riepilogo sono descritti nell'argomento seguente: [stili casella di riepilogo](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="929db-146">Classe del controllo Scroll-Bar</span><span class="sxs-lookup"><span data-stu-id="929db-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="929db-147">Un controllo barra di scorrimento è un rettangolo che contiene un cursore di scorrimento e con frecce di direzione a entrambe le estremità.</span><span class="sxs-lookup"><span data-stu-id="929db-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="929db-148">La barra di scorrimento invia un messaggio di notifica al padre ogni volta che l'utente fa clic sul mouse nel controllo.</span><span class="sxs-lookup"><span data-stu-id="929db-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="929db-149">Se necessario, l'elemento padre è responsabile dell'aggiornamento della posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="929db-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="929db-150">I controlli barra di scorrimento hanno lo stesso aspetto e la stessa funzione delle barre di scorrimento utilizzate nelle finestre normali.</span><span class="sxs-lookup"><span data-stu-id="929db-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="929db-151">Tuttavia, a differenza delle barre di scorrimento, i controlli barra di scorrimento possono essere posizionati in qualsiasi punto all'interno di una finestra e usati quando necessario per fornire input di scorrimento per una finestra.</span><span class="sxs-lookup"><span data-stu-id="929db-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="929db-152">Gli stili della barra di scorrimento sono descritti nell'argomento seguente: [stili del controllo barra di scorrimento](../controls/scroll-bar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="929db-153">Classe del controllo statico</span><span class="sxs-lookup"><span data-stu-id="929db-153">The Static Control Class</span></span>

<span data-ttu-id="929db-154">I controlli statici sono semplici campi di testo, caselle e rettangoli che possono essere usati per etichettare, box o separare altri controlli.</span><span class="sxs-lookup"><span data-stu-id="929db-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="929db-155">I controlli statici non accettano input e non forniscono alcun output.</span><span class="sxs-lookup"><span data-stu-id="929db-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="929db-156">Gli stili del controllo statico sono descritti nell'argomento seguente: [stili del controllo statico](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="929db-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 