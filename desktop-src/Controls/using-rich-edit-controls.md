---
title: Uso di controlli Rich Edit
description: Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474518"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="4fcdb-103">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="4fcdb-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="4fcdb-104">Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fcdb-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4fcdb-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fcdb-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="4fcdb-106">Topic</span></span></th>
<th><span data-ttu-id="4fcdb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fcdb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4fcdb-108"><a href="create-rich-edit-controls.md">Come creare controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-109">Per creare un controllo Rich Edit, chiamare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , specificando la classe della finestra Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="4fcdb-110">Per Microsoft Rich Edit 4,1 (Msftedit.dll) specificare MSFTEDIT_CLASS come classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="4fcdb-111">Per tutte le versioni precedenti, specificare RICHEDIT_CLASS.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="4fcdb-112">Per ulteriori informazioni, vedere <a href="about-rich-edit-controls.md">versioni di Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="4fcdb-113">I controlli Rich Edit supportano la maggior parte degli stili della finestra utilizzati con i controlli di modifica e altri stili.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="4fcdb-114">È necessario specificare lo stile della finestra <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> se si desidera consentire più di una riga di testo nel controllo.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="4fcdb-115">Per altre informazioni, vedere <a href="rich-edit-control-styles.md">stili del controllo Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-116"><a href="format-text-in-rich-edit-controls.md">Come formattare il testo nei controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-117">Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare i caratteri e i paragrafi e recuperare le informazioni di formattazione.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="4fcdb-118">Gli attributi di formattazione dei paragrafi includono l'allineamento, le tabulazioni, i rientri, la numerazione e le tabelle semplici.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="4fcdb-119">Per i caratteri, è possibile specificare il nome, la dimensione, il colore e gli effetti del tipo di carattere, ad esempio grassetto, corsivo e protetto.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fcdb-120"><a href="interact-with-the-current-selection.md">Come interagire con la selezione corrente</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-121">L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="4fcdb-122">La <em>selezione corrente</em> è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="4fcdb-123">Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando viene modificata e mostrare o nascondere l'evidenziazione della selezione.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-124"><a href="use-rich-edit-text-operations.md">Come usare le operazioni Rich Edit Text</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-125">Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="4fcdb-126">È possibile recuperare il testo selezionato o un intervallo di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fcdb-127"><a href="use-word-and-line-break-information.md">Come usare le informazioni relative a parole e interruzioni di riga</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-128">Un controllo Rich Edit chiama una funzione chiamata procedura di interruzione di parola per individuare le interruzioni tra le parole e per determinare la posizione in cui è possibile interrompere le righe.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="4fcdb-129">Il controllo utilizza queste informazioni quando si eseguono operazioni di ritorno a capo automatico e quando si elaborano le combinazioni di tasti CTRL + freccia sinistra e CTRL + freccia destra.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="4fcdb-130">Un'applicazione può inviare messaggi a un controllo Rich Edit per sostituire la routine di Word break predefinita, per recuperare le informazioni sull'interruzioni di parola e per determinare la riga in cui si trova un determinato carattere.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-131"><a href="use-rich-edit-clipboard-operations.md">Come utilizzare le operazioni Rich Edit Clipboard</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-132">Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="4fcdb-133">È inoltre possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fcdb-134"><a href="use-streams.md">Come usare i flussi</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-135">È possibile utilizzare i flussi per trasferire i dati all'interno o all'esterno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="4fcdb-136">Un flusso è definito da una struttura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , che specifica un buffer e una funzione di callback definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-137"><a href="automatically-resize-rich-edit-controls.md">Come ridimensionare automaticamente i controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-138">Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="4fcdb-139">Un controllo Rich Edit supporta questa cosiddetta funzionalità senza <em>fondo</em> inviando la finestra padre di un <a href="en-requestresize.md">EN_REQUESTRESIZE</a> codice di notifica ogni volta che viene modificata la dimensione del contenuto del controllo.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fcdb-140"><a href="use-rich-edit-control-notification-codes.md">Come utilizzare i codici di notifica del controllo Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-141">Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="4fcdb-142">I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-143"><a href="use-font-binding-in-rich-edit-controls.md">Come usare l'associazione di tipi di carattere nei controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-144">Microsoft Rich Edit 3,0 assegna un set di caratteri a caratteri testo normale a seconda del contesto.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="4fcdb-145">Di seguito sono riportati alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="4fcdb-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="4fcdb-146">I caratteri greci vengono assegnati <strong>GREEK_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="4fcdb-147">I simboli Hangul sono assegnati <strong>HANGUL_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="4fcdb-148">I caratteri cinesi vengono assegnati <strong>SHIFTJIS_CHARSET</strong> se sono presenti caratteri Kana vicini o <strong>GB2312_CHARSET</strong> se non sono stati trovati caratteri Kana nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="4fcdb-149">I caratteri ANSI non neutri vengono assegnati <strong>ANSI_CHARSET</strong> in qualsiasi evento.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4fcdb-150"><a href="using-rich-edit-com.md">Come utilizzare OLE nei controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-151">In questa sezione vengono fornite informazioni sull'utilizzo di Object Linking and Embedding (OLE) in controlli Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4fcdb-152"><a href="printing-rich-edit-controls.md">Come stampare il contenuto dei controlli Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="4fcdb-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="4fcdb-153">Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

