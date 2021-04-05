---
description: Il controllo InkEdit fornisce un modo semplice per acquisire, riconoscere e visualizzare input penna.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Controllo InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882782"
---
# <a name="inkedit-control"></a><span data-ttu-id="cad56-103">Controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="cad56-103">InkEdit Control</span></span>

<span data-ttu-id="cad56-104">Il controllo [InkEdit](inkedit-control-reference.md) fornisce un modo semplice per acquisire, riconoscere e visualizzare input penna.</span><span class="sxs-lookup"><span data-stu-id="cad56-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="cad56-105">Questa implementazione del controllo [InkEdit](inkedit-control-reference.md) è basata sul controllo [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="cad56-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="cad56-106">L'implementazione gestita (.NET Framework) di [InkEdit](/previous-versions/ms835842(v=msdn.10)) si basa sul controllo [**RichTextBox**](/previous-versions/windows/) .</span><span class="sxs-lookup"><span data-stu-id="cad56-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="cad56-107">Lo scopo principale del controllo [InkEdit](inkedit-control-reference.md) è raccogliere input penna, riconoscerlo e visualizzarlo in formato testo.</span><span class="sxs-lookup"><span data-stu-id="cad56-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="cad56-108">Inoltre, supporta la visualizzazione di input penna come oggetto incorporato con funzionalità di formattazione del testo, ad esempio grassetto e sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="cad56-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="cad56-109">Movimenti e correzione</span><span class="sxs-lookup"><span data-stu-id="cad56-109">Gestures and Correction</span></span>

