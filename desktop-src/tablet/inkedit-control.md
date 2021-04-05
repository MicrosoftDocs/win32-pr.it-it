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
# <a name="inkedit-control"></a>Controllo InkEdit

Il controllo [InkEdit](inkedit-control-reference.md) fornisce un modo semplice per acquisire, riconoscere e visualizzare input penna.

Questa implementazione del controllo [InkEdit](inkedit-control-reference.md) è basata sul controllo [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . L'implementazione gestita (.NET Framework) di [InkEdit](/previous-versions/ms835842(v=msdn.10)) si basa sul controllo [**RichTextBox**](/previous-versions/windows/) .

Lo scopo principale del controllo [InkEdit](inkedit-control-reference.md) è raccogliere input penna, riconoscerlo e visualizzarlo in formato testo. Inoltre, supporta la visualizzazione di input penna come oggetto incorporato con funzionalità di formattazione del testo, ad esempio grassetto e sottolineatura.

## <a name="gestures-and-correction"></a>Movimenti e correzione

[InkEdit](inkedit-control-reference.md) supporta i movimenti seguenti.



| Movimento                                                                    | Nome movimento              | Azione               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![movimento in basso a sinistra](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | In basso a sinistra<br/>      | Immettere<br/>     |
| ![movimento in basso a sinistra](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | In basso a sinistra-lungo<br/> | Immettere<br/>     |
| ![movimento attivo](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | In alto a destra<br/>       | Scheda<br/>       |
| ![movimento a destra-lungo.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Up-right-Long<br/>  | Scheda<br/>       |
| ![gesto destro](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Destra<br/>          | Space<br/>     |
| ![movimento sinistro](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Sinistra<br/>           | Backspace<br/> |



 

Gli eventi di movimento che è possibile gestire contengono informazioni sui movimenti, i tratti e i cursori che è possibile utilizzare per inviare il testo a [InkEdit](inkedit-control-reference.md) o inserire i dati negli Appunti.

[InkEdit](inkedit-control-reference.md) fornisce inoltre un'interfaccia utente di correzione che consente agli utenti di visualizzare e selezionare le alternative, utilizzare la tastiera su schermo e i riconoscitori di caratteri/lettere/blocchi.

## <a name="other-details"></a>Altri dettagli

[InkEdit](inkedit-control-reference.md) è progettato per funzionare correttamente in uno scenario di form per una singola riga, nonché per la modifica e l'immissione di testo su più righe. L'uso principale previsto per InkEdit consiste nell'ottenere l'input di testo da un utente sotto forma di grafia. Per impostazione predefinita, l'input penna viene riconosciuto e il testo viene inserito al suo posto. L'interfaccia utente predefinita per InkEdit è simile a quella del controllo [**RichTextBox**](/previous-versions/windows/) , tranne quando l'utente sta disponendo l'input penna. È possibile visualizzare l'input penna originale anziché il testo; Tuttavia, l'input penna viene ridimensionato in modo da aumentare le dimensioni del carattere di input corrente del controllo InkEdit e viene visualizzato inline con altro testo.

> [!Note]  
> Per motivi di sicurezza, è necessario usare le procedure standard per aprire o chiudere un file, trasmettere l'input/output e impostare la proprietà [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) o [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .

 

Per impostazione predefinita, il controllo [InkEdit](inkedit-control-reference.md) è impostato in modo da riconoscere l'input penna come testo. Per consentire agli utenti di aggiungere input penna come input penna, impostare la proprietà [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) su **InsertAsInk**.

Per informazioni di riferimento dettagliate sul controllo [InkEdit](inkedit-control-reference.md) , vedere InkEdit.

> [!Note]  
> Se si usa il controllo [InkEdit](inkedit-control-reference.md) Win32 e lo si inserisce in una casella di gruppo, assicurarsi che la casella abbia uno stile trasparente; in caso contrario, InkEdit non è in grado di raccogliere input penna.

 

> [!Note]  
> Per assicurarsi che l'input penna venga visualizzato correttamente, chiamare il metodo di [**aggiornamento**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) del controllo [InkEdit](inkedit-control-reference.md) quando riceve un evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) o [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .

 

Le sezioni seguenti illustrano in dettaglio l'uso del controllo [InkEdit](inkedit-control-reference.md) :

-   [Creazione di un'istanza di InkEdit](instantiating-inkedit.md)
-   [Riconoscimento di parole e caratteri](word-vs--character-recognition.md)
-   [Visualizzazione di input penna come input penna](displaying-ink-as-ink.md)
-   [Utilizzo di InkEdit nelle versioni precedenti di Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Uso di un dizionario applicazioni con InkEdit](using-an-application-dictionary-with-inkedit.md)

 