<span data-ttu-id="cad56-110">[InkEdit](inkedit-control-reference.md) supporta i movimenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cad56-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="cad56-111">Movimento</span><span class="sxs-lookup"><span data-stu-id="cad56-111">Gesture</span></span>                                                                    | <span data-ttu-id="cad56-112">Nome movimento</span><span class="sxs-lookup"><span data-stu-id="cad56-112">Gesture Name</span></span>              | <span data-ttu-id="cad56-113">Azione</span><span class="sxs-lookup"><span data-stu-id="cad56-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![movimento in basso a sinistra](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="cad56-115">In basso a sinistra</span><span class="sxs-lookup"><span data-stu-id="cad56-115">Down-left</span></span><br/>      | <span data-ttu-id="cad56-116">Immettere</span><span class="sxs-lookup"><span data-stu-id="cad56-116">Enter</span></span><br/>     |
| ![movimento in basso a sinistra](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="cad56-118">In basso a sinistra-lungo</span><span class="sxs-lookup"><span data-stu-id="cad56-118">Down-left-long</span></span><br/> | <span data-ttu-id="cad56-119">Immettere</span><span class="sxs-lookup"><span data-stu-id="cad56-119">Enter</span></span><br/>     |
| ![movimento attivo](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="cad56-121">In alto a destra</span><span class="sxs-lookup"><span data-stu-id="cad56-121">Up-right</span></span><br/>       | <span data-ttu-id="cad56-122">Scheda</span><span class="sxs-lookup"><span data-stu-id="cad56-122">Tab</span></span><br/>       |
| ![movimento a destra-lungo.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="cad56-124">Up-right-Long</span><span class="sxs-lookup"><span data-stu-id="cad56-124">Up-right-long</span></span><br/>  | <span data-ttu-id="cad56-125">Scheda</span><span class="sxs-lookup"><span data-stu-id="cad56-125">Tab</span></span><br/>       |
| ![gesto destro](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="cad56-127">Destra</span><span class="sxs-lookup"><span data-stu-id="cad56-127">Right</span></span><br/>          | <span data-ttu-id="cad56-128">Space</span><span class="sxs-lookup"><span data-stu-id="cad56-128">Space</span></span><br/>     |
| ![movimento sinistro](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="cad56-130">Sinistra</span><span class="sxs-lookup"><span data-stu-id="cad56-130">Left</span></span><br/>           | <span data-ttu-id="cad56-131">Backspace</span><span class="sxs-lookup"><span data-stu-id="cad56-131">Backspace</span></span><br/> |



 

<span data-ttu-id="cad56-132">Gli eventi di movimento che è possibile gestire contengono informazioni sui movimenti, i tratti e i cursori che è possibile utilizzare per inviare il testo a [InkEdit](inkedit-control-reference.md) o inserire i dati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="cad56-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="cad56-133">[InkEdit](inkedit-control-reference.md) fornisce inoltre un'interfaccia utente di correzione che consente agli utenti di visualizzare e selezionare le alternative, utilizzare la tastiera su schermo e i riconoscitori di caratteri/lettere/blocchi.</span><span class="sxs-lookup"><span data-stu-id="cad56-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="cad56-134">Altri dettagli</span><span class="sxs-lookup"><span data-stu-id="cad56-134">Other Details</span></span>

<span data-ttu-id="cad56-135">[InkEdit](inkedit-control-reference.md) è progettato per funzionare correttamente in uno scenario di form per una singola riga, nonché per la modifica e l'immissione di testo su più righe.</span><span class="sxs-lookup"><span data-stu-id="cad56-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="cad56-136">L'uso principale previsto per InkEdit consiste nell'ottenere l'input di testo da un utente sotto forma di grafia.</span><span class="sxs-lookup"><span data-stu-id="cad56-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="cad56-137">Per impostazione predefinita, l'input penna viene riconosciuto e il testo viene inserito al suo posto.</span><span class="sxs-lookup"><span data-stu-id="cad56-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="cad56-138">L'interfaccia utente predefinita per InkEdit è simile a quella del controllo [**RichTextBox**](/previous-versions/windows/) , tranne quando l'utente sta disponendo l'input penna.</span><span class="sxs-lookup"><span data-stu-id="cad56-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="cad56-139">È possibile visualizzare l'input penna originale anziché il testo; Tuttavia, l'input penna viene ridimensionato in modo da aumentare le dimensioni del carattere di input corrente del controllo InkEdit e viene visualizzato inline con altro testo.</span><span class="sxs-lookup"><span data-stu-id="cad56-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="cad56-140">Per motivi di sicurezza, è necessario usare le procedure standard per aprire o chiudere un file, trasmettere l'input/output e impostare la proprietà [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) o [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .</span><span class="sxs-lookup"><span data-stu-id="cad56-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="cad56-141">Per impostazione predefinita, il controllo [InkEdit](inkedit-control-reference.md) è impostato in modo da riconoscere l'input penna come testo.</span><span class="sxs-lookup"><span data-stu-id="cad56-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="cad56-142">Per consentire agli utenti di aggiungere input penna come input penna, impostare la proprietà [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) su **InsertAsInk**.</span><span class="sxs-lookup"><span data-stu-id="cad56-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="cad56-143">Per informazioni di riferimento dettagliate sul controllo [InkEdit](inkedit-control-reference.md) , vedere InkEdit.</span><span class="sxs-lookup"><span data-stu-id="cad56-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="cad56-144">Se si usa il controllo [InkEdit](inkedit-control-reference.md) Win32 e lo si inserisce in una casella di gruppo, assicurarsi che la casella abbia uno stile trasparente; in caso contrario, InkEdit non è in grado di raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="cad56-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="cad56-145">Per assicurarsi che l'input penna venga visualizzato correttamente, chiamare il metodo di [**aggiornamento**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) del controllo [InkEdit](inkedit-control-reference.md) quando riceve un evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) o [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="cad56-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="cad56-146">Le sezioni seguenti illustrano in dettaglio l'uso del controllo [InkEdit](inkedit-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="cad56-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="cad56-147">Creazione di un'istanza di InkEdit</span><span class="sxs-lookup"><span data-stu-id="cad56-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="cad56-148">Riconoscimento di parole e caratteri</span><span class="sxs-lookup"><span data-stu-id="cad56-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="cad56-149">Visualizzazione di input penna come input penna</span><span class="sxs-lookup"><span data-stu-id="cad56-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="cad56-150">Utilizzo di InkEdit nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="cad56-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="cad56-151">Uso di un dizionario applicazioni con InkEdit</span><span class="sxs-lookup"><span data-stu-id="cad56-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

